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

Design Decision| Rational|
-|-
Service Application|<li> The services layer effectively provides an alternative view that allows clients to use a different channel to access the application **[CON-3]** <li> users can access the application through the presentation layer, which communicates either directly with the components in the business layer; or through an application façade in the business layer if the communication methods require composition of functionality. Meanwhile, external clients and other systems can access the application and make use of its functionality by communicating with the business layer through service interfaces. This allows the application to better support multiple client types, and promotes re-use and higher level composition of functionality across applications. **[CON-8,9] [QA-4]**
Rich Client Application|<li> connected applications that have broad cross-platform reach, are highly graphical, and support rich media and presentation features **[CON-5]** 
Pub-Sub Pattern|<li> In congruence with course messaging system **[CON-7]**
3-Tire|<li> Implementations move presentation logic to the client. resulting in performance optimization **[CON-4] [QA-4]**
Layered Architecture|<li> Layers help to differentiate between the different kinds of tasks performed by the components, making it easier to create a design that supports *reusability* of components **[QA-10]** <li> Dividing an application into separate layers that have distinct roles and functionalities helps you to maximize *maintainability* of the code, optimize the way that the application works when deployed **[QA-3,4,6,9,11]** **[CON-1,2,4,6]**

#### Step5: Instantiate architectural elements, allocate responsibilities and define interfaces
* Interfaces are not defined in the first iteration

#####Client Side
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

#####Server Side

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
Time Server Access|Controls the time sequences for asynchronous communication ||
DATA|responsible for Physical storage of the data at very low level||



#### Step6: Sketch views and record design decisions


#### Step7: Perform analysis of current design and review iteration goal and design objectives 
Quality Attributes|Constrains|
-|-


### 2nd Iteration
----

#### Step2: Establish iteration goal by selecting drivers
Goal|Defining the components of the architecture to achieve the functional requirements of the system|
--|--

#### Step3: Choose one of more elements of the system to decompose


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


