# Data Analysis

### Table of Contents
- Explaining the Variables
- Data Analysis
	- Basic Exploration
	- Gender
	- Student Performance
	- Work Experience
	- Placement
	- Salary
	- Performance Correlations

### Explaining the Variables

- `gender`: Gender (M or F)
- `ssc_p`: Secondary Education percentage (10th Grade)
- `ssc_b`: Board of Secondary Education (Central or Others)
- `hsc_p`: Higher Secondary Education percentage (12th Grade)
- `hsc_b`: Board of Higher Secondary Education (Central or Others)
- `hsc_s`: Specialization in Higher Secondary Education
- `degree_p`: Undergraduate Degree percentage
- `degree_t`: Undergraduate Degree Subject
- `workex`: Work Experience (1 or 0)
- `etest_p`: Employability Test percentage
- `specialisation`: Postgraduate Subject
- `mba_p`: Postgraduate percentage
- `placed`: Placement (1 or 0)
- `salary`: Salary Offered

### Data Analysis
The data analysis and visualisation for this project was conducted in Python and Tableau.

##### Basic Exploration
The data is a record of 215 students.

- The male to female ratio is ~ 65:35.
- ~ 69% of the students were placed.
- The average salary offered to placed students is ~ 288,655.
- There are 3 academic routes a student can take during Higher Secondary Education.
- There are 3 academic routes a student can take during Undergraduate.
- There are 2 academic routes a student can take during Postgraduate.
- ~ 34% of the students have work experience.

##### Gender
Female students have consistently outperformed male students in academics. They only time male students, on average, scored higher than female students was in `etest_p` (Employability Test).

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/ssc_gender_dist.png' width='1000'> |
| :--: |
| _Figure 1 - Secondary Education Gender Performance_ |

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/hsc_gender_dist.png' width='1000'> |
| :--: |
| _Figure 2 - Higher Secondary Education Gender Performance_ |

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/degree_gender_dist.png' width='1000'> |
| :--: |
| _Figure 3 - Undergraduate Gender Performance_ |

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/mba_gender_dist.png' width='1000'> |
| :--: |
| _Figure 4 - Postgraduate Gender Performance_ |

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/etest_gender_dist.png' width='1000'> |
| :--: |
| _Figure 5 - Employability Test Gender Performance_ |

##### Work Experience

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/analysis_workex.png' height='360'> |
| :--: |
| _Figure 6 - Work Experience Analysis_ |

##### Placement

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/analysis_placement.png' height='360'> |
| :--: |
| _Figure 7 - Placement Analysis_ |

##### Salary

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/analysis_salary.png' height='360'> |
| :--: |
| _Figure 8 - Salary Analysis_ |

Despite their better academic performance, female students are, on average, paid less than male students. This leads to the following possibilities:

- Academic performance is not a determinant of salary.
- There are other determinants of salary:
	- Choice of subjects.
	- Work experience.
	- Employability test.
	- Other factors, not present in the data.
- There is a gender bias.

**Academic performance is not a determinant of salary**

To assess this, I plotted scatterplots of individual academic exams against `salary`. There were no significant corellations. I then plotted the accumulation of all individual academic exams and plotted it against `salary`. The result was the same (fig. 9).

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/salary_totalmarks.png' width='1000'> |
| :--: |
| _Figure 9 - Salary Offered and Academic Performance_ |

Therefore, it can be concluded that academic performance is not a determinant of salary.

**Choice of subjects is a determinant of salary**

In order to assess this, I made a `salary` barchart of all possible subject combinations, differentiated by `gender` (fig. 10). 

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/tableau_salary.png' width='1200'> |
| :--: |
| _Figure 10 - Salary according to Choice of Subjects_ |

From figure 10, it can be concluded that, in most cases, postgraduate `specialisation` in 'Mkt&Fin' pays more than in 'Mkt&HR'. Apart from that, there are no patterns in terms of subject combinations.
Out of all possible subject combinations, for male students, 3 combinations have led to a `salary` higher than the overall average; compared to only 1 combination for female students. The combination the pays the highest on average -- Sci&Tech and Mkt&Fin -- does not reflect in regards to female students.
Therefore, it can be concluded that choice of subjects is not a clear determinant of `salary`.

**Work experience**

In order to assess this, I plotted a barchart for the salaries of male students with and without work experience, and female students with and without work experience.

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/salary_gender_workex_bar.png' width='1000'> |
| :--: |
| _Figure 11 - Salary according to Work experience_ |

Figure 11 suggests that, although for each gender having work experience secures a higher `salary`, gender differences still exist. Male students _without_ work experience are offered a higher `salary` than female students _with_ work experience.
Therefore, work experience does influence `salary`, but not absolutely.

**Employability test**

The scatterplot (fig. 12) suggests that there is no significant correlation between the `etest` performance and `salary`. Therefore, it is not a determinant of salary.

| <img src='https://github.com/meehadjawwad/Campus-Recruitment/blob/master/images/etest_salary.png' width='1000'> |
| :--: |
| _Figure 12 - Salary according to Employability Test_ |

