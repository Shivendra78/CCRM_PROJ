<img width="660" height="639" alt="image" src="https://github.com/user-attachments/assets/49bac89e-857d-4fb8-90da-80f8a420498b" /># CCRM_PROJ
Markdown

# Campus Course & Records Manager (CCRM)

This is a comprehensive console-based Java application designed to manage the core data and processes of a higher education institution. It's built to handle everything from student and course information to managing enrollments and grades, all while keeping your data safe with robust file operations.

# Project Overview

The Campus Course & Records Manager (CCRM) is a hands-on project that puts fundamental and advanced Java programming concepts into a single, functional application. It's a great example of object-oriented programming, modern Java APIs, and file handling in action.

Key Features:

* Student Management: You can create, list, update, and even deactivate student records.
* Course Management: Easily create, update, and deactivate courses, and assign instructors to them.
* Enrollment & Grading: Manage student enrollments, making sure they don't exceed credit limits, and handle grading and GPA calculations.
* File Operations: Import and export data in CSV format using modern NIO.2 file operations.
* Backup System: Create timestamped backups with recursive directory operations to protect your data.
* System Reports: Generate comprehensive statistics and reports to get a clear overview of the system.

# The Evolution of Java

Java has a rich history of evolution, constantly improving to meet the needs of modern development. Here's a brief timeline:

* 1995: Java 1.0 - The original release that introduced the "Write Once, Run Anywhere" (WORA) philosophy.
* 1997: Java 1.1 - Added new features like inner classes and JDBC (Java Database Connectivity).
* 1998: Java 2 (J2SE, J2EE, J2ME) - A major update that established the three main platforms: Standard Edition, Enterprise Edition, and Micro Edition.
* 2004: Java 5 (J2SE 5.0) - A huge release that brought us generics, enums, and the enhanced for-loop, among other things.
* 2014: Java 8 - A game-changer with the introduction of lambda expressions and the Streams API, making functional programming in Java a reality.
* 2017: Java 9 - Introduced the Java Platform Module System (JPMS), which modularized the JDK.
* 2018: Java 11 - The first long-term support (LTS) release under the new release cadence, which removed some of the older Java EE modules.
* 2023: Java 21 - The latest LTS release, featuring modern concurrency with virtual threads and enhanced pattern matching.

# Java Platform Comparison

Here’s a simple breakdown of the different Java platforms:

* Java SE (Standard Edition): This is for building standard desktop, server, and embedded applications. It includes the core Java APIs, which is what this project uses.
* Java EE (Enterprise Edition): This platform is for large-scale, multi-tiered enterprise applications. It provides APIs for things like servlets, JSPs, and web services.
* Java ME (Micro Edition): This version is specifically for mobile and embedded devices with limited resources.

# Java Architecture: JDK, JRE, and JVM

The Java platform is built on three key components that work together seamlessly.

* JDK (Java Development Kit): Think of this as the complete toolbox for a Java developer. It includes the compiler ('javac'), a debugger, and all the other tools you need to write and build a Java program.
* JRE (Java Runtime Environment): This is what you need to run a Java program. It includes the JVM and the necessary class libraries. You can't develop with it, but you can definitely run applications.
* JVM (Java Virtual Machine): This is the magic behind Java's "Write Once, Run Anywhere" philosophy. The JVM takes the platform-independent bytecode from your compiled code and translates it into code that your computer can understand and execute.

# Getting Started

#### Prerequisites

* Java 8 or higher
* Any Java IDE (like Eclipse, IntelliJ IDEA, or VS Code)
* Command-line access

#### Installation & Setup

1. Clone or download the project
'git clone <repository-url>'
'cd campus-course-records-manager'

2. Compile the project
'javac -d . src/main/java/com/ccrm/*.java src/main/java/com/ccrm/**/*.java'

3. Run the application
'java com.ccrm.CampusCourseRecordsManager'

# Setting up the Project in Eclipse IDE

1. Launch Eclipse and select File > Import...
2. Choose Git > Projects from Git (with smart import) and click Next.
3. Select Clone URI and paste the project's repository URL. Click Next.
4. Choose the main branch and click Next.
5. Set the local directory for the project and click Next.
6. Eclipse will automatically recognize it as a Java project. Click Finish.

Now that the project is in your workspace, you can run it by right-clicking on 'CampusCourseRecordsManager.java' in the Package Explorer and selecting Run As > Java Application.

# Project Requirements Mapping

Here's a quick look at where you can find each key concept implemented in the code:

