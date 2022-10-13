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

emp_no    first_name    last_name    title    from_date    to_date
10001    Georgi    Facello    Senior Engineer    1986-06-26    9999-01-01
10004    Chirstian    Koblick    Engineer    1986-12-01    1995-12-01
10004    Chirstian    Koblick    Senior Engineer    1995-12-01    9999-01-01
10005    Kyoichi    Maliniak    Staff    1989-09-12    1996-09-12
10005    Kyoichi    Maliniak    Senior Staff    1996-09-12    9999-01-01
10006    Anneke    Preusig    Senior Engineer    1990-08-05    9999-01-01
10009    Sumant    Peac    Assistant Engineer    1985-02-18    1990-02-18
10009    Sumant    Peac    Engineer    1990-02-18    1995-02-18
10009    Sumant    Peac    Senior Engineer    1995-02-18    9999-01-01
10011    Mary    Sluis    Staff    1990-01-22    1996-11-09
10018    Kazuhide    Peha    Engineer    1987-04-03    1995-04-03
10018    Kazuhide    Peha    Senior Engineer    1995-04-03    9999-01-01
10019    Lillian    Haddadi    Staff    1999-04-30    9999-01-01
10020    Mayuko    Warwick    Engineer    1997-12-30    9999-01-01
10022    Shahaf    Famili    Engineer    1999-09-03    9999-01-01
10023    Bojan    Montemayor    Engineer    1999-09-27    9999-01-01
10026    Yongqiao    Berztiss    Engineer    1995-03-20    2001-03-19
10026    Yongqiao    Berztiss    Senior Engineer    2001-03-19    9999-01-01
10035    Alain    Chappelet    Engineer    1988-09-05    1996-09-05
10035    Alain    Chappelet    Senior Engineer    1996-09-05    9999-01-01
10047    Zvonko    Nyanchama    Engineer    1989-03-31    1998-03-31
10047    Zvonko    Nyanchama    Senior Engineer    1998-03-31    9999-01-01
10051    Hidefumi    Caine    Engineer    1992-10-15    1998-10-15
10051    Hidefumi    Caine    Senior Engineer    1998-10-15    9999-01-01

`
2)    To alleviate this problem of duplication we created a unique_titles table. The new table contained only the recently held titles by employees 
`
Unique_titles
`
/Users/Rochelle/Desktop/Pewlett_Hackard_Analysis/unique_titles .numbers
emp_no    first_name    last_name    title
10001    Georgi    Facello    Senior Engineer
10004    Chirstian    Koblick    Senior Engineer
10005    Kyoichi    Maliniak    Senior Staff
10006    Anneke    Preusig    Senior Engineer
10009    Sumant    Peac    Senior Engineer
10018    Kazuhide    Peha    Senior Engineer
10019    Lillian    Haddadi    Staff
10020    Mayuko    Warwick    Engineer
10022    Shahaf    Famili    Engineer
10023    Bojan    Montemayor    Engineer
10026    Yongqiao    Berztiss    Senior Engineer
10035    Alain    Chappelet    Senior Engineer
10047    Zvonko    Nyanchama    Senior Engineer
10051    Hidefumi    Caine    Senior Engineer
10053    Sanjiv    Zschoche    Senior Staff
10057    Ebbe    Callaway    Senior Engineer

`
3)    Finally, the retiring titles table showed the count of employees retiring based on their titles. All employees were part of either of the 7 titles shown in the table below. The total number of employees set to retire was about 72k. Most of those retiring bore the Senior Engineer title, with a count of about 26k.  Thankfully the number of Managers was only 2

`
Retiring_titles
`
/Users/Rochelle/Desktop/Pewlett_Hackard_Analysis/retiring_titles.numbers
count    title
25916    Senior Engineer
24926    Senior Staff
9285    Engineer
7636    Staff
3603    Technique Leader
1090    Assistant Engineer
2       Manager

`
### Mentorship Analysis was conducted on the current employees who were born between January 1, 1965, and December 31, 1965, to determine their eligibility for a mentorship program.
4)    The total number of employees eligible for a mentorship program was 1549
`
Mentorship_Eligibility Table
`
/Users/Rochelle/Desktop/Pewlett_Hackard_Analysis/Mentorship_eligibility.png
emp_no    first_name    last_name    birth_date    from_date    to_date    title
10095    Hilari    Morton    1965-01-03    1994-03-10    9999-01-01    Staff
10122    Ohad    Esposito    1965-01-19    1998-08-06    9999-01-01    Technique Leader
10291    Dipayan    Seghrouchni    1965-01-23    1987-03-30    9999-01-01    Staff
10476    Kokou    Iisaka    1965-01-01    1987-09-20    9999-01-01    Senior Staff
10663    Teunis    Noriega    1965-01-09    1999-02-12    9999-01-01    Technique Leader
10762    Lech    Himler    1965-01-19    1992-01-21    9999-01-01    Senior Staff
10933    Juyoung    Seghrouchni    1965-01-24    1993-08-02    9999-01-01    Senior Engineer
12155    Keiichiro    Glinert    1965-01-21    1993-09-16    9999-01-01    Senior Engineer
12408    Rasiah    Sudkamp    1965-01-10    1995-04-18    9999-01-01    Senior Engineer
12643    Morrie    Schurmann    1965-01-30    1998-12-31    9999-01-01    Staff
13499    Kazuhiko    Sidou    1965-01-16    1991-09-01    9999-01-01    Technique Leader
14075    Denny    Tchuente    1965-01-03    1991-05-30    9999-01-01    Assistant Engineer
14104    Sudhanshu    Demian    1965-01-03    1994-07-23    9999-01-01    Senior Staff
14127    Magdalena    Cannard    1965-01-10    1994-04-22    9999-01-01    Engineer
14158    Caolyn    Setiz    1965-01-22    1990-02-06    9999-01-01    Staff
14476    Sastry    Marrevee    1965-01-19    1999-09-25    9999-01-01    Engineer
14907    Nakhoon    Luga    1965-01-14    1986-12-18    9999-01-01    Senior Staff
15050    Nikolaos    Kruskal    1965-01-18    1990-12-17    9999-01-01    Senior Engineer
`


## Summary: 
## To conclude, the “silver tsunami” will impact 7 roles within the organization, Senior Engineers, Senior Staff, Engineer, Staff, Technique Leader, Assistant Engineer, and Manager.  The numbers show maximum retirement at the Senior Engineers level, with most of the rest in other technical roles. Considering these jobs are high on technical skills these roles are easy to replace. Had the trend been higher retirements on the Managerial level then it would be concerning. 
## While those retiring are in the thousands, those eligible for mentorship are in the meagre 100s. It seems like there is a huge hollow to be filled. This could be because the management has realized that the company is operating with a higher employee count and has imposed hiring freezes. The retirals may be a blessing in disguise. They will significantly reduce headcount resulting in lower employee costs and enhanced profitability. 
## Some of the other queries that could be performed are joining the Salaries table to include a Salaries column along with the titles in the retirement analysis. This would give a picture of the saving that the company would incur owing to the retirements.
## Finally, an analysis could be performed to assess the count of the number of members eligible for the mentorship program. This will be crucial in the revamping phase of the company. Focussing on mentorship at all levels will ensure that there will be a sufficient pipeline of resources ready to hit the ground running. 


