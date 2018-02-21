# noshow-prevention-api

## Problem
There are many great restruant reservation tools that exist in the world. However there is a lack in how there are preventions to stoping people from not showing up.
Restruants do not share information about their customers with others. Which create a disconnected flow of information.

## Solution
This noshow prevention API will allow reservation system to use our APIs to check if users have made reservations in the past and if they showed up on time.
Restrant owners can make the decision to allow or disallow their booking based on history.

### Implementaions
Initially, I only thought restrants were the only customers of this. However, anywhere there are reservation that occur, such as hospitals, event places (ex rock climbing, bowling), can use this tool to have an accurate expected time of arrival based on past experiences.

## API

### create_rsvp
takes in phone number with area code
returns json object with reservation_id, recent reservation history

if customer does not exist, will create a new customer object

### report_noshow
takes in reservation_id  
returns confirmation of report  

### get customer_id
takes in customer_phone number  
returns customer_id  

## Data Objects
### Customer Object
customer_id : `uuid`  
customer_phone : `string`  
customer_name : `string`  
rsvp_history : `rsvp_histroy`  

### rsvp_histroy
rsvp_histroy_id : `uuid`   
customer_id : `uuid`  
created_time : `timestamp`  
no_show : `boolean`  



## Support
If a user got a new phone and the previous user had a bad history, the history can be cleared by contacting customer support.
