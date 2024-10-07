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

---

## API Endpoints

### **Authentication**

- **POST** `/api/auth/register/` - Register a new user.
- **POST** `/api/auth/login/` - User login and retrieve JWT token.
- **POST** `/api/auth/logout/` - Log out the user and invalidate the token.
- **GET** `/api/auth/user/` - Retrieve the currently authenticated user's details.

### **Products**

- **GET** `/api/products/` - List all products.
- **GET** `/api/products/{id}/` - Retrieve details of a specific product.
- **POST** `/api/products/` - Add a new product (Admin only).
- **PUT** `/api/products/{id}/` - Update product details (Admin only).
- **DELETE** `/api/products/{id}/` - Delete a product (Admin only).
### **Cart**

- **GET** `/api/cart/` - View items in the cart for the current user.
- **POST** `/api/cart/` - Add an item to the cart.
- **PUT** `/api/cart/{id}/` - Update item quantity in the cart.
- **DELETE** `/api/cart/{id}/` - Remove an item from the cart.

### **Orders**

- **POST** `/api/orders/` - Create a new order (checkout).
- **GET** `/api/orders/` - View the order history of the current user.
- **GET** `/api/orders/{id}/` - Retrieve details of a specific order.

---

## Installation

### Prerequisites

- Python 3.x
- Django 4.x
- Django REST Framework
- PostgreSQL

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Origina-sudo/DFR-Ecommerce-API.git
   cd EcommerceAPI

2. Set up a virtual environment:

python3 -m venv env
source env/bin/activate  # For Windows, use `env\Scripts\activate`


3. Install dependencies:
pip install -r requirements.txt

4. Set up the database:

Configure the DATABASES setting in ecommerce/settings.py to connect to your PostgreSQL or other relational database.

Run migrations to create the necessary database tables:

python manage.py migrate



5. Create a superuser:

python manage.py createsuperuser


6. Run the development server:

python manage.py runserver


7. Access the API: Open your browser and navigate to http://localhost:8000/api/.




---
 