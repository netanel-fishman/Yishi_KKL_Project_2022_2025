# Spectral Data

This folder contains the **spectral information** collected during the **Yishi experiment** using a **NanoSpec camera** mounted on a DJI 600 drone.  
A **LIDAR sensor** was also mounted on the drone and collected data during the same flights.

> **Note**: All **raw data** from the NanoSpec camera and the LIDAR sensor is **stored on the Givat Ram cloud server** due to large file sizes.  
> This also includes **Venus satellite images** from multiple dates and locations across Israel.  
> **Cloud path**:  
> `/sci/archive/davidhelman/yaron1205/Drone_Images/David_Tamir_Yishi2022Project_Rawfiles/`

---

## 🛠 Data Processing Notes

- Some files on the cloud are **completely raw** and require **initial processing** using the **SpectralView software**.
- Other files have already been **preprocessed** and are stored in folders labeled `processed`.

---

## ☁️ Cloud Directory Structure

Each flight is represented by a **pair of subfolders**:
- One containing the actual data
- One with the suffix `_dark` for **radiometric calibration**

### Flight Organization
- **Flight 1**: Plot 1
- **Flight 2**: Plots 2, 5, 6
- **Flight 3**: Plots 3–4

### `processed/` folders include:
- `masks/`: NDVI and NIR-based binary masks used to exclude non-canopy pixels
- `trees/`: Polygons of individual tree crowns
- `trees_shapefile/`: A shapefile containing all tree crowns together
- `values/`: Per-tree canopy reflectance summaries (mean, median, min, max, std)

> **Note**: In the polygon and value files, species names are abbreviated:  
> - `quer` = *Quercus* (Oak)  
> - `cyp` = *Cypress*  
> - `cera` = *Ceratonia* (Carob)  
> - `pist` = *Pistacia*

---

## 📁 Local Folder Structure

### `Raw_values/`
- Per-date statistics of reflectance for each tree crown (mean, median, std, min, max), exported from QGIS
- Includes `central_table` files summarizing median/std/max across all dates
> These tables were **not used in the final analysis**

---

### `Processed_values/`
- `central_data_table_2`:  
  The **main dataset** used in the study, combining:
  - Spectral data (just the mean values for all the canopies)
  - LWP measurements
  - LAI data  
    *(Note: LAI was ultimately not used; see the [LAI folder README](../LAI/README.md))*

- `Sg_clean_data`:  
  Spectral data after **Savitzky-Golay smoothing**, including LWP values  
  (see **Methods** section in the paper)

- `Data_Cleaning_LWP.py`:  
  Python script for applying Savitzky-Golay smoothing

---

### `Codes/`
- Python scripts used to:
  - Clean
  - Organize
  - Process the **raw spectral data**

---

### `wavelength`
- A file mapping **camera channel indices** to their corresponding **wavelengths**

---

### `Venus_Satellite_data/`
- Contains **clipped image folders** corresponding to selected sites analyzed in the paper
- Full raw images are stored on the **Givat Ram cloud server**
