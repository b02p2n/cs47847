java c
Diploma in Information Technology
Problem Solving
Instruction for CA3 Group Assignment
October 2024 Semester
Assessment
100 marks (This assignment constitutes 40% of the overall assessment)
Deliverables
There are Four (4) deliverables in this assignment, students must complete ALL components.
1. Written project report (6%)
2. Python codes (20%)
3. User guides with sample inputs/outputs (4%)
4. Oral Presentation (10%)
The Task
The objective of this project is to allow students to design and implement a mini program. You are to use flowchart to design your program, with clear steps and flows indicated. You need to use Python programming language to code all the programs, according to the project requirement.
In your report, write a brief description, in 500 words, on your program design. You need to include flowcharts demonstrating the main program flow in the report. You will also include screenshot samples on how the program should run in the report.
In your Python codes, include comments to explain the purpose of each section.
Assessment Marks Allocation
Component Assessed                                       Marks Allocation
1 Part 1 – Report with flowchart                        15
2 Part 2a – Main Programs (Python)                   40
Part 2b – Additional Features                          10
3 Part 3 – User guides with screenshots              10
4 Part 4 – Oral Presentation                               25
Total                                                            100
The Case - Go “MOBILE” Locker is coming to the campus.
The CEO of Go Locker has decided to explore the deployment of “MOBILE” lockers to Nanyang Technological University (NTU).
With Internet making online shopping experience easy and enjoyable, the use of self-service lockers has become popular and a possible business opportunity for Go Locker to service students studying in big campus like NTU.
Currently in NTU, students can only one locker at a fixed location. However, with student studying different modules each semester, not all lecture halls and classrooms can be close to the locker location. Hence, a fixed location locker make it inconvenience and troublesome to access, due to “tourism” and heavy human traffic between lesson.
Combining the use of electric track transport system (not-in-scope), student can access their “MOBILE” locker at any available Go Locker stations. For example, students can request to “send” their lockers to a station nearest to their next lesson, collect and store items before next lesson.
In the pilot phase, Go Locker will allow student to rent up to 2 lockers, at $2 per locker. Student can release/return the locker anytime. Each request to move locker to a specified station will incur 20 cents. When a locker is moved to the specified station, student can proceed to access/open the locker.
As an intern in IMDA (Infocomm Media Development Authority), your supervisor has assigned you to help Go Locker with this pilot project, with objectives to automate the mobile locker rental and operations processes.
Project Requirement
After extensive discussions, Go Locker would like to have the following essential features to be included:
 System Admin functionalities that featured creation of station, locker, updating of locker details, and reports for station, locker usage.
 Station Operations/functionalities that include rent/return locker, request locker moves, enquiring locker location and viewing of usage report.
 Further features to be integrated in the application are configurable rental fees, moving fees, and a background program to process the “moving” of lockers (see BONUS features).
Based on you understanding, the pilot project will have 2 applications: one to allow Go Locker administrators to perform. administrative functionalities, and the other for students to perform. locker operations.
1. Go Locker – Admin
For the Go Locker administrators, the application should display the following menu:
^^^^ Go Locker - Admin ^^^^
1. Setup station
2. Create locker
3. Update locker
4. View station report
5. Track locker usage
0. Exit
Enter option:
Before presenting the menus, your application needs to load/pre-setup the stations, lockers, students from Appendix A and rentals (if any) into collections*.
* Your group can decide to implement using either Dictionary or List.
a. Setup station
This function allows the administrator to setup a new station.
To setup a new station, the following data elements should be collected:
 Station Code: should be unique, in format of NTU-XXX-DD, where XXX represents the building code (e.g., N21, S32), and DD represents digits from 00 to 99.
 Station Name: name description of the station (e.g., The Hive level 1, The Arc level 2)
 Rows: number of rows for this station
 Columns: number of columns for this station
 Status: Open or Closed
The maximum number of lockers for this station will be Rows X Columns. Hence if station NTU-S32-01 has 4 rows and 20 columns, the capacity for this station is 80 slots. Therefore, your application may need to include a collection to represent the 80 slots. These slots will be empty, until student request to move their locker into the station.
When a new station is created, the status should be defaulted to “Open”. The new station will be added into the collection and updated into “Stations.txt” file.
b. Create locker
Locker can be added into the system to meet the demand. To add a new locker, these data elements should be collected:
 ID: starting from 10001, increment by 1 for each new locker created
 Location: “Central store”, “In transit”, or any valid station code. Defaulted to “Central store” at creation.
 Row: default to empty/zero unless the locker is in a station.
 Column: default to empty/zero unless the locker is in a station.
 Status: “Occupied”, “Available” (default), “Suspended”.
 Rental ID: if “Occupied”, need to record the rental ID.
When a new locker is created, then locker should be added into the collection and updated into “Lockers.txt” file.
c. Update locker
The “Update Locker” option allows the administrator to update the locker’s details:
 User should first provide the locker ID to search.
 If there is no locker with this ID, display appropriate error message and return to menu.
 If the ID is valid, your program should display the locker details, and if occupied, the student ID, student name and date started renting this locker.
 Only allow update to Location and Status.
 However, status can only be updated to “Suspended” when current Status is “Available”. When updating Status from “Occupied” to “Available”, the rental record needs to be terminated.
 Any updates should also be affected into “Lockers.txt”
