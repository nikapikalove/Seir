# Seir: From Narrative to Network: A Spatio-Temporal GIS Analysis of the Prophetic Sira

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

This repository contains the data, GIS analysis files, and code for the research project, "From Narrative to Network." We transform the classic narrative of the Prophet's life (Sira) from a linear text into a dynamic, multi-dimensional spatio-temporal network.

By leveraging Geographic Information Systems (GIS) and Spatial Network Analysis, this project moves beyond *what* happened to explore *how and why it happened spatially*, revealing the geographical logic and logistical complexity of the early Islamic state.

---

## 📖 Table of Contents
*   [About the Project](#about-the-project)
*   [Key Features](#key-features)
*   [Technology Stack](#technology-stack)
*   [The Geodatabase](#the-geodatabase)
*   [Installation & Setup](#installation--setup)
*   [How to Replicate the Analysis](#how-to-replicate-the-analysis)
*   [Project Structure](#project-structure)
*   [Key Findings & Visualizations](#key-findings--visualizations)
*   [How to Cite This Work](#how-to-cite-this-work)
*   [License](#license)
*   [Contact](#contact)

---

## 🌟 About the Project

Traditional studies of the Prophetic Sira, while invaluable, are often constrained by a "narrative paradigm." They present events in a linear, chronological sequence, treating geography as a passive backdrop rather than an active agent in history.

This project challenges that paradigm by building a comprehensive **Spatio-Temporal Geodatabase** of all major "movement events" (raids, expeditions, missions, and migrations) documented in classical sources. Using advanced spatial analysis, we model these events as a growing network, allowing for a quantitative understanding of the early Muslim community's expansion, strategic priorities, and logistical capabilities.

The result is a "deep map" of the Sira—an interactive, data-driven model that can be queried and analyzed to answer questions that were previously impossible to address.

---

## ✨ Key Features

1.  **🗺️ Spatio-Temporal Geodatabase:** A meticulously researched and georeferenced database of hundreds of events from the Sira. It serves as an open-source foundation for future digital Islamic humanities research.
2.  **📈 Quantitative Spatial & Network Analysis:** We applied a suite of analytical techniques to uncover hidden patterns:
    *   **Hotspot Analysis:** To identify geographical clusters of intense activity.
    *   **Spatial Network Analysis:** To measure the evolving **centrality** of Madinah as the hub of the nascent state.
    *   **Spatial Correlation:** To statistically test the relationship between movement paths and known historical trade routes.
3.  **⏳ Interactive Time-Lapse Visualization:** A dynamic web map that visualizes the growth of the network year by year, allowing users to explore the spatial unfolding of the Sira.

---

## 🛠️ Technology Stack

*   **GIS Software:** ArcGIS Pro / QGIS
*   **Data Processing & Analysis:** Python (GeoPandas, Pandas, NetworkX)
*   **Geodatabase Format:** Esri File Geodatabase / GeoPackage
*   **Interactive Web Map:** Leaflet.js / Mapbox GL JS
*   **Analysis Environment:** Jupyter Notebooks

---

## 🗃️ The Geodatabase

The core of this project is a comprehensive geodatabase (`sira_events.gdb` / `sira_events.gpkg`) containing point and line features for each documented event.

**Key Attributes for Each Event:**
*   `Event_Name`: The name of the expedition, raid, or migration.
*   `Event_Type`: (e.g., Ghazwa, Sariyya, Hijra).
*   `Date_Start` / `Date_End`: The precise or estimated dates.
*   `Source_Text`: The primary historical source (e.g., Ibn Ishaq, Al-Waqidi).
*   `Geographic_Confidence`: The confidence level of the georeferenced location (Confirmed, Probable, Possible).
*   `Path_Geometry`: The reconstructed route for events involving travel.

Primary sources for data extraction included *Sirat Ibn Ishaq*, Al-Waqidi's *Kitab al-Maghazi*, and historical geographical dictionaries like Yaqut al-Hamawi's *Mu'jam al-Buldan*.

---

## ⚙️ Installation & Setup

To explore the analysis code, you will need a Python environment with geospatial capabilities.

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/your-username/sira-spatial-network.git
    cd sira-spatial-network
    ```
2.  **Create a Conda environment (recommended for handling GIS libraries):**
    ```sh
    conda create -n sira_gis python=3.9
    conda activate sira_gis
    ```
3.  **Install the required packages:**
    ```sh
    conda install -c conda-forge geopandas pandas networkx jupyterlab
    ```

---

## 🚀 How to Replicate the Analysis

1.  **Explore the Geodatabase:** Open the project's GIS files (e.g., `.aprx`, `.qgz`) or the geodatabase in the `/geodatabase` directory using your preferred GIS software.
2.  **Run the Analysis Notebooks:** Launch Jupyter Lab (`jupyter lab`) and navigate to the `/notebooks` directory. The notebooks are structured to follow the research workflow:
    *   `1_Data_Preparation.ipynb`: Shows how the raw data was cleaned and prepared for analysis.
    *   `2_Spatial_Pattern_Analysis.ipynb`: Contains the hotspot and point pattern analysis.
    *   `3_Network_Centrality_Analysis.ipynb`: Details the construction of the network and the calculation of centrality metrics over time.

---

## 📁 Project Structure

```
sira-spatial-network/
├── geodatabase/
│   └── sira_events.gpkg          # The primary geodatabase file
│
├── notebooks/
│   ├── 1_Data_Preparation.ipynb
│   ├── 2_Spatial_Pattern_Analysis.ipynb
│   └── 3_Network_Centrality_Analysis.ipynb
│
├── web_visualization/
│   ├── index.html
│   └── data/
│       └── events.geojson        # Data for the interactive map
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🔬 Key Findings & Visualizations

Our analysis provides data-driven insights into the strategic geography of the Sira.

*   **The Network of Influence:** The analysis quantitatively demonstrates the rapid growth of Madinah's **centrality**. It evolved from an isolated node into the dominant hub of a vast and complex network in less than a decade.
*   **Corridors of Movement:** Statistical analysis confirms a strong spatial correlation between prophetic movements and the major trade routes of the Hejaz, suggesting a deliberate strategy to secure and control vital economic arteries.
*   **Interactive Sira Map:** The project's primary output is a dynamic map that allows users to filter events by year and type, providing an intuitive and powerful tool for exploring the spatial history of early Islam.

![Interactive Sira Map](https://via.placeholder.com/800x450.png?text=Interactive+Spatio-Temporal+Map+of+the+Sira)
*(This is a placeholder. Replace it with a screenshot of your interactive map.)*

---

## ✍️ How to Cite This Work

If you use the dataset or methodology from this project in your research, please cite our publication:

> [Your Name/Team Name]. (Year). "From Narrative to Network: A Spatio-Temporal GIS Analysis of the Prophetic Sira". *Journal of Digital Humanities / Historical Geography*, Volume(Issue), pp. Page-Numbers. [DOI/URL]

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

**Principal Investigator:** [Your Name] – [youremail@example.com]

Project Link: [https://github.com/your-username/sira-spatial-network](https://github.com/your-username/sira-spatial-network)
