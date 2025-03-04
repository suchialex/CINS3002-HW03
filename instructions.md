# Instructions

<details>
  <summary>
    💡 REPL/PyCharm Guide
  </summary>

  - To toggle commenting, highlight the line(s) and press Ctrl + /
  - To move a statement or block of statements one indent to the right, highlight the statement(s)  press Tab
  - To move a statement or block of statements one indent to the left, highlight the statement(s)  press Shift+Tab
  - Avoid using backspaces or spaces to remove or place indents
  - REPL Comments
    - To ask the instructor a code question, highlight the line(s) of code and press Alt + / and type in your question/issue/comment and click on collapse
    - To view comments placed by the instructor click on the comment icon at the end of any highlighted code
    - If your issue is resolved, click on Resolve to remove the comment
</details>


<details>
  <summary>
    Assignment Instructions
  </summary>

- In this assignment will write code for all the update functions, delete and display functions
</details>


<details>
  <summary>
    ✅ Create a new PyCharm project
  </summary>

  - Create a new PyCharm project in a folder of your choice
  - Create a Python file - main.py
  - Inside the project create a new folder **hw03**
  - Create two files functions.py and validations.py inside hw03
  - Copy the code from main.py, functions.py and validations.py from hw02
  - Comment out the existing import statement in main.py and add a statement to import the functions from hw03
</details>


## In functions.py

<details>
  <summary>
    ✅ Modify lookup_employee
  </summary>
  Inside the lookup_employee function<br>

  - Remove the two print statements
  - Open the file hw03/employees.txt in read mode and store the file object in a variable of your choice (we will be using the same file name a lot of times, so you may choose to declare it as a global constant and use that constant in all the functions)
  - Using a for loop, go over the file using the file object above
  - Using readline() methods, read the rest of the employee data into variables and strip the newline character
  - Using an if statement check if the employee id passed as a parameter is equal to the employee id coming from the file
  - 💡 Hint: Don't forget to strip the newline character from for loop variable
  - If they are equal, in the if block
    - Write a print statement to print the values like so
    - `Name: {name}`
    - `Department: {department}`
    - `Salary: {salary}`
  - write a statement to close the file
  - write a return statement that returns the boolean true
  - **Outside the for loop** 🚩 If we made it outside the for loop, it means the employee isn't in the file
  - print `Employee Not Found`
  - return the boolean false
</details>


<details>
  <summary>
    ✅ Modify display_employees
  </summary>
  
  - Inside the display_employees function
  - After the `Displaying Employees` statement
  - Write a statement to open the file hw03/employees.txt in read mode and store the file object in a variable of your choice
  - Using a for loop, go over the file using the file object
  - Delete the variable assignment for employee id
  - Move the remaining three variable assignments inside the for loop (one indent to the right)
  - Remove the hard-coded values and replace with readline() statements. You may also strip the newline characters in the same statement.
  - Convert the salary to a float and store in the same variable ⏩ Tutorial: 2-10a
  - Move the print statement you already wrote (using the f-literal) into the for loop
  - **Outside the for loop**, write statement to close the file
</details>


<details>
  <summary>
    ✅ Modify update_employee_dept
  </summary>
  
  - Inside the update_employee_dept function,
  - After the print statement, write an input statement asking the user to provide an employee id
  - Call the lookup_employee function passing the above employee id as an argument
  💡 Hint: Don't forget to collect the returned value in a variable
  - If the returned variable is False,
    - write a return statement to get out of this function

  - 🚩 If we get this far, it means the employee is in the file
  - Open the file hw03/employees.txt in read mode and store the file object in a variable of your choice
  - Open another file hw03/temp.txt in write mode and store the file object in a variable of your choice
  - Using a for loop, go over the input file using the appropriate file object
  - Using appropriate number of readline() methods, read the rest of the employee data into variables
  - Using an if statement check if the employee id that the user provided above is NOT equal to the employee id that was read from the file
  💡 Hint: Don't forget to strip the newline character<br>
  - If they are not equal, in the if block, write all the employee data as-it-is to the output file
  - If they are equal, in the else block, call the validate_employee_dept and store it in a variable
  - Write the old employee id, old employee name, new department, and old salary to the output file
  💡 Hint: Don't forget to add a newline character to the new department
 - Outside the for loop
 - Write statements to close both the files
 - Import the os module (make sure you write this statement at the very top of the file, outside any function definitions)
 - Using the os module, write statements to delete the hw03/employees.txt file and rename the hw03/temp.txt to hw03/employees.txt - 🚩 before you do this make sure you backup your hw03/employees.txt file
