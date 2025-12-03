# ⚡ Power Plant Capacity & Geospatial Energy Distribution in Indonesia

Project ini menganalisis kapasitas pembangkit listrik dan persebaran energi berdasarkan fuel type di Indonesia menggunakan dataset **Global Power Plant Database**. Analisis difokuskan pada kapasitas energi, distribusi jenis bahan bakar, perbandingan renewable vs fossil, segmentasi kapasitas, serta pemetaan kepemilikan pembangkit.

---

## 📁 Dataset

| File | Deskripsi |
|------|-----------|
| `global_power_plant_indonesia.csv` | Dataset utama pembangkit listrik Indonesia |
| `Global Power Plant Database Indonesia.ipynb` | Notebook analisis, preprocessing & visualisasi |

Dataset memuat:

- 📍 Lokasi (Latitude, Longitude)  
- ⚡ Kapasitas Pembangkit (MW)  
- 🔥 Jenis Energi (Fuel Type)  
- 🌱 Renewable vs Fossil Classification  
- 🏢 Owner/Operator (PLN vs Non-PLN)  
- 📊 Informasi tambahan untuk analisis energi nasional  

---

## 🎯 Objective

Menganalisis kondisi pembangkit listrik Indonesia untuk menjawab:

1. Distribusi pembangkit berdasarkan **fuel type**
2. Kapasitas energi berdasarkan **fuel type**
3. Proporsi energi **Renewable vs Fossil**
4. Segmentasi **capacity size (Small/Medium/Large)**
5. Pemetaan persebaran energi secara geospasial
6. Analisis kepemilikan **PLN vs Non-PLN**

---

## 🔧 Workflow

1. Import dataset  
2. Data Cleansing  
3. Feature Engineering:
   - Renewable/Fossil classification  
   - Capacity segmenting  
4. Exploratory Data Analysis  
5. Visualisasi kapasitas & distribusi energi  

---

## 📊 Key Visualizations

| Visualisasi | Insight |
|------------|---------|
| **Fuel Type Distribution** | Jenis energi paling banyak digunakan |
| **Capacity per Fuel Type** | Fuel mana dengan kapasitas tertinggi |
| **Renewable vs Fossil Comparison** | Seberapa besar kontribusi energi bersih |
| **Capacity Segment (Small/Medium/Large)** | Struktur ukuran pembangkit nasional |
| **Ownership Analysis (PLN vs Non-PLN)** | Pihak dominan dalam aset energi |

Contoh kode:

```python
plt.figure(figsize=(8,5))
df['primary_fuel'].value_counts().plot(kind='bar')
plt.title('Fuel Type Distribution in Indonesia')
plt.xlabel('Fuel Type'); plt.ylabel('Count')
plt.show()
