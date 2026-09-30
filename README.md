# Teaching Python for Geography (ไพทอนเบื้องต้นสำหรับภูมิศาสตร์)

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white) ![Colab](https://img.shields.io/badge/Google-Colab-F9AB00?logo=googlecolab&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy) ![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas) ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C) ![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A)

> **แบบเรียนเชิงปฏิบัติการ การเขียนโปรแกรม Python เบื้องต้นสำหรับนิสิตภูมิศาสตร์ชั้นปีที่ 2** ใช้ข้อมูลสถานีวัดน้ำฝนภาคเหนือเป็นกรณีศึกษาตลอดรายวิชา ตั้งแต่ตัวแปรตัวแรกจนถึงแผนที่เส้นชั้นน้ำฝน ทุก Notebook รันบน Google Colab ได้ทันทีโดยไม่ต้องติดตั้งโปรแกรม

---

## Course philosophy

```
คำถามทางภูมิศาสตร์  →  ข้อมูล (ตาราง / จุด / พื้นที่ / กริด)  →  Python
        ↑                                                         ↓
   การตีความ  ←  แผนที่ / กราฟ  ←  สรุปสถิติ  ←  ทำความสะอาดข้อมูล
```

หลักการที่ใช้ตลอดรายวิชา
- **ค่าที่สถานี ≠ ค่าของทั้งพื้นที่** (ต้องประมาณค่าเชิงพื้นที่ และมีความไม่แน่นอน)
- **EPSG:4326 (องศา) ≠ หน่วยวัดระยะ** → วัดระยะ/พื้นที่ต้องแปลงเป็น UTM
- **ค่าว่าง ≠ ศูนย์** → ต้องตัดสินใจและบันทึกวิธีจัดการอย่างโปร่งใส
- **Correlation ≠ Causation**
- **แผนที่สวย ≠ ผลที่ถูกต้อง** → ต้องตรวจสอบ (validation) เสมอ

ทุก Notebook มีแบบฝึกหัด 3 ระดับ: 🟢 ง่าย · 🟡 ปานกลาง · 🔴 ยาก

---

## Notebooks

| No. | Notebook | ระดับ | เนื้อหาหลัก | ผลการเรียนรู้ | Open |
|---|---|---|---|---|---|
| **00** | **เตรียม Colab + GitHub**<br>`00_Setup_Colab_and_GitHub.ipynb` | 🟢 | Colab, git clone, อัปโหลดไฟล์, Google Drive | รันโค้ดและดึงข้อมูลจาก GitHub ได้ | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/apichayaice7835-png/Teach-Python-Geography/blob/main/00_Setup_Colab_and_GitHub.ipynb) |
| **01** | **พื้นฐาน Python ผ่านโจทย์ภูมิศาสตร์**<br>`01_Python_Basics_for_Geography.ipynb` | 🟢→🟡 | ตัวแปร, list, dict, loop, if, function, DMS→DD, Haversine | เขียนฟังก์ชันคำนวณเชิงภูมิศาสตร์อย่างง่ายได้ | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/apichayaice7835-png/Teach-Python-Geography/blob/main/01_Python_Basics_for_Geography.ipynb) |
| **02** | **NumPy กับกริดเชิงพื้นที่**<br>`02_NumPy_for_Spatial_Data.ipynb` | 🟢→🔴 | array, mask, axis, broadcasting, meshgrid, DEM, slope, lapse rate | คำนวณข้อมูลแบบ raster ด้วย array ได้ | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/apichayaice7835-png/Teach-Python-Geography/blob/main/02_NumPy_for_Spatial_Data.ipynb) |
| **03** | **Pandas จัดการข้อมูลสถานีฝน**<br>`03_Pandas_Rainfall_Stations.ipynb` | 🟡→🔴 | read_csv, datetime, missing values, merge, groupby, pivot_table, anomaly | ทำความสะอาดและสรุปข้อมูลฝนรายสถานีได้ | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/apichayaice7835-png/Teach-Python-Geography/blob/main/03_Pandas_Rainfall_Stations.ipynb) |
| **04** | **กราฟภูมิอากาศ**<br>`04_Matplotlib_Climate_Graphs.ipynb` | 🟢→🔴 | line, bar, climograph (twinx), boxplot, small multiples, rolling mean, savefig | สร้างกราฟพร้อมใช้ในรายงานได้ | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/apichayaice7835-png/Teach-Python-Geography/blob/main/04_Matplotlib_Climate_Graphs.ipynb) |
| **05** | **สถานี + ขอบเขตด้วย GeoPandas**<br>`05_Stations_and_Boundaries_GeoPandas.ipynb` | 🟡→🔴 | points_from_xy, CRS/UTM, sjoin, buffer, distance, choropleth, export GPKG | นำเข้าตำแหน่งสถานีและ shapefile แล้วทำแผนที่ได้ | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/apichayaice7835-png/Teach-Python-Geography/blob/main/05_Stations_and_Boundaries_GeoPandas.ipynb) |
| **06** | **ประมาณค่าฝนเชิงพื้นที่**<br>`06_Rainfall_Interpolation_IDW_Thiessen.ipynb` | 🔴 | Thiessen/Voronoi, IDW (เขียนเอง), isohyet, LOOCV, overlay | ประมาณฝนเฉลี่ยพื้นที่และประเมินความถูกต้องได้ | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/apichayaice7835-png/Teach-Python-Geography/blob/main/06_Rainfall_Interpolation_IDW_Thiessen.ipynb) |
| **07** | **Mini Project**<br>`07_Mini_Project_Template.ipynb` | 🟡→🔴 | รวมทุกทักษะ | ตั้งคำถาม วิเคราะห์ และตีความได้ด้วยตนเอง | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/apichayaice7835-png/Teach-Python-Geography/blob/main/07_Mini_Project_Template.ipynb) |

