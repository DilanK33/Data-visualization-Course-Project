# 📊 Salary Data Analysis

This project explores salary trends based on different factors such as **years of experience, age, and education level**. Using **Python, Pandas, NumPy, Matplotlib, and Seaborn**, this analysis visualizes salary patterns and provides insights into how different attributes impact earnings.  

## 📂 Dataset

The dataset (`Salary Data.csv`) contains the following columns:  
- **Age** 📅  
- **Gender** 🚻  
- **Education Level** 🎓  
- **Job Title** 💼  
- **Years of Experience** 📈  
- **Salary** 💰  

## 🔍 Objectives
- Understand how **years of experience** impact salary.  
- Analyze the correlation between **age and salary**.  
- Identify the **top earners** and their education levels.  
- Compare **average salaries** based on **education levels**.  

---

## 📌 Key Analyses

### 1️⃣ Salary vs. Years of Experience
- A **scatter plot** visualizes the relationship between **years of experience** and **salary**.  
- A **trend line** (linear regression) is added to highlight the correlation.  

**Code snippet:**
```python
plt.scatter(df["Years of Experience"], df["Salary"], color="black", label="Salary vs Experience")
slope, intercept = np.polyfit(df["Years of Experience"], df["Salary"], 1)
plt.plot(df["Years of Experience"], slope * df["Years of Experience"] + intercept, color='red', label='Trend Line')
plt.legend()
plt.show()
