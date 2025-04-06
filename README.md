# Credit_Card_Financial_Dashbord
Power BI Dashbord
Projective Objective : To Develope a comprehensive credit card weekly dashbord that provide real time insight into key performance 
                        metrics and trends, enabling stackholder to monitor and analyze credit card operation effectively.

steps : create some new columns that is
  1) AgeGroup : Create AgeGroup columns from Existing column called Customer Age

       Formula used : AgeGroup = SWITCH(TRUE(),cust_detail[Customer_Age] < 30 ,"20-30", 
                        cust_detail[Customer_Age] >= 30 && cust_detail[Customer_Age] < 40,"30-40",
                        cust_detail[Customer_Age] >= 40 && cust_detail[Customer_Age] < 50 ,"40-50",
                        cust_detail[Customer_Age] >= 50 && cust_detail[Customer_Age] < 60 ,"50-60",
                        cust_detail[Customer_Age] >= 60 ,"60+")
      
  3) IncomeGroup : Create IncomeGroup Column from Income Column that contain three category i.e "Low","Med","High"
     formula Used : SWITCH(TRUE(),
                                    cust_detail[Income] < 35000,"Low",
                            cust_detail[Income]>= 35000 && cust_detail[Income] < 70000,"Med",
                            cust_detail[Income] >= 70000 ,"High"
                            )) 


4) Create a new Measure for Revenue , Previous_week_revenue, Current_week_revenue and Week_over_week revenue to understand data more better way
