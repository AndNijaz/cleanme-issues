# CleanMe

## 1. Introduction

CleanMe is an app designed to make it easier for users to connect with professional cleaners. It allows for quick and simple booking of cleaning services. Users can browse available cleaners, filter them by location, price, and services offered, and easily schedule an appointment. Once a booking is made, all communication remains within the app to ensure transparency and security. In case of cancellations or rescheduling, the system automatically records changes, helping cleaners manage their time and availability more efficiently.


## 2. Features

CleanMe includes the following features:

- **User Registration** – Two types of users can register: cleaner and client.
- **Post-registration for Cleaners** – After basic registration, cleaners can enter their services, hourly rates, working hours, and additional details.
- **Login System** – Secure login for both cleaners and clients, with redirection to their respective dashboards.
- **Client Dashboard** – Clients can search for cleaners using filters such as price, availability, location, and service type.
- **Cleaner Dashboard** – Cleaners can view incoming bookings, accept or decline requests, and update their information.
- **Search and Filtering** – Clients can filter cleaners based on services, working hours, location, and price, with an option to sort by price.
- **Cleaner Profiles** – Each cleaner has a profile card displaying key details, services, pricing, and buttons for booking or saving.
- **Booking Appointments** – Clients can book services by selecting a time, location, and adding comments.
- **Booking Notifications** – Cleaners receive requests that they can accept or decline, while clients get updates on their booking status.
- **Live Chat** – Communication between clients and cleaners is enabled but only within three days of the scheduled service to prevent off-app arrangements.
- **Cancellation and Rescheduling** – Clients can cancel an appointment, except within the last three days before the scheduled service.
- **Rating System** – After the service is completed, clients can rate the cleaner's work.
- **User Protection** – Terms & Conditions, as well as cancellation and rescheduling policies, are in place to ensure a fair and reliable service.
- **TO BE IMPLEMENTED: Secure Payments** – Integrated online payment system within the app to ensure transaction security.


## 3. Pages

CleanMe includes the following user interface pages:

- **Home Page / Login Page** – The main page displaying basic information about the app and allowing users to log in or sign up.
- **User Registration Page** – A page where clients or cleaners can create an account by entering basic information.
- **Cleaner Post-Registration Page** – A page where cleaners enter additional details such as services, hourly rates, and working hours.
- **User Dashboard** – Displays a list of available cleaners with search filters and sorting options.
- **Cleaner Dashboard** – A space where cleaners can view their bookings, update their information, and manage client requests.
- **Cleaner Profile Page** – A detailed cleaner profile showing their services, prices, and ratings, with options for contact and booking.
- **User Profile Page** – Allows clients to update their details such as name, surname, address, and profile picture.
- **Service Reservation Page** – A booking page where clients select the time, location, and leave a comment.
- **Reservation Confirmation Page** – A page displaying confirmation of a successful booking with details and a notification that the cleaner needs to accept the request.
- **My Reservations Page** – A page where users can view their past and upcoming bookings, cancel them, or review details.
- **Cleaner Requests Page (notifications client)** – A page where cleaners see all incoming bookings with options to accept or decline.
- **Notification Page (user)** – Displays all important notifications related to bookings, accepted or declined requests, and ratings.
- **Terms & Conditions Page** – A page containing the app’s terms of use, including cancellation and payment policies.
- **Payment Page** – A page for secure service payments directly through the app.
- **Landing Page** – A promotional page that redirects to the fully functional platform when clicking "Sign In."
- **TO BE IMPLEMENTED: Cleaner Comparison Page** – A page that allows users to compare multiple cleaners based on services, price, and ratings.
- **Chat Page** - A communication page between the client and the cleaner, available only in the last three days before the appointment.
- **Ratings Page** - A modal page where clients can leave reviews and ratings for cleaners after the service is completed.

