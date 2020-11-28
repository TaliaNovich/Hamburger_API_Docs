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


