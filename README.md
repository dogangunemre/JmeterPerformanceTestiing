Performance Test What is it?
Performance testing is for detecting bottlenecks in the application, not bugs of software applications. It measures the performance quality of the application. Basically, a software; It focuses on certain features such as speed, stability and scalability.

Our first step is to download JMeter. You can download it from this address. https://jmeter.apache.org/download_jmeter.cgi

Extract the downloaded zip to the folder and unzip the bin file and click Jmeter to open it.


Right click on existing Test Plan and create a Thread Group.


In this section we will make some configs.


Number of Threads (users): The number of users connecting to the target server.
Ramp-up period (seconds): The time it takes for all users to log into the system and end the test.
Loop Count: Defines how many times the test will be run.
In the above part; It is seen that with 10 users, 10 requests will be sent to the server every second and each user will enter the system 10 times.


If we choose Infinite, it means that it will send requests to the system until we stop the test. That way the tests are more realistic.

Let’s continue by creating HTTP Request Default.


In this section, we give my swagger address. Let’s test the post method in https://petstore.swagger.io/v2/pet.



In the next step, we create the HTTP Request.


We write the Request ,Path and HTTP method here.


In the next step, we create the HTTP Header Manager.


We can click the Add button and then write the headers.


Request is now ready. When we run it, we need a listener that has the quality of a report. You can add whatever you want in the Listener section.


View Results Tree in this way you can examine the request and response.


View Results in Table this way you can view times and sizes.


Aggregate Graph is like this, you can use the values here if you want to keep a report. Average,Median,max,min etc. is located here.


You can generate random values for requests from Random Variables.


If we want to create a random id, we need to separate it between 00001 and 99999 like this.


If we want a string value, it is sufficient to write the Output Format in quotation marks.

Its usage and output is like this.



When we want to read data from a file, it is sufficient to add Data Set Config.


This is how it is set up and used. It is sufficient to separate the csv file with a comma.



To add static values, we just need to add User Defined Variables.