### ลำดับการเรียนที่แนะนำ (15 สัปดาห์)
| สัปดาห์ | Notebook | หมายเหตุ |
|---|---|---|
| 1 | 00 | ติดตั้ง/สมัคร GitHub, fork repo |
| 2–4 | 01 | พื้นฐาน Python (ช้า ๆ ทำแบบฝึกหัดในห้อง) |
| 5–6 | 02 | NumPy + DEM |
| 7–8 | 03 | Pandas + ข้อมูลฝน |
| 9 | สอบกลางภาค | |
| 10–11 | 04 | กราฟภูมิอากาศ |
| 12–13 | 05 | GeoPandas + แผนที่ |
| 14 | 06 | Interpolation (เสริมสำหรับกลุ่มเก่ง หรือบรรยายสาธิต) |
| 15 | 07 | นำเสนอ Mini Project |

---

## Data

| ไฟล์ | คำอธิบาย |
|---|---|
| `data/rain_stations_north.csv` | ตำแหน่งสถานีตัวอย่าง 16 แห่งใน 9 จังหวัดภาคเหนือ: `station_id, name_th, name_en, province, lat, lon, elev_m` |
| `data/rain_monthly_2020_2024.csv` | ฝนรวมรายเดือนและอุณหภูมิเฉลี่ยรายเดือน 2020–2024: `station_id, date, rain_mm, tmean_c` (มีค่าว่าง ~2% โดยตั้งใจ) |

> ⚠️ **ข้อมูลฝนเป็นข้อมูลจำลองเพื่อการสอน** พิกัดใกล้เคียงอำเภอจริง แต่ค่าฝน/อุณหภูมิสร้างจากแบบจำลองตามลักษณะภูมิอากาศภาคเหนือ **ห้ามนำไปอ้างอิงทางวิชาการ**
> ต้องการใช้ข้อมูลจริง: ขอจากกรมอุตุนิยมวิทยา / กรมชลประทาน / สสน. (thaiwater.net) แล้วจัดคอลัมน์ให้ตรงกับตารางข้างบน โค้ดทุก Notebook จะใช้ได้ทันที