d. View station utilization report
The option allows the administrator to view the current station utilization.
 User should first provide the station code to search.
 If there is no station with this code, display appropriate error message and return to menu.
 If the station code is valid, your program should display the station details, and a table showing all the slots (rows x columns) – with locker IDs for those slots that contain the students’ lockers.
e. Track locker usage
The option allows the administrator to track the operations of a specific locker.
 User should first provide the locker ID to search.
 If there is no locker with this ID, display appropriate error message and return to menu.
 If the ID is valid, your program should display the locker details, and if occupied, the student ID, student name and date started renting this locker.
 Your application should ask for the Date-From and Date-To, before generating the report containing all operations for this locker during the specified dates.
 Below is a demonstration of the generation of “Track locker usage” report:
Enter Locker ID: 10002
Locker ID: 10002
Location: Central Store
Status: Occupied
Student ID: 10256499
Student Name: See Sin Ho
Rental Start Date: 14-Sep-2024
Enter Date-From: 14-Aug-2024
Enter Date-To: 15-Oct-2024
Date Time Operation Student ID
-------------------------------------------------------------
15-Aug-2024 12:33 Locker return 10255884
15-Aug-2024 12:34 Move to Central Store -
14-Sep-2024 09:11 Locker rental 10256499
14-Sep-2024 10:23 Move to NTU-S31-06 10256499
14-Sep-2024 10:45 Move to Central Store -
14-Sep-2024 14:55 Move to NTU-N21-02 10256499
14-Sep-2024 15:10 Move to Central Store -
18-Sep-2024 09:01 Move to NTU-S32-06 10256499
18-Sep-2024 09:08 Move to Central Store -
-------------------------------------------------------------
2. Go Locker - Operations
For the students, the application should display the following Operations menu:
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option:
Before presenting the menus, your application needs to load/pre-setup the stations, lockers, students from Appendix A and rentals (if any) into collections*.
* Your group can decide to implement using either Dictionary or List.
a. Rent a locker
To rent a locker, students only need to provide their student ID.
 If the ID is valid, your program should display rented locker details (if any), and if student is renting 2 lockers now, display appropriate error message and return to menu.
 If student can still rent a locker, your program will locate an available locker and create the rental transaction, charging $2 to the student account.
 Rental transaction should include the locker ID, student ID, start date and end date (default to None, until the rental is terminated).
 Your program should generate a unique Rental ID (running number) and display the rental details.
Below are demonstrations of a locker rental:
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage re代 写Diploma in Information TechnologyPython
代做程序编程语言port
0. Exit
Enter option: 1
Enter Student ID: 10255884
---------------------------------------------------------
Locker allocated: 10002 Location: Central store
Rental ID: 2400102
Start date: 14-Sep-2024
$2 is charge to your account.
---------------------------------------------------------
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option: 1
Enter Student ID: 10256499
Sorry, you are already renting 2 lockers.
---------------------------------------------------------
Locker allocated: 10003 Location: NTU-N31-04 (2-05)
Rental ID: 2400101
Start date: 10-Sep-2024
---------------------------------------------------------
Locker allocated: 10001 Location: Central store
Rental ID: 2400099
Start date: 15-Aug-2024
---------------------------------------------------------
b. Request move
To start moving a locker, the student ID and locker ID must be provided:
 Your program must validate both student ID and locker ID.
 If the IDs are valid, your program should display rented locker details.
 If not, display appropriate error message and return to menu.
 Prompt for the station code to move to.
 Create the move transaction record if,
 The station code is valid and is not same as current location.
 The destination has slots for this locker, hence displaying “Station
