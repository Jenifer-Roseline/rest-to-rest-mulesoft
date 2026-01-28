# REST to REST Integration using MuleSoft

## Project Overview
This project demonstrates a simple REST to REST integration built using MuleSoft 4.
The API receives a POST request, transforms the incoming JSON payload using DataWeave 2.0,
invokes an external REST API, and returns the processed response to the client.

This project is intended for entry-level MuleSoft integration practice.

---

## Tools & Technologies Used
- MuleSoft 4
- Anypoint Studio
- DataWeave 2.0
- HTTP Listener
- HTTP Request Connector
- Postman (API testing)

---

## Flow Explanation
1. HTTP Listener receives a POST request from the client.
2. Transform Message component maps the incoming request fields
   (name, email, role) to the required external API format.
3. HTTP Request sends the transformed payload to an external REST API.
4. The external API response is captured and processed.
5. A final success response is returned to the client.
6. Logger component logs the response for monitoring.

---

## Sample Request
POST http://localhost:8081/createUser

```json
{
  "name": "Aruna",
  "email": "aruna@test.com",
  "role": "developer"
}
