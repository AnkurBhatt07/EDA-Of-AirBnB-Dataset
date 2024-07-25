# EDA-Project-on-AirBnB-dataset

Here , we are performing data analysis on the AirBnB dataset . It will provide us various key understandings out of this huge data . 
In the process we will first clean the data from various anomalies and then create subset dataframes for analysis . We will also create visual representation of various key understandings , which makes it easier to spot the trends and patterns from the data. 

The dataset we have,contains **the information of the lodgings present in the boroughs of the New york city**.**The dataset contains 48895 rows and 16 columns.**

# Data Wrangling

There were listings where Price value was equal to 0.This was unrealistic to happen practically so I assume this was some issue in data collection . To solve the issue , I calculated the average prices of each room types from the entire dataset and then replaced these uneven prices for the listings with the average prices based on their room types.

There were 17533 listings where availability 365 was filled with 0 . This implied that these listing are never open for rentals in an entire year. On analysis of these listings , I found that these listing never went well of . It can be seen through the number of reviews in the listings which are very less and through the date of last review which is either NaN or a very past date representing the listing has been shut.

Then we changed the data type of the last_review column from string to datetime.It helped us look upon the date range of the data . Also we were able to sort based on it and derive a basis for data cleaning and preprocessing . As we saw that the date range of the data is from April 2011 to July 2019 , we assumed that the listing who have not got any reviews after 2016 are not out of business. So we dropped those listings.

Then we analysed the reviews_per_month column where there were 5000+ null values . On inspecting it was found that the listings where number of reviews is equal to 0 and has null for last_review column as well , were associated with each such reviews_per_month with null values. So basically these listings were never visited by customers and hence got no reviews . We kept those listings as there was nothing else wrong with them.

Then we checked the minimum_nights column with too high values. Higher minimum nights represents that the listing are available for longer periods.I assumed that these listings are authentic because it could be that the owners want long term gains from the listings. The analysis also made us conclude that too high prices are less frequently visited by the customers in case of listings offered for longer periods . That is very obvious because if someone is staying in a place for a long time period , he will definetely want more economical rental on per day basis. Higher prices per day in case of long stays will diminish customers.

**INSIGHTS FOUND**

According to number of listings in each neighbourhood group , Manhattan is the most preferred by hosts and,by inference most preferred by customers as well.It is followed by Brooklyn and then Queens.

In neighbourhoods , Bedford-Stuyvesant in Brooklyn is most preferred , followed by Williamsburg in Brooklyn , then Harlem in Manhattan.

The maximum number of Entire home/apt are in Manhattan .While the maximum number of Private rooms are in Brooklyn.

The average Price of Entire home/apt is the highest among all room types.

**SOLUTION TO THE PROBLEM STATEMENT:**

1. MANHATTAN is the most preferred neighbourhood group by the tourists.

2. HARLEM neighbourhood is most preferred by tourists in Manhattan.

3. BEDFORD-STUYVESANT is the most preferred neighbourhood in all of the neighbourhood groups.It is in Brooklyn.

4. Entire home/apt is the most preferred room type by the tourists.

5. The average price of Entire home/apt is highest in Manhattan,followed by Brooklyn and Staten Island

6.The average price of Private room is highest in Manhattan , followed by Brooklyn.

7.The price range of top 10 most popular shared rooms is 35 to 70 dollars

8.The price range of top 10 most popular Entire home/apt is 125 to 190 dollars

9.The price range of top 10 most popular Private rooms is 46 to 55 dollars

10.Most reviewed listings are owned by ['Asa', 'Carol', 'Danielle', 'Dona', 'Jj', 'Linda', 'Maya']

11.Most reviewed listings in Manhattan are owned by ['Agnes', 'Carol', 'Jj', 'John', 'Jon', 'Seth', 'Shunichi']

12.Most reviewed listings in Brooklyn are owned by ['Amia', 'Asa', 'Benjamin', 'Dani', 'Dennis', 'Evelyn', 'J. E','Janet-David', 'Martin', 'Waldemar']

13.The most preferred Entire home/apt rentals had minimum nights in range of 1 to 3 days.

**Solution to the business objective:**

The business Objective of the Client Company is to increase the customer's influx to the website and inturn increase company's revenues.To achieve the increase in the customer's influx to the website , we have to implement a multi-faceted strategy .

Firstly , as apparent from the data analysis , there is a high demand of rentals in Manhattan and Brooklyn so increasing the number of listings from these two neighbourhood group will boost the website's influx . It will stabilize the high demand in there and more number of rentals taken by tourists will increase the company's revenues. Similiarly , for Entire home/apt and Private rooms , there is more demand especially for entire home/apt , so increasing the number of these room types will increase the revenues . It can be incentivized by connecting with the owners of the shared rooms which are not able to commercialize to upgrade their listing to private rooms.

Get in touch with the hosts of the top performing listing owners(based on the number of reviews in the listing) . Provide them some incentives that mutually benefits both the host and the company . Like giving task of finding more such attractive listings to those top performing hosts and getting paid accordingly.Or creating more such listings with financial aid from the company , where profits will be shared in a agreeable terms. Or like getting ideas from these top performing owners about how they made their listings so attractive to the tourists . Sharing these ideas with the other owners especially with host having high number of listings.

Provide the hosts with the most suitable plan based on their location.They can be suggested the most attractive minimum nights for their listings and the most attractive Price range for their listings.

The listings that have never been visited by customers , where there are no reviews can be provided suggestions for like changing the price of the listings. Many such listings are too highly priced , that is discouraging the customers . Other reason that can be attributed to the low customer influx to these listings is that the minimum nights are too high and for such high number of minimum nights , the price per day is too expensive. These advices can be a game changer for the hosts as well as the company and it will cause the increase in the profits of the company.

We can also see that rentals in Queens , Staten Islands and Bronx are less demanded.We can commercialize these regions to an extent.Using the latitude and longitude data , we can find out the neighbourhoods in these less demanded neighbourhood groups that lies on the boundaries of the most demanded neighbourhoods of Manhattan and Brooklyn.Here in these less commercialized neighbourhoods , we can promote new listings for rentals and can increase our revenues along with promoting rentals in these new neighbourhoods.



