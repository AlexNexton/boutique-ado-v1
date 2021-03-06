# ![ART.IAL](/media/logo.png) #

[SOLEKI](https://art-ial-app.herokuapp.com/) is an e-commerce website with artwork gallery where you can not only view but also purchase available artwork.

Soleki, is a...

![Site display on different screens](/wireframes/testing-images/responsive-design.jpg)

---

## Contents ##

- [UX](#ux)
  - [Project Goals](#project-goals)
  - [Site Owner Goals](#site-owner-goals)
  - [Site Visitor/User Goals](#site-visitor-user-goals)
  - [User Stories](#user-stories)
  - [User Requirements and Expectations](#user-requirements-and-expectations)
    - [**Requirements**](#--requirements--)
    - [**Expectations**](#--expectations--)
  - [Design Choices](#design-choices)
    - [**Fonts**](#--fonts--)
    - [**Colours**](#--colours--)
- [Wireframes](#wireframes)
  - [**Site Map**](#--site-map--)
  - [**Site Layout**](#--site-layout--)
- [Information Architecture](#information-architecture)
  - [Database Choice](#database-choice)
  - [Database Modelling](#database-modelling)
    - [**Profile App**](#--profile-app--)
      - [Profile](#profile)
    - [**Product App**](#--product-app--)
      - [Product Category](#product-category)
      - [Collection Name](#collection-name)
      - [Tag](#tag)
      - [Artwork Images](#artwork-images)
      - [Images Folder](#images-folder)
      - [Product](#product)
    - [**Checkout App**](#--checkout-app--)
      - [Order](#order)
      - [Order Line](#order-line)
    - [**Home App**](#--home-app--)
      - [About Section](#about-section)
      - [Social Media Icons](#social-media-icons)
- [Technologies](#technologies)
  - [Languages](#languages)
  - [Libraries & Frameworks](#libraries---frameworks)
  - [Tools](#tools)
- [Features](#features)
  - [Implemented Features](#implemented-features)
    - [**User Account**](#--user-account--)
    - [**Super User**](#--super-user--)
    - [**Product page**](#--product-page--)
    - [**Skateteam page**](#--skateteam-page--)
    - [**Shopping bag**](#--shopping-bag--)
    - [**Payments**](#--payments--)
  - [Future Features](#future-features)
- [Changes applied since planning](#changes-applied-since-planning)
- [Testing](#testing)
- [Deployment](#deployment)
  - [Local Deployment](#local-deployment)
  - [Deployment to Heroku](#deployment-to-heroku)
  - [Hosting Media files in AWS](#hosting-media-files-in-aws)
- [Credits](#credits)
  - [Images](#images)
  - [Image editing](#image-editing)
  - [Code ideas](#code-ideas)
- [Acknowledgements](#acknowledgements)

---

## UX ##

### Project Goals ###

This project is my final project for the Code Institute's Full stack development programme. The main goal of this project is to create an e-commerce site using Django framework, which is hosted with AWS as well as implementing a fully functional payment system with Stripe.

### Site Owner Goals ###

- Provide the users with a professional e-commerce online shop to allow secure purchases
- Make profit selling artwork
- Promote the artwork and the brand of the artist

### Site Visitor/User Goals ###

- View Snowboards and Skateboards artist
- Ability to buy the products online

### User Stories ###

**Applies to all site users:**

- As a user, I am able to access the site on my mobile, tablet, and desktop which is adapted to provide the best experience.

- As a user, I am able to easily navigate through the website without too much thought and find what I am looking for quickly.

- As a user, I am able to contact the site owner using via a phone number or email address provided on the main page.

- As a user, I am able to read a description about the products I am interested in (including as images, title etc)

- As a user, I am able to a product to my shopping bag.

- As a user, I am able to change the content of my shopping bag before continuing to completion (add more or remove the products).

- As a user, I am able to see a full breakdown of the total cost, including the shipping charge before proceeding to payment.

- As a user, I am able to purchase the products using my card in a secure environment.

- As a user, I am able to receive an email confirmation once I complete the payment.

**Applies to new site users:**

- As a user, I am able to create an account.

**Applies to all returning users:**

- As a user, I am able to login to my existing account and make a quicker purchase.

- As a user, I am able to view, save and update my personal information.

- As a user, I am able to view past orders.

- As a user, I am able to make purchases quicker by having stored information such as address.

**Applies to a superuser (site owner):**

- As a user, I am able to securely add, edit and delete the information for the specific products on the website.

- As a user, I am able to receive inquiries from the site users after they fill in the contact form straight to my email inbox.

- As a user, I am able to get an email with the customer orders when the purchases are made.

- As a user, I am able to manipulate social??media??icons??in??the??footer??of??the??site (turn social media icons *on/off* and edit URLs).

- As a user, I am able to access the Django server with /admin and edit the website from there.

[Back to content](#contents)

### User Requirements and Expectations ###

#### **Requirements** ####

- Visually pleasant app design
- Easy site navigation
- Information of the content layed out in a simple and clear way on both mobile and larger screens
- Self-explanatory icons where text is absent

#### **Expectations** ####

- User information is protected by the site
- User can manipulate elements of the particular page
- Get exclusivity once a member on new arrivals and see the Skateteam

[Back to content](#contents)

### Design Choices ###

#### **Fonts** ####

- *All the site*

  ```font-family: 'Gugi', cursive;```

#### **Colours** ####

![Colour palette](/wireframes/colour-palette/colour-palette.jpg)

[Back to content](#contents)

## Wireframes ##

### **Site Map** ###

Firstly, I have created a site [map](/wireframes/site-map/sitemap.png) to enable me to clearly plan the site design before I started working on the wireframes. It has also helped me to visualize what apps I will need to create to make this project fit for purpose.

### **Site Layout** ###

I designed my site moc-ups using [balsamiq wireframes](https://balsamiq.com/). I was focusing on defining the basic layout structure of the app and identifying how displays would change on different screen sizes such as [mobile](/wireframes/site-wireframes/gallery-buy.mobile.png), [tablet](/wireframes/site-wireframes/gallery-buy.tablet.png), and [desktop](/wireframes/site-wireframes/gallery-buy.desktop.png).

You can view all wireframes created for this project in [site wireframes](/wireframes/site-wireframes) folder.

  **Please note, as I was developing the project, I have identified some weaknesses in the UX and therefore made the required changes. The deployed site looks somewhat different in comparison to the wireframes. These changes will allow the user to have a better experience and allow easier navigation. Some wireframes that are available to view may not be present in current features. This is due to time constraints and I may consider them for the future, therefore, leaving them. I have also added additional superuser features in the front-end that at the time of the site design didn't realize will be required. Wireframes of these features are not included due to time constraints. The design theme of the features is a close match to the overall site to ensure continuation and flow.*

[Back to content](#contents)

---

## Information Architecture ##

### Database Choice ###

### Database Modelling ###

#### **Profile App** ####

##### Profile #####

| **Title** | **Database Key** | **Field Type** | **Validation** |
--- | --- | --- | ---
 Username | user | OneToOneField 'User' |  on_delete=models.CASCADE
 Full Name | default_full_name | CharField | max_length=200, null=True, blank=True
 Phone number | default_phone_number | CharField | max_length=20, null=True, blank=True
 Address Line1 | default_address_line1 | CharField | max_length=80, null=True, blank=True
 Address Line2 | default_address_line2 | CharField | max_length=80, null=True, blank=True
 Town/City | default_town_or_city | CharField | max_length=40, null=True, blank=True
 County | default_county | CountryField | blank_label='County', null=True, blank=True
 Postcode | default_postcode | CharField | max_length=20, null=True, blank=True
 Country | default_country | CountryField | blank_label='Country', null=True, blank=True

#### **Product App** ####

##### Product Category #####

| **Title** | **Database Key** | **Field Type** | **Validation** |
--- | --- | --- | ---
Programmatic Name | name | CharField | max_length=50, null=True, blank=False, unique=True
Friendly Name | friendly_name | CharField | max_length=50, null=True, blank=False


##### Product #####

| **Title** | **Database Key** | **Field Type** | **Validation** |
--- | --- | --- | ---
 Product Category | category | ForeignKey 'Category' | null=True, blank=False, on_delete=models.SET_NULL
 Name | name | CharField | max_length=254, null=True, blank=False, unique=True
 Description | description | TextField | max_length=800, null=True, blank=False
 Has sizes | has_sizes | BooleanField | default=False, null=True, blank=True
 Price | price | DecimalField |max_digits=6, decimal_places=2, validators=[MinValueValidator(0.01)]
 Images_url | images_url| URLField'| max_length=1024, null=True, blank=True
 Rating | rating | DecimalField | max_digits=6, decimal_places=2, null=True, blank=True
 Image | image |ImageField| null=True, blank=True
 Sku | sku | CharField | max_length=254, null=True, blank=False
 



 ##### Skateteam #####

| **Title** | **Database Key** | **Field Type** | **Validation** |
--- | --- | --- | ---
 Skateteam Teamcat | teamcat| ForeignKey 'Teamcat' | null=True, blank=False, on_delete=models.SET_NULL
 Name | name | CharField | max_length=254, null=True, blank=False, unique=True
 Description | description | TextField | max_length=800, null=True, blank=False
 Images_url | images_url| URLField'| max_length=1024, null=True, blank=True
 Image | image |ImageField| null=True, blank=True
 Sku | sku | CharField | max_length=254, null=True, blank=False
 Rating | rating | DecimalField | max_digits=6, decimal_places=2, null=True, blank=True


#### **Checkout App** ####

##### Order #####

| **Title** | **Database Key** | **Field Type** | **Validation** |
--- | --- | --- | ---
Order Number | order_number | CharField | max_length=32, null=False, editable=False
Profile | use_profile | ForeignKey 'Profile' | on_delete=models.SET_NULL, null=True, blank=True, related_name='orders'
Full Name | full_name | CharField | max_length=50, null=False, blank=False
Email | email | EmailField | max_length=254, null=False, blank=False
Phone number | phone_number | CharField | max_length=20, null=False, blank=False
Address Line1 | address_line1 | CharField | max_length=80, null=False, blank=False
Address Line2 | address_line2 | CharField | max_length=80, null=False, blank=True
Town/City | town_or_city | CharField | max_length=40, null=False, blank=False
County | county | CharField | max_length=80, null=True, blank=True
Country | country | CountryField | blank_label='Country*', null=False, blank=False
Postcode | postcode | CharField | max_length=20, null=True, blank=True
Purchase Date | purchase_date | DateTimeField | auto_now_add=True
Delivery Cost | delivery_cost | DecimalField | max_digits=6, decimal_places=2, null=False, default=0
Order Total | order_total | DecimalField | max_digits=10, decimal_places=2, null=False, default=0
Grand Total | grand_total | DecimalField | max_digits=10, decimal_places=2, null=False, default=0
Original Bag| original_bag | TextField | null=False, blank=False, default=''
Stripe Pid | stripe_pid | CharField | max_length=254, null=False, blank=False, default=''

##### Order Line #####

| **Title** | **Database Key** | **Field Type** | **Validation** |
--- | --- | --- | ---
Order | order | ForeignKey 'Order' | null=False, blank=False, on_delete=models.CASCADE, related_name='lineitems'
Product | product | ForeignKey 'Product' | null=False, blank=False, on_delete=models.PROTECT
Quantity | quantity | IntegerField | null=False, blank=False, default=1
Line Item Total | line_item_total | DecimalField | max_digits=6, decimal_places=2, null=False, blank=False, editable=False
Datetime | datetime | CharField | null=True, blank=True, max_length=20

[Back to content](#contents)

---  

## Technologies ##

### Languages ###

- [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Python](https://www.python.org/)

### Libraries & Frameworks ###

- [Django](https://www.djangoproject.com/)
- [Django Crispy Forms](https://django-crispy-forms.readthedocs.io/en/latest/)
- [Jinja](https://jinja.palletsprojects.com/en/2.10.x/)
- [jQuery](https://jquery.com/)
- [Popper JS](https://popper.js.org/)
- [Bootstrap](https://getbootstrap.com/)
- [Stripe](https://stripe.com/ie)
- [Gunicorn](https://pypi.org/project/gunicorn/)
- [Psycopg2](https://pypi.org/project/psycopg2/)
- [Google fonts](https://fonts.google.com/)
- [Font-Awesome](https://fontawesome.com/icons?d=gallery)

### Tools ###

- [PIP](https://pypi.org/project/pip/)
- [Git](https://git-scm.com/)
- [GitHub](https://github.com/)
- [Heroku](https://www.heroku.com/)
- [Boto 3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
- [AWS bucket](https://aws.amazon.com/s3/)
- [Color editor](https://coolors.co/)
- [Favicons](https://fontawesome.com/icons?d=gallery)
- [Balsamiq](https://balsamiq.com/)

[Back to content](#contents)

---

## Features ##

Soleki's website is designed using five applications: `Home`, `Products`, `Profiles`, `Skateteam`, `Bag`, and `Checkout`.

### Implemented Features ###

- The site has **responsive design** when viewed on a mobile, tablet, and desktop.
- **Easy navigation** to external sites, such as social media accounts.
- The user is given feedback when they interact with the website (i.e. when items are added/deleted from the bag, or payment is processed.
#### **User Account** ####

- The users can **create** an account where they can store personal information such as their address and **edit** their details.
- The user can view the skate team and exclusive new arrivals while logged in. They also have a Search-bar to navigate more effeciently.

#### **Super User** ####

- Existing content about the **Products** can be edited, updated, or completely deleted by the **Super User** in the front end.
- The **Super User** can **add new** products  `Shop` sections of the site.
- The **Super User** can see the history of all orders.
- The **Super User** can use the backend to add new products, verify emails or remove a user.

#### **Skateteam page** ####

- This page is only available to registed users, here they can view the skaters and a mini biography about each of them.

#### **Products page** ####

- All of the products listed on this page are available for purchase.

#### **Shopping bag** ####

- Items added to the shopping bag appear in the shopping bag in the navigation part of the header.
- Items can be removed from the shopping bag.
- The user can choose to proceed to payment.

#### **Payments** ####

- Existing users who have previously made a purchase and are logged in, have their delivery address pre-populated when they proceed to payment.
- Checkout page shows the summary of the order.
- Payment can be made by card using Stripe.

### Future Features ###

- The **Super User** can add the skateteam's videos and news about them.
- The **Registered users** can upload their own content and share it with other members.

---

## Changes applied since planning ##

---

## Testing ##

Testing was done manually throughout the development process. The full rundown of the testing can be found in a separate [TESTING.md](TESTING.md) file.

[Back to content](#contents)

---

## Deployment ##

**Soleki** project was deployed using  **Git** and **GitHub** for version control. It is hosted on **Heroku** and all static files, including images, are hosted in **AWS S3 Bucket**. **Stripe** is used for payments and Google's **gMail** for an email account.

Before deploying the application, install the following:

- Python 3
- PIP
- Git
- Heroku CLI

### Local Deployment ###

To deploy Art-ial locally, take the following steps:

1. From the applications [repository](https://github.com/AlexNexton/soleki), click the *code* button and download the zip file.

    Alternatively, you can clone the repository using the following line in your terminal:

```terminal
git clone https://github.com/AlexNexton/soleki.git
```

2. Access the folder in your terminal window and install the application's required modules with the following command:

```terminal
pip3 install -r requirements.txt
```

3. Create `env.py` file to hold your environmental variables in the root level of the application:

```python

import os

os.environ.setdefault('STRIPE_SECRET_KEY', 'YOUR_STRIPE_SECRET_KEY')
os.environ.setdefault('STRIPE_PUBLIC_KEY', 'YOUR_STRIPE_PUBLIC_KEY')
os.environ.setdefault('STRIPE_WH_SECRET', 'YOUR_STRIPE_WH_SECRET')
os.environ.setdefault('DATABASE_URL', 'YOUR_DATABASE_URL')
os.environ.setdefault('SECRET_KEY', 'YOUR_DJANGO_SECRET_KEY')
os.environ.setdefault('DEVELOPMENT', '1')
os.environ.setdefault('AWS_S3_REGION_NAME', 'YOUR_REGION')
os.environ.setdefault('AWS_STORAGE_BUCKET_NAME', 'YOUR_BUCKET_NAME')
os.environ.setdefault('STRIPE_CURRENCY', 'YOUR_CURRENCY')
os.environ.setdefault('LANGUAGE_CODE', 'YOUR_LANGUAGE_CODE')
os.environ.setdefault('TIME_ZONE', 'YOUR_TIMEZONE')
os.environ.setdefault('EMAIL_HOST_USER', 'YOUR_EMAIL_USER')
os.environ.setdefault('EMAIL_HOST_PASSWORD', 'YOUR_EMAIL_PASSWORD')
os.environ.setdefault('EMAIL_HOST', 'smtp.google.com') # if you use gmail 

```

If you plan to make your repository public, ensure you add `.env` file to `.gitignore` before committing.

4. If your IDE terminal, migrate the models to create the database using the following commands:

```terminal
python manage.py makemigrations
python manage.py migrate
```

5. Create a superuser to access the admin panel using the following command:

```terminal
python manage.py createsuperuser
```

Then follow the instructions to create the superuser.

6. After you login to the admin panel, you can add data to be displayed in your `PRODUCT` apps. Refer to [database modeling](#database-modelling). Alternatively, you can use fixtures, follow below command to load data into the database in the following order:

`PRODUCT APP`:

`product_categories`, `collections`, `tags`, `images`, `images_folder` and only then `products`.


```terminal
python manage.py loaddata <fixture_name>

```
Be sure to load the Categories before the Products to ensure no future errors occur.

7. To initiate the application, type the command `python manage.py runserver` in your terminal. The application is now available in your browser at the address: `http://localhoset:8000`

[Back to content](#contents)

### Deployment to Heroku ###

To deploy the app to Heroku, use the following steps:

1. Ensure you have the following dependancies installed in your app, such as PostgressSQL driver for Python, WSHI HTTP Server and dj database url that connects the the app with the database:

```terminal
pip3 install psycopg2-binary

pip3 install install gunicorn

pip3 install dj_database_url
```

2. If you haven't already, create `requirements.txt` file containing all of the dependancies:

```terminal
pip3 freeze > requirements.txt
```

3. Create a `Procfile` that contains the following: `web: gunicorn art_i_al.wsgi:application`.
4. Push these newly created files to your repository master.
5. Login to Heroku and create a new app.
6. In Heroku dashboard of the new app, click **deploy**, then **deployment** method and select **GitHub** to connect your app to your github repository for automatic deployment.
7. In Heroku Resources tab, navigate to **Add-Ons** section and search for **Heroku Postgres**. I recommend you choose hobby level for this application.
8. In settings tab, navigate to **Reveal Config Vars** and add the following variables:

| **KEY**               | **VALUE**                          |
| --------------------- | -----------------------------------|
| AWS_ACCESS_KEY_ID     | ACCESS_KEY_ID_PROVIDED_BY_AWS      |
| AWS_S3_REGION_NAME    | REGION_PROVIDED_BY_AWS             |
| AWS_SECRET_ACCESS_KEY | SECRET_ACCESS_KEY_PROVIDED_BY_AWS  |
| AWS_STORAGE_BUCKET    | STORAGE_BUCKET_PROVIDED_BY_AWS     |
| DATABASE_URL          | YOUR_DATABASE_URL                  |
| EMAIL_HOST            | smtp.google.com (if using gmail)   |
| EMAIL_HOST_PASS       | YOUR_EMAIL_PASSWORD                |
| EMAIL_HOST_USER       | YOUR_EMAIL_USER                    |
| LANGUAGE_CODE         | YOUR_LANGUAGE_CODE                 |
| SECRET_KEY            | YOUR_DJANGO_SECRET_KEY             |
| STRIPE_CURRENCY       | YOUR_STRIPE_CURRENCY               |
| STRIPE_PUBLIC_KEY     | YOUR_STRIPE_SECRET_KEY             |
| STRIPE_SECRET_KEY     | YOUR_STRIPE_PUBLIC_KEY             |
| STRIPE_WH_SECRET      | YOUR_STRIPE_WH_SECRET              |
| TIME_ZONE             | YOUR_TIME_ZONE                     |
| USE_AWS               | True                               |

9. In settings.py in your IDE, temporarily comment out the database and use below code instead (make sure you do not commit!):

```python
DATABASES = {
        'default': dj_database_url.parse('POSTGRESS URL')
    }
```

10. In terminal, migrate the models to create the Postgress database using the following commands:

```terminal
python manage.py makemigrations
python manage.py migrate
```

11. Create a superuser to access the admin panel using the following command:

```terminal
python manage.py createsuperuser
```

Then follow the instructions to create the superuser.

12. After you login to the admin panel, you can add data to be displayed in your app for `HOME` and `PRODUCT` apps. Refer to [database modeling](#database-modelling). Alternatively, you can use fixtures, follow below command to load data into the database in the following order:

`PRODUCT APP`:

`product_categories`, `collections`, `tags`, `images`, `images_folder` and only then `products`.

`HOME APP`:

`about_section`, `social_media_icons`.

```terminal
python manage.py loaddata <fixture_name>
```

13. Remove the temporary database from settings.py and uncomment the original code, then push the code to origin.
14.  Back to in **Heroku dashboad**, deploy the application.
15.  To view the site, click on **View App**.

### Hosting Media files in AWS ###

The *static* and *media files* are hosted in the [AWS S3 Bucket](https://aws.amazon.com/). To host them, you need to create an account in AWS and create your S3 basket with **public access**. More about setting it up you can read in [Amazon S3 documentation](https://docs.aws.amazon.com/AmazonS3/latest/gsg/CreatingABucket.html) and this [tutorial](https://django-storages.readthedocs.io/en/latest/backends/amazon-S3.html).

[Back to content](#contents)

---

## Credits ##

### Images ###

### Image editing ###

- I have used the snippet tool for capturing screengrabs which I saved as images.
- I have also used [giphy.com](https://giphy.com/) to convert MP4 video files to gif files used in Testing.md.
- [Image size editor](https://tinyjpg.com/)
- [Video Compressor](https://www.freeconvert.com/video-compressor)
- [Videezy](https://www.videezy.com/free-video/lithuania-sea?page=3&from=mainsite&in_se=true) for video content on the home page.

### Code ideas ###

- Project was developed by following the Code Institute video course 'Boutique Ado'.
- Stack Overflow for finding solutions or hints on how to solve issues and how to make it work.
- I referred to the Django documentation sources during the development.
- Former CI student's projects.

[Back to content](#contents)

---

## Acknowledgements ##

I'd like to say thank you to everyone who has supported me throughout this project:

- My husband James and my Sister Indre - you were great at supporting me! Thank you ???
- Fellow CI Students and Tutors - to name a few: [Simon](https://github.com/jumboduck), [Karol](https://github.com/KarolSliwka), [Michael](https://github.com/mparkcode), [Igor](https://github.com/bravoalpha79), [Chris](https://github.com/ckz8780/)
- Big thank you to everyone who tested my site, including [Byllsa](https://github.com/byIlsa), [Daisy](https://github.com/Daisy-McG), [Richard](https://github.com/richardhenyash) and anonymous Ngiap! Thanks for breaking my site and allowing me to fix it! ???
- My mentor [Simen Daehlin](https://github.com/Eventyret) - you're the best.

[Back to content](#contents)