* Encapsulation: You'll find private fields with public getters and setters in files like 'model/Person.java' and 'model/Student.java', ensuring controlled data access.
* Inheritance: The abstract 'Person' class is the base for 'Student' and 'Instructor', allowing them to share common properties and behaviors.
* Abstraction: The 'Person' class defines abstract methods like 'getRole()' that its subclasses must implement, setting a clear contract.
* Polymorphism: A 'Person' reference can hold either a 'Student' or an 'Instructor' object, showcasing flexible code design.
* Singleton Pattern: The 'DataStore' class ensures that only one instance exists throughout the application to manage all data centrally.
* Builder Pattern: The 'CourseBuilder' and 'TranscriptBuilder' are used for building complex objects step-by-step.
* Custom Exceptions: We use our own exceptions like 'MaxCreditLimitExceededException' for more specific error handling.
* NIO.2: Modern file operations using the 'Path' and 'Files' APIs are demonstrated in 'utils/FileUtils.java' and 'utils/BackupUtils.java'.
* Streams: The Streams API is used for declarative data processing and filtering in files like 'core/DataStore.java' and 'services/StudentService.java'.
* Date/Time API: 'LocalDate' is used to handle dates without time zones in 'model/Student.java' and 'model/Enrollment.java'.
* Enums: Our enums like 'Semester.java' and 'Grade.java' provide type-safe constants with associated data and methods.
* Recursion: You can see recursive directory traversal and operations in the 'utils/BackupUtils.java' file.

# Enabling Assertions

To enable assertions, you just need to use the '-ea' flag when you run the Java application from the command line. This is super helpful for debugging and for internal consistency checks.

Sample Command:

'java -ea com.ccrm.CampusCourseRecordsManager'

*ScreenShot of the Operations included in this program
--> Main Output of the code looks like this where you find options to select as per your requirement
<img width="545" height="337" alt="image" src="https://github.com/user-attachments/assets/bf0ae9bf-0303-40e0-9ffc-f3035a79f130" />
---->Now here you can see the option now Enter the option 1 you get menu of Student Management
<img width="337" height="276" alt="image" src="https://github.com/user-attachments/assets/c1dbb63f-aba1-41c5-a3ae-bc30cbe7010f" />
--->In this you can see the options of Student management and perform operations as per your Wish let's do some operations
1. Add New Student
2. View All Students
3. View Student Details
4. Update Student
5. Deactivate Student
6. Generate Student Transcript
0. Back to Main Menu
Here is the ScreenShot
<img width="367" height="247" alt="image" src="https://github.com/user-attachments/assets/a8d84013-ad35-4ffa-b9d3-c7a7f461f17e" />
After Selecting options
<img width="552" height="565" alt="image" src="https://github.com/user-attachments/assets/4ac13555-115d-481e-91c1-94217a0bcc29" />

<img width="1305" height="303" alt="image" src="https://github.com/user-attachments/assets/0330b1dc-5ace-42b8-a03c-a0c5cd7ba9d4" />

When i select option 3
<img width="1272" height="184" alt="image" src="https://github.com/user-attachments/assets/096a941d-7a0c-4df9-9292-4cbb86a4d15a" />

For option 4
<img width="1316" height="352" alt="image" src="https://github.com/user-attachments/assets/d1126768-8926-47b7-baf8-df76e204deeb" />

You can also deactivate Student by option 5
<img width="415" height="260" alt="image" src="https://github.com/user-attachments/assets/562e330e-5505-4bcd-bbe4-0786e0eb7cde" />

Option 6 that is  Generate Student Transcript
<img width="474" height="422" alt="image" src="https://github.com/user-attachments/assets/ca35993c-c861-4c39-8cad-9094a29e719e" />

--->Now we back to our main menu and select COURSE MANAGEMENT option
<img width="577" height="454" alt="image" src="https://github.com/user-attachments/assets/97b74920-b906-4848-92df-a604b13981a2" />

-->IN course Management you see options like
1. Add New Course
2. View All Courses
3. View Course Details
4. Update Course
5. Deactivate Course
6. Search Courses by Department
7. Search Courses by Semester
0. Back to Main Menu
Choose According to your requirement and perform operations lets see some of them
<img width="780" height="807" alt="image" src="https://github.com/user-attachments/assets/8ad72d1e-3ca0-47c8-afec-ba1df641e458" />

When we Select option 2
<img width="1500" height="71" alt="image" src="https://github.com/user-attachments/assets/50391600-e4c2-42b6-84f2-53968ee7c901" />

When we Select option 3
<img width="1533" height="344" alt="image" src="https://github.com/user-attachments/assets/7dc498d4-065d-4747-9ff1-51f0a8303c09" />

We can also update Course
<img width="1587" height="203" alt="image" src="https://github.com/user-attachments/assets/9954111d-98a6-490b-9474-4b78f0db1286" />

