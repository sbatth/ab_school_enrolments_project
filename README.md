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

![im](https://private-user-images.githubusercontent.com/147944185/447742013-59b6ce96-e4bb-4c2d-878e-7f57f422bb9c.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgzMTY3NzQsIm5iZiI6MTc0ODMxNjQ3NCwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NzQyMDEzLTU5YjZjZTk2LWU0YmItNGMyZC04NzhlLTdmNTdmNDIyYmI5Yy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyN1QwMzI3NTRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0wODFlNjQ2ODFmNzkzMmVkZTZlNDE5YTRkMTgxOTQzOGYyNzIzNDUyZjkxMmMxMjcwNjY0MzhkNTA2YWQ3NWQ1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.2B5LeWWHP1Qt-qDpWYYM2U8tSKZixZb83GbA5i1_6xs)

The [PDF](./enrolment_dashboard.pdf) of the PowerBI report can be used for quick overview. To use interactive features of the report, the [pbix](./enrolment_dashboard.pbix) file can be downloaded. 

## Process

### Data Source 

Data was obtained from the [Government of Alberta data portal](https://open.alberta.ca/opendata/student-enrolment-by-school-authority-and-grade-level), covering data for school years 2021/2022 up to 2024/2025. For consistency, I used the enrolment year instead of the whole school year.
For example, school year 2021/2022 became enrolment year 2021 in the data.

### Data Preparation
- Appended data files into one in Power Query.
- The data file contained a column for enrolments of each grade starting from Early Childhood Service (ECS) to Grade 12. Unpivoted these columns to have a long-format data file optimizing usability and storage in PowerBI. 

![Power Query Snapshot](https://private-user-images.githubusercontent.com/147944185/447422468-8d5caa5d-adb8-4c56-9bbc-69055b7f46e2.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgyMzY4MDUsIm5iZiI6MTc0ODIzNjUwNSwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NDIyNDY4LThkNWNhYTVkLWFkYjgtNGM1Ni05YmJjLTY5MDU1YjdmNDZlMi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyNlQwNTE1MDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0wOGNiNTIxNWYzOWZhMGI2YTQ5ZTA4MWU1M2RlOTg2ZDYyNTQ5ODBiMWJkZWY0ZDhlMjk2YjhmNTkxYzFmYWE0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.hmBQ9i4d7JHZ7R802tljYX1vzUHPkOHTTABxUrrKrR8)

- Created a new table to change the grade levels to a broader level of Elementary (ECS-6), Junior High (7-9) and Senior High (10-12).

![img](https://private-user-images.githubusercontent.com/147944185/447424664-2c0fb2db-3284-4b12-b663-f1bd087596bf.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgyMzczNTksIm5iZiI6MTc0ODIzNzA1OSwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NDI0NjY0LTJjMGZiMmRiLTMyODQtNGIxMi1iNjYzLWYxYmQwODc1OTZiZi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyNlQwNTI0MTlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1mNThhZjk2MTk4MGYxM2ZkOTVlYTE4NDIzMjlmYzlhMDNkZDIxZGNhOWMzNjE0YjFiNzM1MTEzODBlODczY2E3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.6fSeAnOcwIy2jz-JXUa8BhViGCoyu4akTBRvmheRjrw)


The data model looked as follows

![data_model](https://private-user-images.githubusercontent.com/147944185/447424639-2a72c627-5404-4060-b93e-77f0cb376c5a.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgyMzczNTksIm5iZiI6MTc0ODIzNzA1OSwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NDI0NjM5LTJhNzJjNjI3LTU0MDQtNDA2MC1iOTNlLTc3ZjBjYjM3NmM1YS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyNlQwNTI0MTlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01ZDE4YWM0OGJiMzhlYTc3NDRjMGM5NzQ5ODJiYmViNWYzYTRmNjg0ZDJkNDk3MjNiMzkwMDViZjgxZjJkYTRjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.Cq5xGBvElc94qW_XHCizj3bZCDX9kpgUtETq41vRsLI)

### Tools

- PowerBI, for visualizations.
- Power Query, for data transformation and loading.

### Analysis & Findings

The analysis explored total enrolments, school counts, enrolment distributions across school categories and grade levels, and trends over time.

Key findings in the data

- In 2024, there were a total of around *811,000 student enrolments* and *2,254 schools* that took these enrolments. This indicates the magnitude of schooling in Alberta. 

![kpi](https://private-user-images.githubusercontent.com/147944185/447430212-c01b1a62-8c50-47ef-a051-68f56b40a769.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgyMzg3MzIsIm5iZiI6MTc0ODIzODQzMiwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NDMwMjEyLWMwMWIxYTYyLThjNTAtNDdlZi1hMDUxLTY4ZjU2YjQwYTc2OS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyNlQwNTQ3MTJaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zYmRmZDczYzViMTA0M2MyNDcxMTc5OWJhODNhM2RiYzY2YzNhNjZjNTJhOGI5ZjkxZWFhMWRlODFhYTA0NjQ1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.29D1T_bNG3NlfSfK1lwdNJX0DMIf-ySvG-Tr1xvn7ho)

- In 2024, *52.87%* of the total enrolments were in elementary grades. This emphasizes the importance of early education initiatives in Alberta. The policies that affect public education should consider that they will have the biggest impact on elementary education.
  
![kpi](https://private-user-images.githubusercontent.com/147944185/447716718-412ab4f4-7a35-490f-aecc-b1fe0ac9f578.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgzMDg4NjYsIm5iZiI6MTc0ODMwODU2NiwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NzE2NzE4LTQxMmFiNGY0LTdhMzUtNDkwZi1hZWNjLWIxZmUwYWM5ZjU3OC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyN1QwMTE2MDZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0xNWU4NTZlOTFmODIxNjI5ZTRlYzNiNzkyY2MxMDkyMmNmMmQ3N2NkMmM4MmFlMzEzZjNiYmJkOTVhYTYyOWM4JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.-fLdzgQVOrEKSA0AJ9jS4mbt8hMcWPFLQohC8LGoc3k)

- In 2024, *539k* of the 811k enrolments (66.5%) were in Public schools. This percentage has been in a slight decline since 2021. 67.4% in 2021, 67.4% in 2022, 66.8% in 2023. Over the same period
  - The Private schools went from 6.32% from 2021 to 6.92% in 2024.
  - The Charter schools went from 1.44% in 2021 to 1.90% in 2024.

This can indicate early signs of changing preferences in schools. This likely reflects faster growth in alternative options like charter or private schools. Potential drivers could include greater parental demand for specialized programs, increased funding or expansion of charter schools, or shifts in perception of public education quality.

![kpi](https://private-user-images.githubusercontent.com/147944185/447430210-23fffcdc-c289-4417-b745-e3d536ec4372.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgyOTA0NjUsIm5iZiI6MTc0ODI5MDE2NSwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NDMwMjEwLTIzZmZmY2RjLWMyODktNDQxNy1iNzQ1LWUzZDUzNmVjNDM3Mi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyNlQyMDA5MjVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hOWQ0MmY3YmRhZTA2ZTkxOGFlNTk3OGQ5MjMyNGMxNDhkM2VmMzRhNjEyMjk0NWNmYzQwYmVjZGZiNmFjYjE0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.dGLT4d6Hdo2p4kmFXyOZx64QSBcEI_lXyZmyfs6aVTk)



- The school with the highest enrolments in 2024 was *The Gilbertine Academy* which is a private school. The public school with the highest enrolments was *Jasper High School* with nearly half the enrolments.

  There could be several factors inducing this
  - infrastructure of schools
  - density of schools
  - preference shifts in the area

Further investigation is recommended to identify the issue.  

![kpi](https://private-user-images.githubusercontent.com/147944185/447430211-6a0a5446-ffaa-475b-8832-de1b4ebba6e6.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgyOTA0NjUsIm5iZiI6MTc0ODI5MDE2NSwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NDMwMjExLTZhMGE1NDQ2LWZmYWEtNDc1Yi04ODMyLWRlMWI0ZWJiYTZlNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyNlQyMDA5MjVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT00YmM2YjNmM2UzNTQwYmNkYTcxZjQzZTE0MzRhNzQ4YzE1YjhmZmUwODBlYjg2YjU5NTA0MDE0MjhjMjYxZGNiJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.Y1Di_mYhp9OZ9jccR6hhSJwXEpVLPSC2hULf6m5kJ7s)

For the trends over the years, all the grade categories- Elementary, Junior High, and Senior High saw a *steady increase in number of enrolments* but Senior High enrolments gained significant ground in the percent of total enrolments metric. They went from holding 23.05% of the total enrolments in 2021 to 24.68% in 2024.

![im](https://private-user-images.githubusercontent.com/147944185/447736337-b4fc5860-81a4-49db-9de6-e5225bd075c7.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgzMTUwNzQsIm5iZiI6MTc0ODMxNDc3NCwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NzM2MzM3LWI0ZmM1ODYwLTgxYTQtNDlkYi05ZGU2LWU1MjI1YmQwNzVjNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyN1QwMjU5MzRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01MDU2NzM2YzExNGVhZDViOGY2MmY3Njg5ZjBiMTg1MGQ3NmRkYWRhOTc5MTIyMDgyMDZhMzI2ODM4ZjM2NjQzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.t_nQSfMzKMw9_ClMPmnJpF0OcyDVODuEIRTQxXDizeI)

For the school categories, the **biggest jump** was seen in the *Charter* category schools, enrolments went from 10.6k in 2021 to 15.4k in 2024, a gain of *45%*. This can be attributed to the *significant increase in the number of schools*, changing from 25 to 36 in the same period.

This may point to successful policy support (e.g. lifting of previous caps), growing public awareness, or perceived academic advantages. The trend could signal long-term structural change in Alberta’s education system, especially in urban centres where demand for alternatives is higher.

![im](https://private-user-images.githubusercontent.com/147944185/447737488-2a6cd589-3fa5-4bea-b96c-ff96cb90485d.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgzMTU0MDksIm5iZiI6MTc0ODMxNTEwOSwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NzM3NDg4LTJhNmNkNTg5LTNmYTUtNGJlYS1iOTZjLWZmOTZjYjkwNDg1ZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyN1QwMzA1MDlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0wOTk1YmQxZDY4YjcxYWFlMWNlNTY0MTI5NzdkOTQxNzhhYjU1MzQ5NzE5MTVkYTdiYzI3ODYyMzU0OGM3NTJhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.8pgQu2vwZ37Cx4D2FplRpmBMEoAAhosPWCnay_dbfnQ)

The category with the **second highest increase** was *Private* schools going from 46.4k enrolments in 2021 to 56.2k in 2024, an increase of *22%*. Private schools also saw an increase in the number of schools by 25 during this period.

![im](https://private-user-images.githubusercontent.com/147944185/447738313-2b2129c3-3f02-4ffc-976f-898edeca3f5b.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDgzMTU2NjAsIm5iZiI6MTc0ODMxNTM2MCwicGF0aCI6Ii8xNDc5NDQxODUvNDQ3NzM4MzEzLTJiMjEyOWMzLTNmMDItNGZmYy05NzZmLTg5OGVkZWNhM2Y1Yi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNTI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDUyN1QwMzA5MjBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01YWVjMjVlYmRlNmJhMWUxMWRhZjlhZmM2MGNlNDk1NjNhMzI5ZWRjYWU4YTA1NjUwZTExY2JjNDc4ZDgzMjgxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.4NMXVoFBfAZNPTNfqAH72TiWqhx7EYbrkYkLXPkgkzY)

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

 






