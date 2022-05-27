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
