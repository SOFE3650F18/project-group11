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
##### Reference Architecture Alternatives
* Mobile Applications
* Rich Client Application
* Rich Internet Applications
* Web Application 
* Desktop Application

##### Distributed deployment patterns alternatives
* 2 tier
* 3 tier
* 4 tier

Design Decision| Rational |
-|-
Rich Client Application on the client side | <li> Supports rich user interaction <li> Simple deployment and updating <li> Portability **CON-2**
Service Application on the server side | <li> Application updates and maintenance <li> Combining applications and services <li> Centralization of control <li> Easy maintenance <li> Privacy, Security, Availability, Scalability **CON-4**
3 Tier Application |  
Publish-subscribe Pattern | 
Client - Server Pattern |



##### Tactics

##### Externally developed components (e.g Frameworks)
##### Design Decisions


#### Step5: Instantiate architectural elements, allocate responsibilities and define interfaces
* Interfaces are not defined in the first iteration

Element| Responsibility | Properties
-|-|-
Application Server|
Presentation Layer (Client Side) |
UI Components 
#### Step6: Sketch views and record design decisions
#### Step7: Perform analysis of current design and review iteration goal and design objectives 


### 2nd Iteration
----

#### Step2: Establish iteration goal by selecting drivers
Goal|Defining the components of the architecture to achieve the functional requirements of the system|
--|--

#### Step3: Choose one of more elements of the system to decompose


#### Step4: Choose one or more design concepts that satisfy the selected driver

##### Architectural / Design Patterns
* Object-oriented
* Client-server
* Blackboard
* Event Based
* Publish-subscribe


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
#### Step5: Instantiate architecural elements, allocate responsiblites and define interfaces
#### Step6: Sketch views and record design decisions
#### Step7: Perform analysis of current design and review iteration goal and design objectives 


