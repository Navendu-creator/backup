# ADSFanoutAutomation_Java
Whatever comes to ADS, has to be 'fanned out' to downstream services- FBMS, Charset Service & SFDMS.
This automation suite - collects all MD5s from certain duration (1 day currently) and then checks all these MD5s in the 3 services mentioned above.
There is a file - missingMd5List.txt that will keep missing data from any of the 3 services.
There is a jenkins job : http://noi-qa-jenkins:8080/job/ADS-Fanout-prod/ that runs daily for this suite.

The test suite is best viewed with IntelliJ as a Maven project.
The expectation for the suite to run is that : 
1. Maven and Java are present on the system
2. Maven and Java are in the PATH environment variable.

To run the tests from a command shell (cmd/terminal), call 
`mvn test -Dsurefire.suiteXmlFiles=testng.xml`
from the directory with the file "pom.xml".

## IntelliJ
### Editing Project Folders in IntelliJ
Viewing all project files in IntelliJ
Click file
Open
Click one of many projects
Right click pom.xml
Hover Maven and click Add as maven project
Hover Maven and click Download source and documentation
Hover Maven and click Reimport

### Running tests through IntelliJ
Setting up to run tests
Click on Edit Configurations
Click +
Select TestNG
Select >= 1.7 in JRE
Apply
## Running tests
Ways to run the test :
Right click and click run on CheckADSFanout method with @Test
