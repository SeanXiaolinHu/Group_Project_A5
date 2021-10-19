# Group_Project_A5
Memo of the group project by A5:

1. Executive Summary: 

Based on our best model, we find the total review, neighborhood, room type and 30-day availability of the property are significant factors that will influence the total cost for 2 people staying 4 nights. Specifically, the total review will actually inversely affect the room price. As the coefficient is about -0.0025, then we can say that for every unit of increase in total review, the total cost will decrease by 0.25%. This can be explained as people may want to avoid the properties that are too popular and crowded, which relates to concerns like noise and safety.

As for neighborhood, we have simplified them into five categories: west, east, north, south and central. Our regression results tell us that if the property is in east/north/south part of Milan, then the total cost will all be cheaper than that of the baseline central property by about 50%. However, there is no significant difference for the cost of properties in central part and western part. This can be explained as people always prefer living in the center of a city as it makes life more convenient, and for Milan maybe the west part is also as modern as the center.

Considering room type, we find that compared with entire room, the total cost of private room on average would be cheaper by about 29%. It also makes sense as people would rather choose to enjoy all the rooms buy themselves rather than share some of the rooms with others.

Finally, the availability in next 30 days of a room is positively correlated with the total cost. In other words, for one more availability, the total cost of that room would increase by 2%. This can be explained as people may avoid the too expensive rooms, so the availability of these rooms will be larger than the cheaper ones.


2. Data Exploration and Feature Selection: 

The dataset consists of 4 types of data as following: 24 character data including description and host_name, 5 date data including frist_review and last_reveiw, 8 logical data including host_is_superhost and instant_bookable, and 37 numeric data including beds and accomodates.

After looking at the distribution of price, due to the highly right-skewed distribution of the original price data, we introduced a new variable to log the price to simulate the normal distribution. We also use the IQR rule to elimminate the outliers. As there are 52 unique property types, so we also explore the distribution of the property type, and only keep the top 4 most common property types which make up more than 85% of total properties types. 


3. Model Selection and Validation: 

We use the linear regression to fit the model. We use the data obtained from AirBnB to train the model, and calculate the adjusted r square as well as VIF to determine if it fits the data well without collinearity. We will use different variables in different models, and if the variable is not significant according to the t-statistics, we will remove it and try to add another one that me related to the total cost, and repeat. 

The best model is model 6, which has already be explained in part 1 above. This model is selected as it has the relatively largest adjusted r square while VIFs are low, and all the variables within are significant with a possible economic explanation. We also use a subset of the original data after filtering according to our criteria, to get the predicted results and compare them with the real values. The gaps are always within the 95% confidence interval, which is acceptable,


4. Findings and Recommendations:

As stated, the findings are covered in the part 1. We think for future improvement, we can make the analysis better by trying to test more variables as well as more advanced forms of the regression equation. For example, we can consider the possible interaction between variables, try higher powers of variables, etc.



