README.md Content:

# Enhanced Calculator Microservice

## Description
This microservice provides various arithmetic operations, including exponentiation, square root, and modulus, while ensuring proper input validation.

## Features
- **Addition**, **Subtraction**, **Multiplication**, **Division**
- **Exponentiation** (`base^exp`)
- **Square Root** (Non-negative input validation)
- **Modulus** (Ensures non-zero divisor)
- Floating-point number handling

## Prerequisites
Before running the project, ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/) (if using containerization)
- [MicroK8s](https://microk8s.io/) (if deploying on Kubernetes)

---

## Running the Microservice Locally

1. Clone the repository:
   ```sh
   git clone https://github.com/Oyeyuvii/sit323-2025-prac4c.git
   cd sit323-2025-prac4c
Install dependencies:
npm install
Start the service:
node server.js
Test API using:
curl http://localhost:3000/add?n1=5&n2=3
Running with Docker

Build the Docker image:
docker build -t calculator-microservice .
Run the container:
docker run -p 3000:3000 calculator-microservice
Deploying to Kubernetes (MicroK8s)

Enable MicroK8s services:
microk8s enable dns storage
Apply the deployment:
kubectl apply -f deployment.yaml
API Endpoints

Method	Endpoint	Description
GET	/add?n1=5&n2=3	Adds two numbers
GET	/subtract?n1=5&n2=3	Subtracts second number from first
GET	/multiply?n1=5&n2=3	Multiplies two numbers
GET	/divide?n1=6&n2=3	Divides first number by second
GET	/power?base=2&exp=3	Raises base to the exponent
GET	/sqrt?n=9	Computes square root
GET	/modulus?n1=10&n2=3	Computes modulus
Notes

Ensure all parameters are valid numbers.
Division and modulus operations require non-zero denominators.
Author

Yuvraj Singh (s223210987)
