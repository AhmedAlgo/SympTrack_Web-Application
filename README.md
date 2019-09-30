# Symp+Rack 


## 1. Introduction 

This section outlines the project background, scope, timeline, risks and dependency if any.

### 1.1 Project Background

SymTrack aims to provide the patient journey from the day 1 of their chronic illness until
recovery by both the Physicians and the patients. Tracking the information daily allows both
patients and doctors to obtain a clear picture of the both the severity and frequency of symptoms
over an extended period. This app stores the data in the backend to generate weekly, monthly,
and biannual reports in a line graph and sent as email to the physicians.

### 1.2 Project Scope

- Requirement Gathering and Story creation
- System Design, Build, Test and Deploy. DevOps and Source code management
- Design front end UX, service layer, backend data store for reports and analytical operation. Support both Web based as well as Mobile based browsing
- Wireframe creation for front end visuals that demonstrate Mockup of emails complete with graphs sent to patients and doctors. Mockup of set up and data entry
- Data security and management (HIPAA compliance applicable to product)
- User Acceptance Testing
- Application Launch and Monitoring

### 1.3 Project Requirements

- System should be able to track up to 5 symptoms entered by the patient.
- System should store the current treatment plan.
- System should allow the patient to rate the severity of the symptom on a daily basis till the date of their next appointment. Includes additional features to accept manual entries for blood sugar levels, blood pressure and pulse from the patient.
- System should generate weekly, monthly, and biannual reports in a line graph.
- Reports should be available to the patient and a copy should be sent to the medical team via email.

### 1.4 Project Timeline

Our project team adapted agile methodology that engaged a team of 4 individuals for 6 sprints with 2 weeks per sprint – model implementing symp+rack through scrum delivery framework.

### 1.5 Project Risks and Dependency

- Being HIPAA compliant app, the security measures and data security required complete auditing and certification process
- Dependent with actual Physician and Patient data sets to validate the functionality of the symp+rack app

## 2 Symp+Rack Product Manual

This section outlines the detailed description of the symp+rack product and its system design, functionality, architecture and deployment model.

### 2. 1 Symp+Rack Product Overview

Millions of Americans face the day to day suffering that stems from one or more chronic illnesses. They struggle to make sense of their symptoms. They fight for care standards, work with care teams, and try to balance their illness or illnesses with their lives. Symp+rack wants to help make their lives a little easier while having an impact on the level of care received by providing an easy to use symptom diary available on either the web or a mobile device. Symp+rack will collect user data about symptoms, store it, and display the data collected in an easy to use and understand graph. Users will be able to track their data on a weekly, monthly, and annual basis. Additionally, Symp+rack will push the collected data to doctors, nurses, and other care staff allowing accurate information sharing between patient and care team regarding the severity and frequency of symptoms. Having this information will cut down on the amount of time spent checking in with patients and will offer more concrete data points for treatment plans.

### 2.2 Symp+Rack Product Flow Diagram 
 
![alt text](https://github.com/AhmedAlgo/SympTrack_Web-Application/blob/master/Report/Symp%2BRack%20Product%20Flow%20Diagram.JPG "Product Flow Diagram")

### 2.3 Symp+Rack Data Flow Diagram
![alt text](https://github.com/AhmedAlgo/SympTrack_Web-Application/blob/master/Report/Symp%2BRack%20Data%20Flow%20Diagram.JPG "Data Flow Diagram")

### 2.4 Symp+Rack Component Architecture Overview 
This product requires highly scalable, available infrastructure to store massive volume of patient day to day data in a real time fashion to the end users. Hence leverages AWS public cloud platform on a highly secured infrastructure

![alt text](https://github.com/AhmedAlgo/SympTrack_Web-Application/blob/master/Report/Symp%2BRack%20Component%20Architecture%20Overview.JPG "Component Architecture Overview ")

**Below is the architectural component used to host the symp+rack application:**

1. Load Balancing with Elastic Load Balancing (ELB)/Application Load Balancer (ALB) – Allows you to spread load across multiple Availability Zones and Amazon EC2 Auto Scaling groups for redundancy and decoupling of services.
2. Firewalls with Security Groups –Moves security to the instance to provide a stateful, host- level firewall for both web and application servers.
3. Caching with Amazon ElastiCache – Provides caching services with Redis or Memcached to remove load from the app and database, and lower latency for frequent requests.
4. Managed Database with Amazon RDS – Creates a highly available, Multi-AZ database architecture with six possible DB engines.
5. DNS Services with Amazon Route 53 – Provides DNS services to simplify domain management.
6. Edge Caching with Amazon CloudFront – Edge caches high- volume content to decrease the latency to customers.
7. Edge Security for Amazon CloudFront with AWS WAF – Filters malicious traffic, including XSS and SQL injection via customer-defined rules.
8. DDoS Protection with AWS Shield – Safeguards your infrastructure against the most common network and transport layer DDoS attacks automatically.
9. Static Storage and Backups with Amazon S3 – Enables simple HTTP-based object storage for backups and static assets like images and video.

### 2.5 Symp+Rack System Design and Installation 

### System Menu

SympTrack is page-based website/application, which consists of 9 pages. A Home page, three pages show relevant information to the users, a page, Reports, represents a form for collecting users’ data, and one page shows the users’ calendar. The second last tab has a communication platform, while the last handles the login area.
![alt text](https://github.com/AhmedAlgo/SympTrack_Web-Application/blob/master/Report/System%20Menu.JPG "System Menu")

### Home Page
The Home page consists of a header, containing a horizontal navigation bar, a body displays the application slogan, and a footer with a sitemap and contact information.

### Records Page
The Records Page where the users can see their past medical records, symptoms, medication progress and browse their logs.

### Your Doctors Page
The Your Doctors page display the users’ health service providers’ information

### About us Page
The About us page gives customers more insight into who is involved with SympTrack and exactly what it does, expressed through short articles, accompanied by photographs.

### Profile Page
The Profile page entering the user’s personal information as well as changing some application settings, such as source of contact preference information, and contact time.

### Reports Page
The Reports where patients/ health providers can report symptoms, information about care plans/medications progress.

**Report Procedures**
Each user can see only information about own health records. Data collected using the application are saved as in the database and can only be accessed by health services providers who are authorized by the user.

### Calendar Page
The calendar interface helps the user to track their appointments and medication process. They can scroll through different months and select an entire date just by clicking the box. The flyout calendar widget is the same width as the input field so it doesn’t take up that much space.

### Message Board
For this product, we will be using a Message Board Hosting service. There are many message board hosting services available. Some will charge a fee, others will host the board free. Using a Message Board Hosting service, eliminates the need and expertise to purchase, install, and maintain the software, and there is much less need for technical expertise using a hosting service. We will be using a semi-threaded board, since the Board is "Discussion Topic" oriented, and allows replies to message topics.

### Logging In
We are using a third-party framework of python for website development. The most useful part of this framework is that for account registrations and login, we can use a package known as registration-redux. All what we need to do is to install that package on the virtual environment of the PC with all the source code and include it in my project to do my work.

### Changing User ID and Password
User ID and password can be changed only by contacting producer

 **To read the full report, [click here](https://github.com/AhmedAlgo/SympTrack_Web-Application/blob/master/Report/Symp%2BRack-Report.pdf "PDF file")** 
