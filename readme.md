# Emma & Austin’s Downtown Raleigh Wedding Hotels

This web map shows hotel options within walking distance of Emma Watkins and Austin Gifford’s wedding venue in downtown Raleigh, North Carolina. Each hotel marker is styled using the wedding colors (burgundy, wine red, white, and black) and links to more information for guests.

---

## Map Contents

- **Wedding Venue**  
  - Single heart marker at the ceremony/reception location  
  - Layer: `assets/wedding_venue.geojson`

- **Hotels**  
  - 8 nearby hotels within ~1.5 km of the venue  
  - Layer: `assets/downtown_raleigh_hotels.geojson`  
  - Popups show:
    - Hotel name  
    - Star rating (out of 5)  
    - Average nightly rate  
    - Website link  

- **Symbology**
  - Hotel icons use a 4-class color ramp based on **average nightly rate**:  
    - Under \$175  
    - \$175–\$224  
    - \$225–\$299  
    - \$300 and up  
  - Colors are derived from the wedding palette (burgundy, wine red, white, black).  
  - The venue uses a large wine-red heart icon.

---

## Data Sources & Processing

- **Hotel locations:**  
  - Downloaded from **OpenStreetMap** using **Overpass Turbo** (`tourism=hotel`) within a radius of the wedding venue.
- **Attributes added in QGIS:**  
  - `stars` – decimal rating out of 5  
  - `avg_cost` – estimated average cost per night (USD)  
  - `website` – official hotel website
- **Venue point:**  
  - Created in QGIS at the coordinates  
    `35.778611, -78.637833` (EPSG:4326)

Both layers were exported from QGIS as GeoJSON into the `assets` folder.

---

## Technologies Used

- **Leaflet** for interactive web mapping  
- **leaflet-ajax** for loading GeoJSON layers  
- **chroma.js** for the custom wedding color ramp  
- **Font Awesome** for hotel and heart icons  
- **Carto Light** basemap (Carto + OpenStreetMap)  
- **QGIS** and **Overpass Turbo** for data creation and editing
