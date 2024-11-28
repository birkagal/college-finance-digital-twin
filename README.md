<h1>College Finance Digital Twin</h1>

> Course project for the Integrative Software Development course.
> March-July 2021.

Developed a full stack application from scratch with five other team members in an agile development cycle working on bi-weekly sprints as part of the integrative software development course.
The main component we developed was the server, which was written using `Spring Boot Framework.` 
The data is maintained using `MySQL`.
We also made a small and simple client side with `HTML` and `Javascript` that communicate with the server.

The first step of the process was writing the Requirment document. That document was the guiding hand during developing stage.

<h2>Requirements Document</h2>
<h3>1. Introduction</h3>
<li>As in every public institute there is a need for a finance department to manage and process the finances for its operation. In our project we build a finance department for such an institute.</li>
<li>The system is one that simulates the digital twin of a college financial department. Our system takes into account a college in which we have students attending predetermined courses. As in a student receives a curriculum he cannot change. A worker that teaches predetermined classes and an office that oversees and manages the payment surrounding them.</li>
<h4>1.1.	Purpose of system</h4>
<li>The system will manage salary payments to lecturers.
<li>The system will allow students to keep track of payments to the college, make a payment.
<li>The system will serve to manage the finances and assist the administrative staff in organizing the salaries of workers and payments form students.
<h>1.2.	Scope of System
<li>
  The scope of this system is a web-based application to be used as an interface for managing           financial information such as worker salary, student balance and generation of reports.
  Payment processing, course managing, messaging are not a part of the system.
</li>
<h3>2.	Actors and Goals</h4>
<h4>2.1.	Primary Actor</h4>
<li>Student</li>
<li>Worker</li>
<li>Office worker</li>
<h4>2.2.	Support Actor</h4>
<li>Bank</li>
<li>Credit card center</li>


  <h3>3. Functional Requirement</h3>
<h4>3.1. Use Case Diagram</h4>

![use-case-diagram](https://user-images.githubusercontent.com/69447915/120472323-6a4ba400-c3ae-11eb-9afe-a488dc7d1d38.png)

<h4>3.2.	Use Case Details</h4>
<h5>3.2.1.	Student Payment Statement View</h5>

![image](https://user-images.githubusercontent.com/69447915/120472463-97985200-c3ae-11eb-8996-24f9d1e33f05.png)

<h5>3.2.2.	Worker Salary Statement View</h5>

![image](https://user-images.githubusercontent.com/69447915/120472472-99faac00-c3ae-11eb-9412-2ef90ba5855e.png)

<h5>3.2.3.	Office Issues Payment to Worker</h5>

![image](https://user-images.githubusercontent.com/69447915/120472484-9cf59c80-c3ae-11eb-9976-90fbd06b99ac.png)

<h5>3.2.4.	Office Updates Student’s Payment</h5>

![image](https://user-images.githubusercontent.com/69447915/120472491-9ebf6000-c3ae-11eb-976f-f51770d7d958.png)

<h5>3.2.5.	Generate Report</h5>

![image](https://user-images.githubusercontent.com/69447915/120472497-a121ba00-c3ae-11eb-902e-d5445a4745d4.png)


<h5>3.2.6.	Add New Student</h5>

![image](https://user-images.githubusercontent.com/69447915/120472508-a54dd780-c3ae-11eb-9c95-89f7ab7bed9a.png)

<h5>3.2.7.	Add New Worker</h5>

![image](https://user-images.githubusercontent.com/69447915/120472519-a848c800-c3ae-11eb-9edb-4583168213d5.png)

  <h3>4.	Non-Functional Requirements</h3>
  
![image](https://user-images.githubusercontent.com/69447915/120472528-aa128b80-c3ae-11eb-8890-051b83c64758.png)

  <h3>Technological Stack and Tools</h3>
  <h4>1.	Front End</h4>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
  <h4>2.	Back End</h4>
  <li>Java</li>
  <li>Spring Boot</li>
  <h4>3.Database
  <li>MySQL</li>
  <li>Clever Cloud</li>
  <li>MySQL Workbench</li>
  <h4>4.	Testing</h4>
  <li>Postman</li>
  <li>Junit</li>
  <h4>5.	Miscellaneous </h4>
  <li>Microsoft Office</li>
  <li>Google Docs</li>
  <li>Trello (Kanban)</li>
  <li>StarUML</li>

  <h4>Usage of client</h4>
  <h5>Information on how to run the client<5>

0. In order to config the urls for the client to work it is a few steps are needed:
	- Start the server and check the port number which should be 8042.
	- in the index.js file, there are two global variable which control the url prefixes for interacting with the localhost of the server.
	  sessionServerURLPrefix contains the url for the server.
	  sessionCurrentURLPrefix contains the url for the current client website running in the browser.
	  Insert into the proper variable your url address and the rest of the client follows automatically.
	  
1. index.html is the starting point for the website. It is the login page for any of the users in the system (no admin though).

2. Depending on the email entered we are redirected to student.html (player@example.com), worker.html(worker@example.com) or office.html (manager@example.com).

3. student.html:
	In this page we load the information for the specific student that logged in.
	The course content is stubbed and not from the server.
	Name and balance is loaded from server.
	
4. worker.html:
	In this page we load the information for the specific worker that logged in.
	The course content is stubbed and not from the server.
	Name and balance is loaded from server.
	
4. office.html:
	The control panel for the office worker. 
	There are three sections to this page, student controls, ,worker controls and report generation.
	- clicking on "add student"/"add worker" opens a modal to be filled with information to create a new student\worker and add them to the system.
	- clicking on "show students"/"show workers" displays the current items in the systems according to type.
	- clicking on "generate report" redirects to report.html in which we show financial data calculated form the system.
	
IMPORTANT:
	There is a user and an item in the database which have a unique ID that is required for certain methods to work.
	ERASING IT WILL BREAK ITEM GETTING FROM SERVER.
	
	The user is:
		2021b.Shahar.Hilel.Michael:player@example.com | player.jpg | player@example.com | PLAYER | 2021b.Shahar.Hilel.Michael | player
	The item is:
		2021b.Shahar.Hilel.Michael:ae1260fa-244a-4108-8660-e6e15b281f81 | true | manager@example.com | 2021-05-30 09:35:24.682000 |
		{"userId":{"space":"2021b.Shahar.Hilel.Michael","email":"player@example.com"},"role":"PLAYER","username":"player","avatar":"player.jpg","balance":"0"} |
		ae1260fa-244a-4108-8660-e6e15b281f81 | 2021b.Shahar.Hilel.Michael | {"lat":0,"lng":0} | player player | student.
