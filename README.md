# Online-Stationary-Mart-Microservices
Developed Spring Boot Project depicting the digitized simulation of Online Stationary Mart and demonstrating the advantages of a microservices-based approach.

                ┌──────────────────────────┐
                │     Eureka Registry       │
                │  (Service Discovery)     │
                └─────────▲──────▲─────────┘
                          │      │
             (services register / Gateway discovers)
                          │      │
[ Client (Web/Mobile) ] → [ API Gateway ] 
                             │
         ┌───────────┬───────┴───────────┬─────────────┐
         │           │                   │             │
  [ User Service ] [ Product Service ] [ Order Service ] 
   (Auth/Profile)    (Catalog)          (Create Orders)
                         │
                         ▼
               [ Inventory Service ]
                (Stock Validation)
                         │
                         ▼
           ┌─────────────┬─────────────┐
           │             │             │
      [ Email Service ][ Batch Service ][ PromptAI Service ]
    (Order emails)   (Scheduled jobs)  (AI queries)

