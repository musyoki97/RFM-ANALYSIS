# RFM-ANALYSIS


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hpb2q80opkuujnrkj9c8.png)
>**RFM (recency, frequency, monetary)** analysis is a marketing technique used to quantitatively rank and group customers based on the recency, frequency and monetary total of their recent transactions to identify the best customers and perform targeted marketing campaigns. 

RFM analysis is a powerful technique used by companies to better understand customer behaviour and optimize engagement strategies.<br>  
The given dataset is provided by an e-commerce platform containing customer transaction data including customer ID, purchase date, transaction amount, product information, ID command and location. The platform aims to leverage RFM (recency, frequency, monetary value) analysis to segment customers and optimize customer engagement strategies.<br>  
This Python code performs RFM (Recency, Frequency, Monetary) analysis on the customer dataset and then segments customers based on their RFM scores. Here's a breakdown of each part of the step by step analysis:<br>  
- **1. Import Libraries:**
I started by importing the Pandas library for data manipulation and analysis, datetime for handling date and time data and Matplotlib library for creating visualizations.
  
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ymqqs8iwwpiuf0cz8qjc.png)
 Convert PurchaseDate to datetime:  
- **2. Read Data:**  
Reads the Excel file with data set named "rfm_data.xlsx" and stores it in a Pandas DataFrame called df.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hn3c1n2ybhrmq6e3vn3m.png)
- **3. Convert Date to Datetime:**  
Converts the 'PurchaseDate' column to a datetime format using the specified date format.
This indicates that the following line of code is converting the 'PurchaseDate' column in the DataFrame df to a datetime format using the specified date format. This is essential for working with date-based calculations in RFM analysis.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2bioe2kub00io9x81mjo.png)
- **4. Calculate recency, frequency, and monetary values:**
This signals the beginning of the section where recency, frequency, and monetary values are calculated for each customer. These values are crucial for RFM analysis as they help in understanding customer behavior.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/bbvd3djyl8s6xw0wylh2.png)
- **5. Rename the columns:**
Here, the code is renaming the columns in the DataFrame rfm_df for clarity. The columns are renamed to 'CustomerID', 'Recency', 'Frequency', and 'Monetary' for easier interpretation.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/wst2fbi6su9c8ye9swtv.png)
- **6. RFM Scoring:**
I introduced the section where RFM scores are assigned to each customer. RFM scores are calculated based on quartiles, and there are separate functions for scoring recency, frequency, and monetary metrics. These scores are then stored in the 'R_Score', 'F_Score', and 'M_Score' columns.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vv5pl8gdh9a0f3osn8x5.png)
- **7. Calculate RFM Score:**
This code indicates that the code calculates the overall RFM score for each customer by combining the individual Recency, Frequency, and Monetary scores. The result is stored in the 'RFM_Score' column.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/f1wuet8cgi0t2gfbzdps.png)
- **8. Customer Segmentation:**
This marks the beginning of the customer segmentation section. The code defines a function, segment_customer, which assigns customer segments ('High-Value', 'Mid-Value', or 'Low-Value') based on their RFM scores. The results are stored in the 'Segment' column of the rfm_df DataFrame.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ekx8bt8wqshzqns2wc4c.png)
- **9. Count the number of customers in each segment:**
The code counts the number of customers in each of the segments created in the previous step. The counts are stored in the segment_counts variable, and this information is used for further analysis and visualization.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sdm548tuk97uizx2vc3k.png)
- **10. Create a bar plot to visualize the segments:**
Here, the code prepares to create a bar plot using Matplotlib to visualize the customer segments. It sets the figure size, assigns a color to the bars, and adds a title and axis labels to the plot.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0m67hk6eajd2gx15b06t.png)
- **11. Annotate the bars with segment counts:**
This explains that the code loops through the segments and annotates the bars in the bar plot with the respective segment counts. This step provides a visual representation of the number of customers in each segment.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/z924usjlevu686q3wk57.png)
- **12. Show the Plot:**
The final code instructs the code to display the created bar plot with the annotated bars, allowing you to visualize the customer segmentation based on the RFM analysis.  

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0e38pnknrkhf2o1p770e.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/thsh83ffsmlvbkn2npzt.jpg)
