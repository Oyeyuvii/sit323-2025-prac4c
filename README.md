# Enhanced Calculator Microservice

## Description
This microservice provides a suite of arithmetic operations including advanced functions such as exponentiation, square root, and modulus. It ensures robust input validation and supports floating-point numbers.

## Features
- Basic Operations: Addition, Subtraction, Multiplication, Division
- Advanced Operations:
  - Exponentiation (`base^exp`)
  - Square Root (validates non-negative input)
  - Modulus (ensures divisor is non-zero)
- Handles floating-point inputs
- Input validation for safe operation

## Prerequisites
Before running the project, make sure the following tools are installed:
- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/) (optional, for containerization)
- [MicroK8s](https://microk8s.io/) (optional, for Kubernetes deployment)

---

## Running the Microservice Locally

1. Clone the repository:
   ```sh
   git clone https://github.com/Oyeyuvii/sit323-2025-prac4c.git
   cd sit323-2025-prac4c
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Start the service:
   ```sh
   node server.js
   ```

4. Test an API endpoint:
   ```sh
   curl http://localhost:3000/add?n1=5&n2=3
   ```

---

## Running with Docker

1. Build the Docker image:
   ```sh
   docker build -t calculator-microservice .
   ```

2. Run the container:
   ```sh
   docker run -p 3000:3000 calculator-microservice
   ```

---

## Deploying to Kubernetes (MicroK8s)

1. Enable required MicroK8s services:
   ```sh
   microk8s enable dns storage
   ```

2. Apply the Kubernetes deployment:
   ```sh
   kubectl apply -f deployment.yaml
   ```

---

## API Endpoints

| Method | Endpoint                        | Description                          |
|--------|----------------------------------|--------------------------------------|
| GET    | /add?n1=5&n2=3                  | Adds two numbers                     |
| GET    | /subtract?n1=5&n2=3             | Subtracts second number from first  |
| GET    | /multiply?n1=5&n2=3             | Multiplies two numbers               |
| GET    | /divide?n1=6&n2=3               | Divides first number by second       |
| GET    | /power?base=2&exp=3             | Raises base to the exponent          |
| GET    | /sqrt?n=9                       | Computes square root                 |
| GET    | /modulus?n1=10&n2=3             | Computes modulus                     |

---

## Notes
- Ensure all input parameters are valid numbers.
- Division and modulus operations require non-zero denominators.

---

## Author
Yuvraj Singh (s223210987)
