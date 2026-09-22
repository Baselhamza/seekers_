AmazIEEE


REQUIERMENTS

Functional
-The system receives orders.
- The system checks that every item is available and reserves it. 
-The system decides how many robots are needed to collect it.
-The system sends pick tasks to the assigned robots and follows their progress.
-Packing & Handoff: When all robots assigned to an order have finished, the system knows the order is fully collected, 
and it moves the order to the packing station and then to shipping.
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
-products list[]
-quantities
-status: Received → Confirmed → Picking → Collected
 → Packed → Ready for Shipping, or Cancelled / Failed
-total price
-number of robots assigned to collect it
-timestampe


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
-




---------------------------------------------------------------------------------------------------------------------------------------------
<img width="1364" height="808" alt="image" src="https://github.com/user-attachments/assets/55b1e874-1964-462e-aabb-a50271d48c70" />

---------------------------------------------------------------------------------------------------------------------------------------------
high level design
<img width="648" height="365" alt="Screenshot 2026-09-22 at 1 32 35 PM" src="https://github.com/user-attachments/assets/31cec687-cf56-4890-b80d-8f2fb5e03556" />



