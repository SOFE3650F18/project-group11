# 1st Deliverable

- [x] Design objective
- [x] Capture Use Cases
- [x] Quality Attributes 
- [x] Scenarios 
- [x] Constrain Requirements 
- [x] Concerns

# 2nd Deliverable-Design Process
----
## 3 Step Iterative Process 

### 1st Iteration
---- 

#### Step1: Review Inputs 

#### Step2: Establish iteration goal by selecting drivers

Goal|Defining the structure of the System |
--|--

Drivers| All Inputs|
-|-

#### Step3: Choose one of more elements of the system to decompose
* Since this is a greenfield system, the only element to decompose is the system itself

#### Step4: Choose one or more ==design concepts== that satisfy the selected driver
##### Architectural / Design Patterns
* Object-oriented
* **Client-server** : Layered Style 
* Blackboard
* Event Based
* **Publish-subscribe**

##### Reference Architecture Alternatives
* Mobile Applications
* **Rich Client Application**
* Rich Internet Applications
* Web Application 
* **Service Application**
##### Distributed deployment patterns alternatives
* 2 tier
* **3 tier**
* 4 tier

Choice|
----
![](images/layered.png)|
![](images/richClient.png)|
![](images/servicesLayer.png)|
![](images/distributedDeploymentPattern.png)|

Design Decision| Rational|
-|-
Service Application|<li> The services layer effectively provides an alternative view that allows clients to use a different channel to access the application  [UC-20,21,23] <li> users can access the application through the presentation layer, which communicates directly with the components in the business layer. Meanwhile, external clients and other systems can access the application and make use of its functionality by communicating with the business layer through service interfaces.[QA-8] [UC-4,13,14,10,11,15,16] [CON-6] This allows the application to better support multiple client types, and promotes re-use and higher level composition of functionality across applications. **[CON-7,8,9] [QA-3,4,7]** [UC-4,19,23,12,9]  [CRN-7,10]
Rich Client Application|<li> connected applications that have broad cross-platform reach, are highly graphical, and support rich media and presentation features this will allow dynamic and static search for courses as well as getting in user inputs [UC-1,2,3,5,8] **[CON-5]**  <li> RCA would also provide highly modifiable and flexible interface on the client side to take care of accessiblity needs and notification view modification. [QA-10,2,15] [UC-14] <li> RCI would also allow for state and exception management within client interface resulting [CRN-1,4] 
Pub-Sub Pattern|<li> In congruence with course messaging system **[CON-7]** [UC-6,11,22] 
3-Tire|<li> Implementations move presentation logic to the client. resulting in performance optimization **[CON-4]** <li> Some type of replication is needed on both web/app tier and the database tier to support [QA-3]. <li> Web/App tier would also perform authentication and password reset functionality. [UC-7]. [QA-5,12,13] [CRN-6]
Layered Architecture|<li> Layers help to differentiate between the different kinds of tasks performed by the components, making it easier to create a design that supports *reusability* of components **[ ]** <li> Dividing an application into separate layers that have distinct roles and functionalities helps you to maximize *maintainability* of the code, optimize[CON-5] the way that the application works when deployed. This will also allow authentication [CON-3] [CRN-2,3] and retrival of data based on user priviliges **[QA-1,11,13]** ** ** ** [UC-7,9].

#### Step5: Instantiate architectural elements, allocate responsibilities and define interfaces
* Interfaces are not defined in the first iteration
![](images/firstItr.png)
![](images/deployment.png)
##### Client Side
Element| Responsibility | Properties
-|-|-
User Work Station|Incorporates client side components and connects with the application server|OS = Windows, Linux, Mac, Runs on Java|
Presentation Layer| defines the logical behavior and structure of the application in a way that is independent of any specific user interface implementation.| Flash Player |
Business Layer| This layer implements core functionality of the system, and encapsulates the relevant business logic.||
Data Layer:|The data layer exposes generic interfaces that the components in the business layer can consume|json|
UI Components| These are the application's visual elements used to display information to the user and accept user input.||
UI Processor Components| This component process the user input and prepares it to be sent to business layer in a manner that is representative.|| 
Business Components| After the UI processor collect the required data from the user and pass it to the business layer, the application can use this data to perform a business process. ||
Business Entities| Business entities encapsulate the business logic and data necessary to represent real world elements|business objects|
Communication Components|Responsible for interaction with the application server|internet connection|

##### Server Side

