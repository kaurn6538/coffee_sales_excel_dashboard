## Coffee Sales Dashboard
This Excel dashboard provides a comprehensive analysis of coffee sales data, featuring various charts and filters to enhance data exploration. The dashboard includes the following key components:

## Features
1. Bar Chart by Country: Displays sales distribution across different countries.
2. Top 5 Customers Chart: Highlights the top 5 customers based on sales.
3. Line Chart of Total Sales: Shows the trend of total sales over time.
4. Filters:
  *    Timeline Filter: Allows filtering of data by specific time periods.
  *    Roast Type Filter: Filters data based on the type of coffee roast (Medium, Light, Dark).
  *    Loyalty Card Filter: Filters data based on whether customers have a loyalty card.

## Data Preparation
Orders Sheet

Coffee Name: Derived using the formula:
  *     =IF(I2="Rob","Robusta",IF(I2="Exc","Excelsa",IF(I2="Ara","Arabica",IF(I2="Lib","Liberica",""))))

Roast Type Name: Derived using the formula:
  *     =IF(J2="M","Medium",IF(J2="L","Light",IF(J2="D","Dark","")))

Loyalty Card: Created using the formula:
  *     =XLOOKUP([@[Customer ID]],customers!$A$1:$A$1001,customers!$I$1:$I$1001,,0)

Country :Derived using the formula:
 *     =XLOOKUP(C2,customers!$A$1:$A$1001,customers!$G$1:$G$1001,,0)

Coffee Type: Derived using the formula:
  *     =INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!I$1,products!$A$1:$G$1,0))

Roast Tpye: using the formna:
 *     =INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!J$1,products!$A$1:$G$1,0))

Size: Derived Using the formula:
 *     =INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!K$1,products!$A$1:$G$1,0))

Unit Price: Using the formula:
 *     =INDEX(products!$A$1:$G$49,MATCH(orders!$D2,products!$A$1:$A$49,0),MATCH(orders!K$1,products!$A$1:$G$1,0))

## Charts and Pivot Tables
1. Bar Chart by Country: Created using a pivot table to display the sales distribution by country.
2. Top 5 Customers Chart: Created using a pivot table to highlight the top 5 customers based on sales.
3. Line Chart of Total Sales: Created using a pivot table to show the total sales trend over time.

## How to Use
1. Open the Excel file.
2. Use the filters to explore the data based on different criteria such as timeline, roast type, and loyalty card.
3. Review the charts to gain insights into sales performance across various dimensions.

## Installation
Download the Excel file from this repository.

Open the file in Excel.

## Contribution
Feel free to contribute to this project by submitting issues or pull requests. Any improvements or suggestions are welcome.

## License
This project is licensed under the MIT License.
