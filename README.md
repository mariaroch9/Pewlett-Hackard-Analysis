# Overview of the analysis
## Background
Pewlett Hackard is a large company boasting several thousand employees, and it's been around for a long time. As baby boomers begin to retire at a rapid rate, Pewlett Hackard is looking toward the future in two ways. First, it's offering a retirement package for those who meet certain criteria. Second, it's starting to think about which positions will need to be filled in the near future.
The number of upcoming retirements will leave thousands of job openings. What would happen to a company if it didn't look ahead and prepare for these vacancies? It probably wouldn't be pretty.

## Purpose

1)    To determine the number of retiring employees per title
2)    To identify employees who are eligible to participate in a mentorship program

# Results
## Retiring employees analysis was conducted based on birth dates,  those born between January 1, 1952 and December 31, 1955

1)    The retirement_titles table highlighted the number of people expected to retire based on the birth dates of employees. However, closer inspection revealed several rows with duplicate employee names
`
Retirement_titles
`
/Users/Rochelle/Desktop/Pewlett_Hackard_Analysis/Retirement_titles.png

`
2)    To alleviate this problem of duplication we created a unique_titles table. The new table contained only the recently held titles by employees 
`
Unique_titles
`
/Users/Rochelle/Desktop/Pewlett_Hackard_Analysis/unique_titles .numbers


`
3)    Finally, the retiring titles table showed the count of employees retiring based on their titles. All employees were part of either of the 7 titles shown in the table below. The total number of employees set to retire was about 72k. Most of those retiring bore the Senior Engineer title, with a count of about 26k.  Thankfully the number of Managers was only 2

`
Retiring_titles
`
/Users/Rochelle/Desktop/Pewlett_Hackard_Analysis/retiring_titles.numbers

2       Manager

`
### Mentorship Analysis was conducted on the current employees who were born between January 1, 1965, and December 31, 1965, to determine their eligibility for a mentorship program.

4)    The total number of employees eligible for a mentorship program was 1549
`
Mentorship_Eligibility Table
`
/Users/Rochelle/Desktop/Pewlett_Hackard_Analysis/Mentorship_eligibility.png


## Summary: 
## To conclude, the “silver tsunami” will impact 7 roles within the organization, Senior Engineers, Senior Staff, Engineer, Staff, Technique Leader, Assistant Engineer, and Manager.  The numbers show maximum retirement at the Senior Engineers level, with most of the rest in other technical roles. Considering these jobs are high on technical skills these roles are easy to replace. Had the trend been higher retirements on the Managerial level then it would be concerning. 
## While those retiring are in the thousands, those eligible for mentorship are in the meagre 100s. It seems like there is a huge hollow to be filled. This could be because the management has realized that the company is operating with a higher employee count and has imposed hiring freezes. The retirals may be a blessing in disguise. They will significantly reduce headcount resulting in lower employee costs and enhanced profitability. 
## Some of the other queries that could be performed are joining the Salaries table to include a Salaries column along with the titles in the retirement analysis. This would give a picture of the saving that the company would incur owing to the retirements.
## Finally, an analysis could be performed to assess the count of the number of members eligible for the mentorship program. This will be crucial in the revamping phase of the company. Focussing on mentorship at all levels will ensure that there will be a sufficient pipeline of resources ready to hit the ground running. 


