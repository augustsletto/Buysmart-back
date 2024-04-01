# [Live Backend Heroku Project](https://buysmart-react-a67a60d44e70.herokuapp.com/)


- [Live Backend](https://buysmart-frontend-7289ed9987fe.herokuapp.com/)
- [Backend GitHub Repository](https://github.com/augustsletto/Buysmart-back)


### Table of Contents


- [Testing API URLs with Associated Views](#testing-api-urls-with-associated-views)
- [Settings](#settings)
  - [Installed Apps](#installed-apps)
  - [Middleware](#middleware)
  - [Database](#database)
  - [Authentication](#authentication)
  - [Other Settings](#other-settings)
- [Dependencies](#dependencies)
- [Usage](#usage)



![Structure](https://res.cloudinary.com/dt4sw7qtl/image/upload/v1711928626/SneakReadMeImages/cc6fro1meohanbho2z32.jpg)





## Testing API URLs with Associated Views

| #   | URL                             | View                                 | Expected Outcome                              |
| --- | ------------------------------- | ------------------------------------ | --------------------------------------------- |
| 1   | `/`                             | `root_route`                         | :white_check_mark:                            |
| 2   | `/admin/`                       | `admin.site.urls`                    | :white_check_mark:                            |
| 3   | `/api/products/`                | `base.urls.product_urls`             | :white_check_mark:                            |
| 4   | `/api/users/`                   | `base.urls.user_urls`                | :white_check_mark:                            |
| 5   | `/api/orders/`                  | `base.urls.order_urls`               | :white_check_mark:                            |
| 6   | `/api/orders/`                  | `views.getOrders`                    | :white_check_mark:                            |
| 7   | `/api/orders/add/`              | `views.addOrderItems`                | :white_check_mark:                            |
| 8   | `/api/orders/myorders/`         | `views.getMyOrders`                  | :white_check_mark:                            |
| 9   | `/api/orders/<str:pk>/deliver/` | `views.updateOrderToDelivered`       | :white_check_mark:                            |
| 10  | `/api/orders/<str:pk>/`         | `views.getOrderById`                 | :white_check_mark:                            |
| 11  | `/api/orders/<str:pk>/pay/`     | `views.updateOrderToPaid`            | :white_check_mark:                            |
| 12  | `/api/products/`                | `views.getProducts`                  | :white_check_mark:                            |
| 13  | `/api/products/create/`         | `views.createProduct`                | :white_check_mark:                            |
| 14  | `/api/products/upload/`         | `views.uploadImage`                  | :white_check_mark:                            |
| 15  | `/api/products/<str:pk>/reviews/` | `views.createProductReview`        | :white_check_mark:                            |
| 16  | `/api/products/top/`            | `views.getTopProducts`               | :white_check_mark:                            |
| 17  | `/api/products/<str:pk>/`       | `views.getProduct`                   | :white_check_mark:                            |
| 18  | `/api/products/update/<str:pk>/` | `views.updateProduct`               | :white_check_mark:                            |
| 19  | `/api/products/delete/<str:pk>/` | `views.deleteProduct`               | :white_check_mark:                            |
| 20  | `/api/login/`                   | `views.MyTokenObtainPairView` | :white_check_mark:                        |
| 21  | `/api/register/`                | `views.registerUser`                 | :white_check_mark:                            |
| 22  | `/api/profile/`                 | `views.getUserProfile`               | :white_check_mark:                            |
| 23  | `/api/profile/update/`          | `views.updateUserProfile`            | :white_check_mark:                            |
| 24  | `/api/users/`                   | `views.getUsers`                     | :white_check_mark:                            |
| 25  | `/api/users/<str:pk>/`          | `views.getUserById`                  | :white_check_mark:                            |
| 26  | `/api/users/update/<str:pk>/`   | `views.updateUser`                   | :white_check_mark:                            |
| 27  | `/api/users/delete/<str:pk>/`   | `views.deleteUser`                   | :white_check_mark:                            |




# Settings

## Installed Apps
- `django.contrib.admin`: Django's built-in admin interface.
- `django.contrib.auth`: Authentication system.
- `django.contrib.contenttypes`: Content types framework.
- `django.contrib.sessions`: Session management.
- `django.contrib.messages`: Messaging framework.
- `cloudinary_storage`: Cloudinary storage for media files.
- `django.contrib.staticfiles`: Serving static files.
- `cloudinary`: Cloudinary integration.
- `rest_framework`: Django REST framework for building APIs.
- `corsheaders`: Handling Cross-Origin Resource Sharing (CORS).

## Middleware
- `corsheaders.middleware.CorsMiddleware`: CORS middleware.
- `django.middleware.security.SecurityMiddleware`: Security middleware.
- `django.contrib.sessions.middleware.SessionMiddleware`: Session middleware.
- `django.middleware.common.CommonMiddleware`: Common middleware.
- `django.middleware.csrf.CsrfViewMiddleware`: CSRF middleware.
- `django.contrib.auth.middleware.AuthenticationMiddleware`: Authentication middleware.
- `django.contrib.messages.middleware.MessageMiddleware`: Message middleware.
- `django.middleware.clickjacking.XFrameOptionsMiddleware`: Clickjacking protection middleware.

## Database
- SQLite for development.
- PostgreSQL for production (configured via DATABASE_URL environment variable).

## Authentication
- JWT authentication using `rest_framework_simplejwt`.

## Other Settings
- Cloudinary storage configuration.
- CORS settings to allow specific origins or all origins.
- Pagination settings for Django REST framework.
- Default renderer classes for production and development.
- JWT authentication settings including token lifetimes and cookie names.

# Dependencies
- asgiref==3.8.1
- certifi==2024.2.2
- charset-normalizer==3.3.2
- cloudinary==1.39.1
- dj-database-url==0.5.0
- Django==5.0.3
- django-cloudinary-storage==0.3.0
- django-cors-headers==4.3.1
- djangorestframework==3.15.1
- djangorestframework-simplejwt==5.3.1
- gunicorn==21.2.0
- idna==3.6
- packaging==24.0
- pillow==10.2.0
- psycopg2==2.9.9
- PyJWT==2.8.0
- requests==2.31.0
- six==1.16.0
- sqlparse==0.4.4
- urllib3==2.2.1

# Usage
1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Install dependencies using `pip install -r requirements.txt`.
4. Set up your environment variables, including `SECRET_KEY` and `DATABASE_URL`.
5. Run migrations using `python manage.py migrate`.
6. Start the development server using `python manage.py runserver`.
7. For production deployment, consider configuring a production-ready web server like Nginx or Apache along with a WSGI server like Gunicorn. Additionally, set `DEBUG=False` in your production settings and ensure proper security configurations.