**ขอบเขตจังหวัด** ใน Notebook 05–06 อ่านจาก GeoJSON สาธารณะ `apisit/thailand.json` บน GitHub หากต้องการให้แบบเรียนไม่พึ่งลิงก์ภายนอก ให้นำไฟล์ขอบเขตของตนเอง (เช่น จากกรมการปกครอง หรือ GISTDA) มาบันทึกเป็น `data/thailand_provinces.geojson` (ตรวจสอบเงื่อนไขการเผยแพร่ของแหล่งข้อมูลก่อน) โค้ดจะเลือกใช้ไฟล์ในเครื่องก่อนเสมอ

### ใช้ไฟล์ของตนเอง
| ต้องการนำเข้า | รูปแบบที่รองรับ | ดู Notebook |
|---|---|---|
| ตำแหน่งสถานีวัดน้ำฝน | `.csv` / `.xlsx` ที่มีคอลัมน์ lat, lon (หรือ E, N แบบ UTM) | 03, 05 |
| ขอบเขตการปกครอง / ลุ่มน้ำ | Shapefile บีบอัด `.zip`, `.geojson`, `.gpkg` | 05, 06 |

---

## How students should use this repository

**Option A — เรียนอย่างเดียว:** กด **Open in Colab** → รันจากบนลงล่าง → *File → Save a copy in Drive*

**Option B — เก็บงานใน GitHub ของตนเอง (แนะนำ)**
1. กด **Fork** repository นี้
2. เปิด Notebook ด้วยปุ่ม Colab
3. *File → Save a copy in GitHub* → เลือก `ชื่อนิสิต/Teach-Python-Geography`
4. ส่งลิงก์ Notebook ใน fork ของตนเองเป็นงาน

---

## Troubleshooting
| อาการ | วิธีแก้ |
|---|---|
| ตัวอักษรไทยในกราฟเป็น □□□ | รันเซลล์ `setup_thai_font()` ด้านบนของ Notebook ก่อน |
| Colab badge ขึ้น *Notebook not found* | ชื่อไฟล์ใน URL ต้องตรงกับ GitHub ทุกตัวอักษร และ repo ต้องเป็น Public |
| อ่าน CSV ภาษาไทยแล้วเพี้ยน | `pd.read_csv(..., encoding="cp874")` หรือ `"utf-8-sig"` |
| จุดสถานีไปอยู่ผิดที่ | สลับ lat/lon → `points_from_xy(lon, lat)` |
| ชั้นข้อมูลไม่ซ้อนกัน | CRS ไม่ตรงกัน → `to_crs()` |

## Repository structure
```
Teach-Python-Geography/
├── README.md
├── 00_Setup_Colab_and_GitHub.ipynb
├── 01_Python_Basics_for_Geography.ipynb
├── 02_NumPy_for_Spatial_Data.ipynb
├── 03_Pandas_Rainfall_Stations.ipynb
├── 04_Matplotlib_Climate_Graphs.ipynb
├── 05_Stations_and_Boundaries_GeoPandas.ipynb
├── 06_Rainfall_Interpolation_IDW_Thiessen.ipynb
├── 07_Mini_Project_Template.ipynb
└── data/
    ├── rain_stations_north.csv
    └── rain_monthly_2020_2024.csv
```

## References
[NumPy](https://numpy.org/doc/) · [Pandas](https://pandas.pydata.org/docs/) · [Matplotlib](https://matplotlib.org/stable/) · [GeoPandas](https://geopandas.org/) · [Shapely](https://shapely.readthedocs.io/) · [Google Colab](https://colab.research.google.com/)

แนวทางการออกแบบ README ได้รับแรงบันดาลใจจาก [nattaponm/Teach-Urban-RS](https://github.com/nattaponm/Teach-Urban-RS)
