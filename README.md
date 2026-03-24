# 🌡️ SST Datasets — Plot and Comparison

A Jupyter Notebook for loading, visualizing, and comparing **Sea Surface Temperature (SST)** data from two satellite-based sources: **TMI (TRMM Microwave Imager)** and **Aqua MODIS**, over the Indian Ocean region.

---

## 📌 Overview

This notebook:

1. Loads SST data from two NetCDF sources — TMI and Aqua MODIS
2. Subsets the data to the **Indian Ocean region** (40°E–100°E, 10°S–30°N)
3. Visualizes SST fields using `viridis` colormap with calibrated colorbars
4. Compares the two datasets spatially and visually

---

## 🛰️ Datasets Used

| Dataset | Sensor | Resolution | File Format |
|---|---|---|---|
| **TMI SST** | TRMM Microwave Imager (F12) | ~0.25° (~25 km) | NetCDF (`.nc`) |
| **Aqua MODIS SST** | Aqua MODIS Level-3 Daily | ~4 km | NetCDF (`.nc`) |

- **TMI file**: `f12_20060124v7.nc` — Contains ascending pass SST on a 720×1440 global grid
- **MODIS file**: `AQUA_MODIS.20060124.L3m.DAY.SST.sst.4km.nc` — Daily Level-3 mapped SST product

> Both files correspond to **24 January 2006**.

---

## 🗺️ Study Region

| Parameter | Value |
|---|---|
| Longitude | 40°E – 100°E |
| Latitude | 10°S – 30°N |
| Region | **Indian Ocean** |

---

## 📁 Repository Structure

```
goruu007-SST-datasets-Plot-and-Comparison/
│
└── SST_datasets_Plot_and_Comparison.ipynb   # Main analysis notebook
```

---

## 🛠️ Requirements

- Python 3.7+
- Jupyter Notebook / Google Colab
- xarray
- matplotlib
- numpy

Install dependencies:

```bash
pip install xarray matplotlib numpy netCDF4
```

---

## 🚀 Usage

1. Clone the repository:

```bash
git clone https://github.com/goruu007/goruu007-SST-datasets-Plot-and-Comparison.git
```

2. Open the notebook in Jupyter or Google Colab.

3. Update the file paths at the top of the notebook to point to your local copies of the TMI and MODIS NetCDF files:

```python
file_path   = '/path/to/f12_20060124v7.nc'         # TMI SST
file2_path  = '/path/to/AQUA_MODIS.20060124...nc'   # Aqua MODIS SST
```

4. Run all cells.

---

## 📊 Output

The notebook produces:

- **TMI SST map** — Sea Surface Temperature (in Kelvin) over the Indian Ocean from the TMI sensor
- **MODIS SST map** — Higher-resolution SST from Aqua MODIS for the same region and date
- **Side-by-side visual comparison** of both products

---

## 📐 Notes on the Data

- TMI SST is retrieved via **passive microwave** sensing, which can see through clouds but has lower spatial resolution (~25 km)
- MODIS SST is retrieved via **thermal infrared**, offering much higher resolution (~4 km) but is blocked by cloud cover
- Comparing these two products highlights the trade-off between **coverage** (TMI) and **resolution** (MODIS)

---

## 🙏 Acknowledgements

- TMI data provided by **Remote Sensing Systems (RSS)**
- MODIS data provided by **NASA Ocean Biology Processing Group (OBPG)**
- Developed at **SAC ISRO**, Ahmedabad

---

## 📄 License

MIT License
