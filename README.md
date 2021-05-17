# Analyze Supermarket Data Across the Country - Company XYZ

In this project, I analyze and report findings on the **Sales** data for Company XYZ which owns a supermarket chain across the country. Each major branch of the supermarket is located in 3 cities across the country and the data consist of a record of sales information for 3 months. The aim of this project is to help the company understand its sales trends and determine its growth, and possibly make a few recommendations to improve the business.

# Project Steps

Each branch of the supermarket in the 3 cities have submitted similar datasets containing the same information across a 3-month period. Some of these information include:
    * City
    * Customer type
    * Product line
    * Gender
    * Payment type
    * Details of goods purchased like quantity and amount paid
    * Time and Date of purchase
    * Customer Satisfaction rating
    * etc
    
Below are the steps I have followed in preparing and analyzing the dataset in order to obtain insights and trends from the sales records:
### Step 1
* Each dataset (file) per branch which is available in a `.csv` file is combined into a single file, exported into a `.csv` and read into a pandas dataframe.
### Step 2
* A data exploration was done on the combined dataframe to confirm its shape, object type, missing value, and to get a statistical summary of the data.
### Step 3
* The `Date` and `Time` datatype were updated to the `datetime` datatype.
* Features of `Date` and `Time` were extracted into separate additional columns for further analysis.
### Step 4
* A list of all unique entries in all the categorical columns of the dataframe was obtained, as well as a count of all unique entries per column.
### Step 5
With the intent of analyzing the supermarket data across the 3 branches, an Aggregation with Groupby method across the 3 branches of interest was done on the dataset; and the following analysis done:
    * The `sum` and `mean` of the **gross income** across the branches was calculated.
    * The time of the day with the most shopping payments across the cities.
    * The City (branch) with the highest rating by Customer Satisfaction
    * The City (branch) with the highest Total Quantity of purchases
### Step 6
In this Step, further analysis was done using **Charts** and **Graphs** to obtain the following:
    * Determined the branch with the highest sales record using a `countplot`.
    * Determined the payment type breakdown per branch, using a `countplot`.
    * Determined the highest & lowest sold product line, using `Countplot`.
    * Determined the Payment channel used by most customer to pay for each product line.
    * Determined the Payment channel for each branch.
    * Determined the branch with the lowest rating using a box plot.
    * An analysis of the gender type versus the kind of products being purchased at the supermarket was done using the `catplot`.
    * The interaction of Unit price on the Quantity of goods purchased. 

# Insights

Below is a summary of the insight obtained from the indepth analysis performed.

* The city with the highest total gross income: Port Harcourt
* The time of day with most shopping payments in Port-Harcourt is the 10th hour.
* The time of day with most shopping payments in Abuja is the 19th hour.
* The time of day with most shopping payments in Lagos is the 10th hour.
* The city with the highest Customer Satisfaction rating on average on their overall shopping experience is Port Harcourt.
* The city with the highest Total Quantity of Purchases is Lagos.
* **Branch A**, which corresponds to Lagos has the highest sales record.
* **Epay** ranks as the most used form of payment in Branch A and Branch B, while **Cash** payment tops the charts for Branch C.
* The **Fashion accessories** product line registered the highest number of sales, while the **Health and beauty** line was the least sold across the Branches.
* **Cash** stands out as the most preferred payment for **Electronic accessories**, while **Epay** is preferred for **Home and lifestyle**.
* The branch with the lowest rating is Branch B, which corresponds to the city of Abuja.
* Across the Branches, females purchased more of the all the available Product line except for **Health and beauty**, than males.
* Although the analysis shows that Males spent more money than Females in the **Sports and travel** Product line, even though Females purchased more in quantity.
* Males also spent more money in the **Health and beauty** Product line, and purchased more quantities than Females here as well.
* The most expensive product by unit price is the **Fashion accessories** line, which registers the least patronage from customers across all the product lines.
* Though the **Sports and travel** product line is one of the most expensive products, customers patronage is not as low when compared to the **Fashion accessories** product line. This could mean that customers value **Sports and travel** more than they do **Fashion accessories**.
* The cheapest product by unit price is **Electronic accessories** which shows a corresponding high patronage by Quantity.


# Future Work

Future work on this project would involve analyzing the fastest and slowest moving moving Product line by being able to combine the frequency and Quantity of purchases. This can then be used to recommend products to promote or products to roll back investment on.

# Standout Section

I explored the interaction between Customer type and Quantity of Product line purchased using a `catplot`.

* Use the `catplot()` to plot `Product line`, and `Quantity` purchased. Set the kind parameter to `box`, and set the hue to `Gender`.

#### Insights

The average quantity purchased by either male or female is the same for the following Product lines:
    * Food and beverages
    * Electronic accessories
    * Sports and travel

The average quantity purchased by Female is more than that purchased by their male counterpart for the following Product lines:
    * Fashion accessories
    * Home and lifestyle
    
The average quantity purchased by Male is more than that purchased by their female counterpart in the Health and beauty Product line.