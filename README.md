<h1> Creating SQL Triggers </h1>

<h2>Description</h2>
This project demonstrates the use of SQL triggers to automate inventory management and track price changes in a product database. In Part 1, a trigger updates the Product_ReOrder field when inventory levels fall below a set threshold. In Part 2, a trigger logs changes to product pricing by capturing old and new values, change dates, and product IDs in an audit_log table. The project highlights essential SQL skills, including table creation, data manipulation, and trigger-based automation for inventory control and data auditing.
<br />


<h2>Languages Used</h2>

- <b> SQL </b> 

<h2>Project walk-through:</h2>
<p align="left">
<b> Part 1 </b> 
</p>
<p align="left">
The first step of this project was to CREATE a TABLE for “Products”. We did so by utilizing the following query: <br/><br/>
  <img src="Screenshot 2025-04-17 160044.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
<p align="left">
After creating the table, the next step was to insert values into the Products table.
We added 'PowerSupplies'  <br/> and 'Hard Disks' as the initial products, along with the corresponding values for each. <br/><br/>
  <img src="Screenshot 2025-04-17 160628.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
<p align="left">
Now that the last command was successful, we used the SELECT statement to retrieve and verify the inserted  <br/> values in the Products table. <br/><br/>
  <img src="Screenshot 2025-04-17 160649.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
<p align="left">
Next, we created a trigger on the Product_ReOrder field,as its initial value was set to 0—making it easy to verify  <br/> whether the trigger executed successfully. <br/><br/>
  <img src="Screenshot 2025-04-17 160703.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
<p align="left">
Then, we updated the Product_QOH and Product_MIN values to meet the trigger condition and activate the query. <br/><br/>
  <img src="Screenshot 2025-04-17 160715.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
<p align="left">
Finally, we used the SELECT statement to view the Products table and confirmed that the Product_ReOrder value  <br/> successfully changed from 0 to 1. <br/><br/>
  <img src="Screenshot 2025-04-17 160730.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>

<p align="left">
<b> Part 2 </b> 
</p>
<p align="left">
The first step is to create a new table called audit_log to record the old and new product prices, the date of each  <br/> change,and the corresponding product ID. <br/><br/>
  <img src="Screenshot 2025-04-17 160812.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
<p align="left">
Next, we created a trigger on the Price_History to capture and log price changes. <br/><br/>
  <img src="Screenshot 2025-04-17 160826.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
<p align="left">
Then, we updated the Products table by setting a new list price of 50 for the product with a code of 1. <br/><br/>
  <img src="Screenshot 2025-04-17 160846.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
<p align="left">
Finally, we used the SELECT statement to view the audit_log table and verify the recorded changes. <br/><br/>
  <img src="Screenshot 2025-04-17 160859.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
</p>
