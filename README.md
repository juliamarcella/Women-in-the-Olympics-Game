# Women-in-the-Olympics-Game
Interactive dashboard and analysis of gender participation and medal equity in the Olympic Games.

# Olympics Gender Gap Analysis and Dashboard

This project explores more than a century of Olympic history to understand how gender representation has evolved across sports, countries, and medal events. It combines data cleaning, feature engineering, and visualization to highlight when women were first allowed to compete in each discipline, how participation changed over time, and how medal distribution compares across genders.

## Key insights
- Some sports show extremely long delays between men’s and women’s first participation, with gaps exceeding 100 years.
- Women’s participation has grown sharply since the late 20th century, but representation still varies widely by sport and season.
- Medal distribution reflects both participation levels and structural access to events, revealing persistent differences across disciplines and countries.

## Data and features
The dataset includes athlete- and event‑level information such as:
- `discipline_title`, `event_title`, `game_year`, `game_season`, `game_location`
- `athlete_gender` (standardized to *women*, *men*, *mixed*)
- Medal indicators: `Gold_event_details`, `Silver_event_details`, `Bronze_event_details`
- Country information and participation metadata

Additional engineered fields:
- `total_medals` — sum of gold, silver, and bronze flags
- `first_men_year` and `first_women_year` — earliest participation per sport
- `years_difference` — gap between men’s and women’s first appearance
- Gender‑specific medal totals and participation counts

## Methods
1. **Data cleaning**  
   Standardization of gender labels, event names, and team/individual classifications.

2. **Gap calculation**  
   Identification of the first year men and women competed in each discipline and computation of the difference.

3. **Medal aggregation**  
   Conversion of medal flags into total medal counts and gender‑specific medal metrics.

4. **Visualization**  
   Construction of an interactive dashboard in Looker Studio with filters for year, season, sport, and country.

## Dashboard
The interactive dashboard includes:
- Participation trends by gender from 1896 to the present  
- Medal totals and medal share by gender  
- A world map of women’s participation  
- A ranked table of sports showing the gender‑entry gap  
- Normalized metrics such as medals per 100 athletes

## Repository structure
- `notebooks/` — data cleaning, feature engineering, and exploratory analysis  
- `data/` — cleaned datasets or instructions for obtaining them  
- `lookerstudio/` — calculated field formulas and dashboard setup notes  
- `README.md` — project documentation  

## How to reproduce
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
