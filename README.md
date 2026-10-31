# Swiggy-data-analysis
<div align="center">

# 🍽️ Swiggy Restaurant Analytics & Q&A Chatbot

**Clean the data. Find the insights. Just ask.**

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B?logo=streamlit&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-xAI%20Grok-1C3C3C)

</div>

---

## 📌 About

An end-to-end analytics project on **118 Swiggy restaurants** across Bangalore (Koramangala, BTM, HSR, Jayanagar):

1. 🧹 **Clean** raw data (broken ₹ symbols, missing ratings, messy locations)
2. 📊 **Analyze** KPIs and visualize them in a **Power BI dashboard**
3. 🤖 **Chat** with the data using a Streamlit Q&A bot powered by **Grok (xAI)**

## 📈 Highlights

| Restaurants | Avg Rating | Avg Cost for Two | Rated ≥ 4.0 |
|:-----------:|:----------:|:----------------:|:-----------:|
| **118** | **4.10 ⭐** | **₹321** | **78%** |

- 📍 Koramangala has the most restaurants (64), followed by BTM (35) and HSR (18)
- 💰 HSR is the priciest area (~₹389); Koramangala is the most affordable (~₹298)
- 🏆 Top rated: Khichdi Experiment (4.8)

## 📁 Project Structure

```
├── swiggy.xls                       # Raw data
├── swiggy_cleaned.csv               # Cleaned data
├── Swiggy_Data_Cleaning_KPIs.ipynb  # Cleaning + KPI analysis
├── Swiggy.pbix                      # Power BI dashboard
├── swiggy_chatbot_app.py            # Streamlit chatbot
├── Swiggy_QA_Chatbot.ipynb          # Notebook chatbot
└── requirements.txt
```

## 🚀 Quick Start

```bash
# Install
pip install -r requirements.txt

# Run the chatbot
streamlit run swiggy_chatbot_app.py
```

Then paste your [xAI API key](https://console.x.ai/) in the sidebar and start asking.

> To run the cleaning notebook, also `pip install xlrd openpyxl matplotlib seaborn` and update the `/workspace/...` file paths to local ones.

## 💬 Try Asking

- *Highest rated restaurants in Koramangala?*
- *Biryani places under Rs.400*
- *Best value North Indian restaurants*
- *Compare biryani options in Koramangala vs BTM*

## 🧠 How the Chatbot Works

```
Question → Keyword retrieval (top-k restaurants) → Prompt → Grok → Answer
```

Each restaurant is turned into a text chunk, the most relevant ones are retrieved, and Grok answers using only that data.

## ⚠️ Limitations

- Keyword retrieval isn't semantic, and only the top 10–12 matches reach the model, so "average" / "how many" questions may be approximate.
- Data is a point-in-time snapshot.

## 🔮 Roadmap

- [ ] Pandas-based aggregation for exact counts and averages
- [ ] Embedding-based semantic search
- [ ] Docker + Streamlit Cloud deployment

---

<div align="center">

*Educational project. Not affiliated with Swiggy.*

</div>
