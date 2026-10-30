# UAV Flight Data Analysis & Interactive WebGIS Dashboard

An interactive, web-based geospatial decision support dashboard designed to analyze, visualize, and simulate UAV flight telemetry and photogrammetric survey missions. 

This project transforms raw flight logs (GPS/IMU) and sequential aerial exposures into an intuitive mission control platform, featuring real-time flight playback, orientation angles, dynamic telemetry popups, and photogrammetric footprint overlaps.

---

## Interface & Key Features

### Flight Trajectory & Photogrammetric Overlap (Footprints)
Plots the complete mission route with directional markers, capture points, and computed ground footprint polygons to inspect coverage and forward/side overlaps.

<p align="center">
  <img src="assets/flight-path.png" alt="Flight Path and Exposure Points" width="48%">
  <img src="assets/footprints-overlap.png" alt="Photogrammetric Overlap and Footprints" width="48%">
</p>

- **Mission Waypoints:** Interactive vector path highlighting exposure locations, capture order, and heading direction.
- **Footprint Coverage:** Bounding polygon layers displaying the spatial coverage and overlap of each aerial photo frame.

---

### Telemetry Inspection & Mission Summary
Clicking on any exposure point triggers detailed telemetry inspection cards alongside overall mission statistics.

<p align="center">
  <img src="assets/popup-trigger.png" alt="Exposure Node Selection" width="28%">
  <img src="assets/telemetry-card.png" alt="Telemetry Data and Image Preview" width="38%">
  <img src="assets/mission-summary.png" alt="Flight Summary Card" width="30%">
</p>

- **Exposure Popups:** Real-time access to camera altitude, GPS coordinates, spatial orientation parameters (**Roll, Pitch, Yaw**), and high-resolution aerial photo previews.
- **Flight Summary HUD:** Live dashboard panel reporting total exposure count, average flight altitude, altitude ranges, and flight model classification.

---

### Timeline Simulation & Spatial GIS Controls
Interactive playback controls simulate the flight mission along with full GIS navigation utilities.

<p align="center">
  <img src="assets/timeline-player.png" alt="Flight Timeline Player" width="95%">
</p>

<p align="center">
  <img src="assets/gis-toolbar.png" alt="Measurement and Drawing Tools" width="16%">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="assets/layer-control.png" alt="Layer and Export Control" width="18%">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="assets/mini-map.png" alt="Mini Map Overview" width="28%">
</p>

- **Timeline Media Player:** Play, pause, scrub, and adjust playback speed (fps) to replay the mission trajectory chronologically.
- **GIS Measurement & Vector Tools:** On-screen distance, area measurement, and vector geometry annotation tools.
- **Layer & Overview Controls:** Toggleable layer manager, spatial data export option, and synchronized overview mini-map.

---

## Tech Stack & Architecture

- **Python 3.x:** Core backend pipeline for flight log ingestion, spatial coordinate transformation, and map compilation.
- **Pandas:** Tabular data processing, timestamp sorting, and statistical telemetry evaluation.
- **Folium & Leaflet.js:** Dynamic tile rendering, custom layer control, vector styling, and GIS plugin integration.
- **HTML5 / CSS3 / Jinja2:** Fully custom dark-mode mission dashboard HUD, custom control widgets, and modal popups overriding default Leaflet UI.

---

## Dataset

The demonstration dataset is derived from a photogrammetric grid flight executed over the **Hacettepe University Beytepe Campus**.
- **Spatial Positioning:** Synchronized GNSS recordings ($X, Y, Z$ / Latitude, Longitude, Ellipsoidal Height).
- **Attitude / IMU Telemetry:** Angular orientation logs ($\omega, \phi, \kappa$ mapped to Roll, Pitch, Yaw).
- **Sensor:** Calibrated onboard camera exposures matching flight timestamp logs.

---

## Getting Started

### Clone the Showcase Repository
```bash
git clone [https://github.com/glzrygt/iha-webgis-dashboard.git](https://github.com/glzrygt/iha-webgis-dashboard.git)
cd iha-webgis-dashboard

### Author
Developed by Gülüzar Yiğit