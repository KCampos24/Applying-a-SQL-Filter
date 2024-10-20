<h1>Applying Filters in SQL Queries</h1>

### [YouTube Demonstration](https://youtu.be/your_youtube_link_here)

<h2>Description</h2>
This repository demonstrates how to apply filters to SQL queries using operators such as <code>AND</code>, <code>OR</code>, and <code>NOT</code>. These operators are crucial for constructing complex queries to retrieve data efficiently and enhance the security of organizational systems. Below are examples of using these operators in various scenarios:

- Filter results with multiple conditions using <code>AND</code>
- Broaden search results with <code>OR</code>
- Exclude certain records using <code>NOT</code>
- Use the <code>LIKE</code> operator with wildcards for flexible pattern matching

<h2>Languages and Utilities Used</h2>

- <b>SQL</b> 

<h2>Environments Used</h2>

- <b>Windows 10</b>

<h2>Program Walk-through:</h2>

<h3>1. Retrieve Employees in Marketing (East Building)</h3>
To make security updates specifically for employees in the Marketing department located in the East building, we combine the <code>AND</code> operator with the <code>LIKE</code> wildcard to narrow down the results. The query retrieves only those employees whose department is "Marketing" and whose office name starts with "EAST".
<br/>
<code>SELECT *</code><br/>
<code>FROM employees</code><br/>
<code>WHERE department = 'Marketing' AND office LIKE 'EAST%';</code><br/>

This query ensures we’re targeting the right employees in both the Marketing department and the East building by specifying both conditions. The `%` symbol is a wildcard in SQL that matches any number of characters after the specified pattern. This query ensures we target all employees in the Marketing department whose office is located in the East building, regardless of the specific office number.
<p align="center">
<img src="https://i.imgur.com/cOFifJo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h3>2. Retrieve Employees in Finance or Sales</h3>
For system updates across both Finance and Sales departments, we use the <code>OR</code> operator to retrieve records that match either department. This query will return employees from both departments, ensuring updates are applied across both teams.
<br/>
<code>SELECT *</code><br/>
<code>FROM employees</code><br/>
<code>WHERE department = 'Finance' OR department = 'Sales';</code><br/>

This broadens the search results to include employees from either department, making it useful when multiple groups need to be targeted simultaneously.
<p align="center">
<img src="https://i.imgur.com/s0K0hYe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h3>3. Retrieve All Employees Not in IT</h3>
If a specific update has already been applied to the Information Technology (IT) department, but needs to be rolled out to everyone else, the <code>NOT</code> operator is used. This query excludes employees from the IT department and returns all others.
<br/>
<code>SELECT *</code><br/>
<code>FROM employees</code><br/>
<code>WHERE NOT department = 'Information Technology';</code><br/>

This ensures that the IT team is excluded from the results, making the update process more efficient by avoiding redundancy.
<p align="center">
<img src="https://i.imgur.com/Igm2yTK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h2>Conclusion</h2>
Utilizing <code>AND</code>, <code>OR</code>, and <code>NOT</code> operators allows for constructing complex and precise SQL queries. These logical operators help refine data retrieval processes by narrowing or broadening search results, as well as excluding specific data as needed. In combination, they make SQL a powerful tool for efficient and accurate data filtering in cybersecurity and database management tasks.
