# E-Commerce API

An eCommerce API built using Django and Django REST Framework (DRF) that allows users to browse products, add items to their cart, manage orders, and process payments. This API serves as the backend for an eCommerce application, providing essential features like product management, user authentication, cart functionality, and order processing.

---

## Features

- **User Authentication**
  - Register, login, and manage user profiles using JWT (JSON Web Tokens).
  - Support for guest checkouts and authenticated users.

- **Product Management**
  - Create, update, delete, and view products with details such as price, description, and category.
  - Search and filter products by name, category, and price range.

- **Cart Management**
  - Add or remove products from the cart.
  - Update item quantities.
  - Retrieve the cart for a user.

- **Order Processing**
  - Checkout from the cart to create an order.
  - Manage order status (e.g., pending, shipped, delivered).
  - Process payments (integration with Stripe or another payment gateway).

---

## Project Structure

The project is structured as follows:

ecommerce-api/ │ ├── ecommerce/          # Main project directory │   ├── settings.py     # Project settings │   ├── urls.py         # Global URL routing │   └── ... │ ├── products/           # Product app │   ├── models.py       # Product model │   ├── serializers.py  # Product serializers │   ├── views.py        # Product views (API endpoints) │   └── urls.py         # Product URL routing │ ├── carts/              # Cart app │   ├── models.py       # Cart model │   ├── serializers.py  # Cart serializers │   ├── views.py        # Cart views (API endpoints) │   └── urls.py         # Cart URL routing │ ├── orders/             # Order app │   ├── models.py       # Order model │   ├── serializers.py  # Order serializers │   ├── views.py        # Order views (API endpoints) │   └── urls.py         # Order URL routing │ └── users/              # User authentication and management app ├── models.py       # User model ├── serializers.py  # User serializers ├── views.py        # User views (API endpoints) └── urls.py         # User URL routing