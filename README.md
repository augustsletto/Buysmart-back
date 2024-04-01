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



# Deploy to Heroku with ElephantSQL and Connect to React App

To deploy your Django backend to Heroku with ElephantSQL and connect it to your React frontend, follow these steps:

1. **Create a Heroku App:**
   - Log in to your Heroku account or sign up for a new one.
   - Navigate to your dashboard and click on the "New" button, then select "Create new app."
   - Choose a unique app name and select your region.

2. **Set up ElephantSQL Database:**
   - Sign up for an account on ElephantSQL (https://www.elephantsql.com/).
   - Create a new instance with the plan that suits your needs.
   - Copy the PostgreSQL database URL provided by ElephantSQL.

3. **Configure Django Settings:**
   - Install `dj_database_url` using `pip install dj_database_url psycopg2`.
   - In your Django settings, import `dj_database_url`.
   - Configure the database settings to use the PostgreSQL database URL provided by ElephantSQL. For example:
     ```python
     import dj_database_url

     if 'DEV' in os.environ:
     DATABASES = {
         'default': {
             'ENGINE': 'django.db.backends.sqlite3',
             'NAME': BASE_DIR / 'db.sqlite3',
         }
     }
     else:
       DATABASES = {
           'default': dj_database_url.parse(os.environ.get("DATABASE_URL"))
     }
     ```

     Make sure you have you env.py file with the following content.
     ```
     import os
     os.environ['CLOUDINARY_URL'] = "cloudinary://..."
     os.environ['SECRET_KEY'] = "Z7o..."
     os.environ['DEV'] = '1'
     os.environ['DATABASE_URL'] = "postgres://..."

      ```

4. **Update Allowed Hosts:**
   - Add your Heroku app URL to the `ALLOWED_HOSTS` list in your Django settings.

5. **Create Procfile:**
   - Create a file named `Procfile` in your project root directory.
   - Add the following line to the `Procfile` to tell Heroku how to run your web server:
     ```
     web: gunicorn your_project_name.wsgi --log-file -
     ```

6. **Set Up Environment Variables:**
   - Add environment variables for `SECRET_KEY`, `DATABASE_URL`, and other sensitive information using Heroku CLI or the Heroku dashboard. Make sure to set the `DATABASE_URL` variable to the ElephantSQL database URL.

7. **Deploy Your App:**
   - Initialize a Git repository if you haven't already (`git init`).
   - Add and commit your changes (`git add .` and `git commit -m "Initial commit"`).
   - Add Heroku as a remote repository (`heroku git:remote -a your_heroku_app_name`).
   - Push your code to Heroku (`git push heroku master`).

8. **Run Migrations and Collect Static Files:**
   - Run migrations on the Heroku server using `heroku run python manage.py migrate`.
   - Collect static files using `heroku run python manage.py collectstatic`.

9. **Connect to React Frontend:**
   - In your React app, update API URLs to point to your Heroku backend.
   - For example, if your Django backend is deployed at `https://your-heroku-app.herokuapp.com/`, update API URLs accordingly.

10. **Test Your Deployment:**
    - Visit your Heroku app URL in a web browser to ensure that your Django backend is running correctly.
    - Test API endpoints to verify that data is being served as expected.

11. **Monitor and Troubleshoot:**
    - Monitor your Heroku app's logs using `heroku logs --tail` to debug any issues.
    - Check the Heroku dashboard for any errors or warnings.

12. **Finalize Configuration:**
    - Once everything is working as expected, you can continue to customize your Heroku app settings, such as adding a custom domain or enabling HTTPS.

Congratulations! Your Django backend is now deployed to Heroku with ElephantSQL and connected to your React frontend.