![image](https://github.com/user-attachments/assets/064163d2-71ad-48e2-acb7-3a5c31829a38)

## 4. Functionality
4.1. Home Page #1
Home page displays basic information about the app, and allows users to navigate to other pages through a navbar. If the user is not logged in, any protected page will redirect the user to login.


4.2. Register Page #2
The register page consists of two radio box elements (a switch) which will decide on whether the person registering is a user or a cleaner. The form to register will consist of three input fields:
email
password
confirm password
with the addition of a show passwords checkbox. Additionally, it will contain a link leading to terms and conditions, as well as a link to the Login page.




4.3. Login Page #3
The login page will contain a form with two input fields:
email
password
The page will additionally have an eye icon in the password input for show password functionality, a Remember me checkbox, and two links, one leading to terms and conditions and the other to the registration page. 

4.4. Dashboard #4
Dashboard will be conditionally rendered based on the type of user logged in (user or cleaner)
User Dashboard allows users to browse available cleaners and book services.
Components on this page:
Filters for services, working hours, location, saved appointments, and price 
Sorting cleaners by price
Cleaner cards displaying profile information, available services, and prices
"Hire Now" button to initiate a booking
Navigation:
Link to the Cleaner Page for a detailed view of the cleaner


Cleaner Dashboard allows cleaners to manage their bookings and update their profile.
Components on this page:
List of active requests with options to accept or decline
Notifications for new requests

In addition, the cleaner will get a modal on first login, as a post registration component, where they will need fill out the form regarding:
Profile picture (optional)
Description (optional)
Services they offer
Hourly rates
Working hours
If this part is skipped, there will be a disclaimer on the dashboard which will tell the cleaners that users will not be able to view their profile until they fill out the necessary information on the profile page.





4.5. Profile Page #5
The page displays details about the cleaner or user.
Components on this page (all of which are editable):
Profile picture 
First name
Last name
Description (cleaner only)
List of available services as tags (cleaner only)
Hourly rate (cleaner only)


4.6. Cleaner Page #6
The page displays details about the cleaner This will be a dynamic page based on the id of the cleaner.
Components on this page:
Profile picture
Description 
List of available services as tags
Hourly rate 
"Hire Now" button for booking 
"Save for Later" button for saving favorites 
Navigation:
Link to the Service Reservation Page to schedule a service (“Hire Now” button)


4.7. Service Reservation Page #7
A page where the client can book a service by selecting a time, location, and leaving a comment to the cleaner. This will be a dynamic page based on the id of the cleaner.
Components on this page:
Calendar for selecting an available time slot
Input field for location
Field for adding a comment
"Book Now" button to confirm the appointment



4.8. My Reservations Page #8
A page where users can view their past and upcoming reservations.
Components on this page:
List of reservations with statuses (accepted, declined, pending)
Cancellation button (available only until the last three days before the appointment)
Chat button with the cleaner (active only in the last three days before the appointment until the completion of the appointment)
Navigation:
Link to the Live Chat Page for communication with the cleaner


4.9. Live Chat Page #9
A page for direct communication between the client and the cleaner, available only in the last three days before the appointment to the point where the appointment is finished.
Components on this page:
Chat window with messages
Send message button


4.10. Notification Page #10
Displays all notifications related to bookings and ratings.
Components on this page:
List of notifications with request statuses
Bell icon with the number of new notifications (on the navbar)

4.11. Rating & Reviews Modal #11
A modal where clients rate cleaners after the service is completed.
Components on this page:
Rating input field (1-5 stars)
Text field for a written review
"Submit Rating" button


4.12. Terms & Conditions Page #12
A page with the app's terms of use.
Components on this page:
Text display of terms and conditions
"I Accept the Terms and Conditions" button


4.13. Navigation Bar Component #13
A component present in all of the pages, used to navigate between different pages.
User navbar view:
Home -> leading to home page
Dashboard -> leading to the dashboard (user view)
My Reservations -> leading to my reservations page
Bell icon -> leading to notifications page
Profile -> leading to profile page (user view)
Cleaner navbar view:
Home -> leading to home page
Dashboard -> leading to the dashboard (cleaner view)
Bell icon -> leading to notifications page
Profile -> leading to profile page (cleaner view)



## 5. API Documentation
### CRUD Operations

### Data Transfer Objects


## 6. Technical Requirements


## 7. Out of Scope
