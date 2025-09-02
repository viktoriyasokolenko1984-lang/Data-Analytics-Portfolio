
SELECT title, dept_name, AVG(salary) AS avg_salary
FROM salaries AS s
INNER JOIN titles AS t ON(s.emp_no=t.emp_no)
INNER JOIN dept_emp AS de ON(s.emp_no=de.emp_no)
INNER JOIN departments AS d ON(de.dept_no=d.dept_no)
GROUP BY title, dept_name
ORDER BY avg_salary DESC, dept_name;
