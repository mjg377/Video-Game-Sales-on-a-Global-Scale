# Video-Game-Sales-on-a-Global-Scale
Business analysis of global video game sales with a focus on Nintendo’s performance, market trends, and competitor insights.
This project analyzes a dataset of 16,598 video game sales records across platforms, publishers, and regions.  
The goal is to explore **Nintendo's performance** in the global gaming market, compare it with competitors, and highlight business insights.

## Dataset
Source: Kaggle (Video Game Sales)  
- 16,598 records, cleaned to remove incomplete entries.  
- Features: Name, Platform, Year, Genre, Publisher, Regional Sales, Global Sales.  

## Key Business Questions
1. How does Nintendo compare to Sony and Microsoft in global sales?  
2. Which genres and platforms drive Nintendo’s success?  
3. Which regions contribute most to Nintendo’s sales?  
4. What trends emerge over time for Nintendo consoles?  

## Project Structure
- `data_cleaning_vgsales.ipynb` – Preparing and cleaning the dataset.  
- `EDA_Nintendo_insights.ipynb` – Exploratory analysis of Nintendo vs competitors.  
- `figures`folder – Business-focused charts and dashboards.
- `modeling.ipynb` - Logistic and Random Forest Regression models with Confusion Matrix visuals and Results

## Tools
- Python (pandas, matplotlib, seaborn, plotly)  
- Jupyter Notebooks  

## Modeling
## 🤖 Predictive Modeling — Hit Game Classification

To predict whether a game would sell more than **1M copies globally**, I compared two models: **Logistic Regression** and **Random Forest**.

### Model Performance

| Metric | Logistic Regression | Random Forest |
|-------|------------------|-------------|
| Accuracy | 0.61 | **0.70** |
| Precision (Hit) | 0.19 | **0.22** |
| Recall (Hit) | **0.67** | 0.54 |
| F1-Score (Hit) | 0.30 | **0.31** |
| ROC-AUC | **0.70** | 0.68 |

### Key Insights
- Logistic Regression achieved **higher recall** (caught more hits), but at the cost of very low precision and overall accuracy.
- Random Forest provided a **better balance** of precision, recall, and accuracy, making it the preferred model.
- **Feature importance** analysis showed that Platform, Genre, and Year strongly influence a game’s likelihood of being a hit, with platforms like Wii and DS dominating.

### Final Model Selection
**Random Forest** was chosen as the final model because it generalizes better and offers interpretable attribute importances that support business decisions.

### Business Takeaways
- **Platform choice is critical**: Nintendo’s most successful periods align with strong console cycles (Wii, DS).
- **Genre strategy matters**: Platform and Role-Playing titles drive the bulk of hit games.
- This model can be used as a **screening tool** to flag potential hits for further marketing or production investment.