Add more couses
<img width="660" height="555" alt="image" src="https://github.com/user-attachments/assets/10a8ce47-fea1-4b03-9a74-9188a2be2728" />
-->BY selecting option 5 you can deactivate the course
<img width="639" height="342" alt="image" src="https://github.com/user-attachments/assets/0798f7f4-1352-4e20-8e9c-bf036abfbae9" />

...->We can also Search by Course
<img width="1554" height="596" alt="image" src="https://github.com/user-attachments/assets/b1714a5b-8f89-4214-9dfe-e2eb3f36a2a6" />

--->We can also Search by SEMESTER
<img width="1631" height="406" alt="image" src="https://github.com/user-attachments/assets/8fb1b08d-314f-4c09-9ca4-4a07ac15d8f7" />

------------------------------------------------------------------------------------------------------------------------------------------

NOW WE SEE ENROLLMENT AND GRAADING MENU BY SELECTING OPTION FROM MAIN MEnu
<img width="611" height="766" alt="image" src="https://github.com/user-attachments/assets/a4a43a49-1f94-4b6f-b1c1-b48739482238" />

-->Adding Student to the course
<img width="563" height="290" alt="image" src="https://github.com/user-attachments/assets/722ae154-5baf-4576-804a-aa4525e474d3" />

--->You can also unenroll student by selecting option 2
-->> now we Record Grade for the Student
<img width="338" height="343" alt="image" src="https://github.com/user-attachments/assets/ef7a22c0-f8ad-4a41-9a2e-78c26d777f84" />

-->You can also see the student enrolllment by selectiing option 4
<img width="1260" height="326" alt="image" src="https://github.com/user-attachments/assets/f304aa0b-d0ea-4b9d-95d0-53290450e029" />

--->You can also calculate Gpa of student 
<img width="338" height="324" alt="image" src="https://github.com/user-attachments/assets/66f60c83-d066-497e-a030-2cae5c787527" />

## We can also perform === FILE OPERATIONS === on this by selecting option 4 on main menu
<img width="449" height="490" alt="image" src="https://github.com/user-attachments/assets/5484b163-5a3a-4e5a-8fac-a62f24aae05d" />
Here by entering choice 1 i can export student data

-->now by option 2
 we can Export Courses to CSV
 <img width="407" height="240" alt="image" src="https://github.com/user-attachments/assets/b4abd812-f3a3-430f-a452-97c2946b40fb" />


 -->You can also expoert Enrollments to CSV
 <img width="468" height="251" alt="image" src="https://github.com/user-attachments/assets/771734ab-fd2c-4643-a1c6-2755a5d495ca" />

 -->you can also import Student

 <img width="895" height="274" alt="image" src="https://github.com/user-attachments/assets/e7aae5d3-d164-4084-b802-f8ff5df24b5b" />

 -->you can also import course to csv by option 5
 <img width="897" height="254" alt="image" src="https://github.com/user-attachments/assets/a40eca7a-45c2-4fbc-8eb1-eac7cd66fab6" />

 -->you can also import enrollment to csv file by option 6
 <img width="987" height="260" alt="image" src="https://github.com/user-attachments/assets/78e0cd17-9bc5-483b-b6b1-00a4c1d862c1" />


 ===>Now by selection option 5 from the main menu you can see  System Reports in which you can see
 <img width="340" height="238" alt="image" src="https://github.com/user-attachments/assets/5ce714a5-e70b-4670-a7d8-d6fee5f03a46" />

 Furthur you can select operation which you wnt to perform or see here is the screenShot of that record
 <img width="467" height="610" alt="image" src="https://github.com/user-attachments/assets/e681ac6d-5834-4181-9f7a-6e78cc54707b" />
 <img width="660" height="639" alt="image" src="https://github.com/user-attachments/assets/0f89a6fc-e6cc-4938-a5a8-5e178ab76d74" />


==>You can also add  Backup Operations by selecting option 6 from the mein menu
<img width="626" height="382" alt="image" src="https://github.com/user-attachments/assets/04d99bae-7aeb-46be-81e9-e8e739e852de" />

Here you can perform 4 operations which are listed as follow
1. Create Backup
2. List Backup Files
3. Calculate Backup Size
4. Cleanup Old Backups

ScreenShot of these operations are as follow:
<img width="681" height="730" alt="image" src="https://github.com/user-attachments/assets/b970c0aa-f1f5-41f9-a5a5-53cf21f3da4b" />
<img width="565" height="230" alt="image" src="https://github.com/user-attachments/assets/fd581d5e-34ba-4c3b-93c3-ff1727c66784" />

Thank you



