</details>


<details>
  <summary>
    ✅ Modify update_employee_salary
  </summary>
  Inside the update_employee_salary function<br>

  - After the print statement, write an input statement asking the user to provide and employee id<br>
  - Call the lookup_employee function passing the above employee id as an argument<br>
  💡 Hint: Don't forget to collect the returned values in variables<br>
  - If the returned variable is False,<br>
    - print <code>Employee Not Found</code>
    - write a return statement to get out of this function<br>

  - 🚩 If we get this far, it means the employee is in the file<br>
  - Open the file employees.txt in read mode and store the file object in a variable of your choice<br>
  - Open another file temp.txt in write mode and store the file object in a variable of your choice<br>
  - Using a for loop, go over the input file using the appropriate file object<br>
  - Using appropriate number of readline() methods, read the rest of the employee data into variables
  - Using an if statement check if the employee id that the user provided above is NOT equal to the employee id coming from the file<br>
  💡 Hint: Don't forget to strip the newline character<br>
  - If they are not equal, in the if block, write all the employee data as-it-is to the output file<br>
  - If they are equal, in the else block, call the validate_employee_salary and store it in a variable.<br>
  - Write the old employee id, old employee name, old employee department, and new salary to the output file.<br>
  💡 Hint: Don't forget to add a newline character to the new salary
 - Outside the for loop,<br>
 - Write statements to close both the files<br>
 - Import the os module (make sure you write this statement at the very top of the file, outside any function definitions)
 - Using the os module, write statements to delete the employees.txt file and rename the temp.txt to employees.txt
</details>


<details>
  <summary>
    ✅ Modify update_employee_salary and update_employee_name
  </summary>
  
  - Follow the same code logic as the above function and write code to modify an employee salary and name given their employee ID
  - 🚩 Remember! Employee name is employee first name, space and employee last name. So you will be calling two validate functions and concatenating those values appropriately to get the full new name
  - 📜 Execute to make sure they work correctly
</details>


<details>
  <summary>
    ✅ Modify delete_employee
  </summary>

  - Write code to delete employee from the file, given the employee ID
  - This will be similar to that of any of the update functions, except there will be **no else block**
  - 📜 Execute to make sure it works correctly
</details>

## In validations.py

<details>
  <summary>
    ✅ Modify generate_employee_id()
  </summary>
  This function accepts no parameters but returns a string<br>
  The objective is to open the employees file and lookup the last employee id and add 1 to it to get the next employee id (for a new employee)

  - Delete the input statement
  - Open the employees file in read mode and get the file object
  - Using the file object, start a for loop, choose a loop variable name
  - Place three readline statements inside the for loop to read every 4th line in the for loop variable (because we know Employee ID is at every fourth line)
  - **Outside the for loop,**
  - Check if the for loop variable has a value (if the file is empty for loop variable will not have any value)
  - If yes
    - convert the for loop variable to int and store in the same variable (The loop variable will store the last employee ID of the file)
    - Add one to the above variable and **convert it back to string**
    - Return the above string
  - If not, in the else block
    - return a default value like '1234'
  - 📜 Execute main.py and press 1 to test Add Employee and make sure the new employee ID is inserted into the file with a calculated ID
</details>


## In functions.py and validations.py

<details>
  <summary>
    ✅ Exception handling
  </summary>

  - Wherever you are opening the file in read mode (we open file in read mode in delete_employee, lookup_employee, display_employees, generate_employee_id and all the update functions)
  - Place the open statement in try suite
  - Write an except clause to print, `File Not Found`
  - Move the remaining code **in that block**, into the else suite
  - 💡 "in that block" means, if your try is inside an if block or a while block, then your except and else clause also will be inside the same block
</details>


<details>
  <summary>
    ✅ Code improvement
  </summary>

  - Wherever you have <code>if found == True:</code> replace it with <code>if found:</code>
  - Wherever you have <code>if found == False:</code> replace it with <code>if not found:</code>
</details>


## Hierarchy Chart

<details>
  <summary>
    🚩 Hierarchy Chart
  </summary>

  - Draw hierarchy chart to reflect the updated code. You may hand draw or use any online visual tool like (draw.io)
</details>

## Copy code to replit

<details>
  <summary>
    ✅ Copy code to replit
  </summary>
  
  - Copy the contents of functions.py, validations.py and employees.txt to replit under folder hw03
  - Comment out the existing import statement and code in main function body
  - Copy and paste the import statement and code from main.py in your PyCharm Project
  - Submit the URL on Canvas assignment
</details>




