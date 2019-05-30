# Data-blog-project

## Required libraries

- python 3.6.3
- pandas 0.20.3
- numpy 1.12.1
- matplotlib 2.1.0

## Introduction

This project is to provide an answer for the transaction analysis of a retail store in a country.Dataset used is present on "https://www.kaggle.com/azzabiala/corporacin-favorita-grocery-sales-forecasting%22"

Here are the business questions that need to be answered:

1)What is the total number of transactions has been done in each state?

2)Which state got the highest and minimum transaction along with their values?

3)Which city has National Holidays in 2017 ?

4)What are the average oil price in every year and in which year oil prices were increased too much on an average?

5)Which family has the lowest item numbers?

6)Describe the transactions on weekly basis?

## Files

- Data_blog.ipynb: It answer the question asked
- Data_blog.html: As the same of above notebook but format is html.

The link for blog post is https://medium.com/@shivangipatel255064/data-blog-project-udacity-8a1cbde23903. Datasets Link: https://www.kaggle.com/c/favorita-grocery-sales-forecasting.

## Answers

![alt text](https://github.com/Shivwinx100/Data-blog-project/blob/master/pic1.png)

1) Above graph show state wise total transaction, we just need to group them by state and sum up.


|         State                 |   Transaction     |
|-------------------------------|-------------------|
|Azuay                          |    	5673847       | 
|Bolivar                        |   	2107489       |
|Chimborazo	                    |    2287850        |
|Cotopaxi                       |    	3531356       |
|El Oro	                        |    3945341        |
|Esmeraldas                     |   	2182356       |
|Guayas	                        |    21894000       |
|Imbabura	                      |    2209898        |
|Loja	                          |    2867052        |
|Los Rios                       |     4049047       |
|Manabi                         |   	2906765       |
|Pastaza                        |    	504156        |
|Pichincha                      |   	74971545      |
|Santa Elena	                  |      1520362      |
|Santo Domingo de los Tsachilas | 	  4655266       |
|Tungurahua	                    |    6172615        |

2) As per graph Pichincha satae has the highest with 74971545transaction and Pastaza state has the minimum with 504156 transactions.

3) For this we first need to merge the stores and holidays dataset then we need to find out those rows which fall under 2017 year and   has national holiday and its respective city, lastly We have to group by city to get list of the cities. As the result cities are 		
Ambato
Babahoyo
Cayambe
Cuenca
Daule
El Carmen
Esmeraldas
Guaranda
Guayaquil	
Ibarra	
Latacunga
Libertad
Loja	
Machala	
Manta	
Playas
Puyo	
Quevedo
Quito	
Riobamba
Salinas	
Santo Domingo

![alt text](https://github.com/Shivwinx100/Data-blog-project/blob/master/pic2.png)

4) For this first We need to merge the store and oil dataset. Ten calculate the year wise mean of oil price. From above graph we can tell the answer is 2013.

![alt text](https://github.com/Shivwinx100/Data-blog-project/blob/master/pic3.png)

5) For this question's answer we just need to gruop it by family and item number and gets its count.The answer is Baby Care, Home appliances and Books.

![alt text](https://github.com/Shivwinx100/Data-blog-project/blob/master/pic4.png)

6) For this we need to group it by week and get the total transaction. From above graph we conclude that 52 week has highest and 35 week has the minimun transaction recorded.


## Conclusion

We have successfuly answer the all the Question. Most of the Question's answer was easily derivable from the graphs but for the count and preciseness we need to refer the output of the code.

As far cleaning of Data is concerned We have chose to drop and replace the NaN value as per the requirement.For example in the Q-3 we just need the rows in which holiday rows where mention so there we drop the NaN values while finding the average oil price we required all the rows so we replace the Nan value with mean values. Imputation was not implemented as the dataset was not that big or complex or any training models were used to perform the analysis that would required to write imputer code which in would have it more complex to see.
