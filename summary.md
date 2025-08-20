# Summary of Findings

**Objective.** Measure students' adaptability to online education and analyse associated factors.

**Data.** 1,205 records, 14 variables: demographics (age, gender), institution level & type, IT-student status, town location, load shedding level, family financial condition, internet type, device used, network type, daily class duration, institution's LMS availability, and the target (adaptability level).

**Approach.**
- Encoded categorical variables and the 3-class target.
- Trained Decision Tree and Linear SVM; evaluated with accuracy, precision, recall, F1; drew ROC curves.
- Used LIME to interpret feature influence.

**Headline results.**
- Decision Tree ≈ 91.2% accuracy; SVM ≈ 74% accuracy.
- Influential features included institution type and LMS availability; others: class duration, IT-student status, age, internet type, financial condition, education level, network type.

**Implication.**
Institutions can improve adaptability by ensuring robust LMS access, better connectivity, and targeted support (tech assistance, time management, equitable device/internet access).