# public-transport-ticketing-system

Repository for the project of the Web Applications II course at Polytechnic University of Turin (academic year
2021-2022).

## Group 12 members:

| Student ID | Surname | Name |
| -- | --- | --- |
| s****** | Ballario | Marco |
| s****** | Galazzo | Francesco |
| s****** | Tangredi | Giovanni |
| s****** | Ubertini | Pietro |

## Description

In order to manage seasonal tickets and all the new features requested the we modified the `wa2-g12-traveler-service`
lab 4 project:

- We added a new `POST /tickets/acquired` endpoint in order to generate the new tickets
- We modified the `ticket_purchased` table schema
- We modified the `GET admin/traveler/{userID}/tickets` and the  `GET my/tickets` tickets endpoints

### Project structure:

- `wa2-g12-user-registration`: Contains the login service
- `wa2-g12-traveler-service`: Contains the traveler service and the instructions to setup the Postgres database
  container.
- `wa2-g12-ticket-catalogue-service`: Contains the catalogue service and the instructions to setup Apache Kafka.
- `wa2-g12-payment-service`: Contains the payment service. It requires Kafka.
- `wa2-g12-bank-service`: Contains the bank service, used to mock a real bank service. It requires Kafka.
- `wa2-g12-discovery-service`: Contains the discovery service, based on SpringCloud Netflix Eureka.
- `wa2-g12-gateway-service`: Contains the gateway service.
- `wa2-g12-report-service`: Contains the report service, used to compute reports about tickets and transits. It requires Apache Kafka.
- `wa2-g12-machine-service`: Contains the machine service, used to mock a real ticket QR Code reader.
- `wa2-g12-transit-service`: Contains the transit service, used to verify the tickets validity and store information about transits

### Services

| Service                  | Port |
|--------------------------|------|
| login-service            | 8081 |
| traveler-service         | 8082 |
| ticket-catalogue-service | 8083 |
| payment-service          | 8084 |
| bank-service             | 8085 |
| discovery-service        | 8761 |
| gateway-service          | 8080 |
| report-service           | 8086 |
| transit-service          | 8087 |

