# Ex. No: 4 Creating Procedures using PL/SQL
## Date: 24/8/23
### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
create table emp(empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
CREATE OR REPLACE PROCEDURE emp_data AS
  2  BEGIN
  3  INSERT INTO emp(empid,empname,dept,salary)
  4  values(1,'ajith','CSE',5000);
  5  INSERT INTO emp(empid,empname,dept,salary)
  6  values(2,'vijay','IT',50000);
  7  INSERT INTO emp(empid,empname,dept,salary)
  8  values(3,'suriya','ECE',20000);
  9  COMMIT;
 10  FOR emp_rec IN (SELECT * FROM emp)LOOP
 11  DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);

 12  END LOOP;
 13  END;
 14  /


SQL> begin
  2  emp_data;
  3  end;
  4  /



SQL> select * from emp;
```

### Output:
![image](https://github.com/collinsjoel10/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118626456/25ef493c-21a8-4021-84d2-393348ad0a29)

### Result:

the commands using Procedures using PL/SQL has been executed successfully.
