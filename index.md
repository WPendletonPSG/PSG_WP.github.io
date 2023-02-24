
## Professional Self-Assessment

This path that we call Computer Science (CS) is one without end. Not a path to nowhere. Quite the opposite. It is a path to everywhere. This is the very idea behind the old adage that the journey is more valuable than the destination. Though I have never been accused of not having one it is through the program guiding me down this path that I found my true voice.
      
The CS program has helped me grow in my career by transitioning from a Mechanical Designer to managing the department in charge of IT and Integration. This was accomplished through communicating to internal stakeholders the best practices and techniques learned from the IT courses to harden our network and protect it from unauthorized influencers. The DAT and DAD courses provided me with an unparalleled advantage in the workspace with data management and how to use it to convert information into wisdom and insights. This allowed me to foster a culture of collaborative data driven decision making that has increased productivity and reduced overall workloads through changes to processes and procedures. The CS courses provided me with the knowledge of data structures and algorithms required to automate some of the more laborious and error prone computer related processes by integrating different systems together and creating custom reports and dashboards via our various system APIs. This success has allowed me to hire two other people to work for me creating the Integration Department where all things technology get reviewed and signed off on prior to purchase and implementation. 
      
## Code Review

The code review in the link at the bottom of this section illustrates my ability to objectively analyze and review my own code and by extension the code of others. In reviewing my own code, I had to step outside of the role of developer and set aside all emotional attachment to the project to provide an objective review of the code for the sake of the product.
      
Proficiency of _[CS-499-02] Design, develop, and deliver professional-quality oral, written, and visual communications that are coherent, technically sound, and appropriately adapted to specific audiences and contexts_ course outcome was fully demonstrated in this code review, linked below, and the professional assessment.

[Code Review](https://youtu.be/R0OlxKgjNd0)
      
## Artifact Choice

A single artifact, Weight Tracking application developed for the CS-360 class in December of 2022, was chosen to enhance for the portfolio project. This application was originally developed for the Android platform with Java, XML, and SQL using Android Studio. There are three screens in this application. The Logon screen, User Information screen, and the Text Messages Privileges screen. The login screen has a username and password text field and two buttons one for logging in and another for creating a new account. The text message privileges screen allows the user to opt-in to receive text messages from the application. The user information screen has the user weigh with a time and date stamp along with a row to input new weights and set a target weight. 

[Original Artifact](https://github.com/SNHU-WPendletonPortfolio/WeightTrackingApp_cs360)

[Enhanced Artifact](https://github.com/SNHU-WPendletonPortfolio/cs499_WeightTracking_webApp)
      
## Software Design and Engineering

The original project was built in Java and XML in Android Studio. In this original configuration the code had no comments, and the solution was limited to the Android platform. The enhancement for this project is achieved by converting it to a web-based application using HTML, CSS, JavaScript, and MongoDB with adequate commenting for collaborative development and maintenance of the application. This enhancement choice allows the application to be used across all platforms with web access, not just the Android platform. The primary learning experience I received from rebuilding this project is that web development requires a different approach to solving the problem. I approached development of the web application through the lens of UI/UX first, then functionality.
      
Proficiency of _[CS-499-01] Employ strategies for building collaborative environments that enable diverse audiences to support organizational decision making in the field of computer science_ was achieved in this category.

![User Login](https://github.com/SNHU-WPendletonPortfolio/SNHU-WPendletonPortfolio.github.io/tree/main/images/newUI_Login.png)

![App Permissions](https://github.com/SNHU-WPendletonPortfolio/SNHU-WPendletonPortfolio.github.io/tree/main/images/newUI_permissions.png)

![User Data](https://github.com/SNHU-WPendletonPortfolio/SNHU-WPendletonPortfolio.github.io/tree/main/images/newUI_userData.png)

## Algorithms and Data Structure

The original build of the artifact was vulnerable, susceptible buffer overflow attacks or errors and SQL injection attacks. The application was hardened using data validation built into the CRUD structured Javascript. To reduce the potential for buffer overflow attacks or errors type validation was implemented using an IF statement.
      
      ```js
      if (typeof Number(record.weight)){ //validation of number for weight record
      const result = await client.db("weightTrackerApp").collection("recordWeight").insertOne(record);
      	}
      ```
      
To reduce the potential for SQL injection a similar method was employed in areas where the user could manually enter data. A typical method of SQL injection where the equal sign is used to create a true condition in the username or password fields will fail due to an IF statement that is being used to prevent any string containing an equal sign from being passed.
      
      ```js
      if (user.name.contains(!"=")){ //SQL injection prevention measures
      const result = await client.db("weightTrackerApp").collection("userProfile").updateOne({uPassword: user.pword});
      	}
      ```
      
Proficiency of _[CS-499-03] Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution, while managing the trade-offs involved in design choices (data structures and algorithms)_ was fully achieved in this category using the above methods.
      
A high level of proficiency and understanding of _[CS-499-05] Develop a security mindset that anticipates adversarial exploits in software architecture and designs to expose potential vulnerabilities, mitigate design flaws, and ensure privacy and enhanced security of data and resources_ was demonstrated in the development of the fields where the user interacts.

## Databases

The artifact originally had a SQL database on the back end with three tables. The different tables contained the user login credentials, user weight data, phone permissions, and the users’ goal weight. The enhancement on this was a major improvement. I switched from SQL to a Mongo Database that contained two tables. One the user profile where the users’ credentials, text preferences, and goal weight was stored and another containing the record data tracking the users’ weight by date and time. 
      
Though all three key categories contained evidence of this course outcome the Databases category best demonstrates proficiency in _[CS-499-04] Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals (software engineering/design/database)_.

![User Profile](https://github.com/SNHU-WPendletonPortfolio/SNHU-WPendletonPortfolio.github.io/tree/main/images/mongoDB_userProfile.png)

![User Record](https://github.com/SNHU-WPendletonPortfolio/SNHU-WPendletonPortfolio.github.io/tree/main/images/mongoDB_userRecords.png)
