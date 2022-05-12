# log4j_for_processing
log4j library for processing

ported the apache.org log4j to processing by
pulling the most recent version the mavin repository https://mvnrepository.com/artifact/log4j/log4j
The 1.2.17 has been the most recent version sence may 2012

Processing has requirements on naming for it's libraries which the default maven output did not abide.
Putting 
  <!-- https://mvnrepository.com/artifact/log4j/log4j -->
  <dependency>
      <groupId>log4j</groupId>
      <artifactId>log4j</artifactId>
      <version>1.2.17</version>
  </dependency>
into the pom.xml file of an eclipse IDE project pulled in
C:\Users\TPMoyer\.m2\repository\log4j\log4j\1.2.17\log4j-1.2.17.jar

I simply renamed this to log4j_1_2_17.jar and framed it into the directory structure required by processing.

Thanks are expressed to Jake Seigel for having been the pathfinder:   https://jestermax.wordpress.com/2014/06/09/log4j-4-you/
