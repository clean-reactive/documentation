# Architecture

The Clean Reactive Architecture is based on the 
[Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
concept. The architecture can be outlined with the following UML diagram:

<uml-image/>

### Definition of units

- **Entities**: A unit that maintains one or more enterprise business
  entities, application business entities, or a mix of both.
- **Use Case Interactor**: A unit that orchestrates the flow of data to the
  entities, and directs those entities to use their business rules to achieve
  the goals of the use case.
- **Gateway**: A unit that encapsulates access to an external system or
  resource.
- **Controller**: A unit that handles input data from the user interface and
  converts it into a format most convenient for the use cases and
  entities.
- **Presenter**: A unit that converts data from entities into a format most
  convenient for the user interface.
- **User Interface**: A unit that displays information to the user based on the
  data prepared by the presenter, and captures user input and transfers it to
  the controller.
- **External system or resource**: A unit that represents external systems or
  services the application interacts with, databases, storage, or other
  applications or libraries with an API.

### Definition of concepts utilized by the units

- **Enterprise Business Entity**: An entity that encapsulates enterprise
  business rules and data.
- **Enterprise Business Rules and Data**: The most general and high-level
  rules and data that would exist even if the application didn't. These are
  enterprise-wide rules that rarely change and are independent of any specific
  application.
- **Application Business Entity**: An entity that encapsulates
  application-specific business rules and data.
- **Application Business Rules and Data**: Rules and data specific to the
  application's functionality. These are application-wide rules that don't
  exist outside the context of a particular application.
- **State**: The data of entities at a given point in time, typically
  represented as an object structure.
- **Valid State**: One of a finite number of states considered valid according
  to the enterprise and application business rules.
