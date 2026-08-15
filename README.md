# Amsterdam Airbnb Data Explorer

An interactive Streamlit application for exploring and filtering an Amsterdam Airbnb listings dataset with Pandas.

The project focuses on practical dataframe exploration: users can choose which columns to filter, apply category, numeric, date, or text filters, and inspect the resulting subset directly in the browser.

> **Note:** This is an educational data-analysis project and is not affiliated with or endorsed by Airbnb.

## Features

- Interactive dataframe filtering in Streamlit
- Selectable filter columns
- Categorical multi-select filters
- Numeric range sliders
- Date-range filtering when datetime columns are detected
- Text and regular-expression filtering
- Amsterdam listing data including host, neighbourhood, room, pricing, availability, and review fields

## Tech Stack

- Python
- Pandas
- Streamlit

## Project Structure

```text
airbnb-project-pandas/
├── app.py
├── WK2_Airbnb_Amsterdam_listings_proj_solution.csv
├── requirements.txt
├── .gitignore
├── LICENSE
└── README.md
```

## Dataset

The included CSV contains Airbnb listing attributes such as:

- listing ID
- host acceptance rate and Superhost status
- neighbourhood
- latitude and longitude
- room type and capacity
- bedrooms and beds
- nightly price
- minimum and maximum stay
- availability
- recent review activity and rating
- instant-bookable status
- derived pricing and discount fields

The dataset is loaded locally by `app.py`, so no external API key is required.

## Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/HoosseinRahimi/airbnb-project-pandas.git
cd airbnb-project-pandas
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

**Windows**

```bash
.venv\Scripts\activate
```

**macOS / Linux**

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Start the app

```bash
streamlit run app.py
```

Streamlit will print the local URL in the terminal, normally `http://localhost:8501`.

## How the Filtering Works

After enabling **Add filters**, choose one or more dataframe columns. The app selects an appropriate control based on the column type:

- low-cardinality or categorical columns → multi-select
- numeric columns → range slider
- datetime columns → date range
- other text columns → substring or regular-expression input

Each selected filter is applied to the current dataframe, so multiple filters combine to progressively narrow the result.

## Possible Extensions

- Add neighbourhood and price visualisations
- Add a map using latitude and longitude
- Add downloadable filtered results
- Add summary metrics for the current selection
- Add automated tests for filtering behaviour

## License

See [`LICENSE`](LICENSE) for the repository license.