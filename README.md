# REPORT PROPOSAL FOR WEB APPLICATION
TITLE OF THE PROJECT : **ONLINE QURAN TUTOR REGISTRATION AND BOOKING SYSTEM**  
GROUP: **4**  
SECTION: **2**  
SUBMISSION DATE: **27 MAY 2024**

TEAM MATES:
1. **ADLIN HAFIDZ BIN JAMAL SHUPARDI** and **2112133**
2. **NUR AIN BINTI LIZAM** and **2127942**
3. **NUR FATIHAH ADAWIYAH BINTI RUSDI** and **2126644**
4. **AESYAH HAFIDZAH BINTI AB RAHMAN** and **2211158**

CONTENT OUTLINE:
1. **INTRODUCTION**

   The "Online Quran Tutor Registration and Booking System" is an online tool created to make scheduling classes and registering for classes easier. Through the provision of an       effective, user-friendly interface for session management, this platform seeks to streamline the interaction between instructors and students. By concentrating on essential        features like scheduling and registration, the system improves learning by cutting down on administrative work and making sure instructors and students can simply manage their     calendars.

2. **OBJECTIVES**
 
   The Online Tutor Registration and Booking System's main goals are:

    **2.1 Simplify the Registration Process:** Give students access to an intuitive registration portal so they may sign up for classes.
   
    **2.1 Fasten Booking Process:** Save time and smoothen the booking processes without need to go to the place and students can book and adjust schedule anytime and anywhere 
    they like.

    **2.2 Effective Scheduling:** Provide students with the ability to swiftly schedule available times, and provide tutors the ability to oversee and validate these reservations.

    **2.3 Send Students messages Automatically:** Students can get messages about their registration status and session details automatically.  

    **2.4 Improved User Experience:** To guarantee a seamless and enjoyable experience for tutors and students alike, design an intuitive and user-friendly interface.

4. **FEATURES AND FUNCTIONALITIES**

    **3.1 Homepage:**
   
   Background information on the organisation.
   Information about tutors and class sessions, including class fees.
   Call-to-action buttons include "Register Now" and "Book a Session."
   
    **3.2 User Authentication:** Students and tutors have separate logins. The registration page allows new users to sign up.

   **3.3 Student registration:**

   Enter student information.
   Choose available sessions for enrollment.
   Tutors review and approve registrations depending on their eligibility and availability.
   Approved students will get alerts and log-in credentials via WhatsApp and email.  

   **3.4 Session Booking:** Students can see available sessions and reserve them. Tutors can view booked sessions and manage their own calendars.  

   **3.5 Booking Management Dashboard:**

     * **Student Dashboard:** An overview of scheduled sessions, including information and cancellation/rescheduling options.
   
     * **Tutor Dashboard:** An overview of planned sessions, student information for each session, and acceptance or rejection of reservations.
   
   **3.6 Search and Filter Pages:** Advanced search capability allows you to discover specific classes using a variety of parameters.
   
   **3.7 Contact Us Page:** Users can utilise the contact form and details to contact us with any inquiries or concerns.
   
   **3.8 FAQ Page:** Frequently Asked Questions, including answers to registration, booking, payments, and cancellations.
   
   **3.9 Notification System:** Automatic alerts for session confirmations, changes, and reminders.
   
   **3.10 Cancellation and Reschedule:** Students can cancel and reschedule appointments within a specific duration.
   
   **3.11 Feedback and ratings:** Allow students to submit comments and rank sessions after attending.

5. **ERD (DATABASE TABLES WITH RELATIONSHIP)**

!!P/S: Create er diagram based on the description below then paste the actual er diagram , thank you!! 

Tables:

Users: Stores user information (user_id, full_name, email, password, gender, age, user_type (student/tutor)).  

Tutors: Stores tutor-specific information (tutor_id, user_id, qualifications, phone_no).  

Students: Stores student-specific information (student_id, user_id, education_status, preferences (ustaz/ustazah)).  

Sessions: Stores session information (session_id, tutor_id, title, description, time, day, price).  

Bookings: Stores booking details (booking_id, session_id, student_id, status, created_at).  

Feedback: Stores feedback details (feedback_id, session_id, student_id, rating, comments).   

Relationships:

Users (one-to-one) -> Tutors  

Users (one-to-one) -> Students  

Tutors (one-to-many) -> Sessions  

Sessions (one-to-many) -> Bookings  

Students (one-to-many) -> Bookings  

Sessions (one-to-many) -> Feedback  

Students (one-to-many) -> Feedback  

7. **SEQUENCE DIAGRAM TO REPRESENT THE INTERACTION**

!!P/S: Create sequence diagram based on the description below (open edit to have a proper view. the allignment was slightly run, but hopefully u still able to understand the picture) then paste the actual one below , thank you!!  

   **7.1 Registration and Booking Phase:**

   Student         System           Tutor
   |               |               |
   |---Request Booking--->|        |
   |               |               |
   |               |---Check Availability--->|
   |               |               |
   |<---Available/Full--|               |
   |               |               |
   |---Submit Registration--->|        |
   |               |               |
   |               |---Register/Waitlist--->|
   |               |               |
   |               |---Notify Tutor--->|
   |               |               |
   |               |<---Approval/Rejection--| 
   |               |               |
   |<---Confirmation/Rejection--|        |  
   ![registration and booking phase](https://github.com/ainlizam/WebAppProject/assets/170220596/35859117-c9c1-4064-a7c8-fc1960a1238f)

   **7.2 Cancellation and Rescheduling:**  
   
   Student         System
   |               |
   |---Request Cancel/Reschedule--->|
   |               |
   |               |---Process Request--->|
   |               |
   |<---Confirmation--| 
   ![cancel   reschedul](https://github.com/ainlizam/WebAppProject/assets/170220596/aff38ea8-06a1-4cd2-a770-dcbd8f9ae96f)

   **7.3 Feedback Submission:**  
   
   Student         System
   |               |
   |---Submit Feedback--->|
   |               |
   |               |---Store Feedback--->|
   |               |
   |<---Update Ratings--|
   
   ![feedback](https://github.com/ainlizam/WebAppProject/assets/170220596/e7362ed7-03f1-482c-b67c-999e1856a2b6)


9. **REFERENCES**

P/S: For formatting and styling of your proposal via README.md file refer to Markdown 
syntax. Submit the URL of your GitHub README.md file to iTaleem and respect the 
deadline.
