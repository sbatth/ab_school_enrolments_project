# Alberta School Enrolments- PowerBI Project

This PowerBI project analyzes the school enrolments data in Alberta. The dataset includes enrolments from 2021 to 2024.

## Overview

The Alberta Schooling systems has five categories of schools 
- Public
- Private
- Separate (established by religious groups, e.g. Catholics or Protestants)
- Charter (public schools with more autonomy)
- Francophone

The goal of the project was to identify the composition of enrolments in schools by these categories and also spot if public schools were seeing a decline despite the increasing population in Alberta.

## Key Insights

- *66.5%* of the total enrolments in 2024 were in Public Schools.
- The school with the highest enrolments in 2024 was *'The Gilbertine Academy' with around 6k enrolments*.
- *52.87%* of the total enrolments were in Elementary grades (K-Grade 6).

Preview of the report.

![im](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-26%20212739.png)

The [PDF](./enrolment_dashboard.pdf) of the PowerBI report can be used for quick overview. To use interactive features of the report, the [pbix](./enrolment_dashboard.pbix) file can be downloaded. 

## Process

### Data Source 

Data was obtained from the [Government of Alberta data portal](https://open.alberta.ca/opendata/student-enrolment-by-school-authority-and-grade-level), covering data for school years 2021/2022 up to 2024/2025. For consistency, the enrolment year was instead of the whole school year.
For example, school year 2021/2022 became enrolment year 2021 in the data.

### Data Preparation
- Appended data files into one in Power Query.
- The data file contained a column for enrolments of each grade starting from Early Childhood Service (ECS) to Grade 12. Unpivoted these columns to have a long-format data file optimizing usability and storage in PowerBI. 

![Power Query Snapshot](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-25%20231443.png)

- Created a new table to change the grade levels to a broader level of Elementary (ECS-6), Junior High (7-9) and Senior High (10-12).

![img](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-25%20232243.png)


The data model looked as follows

![data_model](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-25%20232231.png)

### Tools

- PowerBI, for visualizations.
- Power Query, for data transformation and loading.

### Analysis & Findings

The analysis explored total enrolments, school counts, enrolment distributions across school categories and grade levels, and trends over time.

Key findings in the data

- In 2024, there were a total of around *811,000 student enrolments* and *2,254 schools* that took these enrolments. This indicates the magnitude of schooling in Alberta. 

![kpi](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-25%20234446.png)

- In 2024, *52.87%* of the total enrolments were in elementary grades. This emphasizes the importance of early education initiatives in Alberta. The policies that affect public education should consider that they will have the biggest impact on elementary education.
  
![kpi](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-26%20191551.png)

- In 2024, *539k* of the 811k enrolments (66.5%) were in Public schools. This percentage has been in a slight decline since 2021. 67.4% in 2021, 67.4% in 2022, 66.8% in 2023. Over the same period
  - The Private schools went from 6.32% from 2021 to 6.92% in 2024.
  - The Charter schools went from 1.44% in 2021 to 1.90% in 2024.

This can indicate early signs of changing preferences in schools. This likely reflects faster growth in alternative options like charter or private schools. Potential drivers could include greater parental demand for specialized programs, increased funding or expansion of charter schools, or shifts in perception of public education quality.

![kpi](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-25%20234539.png)



- The school with the highest enrolments in 2024 was *The Gilbertine Academy* which is a private school. The public school with the highest enrolments was *Jasper High School* with nearly half the enrolments.

  There could be several factors inducing this
  - infrastructure of schools
  - density of schools
  - preference shifts in the area

Further investigation is recommended to identify the issue.  

![kpi](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-25%20234510.png)

For the trends over the years, all the grade categories- Elementary, Junior High, and Senior High saw a *steady increase in number of enrolments* but Senior High enrolments gained significant ground in the percent of total enrolments metric. They went from holding 23.05% of the total enrolments in 2021 to 24.68% in 2024.

![im](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-26%20205919.png)

For the school categories, the **biggest jump** was seen in the *Charter* category schools, enrolments went from 10.6k in 2021 to 15.4k in 2024, a gain of *45%*. This can be attributed to the *significant increase in the number of schools*, changing from 25 to 36 in the same period.

This may point to successful policy support (e.g. lifting of previous caps), growing public awareness, or perceived academic advantages. The trend could signal long-term structural change in Alberta’s education system, especially in urban centres where demand for alternatives is higher.

![im](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-26%20210446.png)

The category with the **second highest increase** was *Private* schools going from 46.4k enrolments in 2021 to 56.2k in 2024, an increase of *22%*. Private schools also saw an increase in the number of schools by 25 during this period.

![im](https://github.com/sbatth/images/blob/main/bi/Screenshot%202025-05-26%20210906.png)

The other categories saw upward trends too but not as significant as the aforementioned two, Public schools saw an increase of 9%, Separate schools saw an increase of 10%, and Francophone schools saw an increase of 11%.

## Recommendations

1. **Expand Charter Schools**

Even though the enrolments in public schools are increasing, they can be attributed to the general popultaion increase upto an extent. There are early signs that the Private and Charter schools are gaining popularity among Albertans. As *Charter schools are specialized public schools*, the government can look to benefit from this trend and create more such schools.

2. **Focus on elementary education**

Elementary grades take up almost *50%* of all the enrolments in any given year. The education initiatives by the goverment should consider the impact it will have on these enrolments.

3. **Learn from High-Performing Schools**

*The Gilbertine Academy* is a leader in student enrolments. Research can be done on the school to identify potential improvements in public schools.

## Areas of improvement

- Geographical Analysis
  
The analysis could benefit from geographical data to identify any hotspots. Geographical density can also be tested as a cause of schools' performances.

- Student-level Data
  
Anonymized data on individual students could also be beneficial. This can help to identify any migrations from public schools to others. If certain schools are experiencing high outward migration, they can be investigated.

 






