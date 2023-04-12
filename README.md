# Distributed and Cloud computing project - Group 28

## Details about service deployed:
The "microservices-demo" repository on GitHub contains the source code for a cloud-native microservices application on Google Cloud Platform. The application comprises 11 different services, each serving a specific purpose, as described below:

* Product Catalog Service: This service manages the product catalog for the application, including product details such as name, description, and price.
* User Service: This service handles user authentication and authorization, as well as user profile management.
* Cart Service: This service manages the user's cart, including adding and removing items from the cart, and calculating the total cost of the items.
* Shipping Service: This service manages the shipping of the user's order, including determining the shipping address and calculating shipping costs.
* Payment Service: This service handles payment processing for the user's order, including validating payment information and charging the user's credit card.
* Recommendation Service: This service provides recommendations for products based on the user's browsing and purchasing history.
* Email Service: This service sends emails to the user, such as order confirmation and shipping notifications.
* Frontend Service: This service provides the user interface for the application, including browsing products, adding items to the cart, and checking out.
* Load Generator Service: This service generates test data to simulate realistic user traffic to the application.
* Ad Service: This service provides targeted ads to the user based on their browsing and purchasing history.
* Queue Master Service: This service manages the queue of orders waiting to be processed by the shipping and payment services, and ensures that the orders are processed in a timely and efficient manner.

Overall, each service in the microservices application has a specific role and contributes to the overall functionality of the application.

## Communication patterns

The application employs the gRPC framework for communication between services, using a synchronous request-response pattern. Whenever a service needs to interact with another service, it sends a request message via gRPC, containing relevant operation data for the destination service to execute. The destination service processes the request, generates a response message containing operation results or error messages in case of failure, and sends it back to the originating service. This communication pattern is beneficial as it allows services to operate independently, scale efficiently, and evolve freely. Additionally, gRPC offers an efficient and high-performance communication mechanism for cloud-native microservices applications.

## Design diagram provided by the developers of the application
<img width="1778" alt="architecture-diagram" src="https://user-images.githubusercontent.com/39703778/225204560-8fbc9f44-62bc-48e8-9cae-89d7722f38bd.png">

## Istio-Kiali Service Mesh view
<img width="1778" alt="architecture-diagram" src="https://raw.githubusercontent.com/garcharjay811/dcs-group28/main/Istio-Kiali%20dashboard.png">
