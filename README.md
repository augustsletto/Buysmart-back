# [Live Backend Heroku Project](https://buysmart-react-a67a60d44e70.herokuapp.com/)


- [Live Backend](https://buysmart-frontend-7289ed9987fe.herokuapp.com/)
- [Backend GitHub Repository](https://github.com/augustsletto/Buysmart-back)


![MMA Quiz Screenshot1](https://res.cloudinary.com/dt4sw7qtl/image/upload/v1711928626/SneakReadMeImages/cc6fro1meohanbho2z32.jpg)



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
