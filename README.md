#Vulnerability Advisory & Exploit

##Affected Version
 
  HR Integrated System (insert-and-view component)

##Vulnerability Type

  SQL Injection in insert-and-view/action.php

##Advisory (Recommendations)

  Use parameterized queries or prepared statements to securely handle SQL queries.

  Transition from deprecated mysql_* functions to mysqli_* or PDO with parameterized queries.

  Implement strict input validation and sanitization.

  Limit database user privileges according to the principle of least privilege.

##Proof-of-Concept (Exploit)
  POST payload example:

    content='); DROP TABLE comment; --

##Exploit Steps:

1.Navigate to the comment submission form.

2.Intercept the POST request.

3.Modify the content parameter with the malicious payload.

4.Submit the modified request to execute arbitrary SQL commands.

