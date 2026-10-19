# Urban Traffic Intelligence — Rebuilt Power BI Project

Built from the uploaded `indian_roads_dataset.csv`.

## Dataset
- Rows: 20,000
- Columns: 24
- States: 7
- Cities: 8
- Road types: 3
- Weather categories: 3
- Severity categories: 3

## Data model
A star-schema style semantic model is included:
- FactAccidents
- DimDate
- DimLocation
- DimRoadType
- DimWeather
- DimCause
- DimSeverity

Relationships connect each dimension to FactAccidents through explicit keys.

## Power Query / M
The model uses Power Query (M), not SQL, because the source is CSV. It performs text cleaning, data type conversion, date/time parsing, null handling, duplicate removal, dimension-key creation, and derived Year/Month/Hour fields.

## DAX measures
Accident Records, Fatal Records, Total Casualties, Average Risk Score, Average Casualties per Accident, Peak Hour Records, Weekend Records.

## Dashboard
Slicers for State, Severity, Road Type and Weather; KPI cards; severity; hourly trend; causes; weather vs severity; state analysis.

## Open
Open `Urban Traffic Intelligence.pbip` in Power BI Desktop. Refresh the model. If your submission requires a `.pbix`, use Power BI Desktop **Save As** after verifying the project.

The uploaded CSV is included in `data/` for reference; the Power Query source uses the same public GitHub CSV URL for refresh.


Date handling fix: the source date is parsed manually as DD-MM-YYYY and the time column is retained as text to avoid locale-dependent refresh errors.
