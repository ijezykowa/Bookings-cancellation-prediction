# Bookings-cancellation-prediction
Prediction of bookings cancellation in hotels
ABOUT THE PROJECT:

In the age of the Internet, new channels for hotel bookings have radically 
changed customer opportunities and behavior. A significant number of hotel 
bookings are missed due to cancellations or underbookings. This is often 
made easier by the ability to do it for free or at a low cost, which 
benefits hotel guests, but is problematic for hotels.
Our goal is to predict potential cancellations of hotel reservations. 
This will allow owners to optimize pricing/reservation conditions.

Data Dictionary

Booking_ID: unique identifier of each booking
no_of_adults: Number of adults
no_of_children: Number of Children
no_of_weekend_nights: Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel
no_of_week_nights: Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel
type_of_meal_plan: Type of meal plan booked by the customer:
required_car_parking_space: Does the customer require a car parking space? (0 - No, 1- Yes)
room_type_reserved: Type of room reserved by the customer. The values are ciphered (encoded) by INN Hotels.
lead_time: Number of days between the date of booking and the arrival date
arrival_year: Year of arrival date
arrival_month: Month of arrival date
arrival_date: Date of the month
market_segment_type: Market segment designation.
repeated_guest: Is the customer a repeated guest? (0 - No, 1- Yes)
no_of_previous_cancellations: Number of previous bookings that were canceled by the customer prior to the current booking
no_of_previous_bookings_not_canceled: Number of previous bookings not canceled by the customer prior to the current booking
avg_price_per_room: Average price per day of the reservation; prices of the rooms are dynamic. (in euros)
no_of_special_requests: Total number of special requests made by the customer (e.g. high floor, view from the room, etc)
booking_status: Flag indicating if the booking was canceled or not.


General conclusions: 

-No missing values
-Booking_ID having the exact amount of unique values as the amount of rows does not influence the cancellation predicition
-There are twice as many canceled bookings as non-cancelled bookings
-No strong correlation between variables - features are not collinear.
-The strongest correlation is visible between a repeated_guest and no_of_previous_cancellations and no_of_previous_bookings_not_canceled but as repeated_guest is a binary data it cannot be comprehended in this way
-There is a correlation between avg_price_per_room and the no_of_adults and no_of_children
-Lead time strongly influences the amount of cancellations (bookings made in longer advance are cancelled more often)
-Bookings for stays during week days do not influence the amount of cancellations
-Bookings for stays during weekends are more often cancelled than not
-Most bookings are made for two adults, without children. When the amount of children equals 2, the possibility of booking cancellation rises.
-Proportion of cancelled and not-cancelled bookings for weekend stays is even.
-The more special requests, the lesser probability of booking cancellation.
-The most often booked is Room_Type 1, at the same time the amount of cancellation rises for Room_Type 6.
-Corporate bookings are cancelled less often.
-The amount of cancellation rises for Meal_Type 2.
-Bookings without parking space are made more often.
-Proportion of cancelled and not-cancelled bookings for arrival on a specific month day is even. The least cancelled bookings is for stays on 25th day of month.
-Bookings are made more often for the second part of the year. The highest risk of booking cancellation is for the summer months (between June and August).
-The amount of not-cancelled bookings is biggest between November and December.
-The most often made bookings are for the price per room between 50 and 150 EUR.
-The shorter period between booking date and arrival date, the lesser the possibility of booking cancellation. For bookings made with 150 days advance period, the possibility of booking cancellation rises.




For better understanding of the actions undertaken in this project, here is the step list:

-EDA
-Data preprocessing
-Pipeline implementations
-Models implementations (Logistic Regression, Dummy Classifier, Random Forest)
-Metrics implementations (F1 score, Confusion Matrix, Accuracy Score)



Final conclusion after implementing metrics: 

The best suited model is Logistic Regression.
