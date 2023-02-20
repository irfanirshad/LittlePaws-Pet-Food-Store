
# LittlePaws Pet Food Store
![landing_page_lp](https://user-images.githubusercontent.com/84003624/220007038-85ff9d33-a701-4df2-9e0d-1762c639ba5f.png)


Experience top-notch pet food shopping with <b>LittlePaws</b>, an ECommerce application built entirely using <b>Python Django</b> and <b>Jinja</b> Templates. With custom user model and cart management, explore unlimited product galleries of categories and items, and check out with ease using secure payment options. LittlePaws ensures hassle-free after-order tasks, such as inventory tracking, email notifications for received orders, cart clearing, order completion page display, and invoicing.

![store_front_lp](https://user-images.githubusercontent.com/84003624/220007079-deb85ced-e626-4782-92d9-65fc6a40bb0c.png)

LittlePaws includes an interactive Review and Rating system that lets you express your thoughts on pet food products and leave star ratings and comments on products they have purchased. Customers can easily manage their accounts by editing their profile, uploading profile pictures, changing passwords, and keeping track of their orders. To ensure optimal performance, scalability and security, we deployed the application on AWS Elastic Beanstalk with RDS + Route 53. With our user-friendly interface and top-notch technology stack, customers can have a seamless shopping experience for their beloved pets' food needs.

## Some of the Other Features

### User Dashboard

![user_profile](https://user-images.githubusercontent.com/84003624/220010683-b3edb7d1-08bb-45ff-a715-2182c7c7ee2a.png)

### Item variations, Reviews and Comments

![item2](https://user-images.githubusercontent.com/84003624/220009645-088e3e10-3b3f-4a60-83d6-defbac9fe988.png)

## Admin Dashboard

### Screenshots on how the admin interface looks like

1) Using the Django built-in admin dashboard, we add extra functionality on top of it such as Monitoring Login Attempts on the Admin(Fake) Login Page using  Paul McMillan’s <b>django-admin-honeypot</b>.
<br/>

![honeypot_attempts_ss](https://user-images.githubusercontent.com/84003624/220009003-28ed7ac0-97ee-4a88-9ff2-383b30f52a3b.png)

2) Variations 
 
<img width="960" alt="variations" src="https://user-images.githubusercontent.com/84003624/220009967-efb799c7-a84c-421f-820d-5d8938cb936d.png">

3) Attempting to Deleting a category revealing its entire object relationship

<img width="960" alt="category_deletion_variations" src="https://user-images.githubusercontent.com/84003624/220010083-6e23661a-d607-44db-915b-5d7c72765b20.png">

4) Payments 

<img width="960" alt="payments" src="https://user-images.githubusercontent.com/84003624/220010094-097177f0-89d1-4e80-9eea-8e8b9bcaf9b3.png">


## Flow diagram of a user attempting to check out system.

### 1) User at the checkout page before clicking on "Checkout" Button
![flow0](https://user-images.githubusercontent.com/84003624/220010733-f49b71cd-0209-47f4-ae13-8f312e01d8fb.png)

### 2) User is redirecting to a page for filling up details Post-clicking on "Checkout" Button
![flow1](https://user-images.githubusercontent.com/84003624/220010748-35be2d11-65d9-4d8f-bc38-bf1d11d74846.png)

### 3) User is requested to review order before making payment. 
![flow1 5](https://user-images.githubusercontent.com/84003624/220007280-00c93020-740f-44bd-94ae-4f574b9183bf.png)

### 4) User can either click on the paypal button or credit/debit card payment for finalizing payment(use a sandbox account for testing) 
![flow2](https://user-images.githubusercontent.com/84003624/220007289-2d32336f-e8d9-4d88-a1ac-2957e4273210.png)

### 5) Post finalizing payment, AWS SES sends an invoice email notifying the order details and date of expected delivery.



# Setup Instructions

1. Clone the repository `git clone https://github.com/irfanirshad/django-ecom-aws`
2. Navigrate to the working directory `cd django-ecom-aws`
3. Open the project from the code editor `code .`
4. Create virtual environment `python -m venv venv`
5. Activate the virtual environment `source venv/bin/activate`
6. Install required packages to run the project `pip install -r requirements.txt`
7. Rename _.env-sample_ to _.env_
8. Fill up the environment variables:
    _Generate your own Secret key using this tool [https://djecrety.ir/](https://djecrety.ir/), copy and paste the secret key in the SECRET_KEY field._

    _Your configuration should look something like this:_
    ```sh
    SECRET_KEY=47d)n05#ei0rg4#)*@fuhc%$5+0n(t%jgxg$)!1pkegsi*l4c%
    DEBUG=True
    EMAIL_HOST=smtp.gmail.com
    EMAIL_PORT=587
    EMAIL_HOST_USER=youremailaddress@gmail.com
    EMAIL_HOST_PASSWORD=yourStrongPassword
    EMAIL_USE_TLS=True
    ```
    _Note: If you are using gmail account, make sure you [turn ON the less secure apps](https://myaccount.google.com/lesssecureapps)_
9. Create database tables
    ```sh
    python manage.py migrate
    ```
10. Create a super user
    ```sh
    python manage.py createsuperuser
    ```
    _GitBash users may have to run this to create a super user - `winpty python manage.py createsuperuser`_
11. Run server
    ```sh
    python manage.py runserver
    ```
12. Login to admin panel - (`https://127.0.0.1:8000/securelogin/`)
13. Add categories, products, add variations, register user, login, place orders and EXPLORE SO MANY FEATURES


[Check Live Demo]()


## Support
💙 If you like this project, give it a ⭐ and share it with friends!

## Contact Me
<p align="left">
  <a href="https://www.linkedin.com/in/irfanirshad123"><img alt="LinkedIn" title="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="mailto:irfanirshad003@gmail.com"><img alt="Gmail" title="Gmail" src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
</p>

##
Made with ❤️ and Python
