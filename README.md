# 📄 Invoice Financing API

This project provides an **OpenAPI 3.0 specification** for a RESTful API that enables **invoice financing** for small and medium-sized enterprises (SMEs). It allows SMEs to upload their invoices, request early financing, and monitor the status of those financing requests.

---

## 🚀 Features

- Upload a new invoice
- List all invoices
- Get invoice by ID
- Verify invoice by buyer
- Apply for financing based on verified invoices

---

## 📄 OpenAPI Spec

You can find the OpenAPI YAML definition here:

👉 [`openapi/invoice-financing.yaml`](openapi/invoice-financing.yaml)

This file is written in **OpenAPI 3.0.0** format and can be visualized using [Swagger Editor](https://editor.swagger.io/).

---

## 🔍 Sample Endpoints

| Method | Endpoint                        | Description                          |
|--------|----------------------------------|--------------------------------------|
| POST   | `/invoices`                     | Submit a new invoice                 |
| GET    | `/invoices`                     | List all invoices                    |
| GET    | `/invoices/{invoiceId}`         | Retrieve a specific invoice by ID    |
| POST   | `/invoice/{invoiceId}/verify`   | Buyer verifies an invoice            |
| POST   | `/financing/apply`              | Apply for financing for an invoice   |

---

## 🧪 Testing

You can test this API using:
- Swagger UI (locally or via SwaggerHub)
- Postman (import the YAML file)

---

## 🔁 API Flow

User uploads an invoice → Buyer verifies → System opens it to financing.

---

## 📦 Installation

This is just a specification file. You can:

# 1. Clone this repo
git clone https://github.com/<your-username>/invoice-financing-api.git

# 2. Open it in Swagger Editor or import into Postman

curl -X POST https://api.faturafinans.com/invoices \
-H "Content-Type: application/json" \
-d '{"invoiceId": "INV-1234", "amount": 2500, "dueDate": "2025-09-15"}'

