# Tracking Prices in Serbia

This repository contains a web scraping pipeline that collects and stores prices of grocery and household products from [cenoteka.rs](https://cenoteka.rs), a Serbian price comparison platform.

The goal is to monitor how the prices of everyday items change over time, providing a consistent and up-to-date dataset that can later be used for data analysis, storytelling, or visualizations related to the cost of living in Serbia.

## How it works

The scraping is done using Python and [Playwright](https://playwright.dev/python/), a browser automation library. The script navigates through a large number of product categories, visits each product listing page, and extracts the following information:
- Product name
- Brand
- Price
- Discount (if any)
- Product category
- Timestamp

The data is saved in the `data/` directory as CSV files, each named with the exact date and time when scraping was performed.

## Automation

This process will be automatically triggered once a week using [GitHub Actions](https://docs.github.com/en/actions). The workflow will run the scraper, save the output, and commit the newly collected data back to the repository. This ensures regular updates without any manual effort.

## Inspiration

The project automation strategy was inspired by [Jonathan Soma’s guide on auto-updating scrapers and visualizations](https://jonathansoma.com/everything/git/auto-updating-scaper-viz/).

---

Feel free to explore the code and use the dataset for your own analysis or visual work. Contributions and feedback are welcome.
