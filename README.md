# Vehicle-managment

Behaviour-driven developed (BDD) CLI and GUI application for registering vehicles and owners
for Vehicle Testing New Zealand (VTNZ) Warrant of Fitness (WoF) test appointments.

Developed with a local SQLite database in limited time for infinite good reasons.
GUI is included later when migrating from Java 8 to 16 given automated
[user-story acceptance](./doc/UserStoryAcceptanceCriteria.pdf) 
[testing with Cucumber and Gherkin](./features/) 
is being assessed, with all test cases passing.

![gui](https://github.com/user-attachments/assets/3b7c5354-966c-49d0-80dd-dd3d0cc55081)

A user of the vehicle  registration app can:
- register, login, logout, edit and remove a user account
- register, edit, and remove their vehicle(s) from a user account
- edit history for a vehicle registration

There are two existing vehicle owner registrations in the DB sample:

```
email: one@test.com
password: one
```

```
email: two@test.com
password: two
```

## Instructions

### Requirements

- Java 16
- Maven

### Test

Navigate to `VehicleRegistration/` containing the `pom.xml` file, then execute in a terminal:

###### Acceptance testing:

Run 35 acceptance tests by executing:

```
mvn clean -Dtest=GenericTestRunner test
```

###### Junit testing:

Run 61 unit tests by executing:

```
mvn clean test
```

### Build

To package to a `.jar` file, navigate to `VehicleRegistration/` containing the `pom.xml` file and execute:

```
mvn clean compile assembly:single
```

Following a successful maven build of the project,
move `WoF-1.0-jar-with-dependencies.jar` to the `VehicleRegistration/`
root directory, so it is with the DB files.

### Run

###### CLI

```
java -jar WoF-1.0-jar-with-dependencies.jar
```

###### GUI

```
java -jar WoF-1.0-jar-with-dependencies.jar gui
```