Code (Row-Column)” for this move. For example, “NTU-N31-04 (1-09)”
Below are demonstrations of a locker move:
++++ Go Locker – Operation ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option: 2
Enter Student ID: 10255884
Enter Locker ID: 10003
Sorry, 10003 is not your locker.
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option: 2
Enter Student ID: 10255884
Enter Locker ID: 10002
---------------------------------------------------------
Locker allocated: 10002 Location: Central store
Rental ID: 2400102
Start date: 14-Sep-2024
---------------------------------------------------------
Enter Station code to move to: NTU-N31-04
Locker is moving to NTU-N31-04 (1-09)
---------------------------------------------------------
Locker allocated: 10002 Location: In transit
Rental ID: 2400102
Start date: 14-Sep-2024
---------------------------------------------------------
c. Return locker
Student can return a locker by providing the student ID and locker ID:
 Your program must validate both student ID and locker ID.
 If the IDs are valid, your program should display rented locker details.
 If not, display appropriate error message and return to menu.
 Prompt for confirmation to return the locker.
 Closed the rental record by updating the end date to current date, update the locker status to “Available” and rental ID for this locker will be None.
 If the current location of the locker is at any station, system will initiate a locker move transaction to “Central store”.
 Your program should present a usage statement for this rental.
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option: 3
Enter Student ID: 10255884
Enter Locker ID: 10002
---------------------------------------------------------
Locker allocated: 10002 Location: NTU-N31-04 (1-09)
Rental ID: 2400102 Start date: 14-Sep-2024
End date: 10-Oct-2024
Moving locker back to Central store.
---------------------------------------------------------
Rental charge: $2.00
Move charges: $2.00 (10 moves)
Penalty charges: $2.00 (2 counts)
Total charges for this rental: $6.00
---------------------------------------------------------
d. Enquire locker location
To find out where the student’s lockers are, student need to provide their student ID.
 Your program should display appropriate error message if there is no student matching the student ID, or currently no rental record for this student.
 If the “active” rental record(s) is located, display the locker(s) details.
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option: 5
Enter Student ID: 10256379
No rental records
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option: 4
Enter Student ID: 10256499
---------------------------------------------------------
Locker allocated: 10003 Location: NTU-N31-04 (1-09)
Rental ID: 2400101
Start date: 10-Sep-2024
---------------------------------------------------------
Locker allocated: 10001 Location: Central store
Rental ID: 2400099
Start date: 15-Aug-2024
---------------------------------------------------------
e. View usage report
Student can view locker usage report by first providing the student ID:
 Your program should display appropriate error message if there is no student matching the student ID; or has no rental record for this student.
 If the rental record(s) is located, display the locker(s) details.
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option: 4
Enter Student ID: 10256379
No rental records
++++ Go Locker – Operations ++++
1. Rent a locker
2. Request move
3. Return locker
4. Enquire locker location
5. View usage report
0. Exit
Enter option: 4
Enter Student ID: 10256499
---------------------------------------------------------
Locker allocated: 10003 Location: NTU-N31-04 (1-09)
Rental ID: 2400101
Start date: 10-Sep-2024
---------------------------------------------------------
Locker allocated: 10001 Location: Central store
Rental ID: 2400099
Start date: 15-Aug-2024
---------------------------------------------------------
Locker allocated: 10006
Rental ID: 2400084
Start date: 10-Jul-2024
End date: 20-Sep-2024
---------------------------------------------------------
Enter Rental ID to view usage: 2400099
Date Time Operation Student ID
-------------------------------------------------------------
14-Sep-2024 09:11 Locker rental 10256499 14-Sep-2024 10:23 Move to NTU-S31-09 10256499
14-Sep-2024 10:45 Move to Central Store -
14-Sep-2024 14:55 Move to NTU-N21-11 10256499
14-Sep-2024 15:10 Move to Central Store -
18-Sep-2024 09:01 Move to NTU-S32-01 10256499
18-Sep-2024 09:08 Move to Central Store -
-------------------------------------------------------------
Rental charge: $2.00
Move charges: $0.60 (3 moves)
Total charges for this rental: $2.60
-------------------------------------------------------------
To show your ability in coding, your supervisor gave you the flexibility to design the structure and interface. Now, you shall apply what you have learnt in the school into practice.
More (BONUS) features for consideration:
You should explore problem solving techniques to design a solution to allow:
a. Dynamic, configurable setup of rental fees and moving fees. Aim is not to re-code and restart application for any changes to rental fees and moving fees.
b. Have a background program processing the locker move requests.
 When a student request for a locker moves, this transaction will be recorded and processed by your background program.
 The locker location will be updated accordingly after 3 min, simulating the movement of the locker vis the electric track delivery system.
 Hence, it will be “In transit”, follow by e.g., “NTU-N32-11” after 3 min.
 Locker move requests can also be initiated by the system, 30 min after the locker has arrived at a station. This is to manage space/slot, ensuring there are slots at each station to serve students.
Instructions for CA3 Report, Python Codes and User Guides
Cover Page
The cover page should include the institution name (and institution logo) the programme and the module name, the semester and year and date of submission. All these must be centralised in the page.
Write FULL Name and Student number as in the register on the cover. Students should a keep a copy of assignment submitted.
Python Codes
Suggested IDE and version: Wing Personal 7, Python 3.8.2 and above.
Please zip all your Python codes into single file and upload it together with the report. If you used any additional Python library apart from the standard package, you need to include them in the submission.
Referencing
No referencing is needed for program designs and codes.
Font and Spacing
Font: Times New Roman
Font size: 12 and 1.5 for line spacing.
Penalty Marks for Late Submission of Assignment
By one day: 20% to be deducted from total marks.
More than one day: submission will NOT be graded.
Plagiarism and Collusion
Students are not allowed to reuse old assignments or submit projects from previous semesters or copy from sources, particularly from the Internet web.
The submitted report must show evidence that this is students’ own work. No marks will be awarded if there are no workings or reasonable explanations. Please be reminded that plagiarism and collusion is a serious offence, and all cases will be referred to the administration. Grades will be withheld if the submission is suspected of plagiarism or collusion till investigations are completed.
Important Dates of CA3 Report
CA3 Group Assignment Deadline: 11 November 2024 11.59 am.
Submit ONE project via Canvas per group, submission must be completed for reports to be graded.
Lecturer Contact
You should contact your lecturer via your SIM email whenever you have any issue about your project.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
