# Real-Life Gamification Dashboard – Power BI Project

## Technologies Used
- **Database & Data Model**: Power BI Data Model  
- **Data Transformation & Preparation**: Power Query  
- **Data Modeling & Relationships**: Simple relational links between tables (no specific schema model) 
- **DAX**: For calculated measures and KPIs  
- **Data Visualization**: Power BI native visuals & custom visuals (Play Axis)  

---

## 1. Project Overview

### 1.1 Objective & Motivation
The aim of this project is to transform daily life goals into an interactive, gamified experience.  
By tracking personal and professional objectives, the dashboard motivates progress towards a final target level of **100**.  
The design blends **data visualization**, **progress tracking**, and **goal management**, making productivity a dynamic and engaging process.

---

## 2. Data Structure & Tables

The project includes:
- **1 Measure Table**: Central location for all calculated measures.
- **5 Data Tables**:
  1. **date_objectifs** – Dates linked to each objective.
  2. **difficultes** – Records of challenges and potential solutions.
  3. **objectifs** – List of all objectives with their category (Pro or Personal).
  4. **objectif_vacances** – Specific objectives related to planned vacations.
  5. **vacances** – Records of planned vacation dates.
<img width="1930" height="970" alt="organisation_mesures" src="https://github.com/user-attachments/assets/d81780af-27f0-47cc-b0d9-f46702c30774" />

---

## 3. Data Model & Relationships

- The only relationship is a **1-to-1** connection between:
  - **date_objectifs** and **objectifs**
- All other tables are standalone, used for specific visuals and calculations.

<img width="1918" height="1013" alt="relation_pbi" src="https://github.com/user-attachments/assets/b8102029-9a79-4a46-b2b8-dd8ce30cf49b" />

---

## 4. Visualization Components

### 4.1 Key Visuals Used
- **Pie Charts**: Breakdown of objectives by category and by year.
- **Card Visuals**: Display of today’s date, next objective count, remaining vacation days, and current level.
- **Table Visual**: Detailed objectives list with planned dates and validation status.
- **Play Axis + Map Visual**: A **Play Axis slicer** is linked to a map visual, allowing users to scroll through all achieved objectives dynamically.
- **KPI Indicator**: Displays current level progression (Level 0 to 100).

---

## 5. Technical Implementation

### 5.1 DAX Calculations for Level Progression
- **Final Level = Objective Progression**
  - Short-term objectives = **50%** of the level.
  - Medium-term objectives = **25%** of the level.
  - Long-term objectives = **25%** of the level.
- Multiple measures were created for each category of objectives and combined into the **final level** measure.

### 5.2 Measure Table Organization
- Measures are stored in a dedicated **Table de Mesures**.
- Measures are grouped into **folders** for better organization:
  - *Calcul niveau débutant*
  - *Calcul niveau intermédiaire*
  - *Calcul niveau professionnel*
  - *Niveau final*
  - *Jours Restants Vacances*

---

## 6. Features & Insights
- **Dynamic Timeline Navigation** with Play Axis for visualizing achieved objectives.
- **Category-Based Tracking**: Clear separation of professional and personal goals.
- **Level-Based Gamification**: Motivation through progressive scoring.
- **Vacation Tracking**: Integrated countdown for upcoming breaks.
- **Difficulty Log**: Helps identify recurring challenges and plan solutions.
