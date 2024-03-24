<h1 style="text-align: center;">
  Products API REST
</h1>

This is a sample project for a products REST API developed using Spring Boot and Java.


## Prerequisites

Make sure you have the following tools installed on your machine:

- JDK (Java Development Kit)
- Maven
- IDE (Eclipse, IntelliJ, etc.) or text editor of your choice
- Postman or another tool for testing REST APIs

## How to Run

- Clone this repository to your local environment:
```
$ git clone https://github.com/ggomes12/products-api-rest.git
```
- Build the project:
```
$ ./mvnw clean package
```
- Run the application:
```
$ java -jar target/SpringbootApplication-0.0.1-SNAPSHOT.jar
```

The application will start and be accessible at http://localhost:8080.

## API Endpoints

Here are the endpoints available in this API:

- GET /api/products: Returns all products.
- GET /api/products/{id}: Returns a specific product by ID.
- POST /api/products: Adds a new product.
- PUT /api/products/{id}: Updates an existing product.
- DELETE /api/products/{id}: Removes an existing product by ID.

To make the HTTP requests below, the httpie tool was used: [httpie](https://httpie.io):

- Create product
```
$ http POST :8080/products name="Notebook dell g7" price="6999.0"

[
  {
    "id": "5d9fdb82-2073-4c54-a489-a861158aeb4e",
    "descricao": "Notebook dell g7",
    "price": "6999.0"
  }
]
```

- List all products
```
$ http GET :8080/products

[
  {
    "id": "5d9fdb82-2073-4c54-a489-a861158aeb4e",
    "descricao": "Notebook dell g7",
    "price": "6999.0"
  }
]
```

- List one products
```
$ http GET :8080/products/5d9fdb82-2073-4c54-a489-a861158aeb4e

[
  {
    "id": "5d9fdb82-2073-4c54-a489-a861158aeb4e",
    "descricao": "Notebook dell g7",
    "price": "6999.0"
  }
]
```

- Remove products
```
http DELETE :8080/products/5d9fdb82-2073-4c54-a489-a861158aeb4e

[ ]
```
