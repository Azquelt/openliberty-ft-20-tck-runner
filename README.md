This is a project to run the Microprofile Fault Tolerance 2.0 TCK against OpenLiberty

Adapted from the OpenLiberty integration tests at https://github.com/OpenLiberty/open-liberty/

##How to use

* Clone this project
* Extract a developer build of openliberty into the root of the project
* Run `mvn test`

##Configuration

To change which tests are run, edit the tck-suite.xml file.

To change the arquillian container parameters (app deploy timeouts etc.), edit src/test/resources/arquillian.xml.

To run against a different version of the TCK (e.g. a locally built snapshot) edit the pom.xml.

##Known issues

Due to OpenLiberty/liberty-arquillian#36, repeated application deployment exceptions in the same server are not always reported correctly. Some tests have been excluded from the tck-suite.xml due to this.