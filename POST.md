# POST/lunch/mealCat/burgerMeal

The following is a POST/lunch request. 
This is what it would look like when a custumer has finished thier order and clicked confirm order.
After the code snippet is an explination of all the variables and thier valuse.


``` JSON
  {
     "mealType":"lunch",
     "mealCat":{
  	  "main":"burgerMeal",
  	  "burger":{
        "pattyType":"”beef”",
        "pattyQty":1,
     	  "pattyWeightG":300,
     	  "pattyCook":"MR",
     	  "bunType":"wholeWheat",
     	  "condiment1":"ketchup",
     	  "condiment2":"secretSauce",
     	  "topping1":"lettuce",
     	  "topping2":"pickles",
     	  "topping3":"None",
     	  "topping4":"None"
  	  },
  	  "sides":{
     	  "side1":{
        	  "type":"frenchFries",
        	  "size":"large"
     	  },
     	  "side2":{
        	  "type":"none",
        	  "size":""
     	  }
  	  },
  	  "drink":{
     	  "type":"Coke",
     	  "size":"large",
     	  "ice":"yes"
  	  },
     },
  }
  
```


The mealType object for this POC is limited to lunch. In the future, mealType can include breakfast and dinner. 
The mealType will be determined by when the order is placed. For example, lunch is between 12:00 PM-5:00 PM. 
The diner can adjust the time of when each meal is served. 

**Note:** The mealtype can not be manually changed in an order.

Lunch is a mealtype that consists of different choices of mealCat. 
For this POC, this document will only include the burgerMeal. 
The bugerMeal consists of 3 objects: A main dish, side dishes, and a drink.
At least one side dish must be ordered.

| Object        | Data Type     | Values     | Defenition    |
| ------------- | ------------- | ---------- | ------------- |
| main          | string        | burgerMeal |Burger with bun, condemints,toppings, a choice of 2 side dishes, and a drink |

## Burger

This is a JSON object of a burger of the burgerMeal in lunch. 
The burger object consists of properties that describe the burger. 
All properties are mandatory, there are no default values.
Use *“none”* for a null value.
Properties marked with an (n) are properties that can be entered more than once, where (n) represents a number. For example, condiments1. 

| Properties    	| Data Type 	| Values                                	| Definition                                                                          	|
|---------------	|-----------	|---------------------------------------	|-------------------------------------------------------------------------------------	|
| pattyType     	| string    	| beef, veggie lamb                     	| Choices of different types of burgers including beef, veggie, and lamb              	|
| pattyQty      	| int       	| 1, 2, 3                               	| The number of patties on the burger. All are the same type. Limit of patties is 3.  	|
| pattyWeightG  	| int       	| 100, 200, 300                         	| The number representing weight of the patty in grams. The limit is 300.             	|
| pattyCook     	| string    	| MR, M, MW                             	| The cook on the patty. MR-medium rare, M-medium, MW-medium well.                    	|
| bunType       	| string    	| white, wholeWheat, none               	| Choices of different types of buns including whole wheat, white, and no bun.        	|
| condiment (n) 	| string    	| ketchup, bbqSauce, secretSauce, none  	| A choice of up to two condiments. A choice of none means no condiment.              	|
| topping (n)   	| string    	| lettuce, pickles, tomato, onion, none 	| A choice of up to four toppings. A choice of none means no toppings                 	|

## Sides

This is the JSON object for side dishes. 
Object side1 is mandatory and must be filled in with values. 
Object side2 can be the same as side one. 
If *“none”* is chosen as a value, size will automatically appear blank in the code.

| Properties 	| Data Type 	| Values                                      	| Definition                           	|
|------------	|-----------	|---------------------------------------------	|--------------------------------------	|
| type       	| string    	| frenchFries, onionRings, potatoWedges, none 	| A choice of different types of sides 	|
| size       	| string    	| small, medium, large                        	| A choice of portion size.            	|

**Note:** Use *"none"* to indicate a null value where applicable.

## Drink

The object drink is mandatory. 
All properties must be filled in with a value. 
If *"none"* is chosen for type size and ice will be filled in as blank in the code.

| Properties 	| Data Type 	| Values                                  	| Definition                           	|
|------------	|-----------	|-----------------------------------------	|--------------------------------------	|
| type       	| string    	| coke, fanta, sprite, water, juice, none 	| A choice of one drink type.          	|
| size       	| string    	| small, medium, large                    	| A choice of drink size.              	|
| ice        	| string    	| yes, no                                 	| A choice of adding ice to the drink. 	|

**Note:** Use *"none"* to indicate a null value where applicable.

## POST Response Example 

When a correct order is placed, the server replies to the app with an acknowledgment. 
This is not displayed to the user.  

```JSON
200 OK

```
