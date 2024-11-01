## Payment Gateway Integration for Stripe, PayPal, and CoinPayments

### My Contribution
I developed a comprehensive payment gateway integration system that combines three popular payment processors: Stripe, PayPal, and CoinPayments. The backend is built using Python Django, while the frontend is developed using React.js with Redux.

### Project Overview
This project implements a payment gateway integration that supports multiple payment methods, enhancing the payment options available to users. The system facilitates secure transactions and provides a seamless user experience, catering to diverse payment preferences through traditional and cryptocurrency options.

### Tech Stack
#### Client:
- ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
- ![Redux](https://img.shields.io/badge/Redux-764ABC?style=flat-square&logo=redux&logoColor=white)
- ![TailwindCSS](https://img.shields.io/badge/TailwindCSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
- ![SCSS](https://img.shields.io/badge/SCSS-CC6699?style=flat-square&logo=sass&logoColor=white)

#### Server:
- ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
- ![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
- ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
- ![Django REST Framework](https://img.shields.io/badge/Django%20REST%20Framework-3F729B?style=flat-square&logo=django&logoColor=white)
- ![Stripe](https://img.shields.io/badge/Stripe-008C45?style=flat-square&logo=stripe&logoColor=white)
- ![PayPal](https://img.shields.io/badge/PayPal-003087?style=flat-square&logo=paypal&logoColor=white)
- ![CoinPayments](https://img.shields.io/badge/CoinPayments-28A745?style=flat-square&logo=coinpayments&logoColor=white)

### Features and Description
- **Stripe Integration**: Enabled payments using credit/debit cards with secure tokenization of sensitive information.
- **PayPal Integration**: Managed the PayPal payment process securely, including user authentication and transaction handling.
- **CoinPayments Integration**: Supported various cryptocurrencies for transactions, ensuring secure payment processing.
- **User-Friendly Interface**: Developed a responsive frontend providing real-time updates and feedback on payment statuses.
- **Transaction Management**: Created a robust system for order processing, payment verification, and error handling.
- **Customization and Scalability**: Designed for easy scalability and customization, allowing future payment processor additions.

### API Reference
#### Products Controller Requests
- **Create Product**
  - `POST /product`
  - Parameters:
    - `name`: string (Required. Product name)
    - `price`: float (Required. Product price)
    - `brand`: string (Required. Product brand)
    - `category`: string (Required. Category of product)

- **Get All Products**
  - `GET /products`

#### Invoice Controller Request
- **Get All Invoices**
  - `GET /invoices`

#### CoinPayments Controller Requests
- **Create Payment**
  - `POST /crypto/create/payment`
  - Parameters:
    - `productId`: string (Required. Product ID)
    - `email`: string (Required. Buyer email)
    - `cryptocurrency`: string (Required. Code of cryptocurrency)

#### PayPal and Stripe Controller Requests
- **Create Payment**
  - `POST /{method}/create/payment`
  - Parameters:
    - `method`: string (Required. paypal or stripe)
    - `productId`: string (Required. Product ID)

