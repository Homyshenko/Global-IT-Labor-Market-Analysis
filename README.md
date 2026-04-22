## 📊 Аналіз глобального ринку ІТ-талантів (на основі Stack Overflow Survey)
Дослідження тенденцій професійного розвитку, рівня зарплат та популярності технологій серед розробників у всьому світі.

### Про проєкт
Основна мета цього проєкту — проаналізувати дані найбільшого у світі опитування програмістів, щоб виявити ключові закономірності на ринку праці. Аналіз дозволяє зрозуміти, які навички зараз найзатребуваніші, як рівень освіти впливає на дохід і як відрізняється компенсація спеціалістів у різних куточках світу.

Найцікавішим викликом була робота з "сирими" даними: обробка множинних відповідей (коли людина вказує кілька мов програмування одночасно) та очищення даних від пропусків для отримання точної статистики. Я опрацював базу даних із десятками тисяч анкет, щоб перетворити розрізнені відповіді на чіткі бізнес-метрики.

### Основні етапи
Реалізація проєкту включала наступні кроки:
* **Підготовка та очищення:** Завантаження великих датасетів та перевірка повноти відповідей за допомогою порівняння структури питань.
* **Статистичне дослідження:** Розрахунок середнього досвіду роботи, медіанних зарплат та аналіз поширеності віддаленої роботи.
* **Глибокий аналіз сегментів:** Вивчення популярності мови Python серед різних вікових груп та аналіз індустрій, де працюють найбільш високооплачувані фахівці.
* **Географічне порівняння:** Групування даних за країнами для порівняння рівня життя та оплати праці розробників.
* **Візуалізація:** Побудова графіків розподілу для наочного представлення результатів.

### Функції та методи
У проєкті використано наступний інструментарій бібліотеки Pandas:
* **Агрегація та групування:** `groupby()`, `agg(['mean', 'median', 'count'])` — для порівняння зарплат по країнах.
* **Фільтрація за умовами:** Використання складних масок та методу `.str.contains()` для пошуку конкретних технологій (наприклад, Python) у списках.
* **Описова статистика:** `describe()`, `quantile()` — для визначення 75-го та 95-го перцентилів доходу.
* **Обробка пропусків:** `dropna()` та `isna()` — для забезпечення чистоти аналізу.
* **Візуалізація:** `Seaborn` та `Matplotlib` для створення графіків розподілу доходів та популярності мов.

### Наступні кроки
Надалі проєкт можна розширити, додавши аналіз динаміки змін (порівняння з даними за минулі роки) та побудову предиктивної моделі, яка могла б прогнозувати рівень зарплати на основі навичок та локації розробника.

---

## 📊 Global IT Talent Market Analysis (based on Stack Overflow Survey)
An exploration of professional development trends, salary benchmarks, and technology adoption among developers worldwide.

### Project Overview
The primary goal of this project was to analyze data from the world's largest developer survey to uncover key labor market patterns. This analysis provides insights into high-demand skills, the correlation between education level and income, and how compensation varies globally.

The most challenging part of the project was handling "raw" data: processing multiple-choice responses (where a respondent lists several programming languages) and cleaning missing values to ensure statistical accuracy. I processed a dataset containing tens of thousands of entries to transform scattered responses into clear, actionable business metrics.

### Main Stages
The project implementation included the following stages:
* **Preparation & Cleaning:** Loading large-scale datasets and verifying data completeness by cross-referencing response structures.
* **Statistical Exploration:** Calculating average work experience, median salaries, and analyzing the prevalence of remote work.
* **Segmented Analysis:** Examining Python's popularity across different age groups and identifying industries with the highest concentration of top earners.
* **Geographical Benchmarking:** Grouping data by country to compare developer compensation and market maturity.
* **Visualization:** Developing distribution plots to present findings in an intuitive, recruiter-friendly format.

### Functions and Techniques
The following Pandas-based tools and techniques were utilized:
* **Aggregation & Grouping:** `groupby()`, `agg(['mean', 'median', 'count'])` to compare salaries across countries.
* **Advanced Filtering:** Using complex masks and `.str.contains()` for identifying specific technologies within multi-value strings.
* **Descriptive Statistics:** `describe()`, `quantile()` to define 75th and 95th income percentiles.
* **Data Integrity:** `dropna()` and `isna()` to manage missing information and ensure robust results.
* **Data Visualization:** `Seaborn` and `Matplotlib` to visualize income distributions and technology trends.

### Next Steps
Future iterations could include a time-series analysis (comparing current results with previous years' data) and developing a predictive model to estimate potential salary based on a developer's skill set and location.
