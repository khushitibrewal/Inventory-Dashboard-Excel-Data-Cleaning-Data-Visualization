# Inventory-Dashboard-Excel-Data-Cleaning-Data-Visualization
This project showcases an interactive Excel-based dashboard designed to track, manage, and analyze inventory data. The dashboard visualizes key inventory metrics, highlights trends, and provides actionable insights, making inventory management easier and more efficient.

## Data Cleaning and Wrangling
**Stock Raw Data**
1. Ensure the Date column is in **Date format**.
2. Note: Here we have some missing values in Date column. We have ignored the missing values as the items in our inventory any way and we can find out the date of purchase in PO Raw Data Sheet.
3. The Branch column represents the different stores.
4. Item code represents Unique SKUs.
5. Category column represents 8 categories available with the company-(Medicines, Vitamins, Wellness, Home remdies, Mkaeup, Skincare, Haircare, Fragrance).
6. Pur Value represents company's cost to the product including gst.
7. Convert the data into table format.
   <img width="929" alt="image" src="https://github.com/user-attachments/assets/405a26b8-a2d9-4902-bb99-4ad160843874" />


**Sales Raw Data**
1. Ensure the date column is in date format.
2. From the date column, we have calculated the month and year column using text() formula.
3. Amount Paid column represents the amount paid by customers including tax.
4. Convert the data into table format.
   <img width="800" alt="image" src="https://github.com/user-attachments/assets/b7b178c0-ac13-4d90-8048-370f52523c5d" />

**PO Raw Data**
1. The month column is calculated using text() function on purchase date column.
2. Note: Negative value in purchase value reprents the item value that is returned to the vendor. Hence, these values are important to include in our final purchase value calculation.
3. Negative value under units column reprents the numbers of Units of that particular SKU returned to the Vendor.
   <img width="824" alt="image" src="https://github.com/user-attachments/assets/3b083f0b-f147-4536-a9b2-1ebb384d0ce7" />

**Tables**

- This table shows the inventory volume present at different stores for different categories. We have used sumifs() in stock Raw data sheet to calculate values in this table.
<img width="835" alt="image" src="https://github.com/user-attachments/assets/3dd92888-c845-412a-a7a5-c1c3a20461f6" />


- This table is calculated basis the previous three table.
- We have taken the average sales of last three months for those store that have been functional over 3 month.
- For newer store, we have taken the last months sales into consideration. 
<img width="736" alt="image" src="https://github.com/user-attachments/assets/bd8910ba-3de8-40b3-9804-40183506667f" />

- Days of inventory on hand (DOH) represents in how many days will the company sale the inventory present with it if it continues to make consistent sale as present.
<img width="653" alt="image" src="https://github.com/user-attachments/assets/0f6a8796-50a5-4fd2-ab2d-c39ac259efad" />

- Unique SKU is the number of unique SKUs present for each category at each location
- For this we first filter out the item code basis location and category using filter() function and then we used unique() function to find uniques skus. We used rows() function to get the count.
<img width="672" alt="image" src="https://github.com/user-attachments/assets/e3595618-7139-495b-a43a-1c24431e5bc7" />

- This shows month wise purchase volume for each category.
<img width="580" alt="image" src="https://github.com/user-attachments/assets/6df3023e-caf9-42fe-a64c-7d44619624b0" />


**Dashboard**

- Click on the cell to activate dropdown option.
- Select Prefered Location.
<img width="779" alt="image" src="https://github.com/user-attachments/assets/711d3401-7b31-42c7-922e-84e86c7f03ba" />

- Select Prefered Category.
<img width="766" alt="image" src="https://github.com/user-attachments/assets/2bdb6d3e-2fe9-4d6a-942c-a213278ddd6a" />


- Inventory Volume and Avg. Sales Per month is calculted basis the location selected.

<img width="491" alt="image" src="https://github.com/user-attachments/assets/5dacc882-062d-4676-bdec-298006a0f21f" />


- Here, select month to determine the purchase volume contribution of pharma and beauty in respective month as shown by pie chart.
- Select Category to determine purchase volume of the category over the month as shown in line graph
<img width="635" alt="image" src="https://github.com/user-attachments/assets/e874ce5f-8d5d-4f61-a87f-252c0b8454ad" />
