# 👁 Littlerome AI Vision — Streamlit App

Pipeline defect detection powered by **YOLOv11 Ensemble** (5 dedicated models)

## 🧠 Detection Models

| ไฟล์ | Class | คำอธิบาย |
|------|-------|---------|
| `Pipeline_Legit_Best_Model.pt` | pipeline_legit ✅ | ท่อปกติ |
| `water_leak_best.pt` | water_leak 💧 | น้ำรั่ว |
| `PipeCrack.pt` | pipe_crack 🔧 | ท่อแตก/ร้าว |
| `Flame_Best_Model.pt` | flame 🔥 | เพลิงไหม้ |
| `Corrosion_Best_Model.pt` | corrosion ⚠️ | สนิม/กัดกร่อน |

---

## 📁 โครงสร้าง Repository

```
littlerome/
├── app.py                          ← Streamlit app หลัก
├── requirements.txt                ← Python dependencies
├── packages.txt                    ← System dependencies (Streamlit Cloud)
├── README.md
├── .streamlit/
│   └── config.toml                 ← Dark theme config
│
├── Pipeline_Legit_Best_Model.pt    ← Model 1
├── water_leak_best.pt              ← Model 2
├── PipeCrack.pt                    ← Model 3
├── Flame_Best_Model.pt             ← Model 4
└── Corrosion_Best_Model.pt         ← Model 5
```

---

## 🚀 Deploy บน Streamlit Cloud

1. Push ทุกไฟล์ขึ้น GitHub (รวม .pt ทั้ง 5 ไฟล์)
2. ไป [share.streamlit.io](https://share.streamlit.io) → **New app**
3. เลือก repo → Main file = `app.py`
4. กด **Deploy**

---

## 💻 รันในเครื่อง

```bash
pip install -r requirements.txt
streamlit run app.py
```

---

## 🗂 Features

| Tab | รายละเอียด |
|-----|-----------|
| 📊 Dashboard | KPI, defect breakdown, system status |
| 📷 Live Camera | Webcam → detect ทันที |
| 🖼 Upload Image | วิเคราะห์รูป + download ผล |
| 🎬 Upload Video | Frame-by-frame + timeline |
| 📋 History | Log + export CSV |
| ⚙️ Settings | Threshold, alerts, ensemble status |
