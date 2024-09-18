# chattadata.py
Work in Progress: ChattaData Python Client.  Simplifies data access.  Support many formats.

## install
```sh
pip install chattadata
```

## supported formats
- csv
- excel
- geojson
- json
- shapefile

## usage
```python
import chattadata

chattadata.get(id="nvdi-c4tt").json()
[
  { "Incident Number": "24-085837", "Incident Date": "2024-09-13T20:33:00.000", ... },
  { "Incident Number": "24-085776", "Incident Date": "2024-09-13T16:38:00.000", ... }
  # ...
]

chattadata.get(id="nvdi-c4tt").geojson()
{ "type": "FeatureCollection", "features": [...] }

chattadata.get(title="Vehicle Incidents").csv()
"Incident Number,Incident Date,..."
```

## advanced usage
```py
chattadata.get(id="nvdi-c4tt", offset=10, limit=500).shapefile()
```
