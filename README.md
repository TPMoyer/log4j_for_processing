# log4j_for_processing
log4j library for processing

Logging is a debugging tactic, and is a more generic alternative to the application specific, set-point centric debuggers provided with IDE's.   Logging is essentially pushing state descriptors to a file, instead of to the console.   Combined with a good editor, substantial output can be quickly output and sifted through to observe patterns in how a program is dealing with it's state of being.  
Logging in iterative applications like Processing can trigger logger output by using conditional statements to avoid output-on-every-draw.    framecount is a useful variable for this.  Alternately a programmer can set up boolean conditions triggered by user action, or key off of time boundries.             

ported the apache.org log4j to processing by
pulling the most recent version the mavin repository https://mvnrepository.com/artifact/log4j/log4j  
The 1.2.17 has been the most recent version sence may 2012

Processing has requirements on naming for it's libraries which the default maven output did not abide.
Putting
```
  <!-- https://mvnrepository.com/artifact/log4j/log4j -->
  <dependency>
      <groupId>log4j</groupId>
      <artifactId>log4j</artifactId>
      <version>1.2.17</version>
  </dependency>
```  
into the pom.xml file of an eclipse IDE project pulled in  
C:\Users\TPMoyer\.m2\repository\log4j\log4j\1.2.17\log4j-1.2.17.jar

I simply renamed this to log4j_1_2_17.jar and framed it into the directory structure required by processing.

Thanks are expressed to Jake Seigel for having been the pathfinder:   https://jestermax.wordpress.com/2014/06/09/log4j-4-you/

This library has been confirmed functional on a 3x2 matrix of 3 OS's (Windows 10, Raspbian 32bit arm , and Raspberry Pi 64Bit) and two Processing versions (3.4 and 4.08)

Examples: All the examples are written as log4j code added to one of the core Processing examples: 
      Basics/Data/CharacterStrings  
The log4j code initialization is called, which outputs some initial "this is the kind of things you can get" lines.
A boolean flag then prevents output for every draw, until you hit a key.  
Then it logs the keystroke you hit while focus is on the sketch execution dialog.       

Log4J_A_Minimal      writes always_Same_Name.log     to the sketch source directory.   
Log4J_Log_Directory  writes Log4J_Log_Directory.log  to  c:/logs   on windows OS and  a /home/pi/logs directory on non-windows OS
Log4J_DateLog_Directory writes a log file to those same directories, with an ISO 8601 date as the first part of the .log file name
Log4J_Log2_Directory   writes two files with identical content to that same directory, one with, one without the date 
Log4J_Log3post4_Directory writes Log4J_Log3post4_Directory.log in that same directory, and waits until you have typed your 5'th character to open
a second log file: Log4J_Log3post4_Directory.log 



