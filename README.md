# Customer Management API

This API is built using Java, Spring Boot, JPA and Hibernate, and provides a simple RESTful web service for managing customers.

## Features

- Retrieve a list of customers
- Add a new customer
- Update customer information
- Delete a customer

## Components

### Customer Entity

The `Customer` class is a JPA entity representing a customer with the following fields:

- `id`: Integer, primary key
- `name`: String, customer's name
- `email`: String, customer's email
- `age`: Integer, customer's age

### Customer Repository

The `CustomerRepository` interface extends the JpaRepository and provides basic CRUD operations for the `Customer` entity.

### Main Class

The `Main` class is the entry point of the application and contains the following methods:

- `main(String[] args)`: starts the Spring Boot application
- `getCustomers()`: retrieves a list of customers
- `addCustomer(NewCustomerRequest request)`: adds a new customer
- `deleteCustomer(Integer id)`: deletes a customer by ID
- `updateCustomer(Integer id, NewCustomerRequest request)`: updates customer information

## Endpoints

- `GET api/v1/customers`: returns a list of all customers
- `POST api/v1/customers`: creates a new customer
- `DELETE api/v1/customers/{customerId}`: deletes a customer by ID
- `PUT api/v1/customers/{customerId}`: updates a customer by ID
