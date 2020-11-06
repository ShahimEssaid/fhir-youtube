* This is a copy of this repository: https://github.com/hapifhir/hapi-fhir-jpaserver-starter
  * It was copied on 11/5/2020 at commit e05d950
* It is copied here to simplify standing up a HAPI FHIR server locally for demo purposes
* You need to have Maven installed.
  * Download and install from: http://maven.apache.org/index.html
* `cd` to the root directory and run `mvn jetty:run`
  * See the original README.md for additional details
  * Running `mvn jetty:run` will start the server AND reuse the same database from the previous run, i.e. it will have any resources from that database
  * To start the server with a clean database run `mvn clean jetty:run`
