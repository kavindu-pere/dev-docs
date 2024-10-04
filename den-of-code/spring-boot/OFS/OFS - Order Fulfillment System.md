OFS will be a system of several microservices which will act to fulfill orders from customer.

Key services will be;
	1. order-service
	2. catalog-service
	3. notification-service

A client will call an endpoint of the order-service to create an order. Then the order-service will validate the contents of the order calling and endpoint of the catalog-service. Once the order is successfully validated, the order will be saved in the database.
Once the order is saved, the order-service will trigger an event accordingly. The notification-service is waiting for the event triggered by the order-service and once
the event is reached, the notification-service will send the outward notification such as email, or any configured medium.
[[OFS-rough-diagram.canvas|OFS-rough-diagram]]

