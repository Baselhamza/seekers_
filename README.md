AmazIEEE


REQUIERMENTS

Functional
-The system receives orders.
- It validates the order and makes sure the same order is never processed twice.
- The system checks that every item is available and reserves it. 
-The system decides how many robots are needed to collect it.
-The system sends pick tasks to the assigned robots and follows their progress.
-The system must handle robot failures
-Packing & Handoff: When all robots assigned to an order have finished, the system knows the order is fully collected, 
and it moves the order to the packing station and then to shipping.
-system must send notifications for operators
------outofscope----------
-
-
-
-


Non functional
-Consistency for making orders same order is never processed twice &
two orders can never claim the same last unit.
-Availability for users
-system must handle high throughput  while high traffic  events
-Observability for robots failures    
-law Latency for 
-----out of scope------
-Security
-
-
-
-
-
---------------------------------------------------------------------------------------------------------------------------------------------
DATA MODEL

1.ORDER:
-id
-product in order list[]
-total quantity of products
-status: (Received → Confirmed → Picking → Collected
 → Packed → Ready for Shipping, or Cancelled / Failed
-total price)
-number of robots assigned to collect it
-timestampe
-metadata...


2.ROBOTS
-id
-battery condition
- location
-assigned order
-assigned task id
-status :available| busy | broke|

3.PRODUCT IN ORDER 
-product id
-order id
-quantity

3.PRODUCTS
-id
-quantity
-location
-metadata....


4.user
-id
-name
email
metadata....



---------------------------------------------------------------------------------------------------------------------------------------------
API
