# GET/tableNo

This is the call that is sent when the server wants to get the bill the GET request includes the table number. 
The order number is included in the response. 
Take out orders are table 99. When this is printed, the customer can pay the bill.

```JSON

{
   "orderNum":123,
   "timestamp":"2020-01-21T07:44:45-05:00",
   "Item1":{
  	"ItemOrdered":{
     	"type":"burgerMeal",
     	"Cost":10.99
  	}
   },
   "Item2":{
  	"ItemOrdered":{
     	"type":"salad",
     	"Cost":9.50
  	}
   }
}


```

## Response Schema

The following table shows the components of the response schema for GET/tableNo.

| Properties 	| Data Type 	| Definition                                                                                      	|
|------------	|-----------	|-------------------------------------------------------------------------------------------------	|
| orderNum   	| int       	| Shows the number that the order has. The counter resets to 1 at the start of business each day. 	|
| timestamp  	| timestamp 	| The timestamp shows the date and time of the order.                                             	|
| item (n)   	| string    	| Shows the items orderd. Including the object ordered and its cost.                              	|

The table below shows the properties for the object item (n).

| Properties 	| Data Type 	| Definition                                      	|
|------------	|-----------	|-------------------------------------------------	|
| type       	| string    	| Shows the type of main ordered.                 	|
| cost       	| float     	| Shows the price of the object that was ordered. 	|
