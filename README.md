# JustWatch Scraping and Analysis

This project contains a Jupyter notebook for scraping movie and TV show data from
[JustWatch India](https://www.justwatch.com/in), cleaning the scraped results, and
performing basic analysis with pandas.

The notebook targets content released from 2000 onward and collects details such
as title, release year, genres, IMDb rating, runtime, age rating, production
country, streaming availability, and JustWatch URL.

## Project Files

- `Numerical_Programming_in_Python_Web_Scraping.ipynb` - Main notebook containing
  the scraping, cleaning, analysis, visualization, and CSV export workflow.

## What the Notebook Does

1. Scrapes movie URLs from JustWatch India.
2. Visits each movie page and extracts movie metadata.
3. Scrapes TV show URLs from JustWatch India.
4. Visits each TV show page and extracts TV show metadata.
5. Converts the scraped data into pandas DataFrames.
6. Cleans numeric fields such as release year and IMDb rating.
7. Filters and analyzes the data, including:
   - High-rated movies and TV shows
   - Recently released titles
   - Children-friendly content
   - Indian productions
   - Genre frequency counts
   - Average IMDb ratings
   - Predominant streaming services
8. Generates a word cloud for streaming services.
9. Exports the final datasets to CSV files.

## Requirements

The notebook uses the following Python packages:

- `requests`
- `beautifulsoup4`
- `pandas`
- `numpy`
- `wordcloud`
- `matplotlib`

Install them with:

```bash
pip install requests beautifulsoup4 pandas numpy wordcloud matplotlib
```

If you are running the notebook in Google Colab, most packages are already
available, but you may still need to install `beautifulsoup4` and `wordcloud`.

## How to Run

1. Open `Numerical_Programming_in_Python_Web_Scraping.ipynb` in Jupyter Notebook,
   JupyterLab, or Google Colab.
2. Run the cells from top to bottom.
3. Wait for the scraping cells to complete. The notebook uses requests to fetch
   JustWatch pages, so runtime depends on network speed and site availability.
4. Review the generated DataFrames and analysis output.
5. Check the exported CSV files in the working directory.

## Output Files

Running the notebook creates:

- `Movies_Data_justwatch.csv`
- `TV_Shows_Data_justwatch.csv`

The notebook also includes Google Drive links for the exported datasets.

## Data Source

Data is scraped from:

- Movies: `https://www.justwatch.com/in/movies?release_year_from=2000`
- TV shows: `https://www.justwatch.com/in/tv-shows?release_year_from=2000`

## Notes

- The scraper depends on JustWatch page structure. If JustWatch changes its HTML
  classes or layout, some selectors may need to be updated.
- The notebook extracts data from HTML pages rather than directly calling a
  JustWatch API.
- Add delays between requests when expanding the scraper to reduce load on the
  target site.
- Scraped data can change over time because streaming availability and ratings
  are updated regularly.

## Disclaimer

This project is intended for educational use. Before scraping any website at
scale, review its terms of service and robots.txt guidance.
