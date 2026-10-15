**UAV Flight Data Analysis and Interactive WebGIS Dashboard**
This project was developed to analyze flight logs (telemetry) and aerial photographs obtained after UAV photogrammetric flight missions in an interactive WebGIS environment.

The project transforms standard datasets from static tables into a dynamic decision support dashboard that provides a timeline-based flight simulation, real-time orientation angles, and spatial data visualization.

* **Interactive Flight Path:** The UAV's mission route is plotted on the map using GPS coordinates (Latitude/Longitude) and enhanced with directional arrows.
* **Flight Simulation:** The flight moment is simulated on the map using time-series data, offering real-time playback with a custom-designed media player.
* **Telemetry and Exposure Analysis** Each photo point on the map is clickable. Pop-up windows display the following for that specific frame:
  * Original aerial photo preview
  * Shooting altitude (Height)
  * Orientation angles (Roll, Pitch, Yaw)
* **Customized UI/UX:** The default interface of the Folium library has been completely customized using Jinja2 and CSS to create a professional, dark-mode mission control panel (Dashboard).
* **Spatial Awareness (Mini Map):** A small-scale overview map is integrated to ensure spatial context is maintained during detailed inspections.

## Technologies Used

* **Python 3.x:** Data processing and map generation logic.
* **Pandas:** Cleaning, sorting, and statistical analysis of flight logs (CSV/TXT).
* **Folium & Leaflet.js:** Web-based mapping infrastructure, layer management, and plugin integration.
* **HTML5 & CSS3:** Mission panel (Dashboard) and interactive pop-up designs.
## Dataset
The dataset belongs to a photogrammetric grid flight conducted at the Hacettepe University Beytepe Campus. It includes GPS (X, Y, Z) and IMU (Omega, Phi, Kappa / Roll, Pitch, Yaw) data for each photograph.

## How to Run?
Clone the repository to your local machine:
   ```bash
   git clone [https://github.com/glzrygt/iha-webgis-dashboard.git](https://github.com/glzrygt/iha-webgis-dashboard.git)