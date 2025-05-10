# Predicting Student Retention in Higher Education

This project analyzes key factors that influence university student dropout, leveraging a dataset from [Kaggle](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention). The ultimate goal is to understand which variables most significantly impact student retention, and how these factors vary across different academic programs.

## 🎯 Project Objective

The initial goal was to identify the main variables associated with student dropout across a university population. Through analysis, it became clear that different programs (courses) exhibited distinct dropout patterns. This led to a more refined objective: to analyze dropout predictors **by academic course** and visualize the results using **Power BI**.

## 📊 Data Description

The dataset contains 4,424 student records and 35 columns, covering:

- **Demographics**: age, gender, marital status, nationality
- **Academic background**: previous qualification, admission mode/order
- **Socioeconomic indicators**: parents’ education and occupation, whether the student is a debtor, scholarship holder, etc.
- **Academic performance**: grades, approved/evaluated/enrolled subjects in both semesters
- **Macroeconomic variables**: unemployment rate, inflation, GDP
- **Target**: Student status – `Dropout`, `Enrolled`, or `Graduate`

Full description of columns and encodings is available on the [UCI repository page](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success).

## 🧪 Data Preprocessing

Key preprocessing steps included:

- Renaming columns for clarity
- Handling outliers using Z-score and imputation
- Normalizing skewed distributions using log and Box-Cox transformations
- Encoding the target variable numerically:  
  - `Dropout` = 0  
  - `Enrolled` = 1  
  - `Graduate` = 2

## 📈 Analysis & Modeling

1. **Exploratory Analysis**
   - Visualized dropout distribution
   - Evaluated feature correlations with the target
   - Discovered course-specific dropout patterns

2. **Feature Importance**
   - Calculated correlations between features and target, both globally and per course
   - Exported correlations to Excel for Power BI visualization

3. **Machine Learning (e.g., Random Forest)**
   - Trained models to predict dropout risk
   - Evaluated model performance using classification metrics and confusion matrix

## 📊 Power BI Dashboard

Final insights were visualized using Power BI. Each academic course was analyzed individually to identify the most impactful dropout factors. This approach allows institutions to create **tailored intervention strategies**.

## 📂 Files

- `cleaned_student_data.xlsx`: Preprocessed dataset for visualization
- `correlation_by_course_sorted.xlsx`: Course-specific correlation results
- Google Colab notebook (available on request)

---

## 🖥️ How to Run This Project

To replicate the analysis on another machine:

1. **Download or clone this repository**:
   ```bash
   git clone https://github.com/florencia-ogorinsky/Predicting-student-retention-in-higher-education.git
   cd student-retention-analysis
   ```

2. **Open the notebook in Google Colab** or Jupyter. The original project was developed in **Google Colab**.

3. **Install dependencies** if running locally:
   ```bash
   pip install pandas matplotlib seaborn scikit-learn scipy openpyxl
   ```

4. **Run the notebook cells sequentially** to:
   - Load and clean the data
   - Apply transformations
   - Train models and generate visualizations

5. **Visualize results in Power BI** using the exported Excel files.

## 🧠 Why These Factors Matter

Student dropout is a complex phenomenon influenced by a variety of interconnected factors:

- **Academic performance**: Low grades and failure in key subjects are strong indicators of potential dropout.
- **Economic variables**: Financial instability, student debt, and tuition payment issues are common dropout triggers.
- **Demographic factors**: Age, gender, and family situation may correlate with persistence or withdrawal from studies.
- **Institutional integration**: Students who are not engaged with their program or campus environment are more likely to abandon it.
- **External pressures**: High unemployment and inflation can pressure students into joining the workforce early, impacting continuation.
- **Scholarships and support systems**: Having financial or institutional support improves retention rates.

Understanding these influences helps institutions design proactive policies—such as academic mentoring, financial aid, and early intervention strategies—to reduce dropout rates.



## 📌 Conclusion
We observed that in the Distribution of Target Variable chart, the Enrolled category represents only 17% of our dataset. This is critical because these are the students we are most interested in — we want to know how many will graduate and how many will drop out.

To improve prediction accuracy for this group, we would need a larger sample of enrolled students. That would make the model more balanced and enhance its performance on the most relevant class.

Despite this limitation, by splitting the data by academic program, we were still able to uncover meaningful insights about which factors most influence dropout in higher education.

📊 Explore More in Power BI
Head over to my repository to check out the interactive Power BI dashboard, where you can explore how dropout factors vary across different academic programs.
Go find them and dive into the data!



## 🚀 How This Can Help

✅  **University Administrators**: Identify high-risk programs and allocate resources effectively  
✅  **Academic Advisors**: Better understand challenges faced by students in specific programs  
✅  **Researchers**: Study program-specific dropout causes  
✅  **Policy Makers**: Design more targeted retention policies  

## 🔧 How to Improve the Model

🔹 **Program-Specific Models**: Fine-tune models for each academic program  
🔹 **Larger Sample Sizes**: Collect more data for underrepresented programs  
🔹 **More Variables**: Include attendance, grades, socio-economic background, etc.  

These improvements would make the analysis more robust and provide actionable insights to reduce student dropout rates.



## 📌 Author: Florencia Ogorinsky