Element| Responsibility | Properties
-|-|-
Application Server| Hosts the element of the service reference architecture. Connects to clients and database server||
Service Layer|Composed of multiple services, each communicating with the others by passing messages. It provides alternative view that allows clients to use a different channel to access the application.||
Business Layer|Contains components which expose service interfaces that other callers can use.||
Data Layer| This layer provides access to data hosted within the boundaries of the system.| |
Service Interfaces| external clients and other systems can access the application and make use of its functionality by communicating with the business layer through service interfaces||
Business Component|<li>Business concerned with the retrieval, processing, transformation, and management of application data.<li>Application of business rules and policies; and ensuring data consistency and validity||
Business Entities Component |Business entities validate the data contained within the entity and encapsulate business logic to ensure consistency and to implement business rules and behavior||
DB Access Component| Database engine(DBMS) that allows Retrieval, modification and maintenance of data. ||
DATA|responsible for Physical storage of the data at very low level||

#### Step6: Sketch views and record design decisions


#### Step7: Perform analysis of current design and review iteration goal and design objectives 

- [x] UC-1 Edit Personal Information 
- [x] UC-2 View Course History
- [x] UC-3 Message
- [x] UC-4 Create Teams
- [x] UC-5 Search Courses
- [x] UC-6 Subscribe-Unsubscribe from exam/course
- [x] UC-7 Reset Passwords
- [x] UC-8 Modify Notification Behaviour
- [x] UC-9 Retrieve Contact Information 
- [x] UC-10 Upload/Download Files
- [x] UC-11 Manage Course Content
- [x] UC-12 Manage Teams
- [x] UC-13 Create Courses
- [x] UC-14 Customize/Merge Teamplates
- [x] UC-15 View Student Details
- [x] UC-16 Manage Student Grades
- [ ] UC-17 Manage Backup (Create/Restore)
- [x] UC-18 Limit Course Usage Space
- [x] UC-19 Update Static Course Info
- [x] UC-20 Restrict Course Enrolment Paramenters
- [x] UC-21 Send Out Course Surveys
- [x] UC-22 Manage Courses
- [x] UC-23 Perform Statistical Calculation on Course Grade




- [X] QA-1 |Performance      
- [x] QA-2 |Modifiability     
- [x] QA-3 |Availability     
- [ ] QA-4 |User Friendliness
- [x] QA-5 |Security         
- [ ] QA-6 |Extensibility    
- [ ] QA-7 |Interoperability 
- [x]  QA-8 |Functionality   
- [ ] QA-9 |Scalability        
- [x] QA-10|Flexibility       
- [x] QA-11|Reliability      
- [x] QA-12|Privacy          
- [x] QA-13|Integrity         
- [ ] QA-14|Maintainability  
- [x] QA-15|Accessiblity     

- [ ] CON-1| System must have high availability and no more than 4hours of downtime |
- [ ] CON-2| System must be extensible/Scalable allowing students, lecturers and admin to add, remove or modify information according to their privilege |
- [x] CON-3| System must be secure and private and allow viewing and based on user privileges |
- [ ] CON-4| Student records should be stored indefinitely.|
- [x] CON-5| Users can securely interact with minimum performance degradation|
- [x] CON-6| System must be able to handle multiple user request|
- [x] CON-7| System must be able to update and notify |
- [x] CON-8| System must be able to handle message-based communication |
- [x] CON-9| System must support multiple user types i.e Students, Lecturers, Administrator.| 


- [x] CRN- 1|Exceptional Handling 
- [x] CRN- 2| Authentication
- [x] CRN- 3| Authorization and Administration privileges
- [x] CRN- 4| Session Management
- [x] CRN- 5| System Structure(i.e Technologies and existing frameworks)
- [x] CRN- 6| Deployment Pattern
- [x] CRN- 7| Team collaboration
- [] CRN- 8| Minimum number of client request/access to information  
- [] CRN- 9| Risk involving modification or expansion of database storage 
- [x] CRN- 10| Dealing with multiple users request simultaneously 
- [] CRN- 11| Database failure 



### 2nd Iteration
----

#### Step2: Establish iteration goal by selecting drivers
Goal|Defining the components of the architecture to achieve the functional requirements of the system|
--|--

Drivers|
---
Use Cases|
Quality Attributes|
Constrains|
Concerns|

Note: All the drivers are the not addressed or partially addressed instances of each. 

#### Step3: Choose one of more elements of the system to decompose
Since functionality is typically supported by elements that are spread across the layers of the system, the elements are the different layers that were identified in the previous iteration

#### Step4: Choose one or more design concepts that satisfy the selected driver




#### Step5: Instantiate architectural elements, allocate responsibilities and define interfaces


#### Step6: Sketch views and record design decisions
#### Step7: Perform analysis of current design and review iteration goal and design objectives 

### 3rd Iteration
---- 


#### Step2: Establish iteration goal by selecting drivers
Goal|Refactoring the architecture to achieve the quality requirements of the system|
--|--

#### Step3: Choose one of more elements of the system to decompose
#### Step4: Choose one or more design concepts that satisfy the selected driver
#### Step5: Instantiate architectural elements, allocate responsibilities and define interfaces
#### Step6: Sketch views and record design decisions
#### Step7: Perform analysis of current design and review iteration goal and design objectives 


