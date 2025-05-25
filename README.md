# European KYC API (OpenAPI Specification)

A secure, GDPR- and AMLD-compliant KYC API designed for onboarding and verifying banking customers in Europe. Built using OpenAPI 3.0.3 for easy integration and standardized documentation.

## 🌍 Overview
This API enables banks and financial services providers to:
- Onboard new customers
- Upload identity verification documents
- Check KYC status
- Perform PEP/sanctions screening
- Handle GDPR data requests (access & deletion)

## 📄 Specification
The full API spec is written in OpenAPI 3.0.3 and available in this repo as [`openapi.yaml`](./openapi.yaml).

## 📦 Features
- OAuth2-based security
- JSON & multipart/form-data support
- Role-based access scopes
- GDPR-compliant data access and deletion
- Modular, schema-based validation

## 📂 File Structure
```
.
├── openapi.yaml              # Full Swagger/OpenAPI definition
├── README.md                 # Project documentation
├── examples/
│   ├── customer_onboard.json
│   ├── document_upload.json
│   ├── kyc_status_response.json
│   └── screening_result.json
├── postman_collection.json   # For use with Postman
```

## 🚀 Usage
You can view and interact with the API using [Swagger Editor](https://editor.swagger.io/) or SwaggerHub:
```sh
# Clone the repo
$ git clone https://github.com/yourusername/european-kyc-api.git
$ cd european-kyc-api

# Open openapi.yaml in Swagger Editor (or any OpenAPI tool)
```

## 🔒 Security
This API uses OAuth2 client credentials flow:
- `kyc.read`: View KYC data
- `kyc.write`: Submit or update customer data

## 📊 Key Endpoints
| Endpoint | Method | Description |
|----------|--------|-------------|
| `/customers` | POST | Onboard a new customer |
| `/customers/{id}/documents` | POST | Upload ID or selfie |
| `/customers/{id}/status` | GET | Check KYC status |
| `/customers/{id}/screening` | GET | View screening result |
| `/customers/{id}/data` | GET | GDPR access request |
| `/customers/{id}` | DELETE | GDPR right to be forgotten |

## ⚖️ Compliance
- GDPR: User consent, data subject rights, data minimization
- AMLD5/6: Customer due diligence, screening

## 🧪 Postman Collection
Import the `postman_collection.json` file into Postman to test the API with preconfigured requests.

### 🔸 Sample Postman Folder Structure
- Create Customer
- Upload Document
- Check Status
- Screening Result
- GDPR Data Access
- Delete Customer

## 🧾 Examples
All JSON payload examples are available in the `examples/` directory.
- `customer_onboard.json`: Sample request body to create a customer
- `document_upload.json`: Example for document upload metadata
- `kyc_status_response.json`: Mock KYC status response
- `screening_result.json`: Example sanctions screening result

## 🤝 Contributions
Feel free to fork or suggest improvements via Pull Requests.

---
© 2025 Your Name. Licensed under MIT.

---

_This project is part of a portfolio demonstrating regulatory-compliant API design for the financial services sector in Europe._
