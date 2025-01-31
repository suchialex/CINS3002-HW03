# Instructions
<details>
  <summary>
    ✅ Copy code from CW02
  </summary>
  Copy main.py, functions.py and validations.py from CW02
</details>

## In functions.py

<details>
  <summary>
    ✅ Modify lookup_employee
  </summary>
  Inside the lookup_employee function<br>

  - Remove the two print statements<br>
  - Open the file employees.txt in read mode and store the file object in a variable of your choice<br>
  - Using a for loop, go over the file using the file object above<br>
  - Using readline() methods, read the rest of the employee data into variables and strip the newline character<br>
  - Using an if statement check if the employee id passed as a parameter is equal to the employee id coming from the file<br>
  💡 Hint: Don't forget to strip the newline character<br>
  - If they are equal, in the if block,<br>
    &ensp;- Write a print statement to print the values like so<br>
    <code>Name: {name}</code><br>
    <code>Department: {department}</code><br>
    <code>Salary: {salary}</code><br>
    &ensp;- write a statement to close the file<br>
    &ensp;- write a return statement that returns the boolean true<br>
  - Outside the for loop, return the boolean false<br>
  🚩 If we made it outside the for loop, it means we didn't find the employee in the file<br>
</details>

<details>
  <summary>
    ✅ Edit the elif block corresponding to lookup employee
  </summary>
  Inside the employee_operations() function body
  Edit the function call to lookup_employee to receive the booloean in a variable of your choice<br>
  Check if the above variable is False, if it is, print <code>Employee Not Found</code><br>
  No else block necessary for now
</details>


<details>
  <summary>
    ✅ Modify display_employees
  </summary>
  Inside the display_employees function<br>
  <ul>
  <li>Comment out the four variable assignments</li>
  <li>Before the print statement, write a statement to open the file employees.txt in read mode and store the file object in a variable of your choice</li>
  <li>Using a for loop, go over the file using the file object</li>
  <li>Using appropriate number of readline() methods, read the rest of the employee data into variables (use the same variable names as the ones you have commented above)</li>
  <li>Strip the newline characters from all the variables</li>
    <li>Convert the salary to a float and store in the same variable ⏩ Tutorial: 2-10a</li>
  <li>Move the print statement you already wrote (using the f-literal) into the for loop</li>
  <li>Outside the for loop,<br>
  Write statement to close the file</li>
  </ul>
</details>


<details>
  <summary>
    ✅ Modify update_employee_dept
  </summary>
  Inside the update_employee_dept function<br>
  
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
  - Using an if statement check if the employee id that the user provided above is NOT equal to the employee id that was read from the file<br>
  💡 Hint: Don't forget to strip the newline character<br>
  - If they are not equal, in the if block, write all the employee data as-it-is to the output file<br>
  - If they are equal, in the else block, call the validate_employee_dept and store it in a variable. Concatenate them with a space<br>
  - Write the old employee id, old employee name, new department, and old salary to the output file.<br>
  💡 Hint: Don't forget to add a newline character to the new department
 - Outside the for loop,<br>
 - Write statements to close both the files<br>
 - Import the os module (make sure you write this statement at the very top of the file, outside any function definitions)
 - Using the os module, write statements to delete the employees.txt file and rename the temp.txt to employees.txt - before you do this make sure you backup your employees.txt file
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




