# dax-maintainable-business-logic

<img src="https://github.com/amolhatwar/dax-maintainable-business-logic/blob/e52d01c6e312928f76bb6f82d75f7eafb9f773eb/dax-maintainable-business-logic.png" width="600">

---

When building Power BI reports, business logic often starts simple.

Over time, new requirements are added:

- New customer categories
- New KPI statuses
- New risk levels
- New performance bands

Many developers solve this by adding more nested IF statements.

While this works, formulas can become difficult to read, test, and maintain.

This repository demonstrates when to use IF and when SWITCH is a better choice for organizing business logic.

---

# Why This Matters

A formula is not finished when it works.

A formula is finished when another analyst can understand and maintain it months later.

The goal of this project is to promote maintainable DAX development rather than simply comparing syntax.

---

# IF Function

Use IF when there are only two possible outcomes.

# Example

```DAX
Status =
IF(
    [Sales] >= [Target],
    "Achieved",
    "Not Achieved"
)
```

# Best Use Cases

- Yes / No decisions
- Pass / Fail results
- Simple validations
- Binary business rules

---

# SWITCH Function

Use SWITCH when multiple outcomes need to be evaluated.

# Example

```DAX
Risk Category =
SWITCH(
    TRUE(),
    [Revenue] > 100000, "Low Risk",
    [Revenue] > 50000, "Medium Risk",
    [Revenue] > 10000, "High Risk",
    "Critical Risk"
)
```

# Best Use Cases

- Customer Segmentation
- Risk Classification
- KPI Status
- Product Categories
- Performance Ratings

---

# Real-World Business Problem

Imagine a dashboard that classifies customers into categories.

Initially:

- Gold
- Silver
- Bronze

A few months later, the business requests:

- Platinum
- Gold
- Silver
- Bronze
- New Customer

Updating a SWITCH statement is generally easier than maintaining a long chain of nested IF statements.

---

# Common Questions

# Should SWITCH replace IF?

No.

IF is ideal for simple TRUE/FALSE decisions.

SWITCH is more suitable when multiple outcomes must be managed.

---

# Is SWITCH faster than IF?

Performance differences are often less important than readability and maintainability.

The primary benefit of SWITCH is cleaner business logic.

---

# Key Takeaways

- Use IF for simple conditions.
- Use SWITCH for multiple outcomes.
- Focus on maintainability.
- Write DAX that future analysts can understand.
- Business requirements change, so formulas should be easy to update.

---

# Skills Demonstrated

- Power BI
- DAX
- Business Logic Design
- Data Analytics

---

Amol Hatwar
Excel | DAX | Data Analytics

📬 Contact Me
If you’d like to collaborate, discuss a project, or simply connect — I’m always open.

🌍 🔗 [Portfolio Website](https://amolhatwar.github.io)
🐙🔗 [GitHub](https://github.com/amolhatwar)
💼 🔗 [LinkedIn](https://www.linkedin.com/in/amolhatwar)

---

⭐ If you found this project useful, consider giving it a star.
