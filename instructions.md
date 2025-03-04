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

# Instructions



<details>
  <summary>
    ✅ Code improvement
  </summary>

  - Wherever you have <code>if found == True:</code> replace it with <code>if found:</code>
  - Wherever you have <code>if found == False:</code> replace it with <code>if not found:</code>
</details>


## In functions.py


<details>
  <summary>
    ✅ Modify update_employee_name
  </summary>
  
  - Follow the same code logic as the other update functions from HW03 and write code to modify an employee name given their employee ID
  - 🚩 Remember! Employee name is employee first name, space and employee last name. So you will be calling two validate functions and concatenating those values appropriately to get the full new name
  - 📜 Execute to make sure it works correctly
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
  - Place three readline statements inside the for loop to read every 4th line in the for loop variable
  - Outside the for loop, convert the for loop variable to int and store in the same variable or another variable (The loop variable will store the last employee ID of the file)
  - Add one to the above variable and **convert it to string**
  - Return the above string
  - 📜 Execute the code and test Add Employee and make sure it is being calculated correctly
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
  - You will receive points if you can handle exceptions in at least three functions. If you run out of time, the remaining must be done at home before the next assignment
</details>

## Hierarchy Chart

<details>
  <summary>
    🚩 Hierarchy Chart
  </summary>

  - Draw hierarchy chart to reflect the updated code. You may hand draw or use any online visual tool like (draw.io)
</details>




