# Payment Gateway Integration for Stripe, PayPal, and CoinPayments

## My Contribution
I developed a comprehensive payment gateway integration system that combines three popular payment processors: Stripe, PayPal, and CoinPayments. The backend is built using Python Django, while the frontend is developed using React.js with Redux.

## Project Overview
This project implements a payment gateway integration that supports multiple payment methods, enhancing the payment options available to users. The system facilitates secure transactions and provides a seamless user experience, catering to diverse payment preferences through traditional and cryptocurrency options.

## Tech Stack
- **Client**: 
  - [React](https://reactjs.org/)
  - [Redux](https://redux.js.org/)
  - [TailwindCSS](https://tailwindcss.com/)
  - [SCSS](https://sass-lang.com/)

- **Server**:
  - [Python](https://www.python.org/)
  - [Django](https://www.djangoproject.com/)
  - [PostgreSQL](https://www.postgresql.org/)
  - [Django REST Framework](https://www.django-rest-framework.org/)
  - [Stripe API](https://stripe.com/docs/api)
  - [PayPal SDK](https://developer.paypal.com/docs/api/overview/)
  - [CoinPayments API](https://www.coinpayments.net/apidoc)

## Features and Description
- **Stripe Integration**: Integrated Stripe to enable users to make payments using credit cards, debit cards, and other supported payment methods. The system ensures the highest level of data security through secure tokenization of sensitive payment information.
  
- **PayPal Integration**: Implemented PayPal payments, allowing users to complete transactions using their PayPal accounts. The system securely manages the entire PayPal payment process, including user authentication and transaction handling.

- **CoinPayments Integration**: Supported cryptocurrency payments through CoinPayments, enabling users to choose from various cryptocurrencies for their transactions, ensuring secure and efficient payment processing.

- **User-Friendly Interface**: Developed a responsive and intuitive frontend using React.js and Redux, providing real-time updates and feedback on payment statuses to enhance the user experience.

- **Transaction Management**: Created a robust transaction management system that efficiently handles order processing, payment verification, and error handling, ensuring reliability and integrity throughout the payment process.

- **Customization and Scalability**: Designed the architecture to be easily scalable and customizable, allowing for the future addition of new payment processors and enhancing the system’s flexibility for expansion.

## API Reference

### Products Controller Requests
- **Create Product**
  - **POST** `/product`
  - **Parameters**:
    - **name**: `string` (Required. Product name)
    - **price**: `float` (Required. Product price)
    - **brand**: `string` (Required. Product brand)
    - **category**: `string` (Required. Category of product)

- **Get All Products**
  - **GET** `/products`

### Invoice Controller Request
- **Get All Invoices**
  - **GET** `/invoices`

### CoinPayments Controller Requests
- **Create Payment**
  - **POST** `/crypto/create/payment`
  - **Parameters**:
    - **productId**: `string` (Required. Product ID)
    - **email**: `string` (Required. Buyer email)
    - **cryptocurrency**: `string` (Required. Code of cryptocurrency)

### PayPal and Stripe Controller Requests
- **Create Payment**
  - **POST** `/{method}/create/payment`
  - **Parameters**:
    - **method**: `string` (Required. `paypal` or `stripe`)
    - **productId**: `string` (Required. Product ID)
