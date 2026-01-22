
# Stock Management System

## Authors

- [@MarceloDanielToledo](https://github.com/MarceloDanielToledo)

## Context

Currently, the product factory faces significant limitations due to its outdated stock management system. This system is not only rigid and difficult to adapt but also operates solely on an old version of Windows and does not integrate well with the factory's current processes. These deficiencies are causing inefficiencies in inventory management, such as frequent stockouts, excess inventory, and limited visibility of material flow, which negatively impacts daily operations and increases costs.

It is necessary to implement a new stock management system that addresses the current and future needs of the factory. This system must be flexible and cross-platform, accessible from any device with a web browser. It will provide real-time data, seamless integrations with other systems, and the ability to customize functions according to the specific needs of the factory, thereby facilitating better decision-making.

This system will benefit production managers, warehouse staff, and the purchasing team by providing them with a more modern and efficient tool that will support the factory's growth and evolution.

## Goals

- Improve accessibility and flexibility: Facilitate access to the system from any device with a web browser.

- Integrate with other systems: Ensure seamless synchronization with the purchasing module and other existing systems.

- Facilitate decision-making: Provide reports and predictive analytics for better planning.

- Optimize management metrics: Improve response times and operational efficiency in inventory management.

## Non-Goals

- No functionalities will be developed outside the scope of stock management.

- The system will not address the upgrade or replacement of existing hardware in the factory, focusing solely on stock management software.

- No additional features unrelated to stock management will be created, such as new functionalities for other departments or processes not defined in the scope.

- Training will be limited to basic user training for the new system; extensive training programs or support for other business processes will not be included.

## Milestones

**Requirement Definition** - 08/30/24

- Meeting to define and agree on system requirements with the client.

**Design and Prototype** - 09/15/24

- Presentation of the initial design and prototype to obtain client feedback.

**Development of Key Features** - 10/15/24

- Delivery of the main system functionalities.

**Integration and Testing** - 11/15/24

- System integration with other modules and testing. Meeting to review the results with the client.

**Deployment and Training** - 12/01/24

- System implementation and basic user training.

**Final Review and Adjustments** - 12/15/24

- Final review with the client to make adjustments based on feedback.


## Existing Solution

The factory currently uses a stock management system developed in FoxPro. This outdated system is limited in terms of functionality and flexibility, making it difficult to adapt to the modern needs of the factory. Users interact with the system through a graphical interface that allows basic operations such as recording inventory entries and exits, generating reports, and viewing stock status.

However, the system has several deficiencies, including limited integration with other factory processes, lack of support for updates and customizations, and compatibility issues with newer operating system versions. This situation has led to inefficient inventory management and an increasing need for a more modern and adaptable solution.


## Proposed Solution

The proposed solution for the new stock management system is a web application based on Blazor WebAssembly. This choice allows for a modern and flexible platform, accessible from any device with a web browser.

### Overview

The system will be a Blazor WebAssembly application using SignalR. This enables a rich and dynamic user experience with a modern interface that facilitates real-time inventory management. The application will connect to a backend API to handle all operations related to inventory data.

### System Architecture

- **User Interface (UI)**: The web application will be developed using Blazor WebAssembly, allowing for a smooth and responsive interface. Users will be able to access the system from any device with a browser, whether on a desktop computer, tablet, or mobile phone.

- **Backend API**: The application will connect to a RESTful API that will handle all system operations, including inventory management, report generation, and synchronization with other factory modules. This API will be built with .NET, providing robustness and scalability.

- **Database**: Inventory information will be stored in a centralized database, enabling efficient queries and secure data storage. The database will be designed to easily integrate with the API and support system operations.

- **Authentication and Security**: The application will include authentication and authorization mechanisms to ensure that only authorized users can access and modify inventory data. Security measures will be implemented to protect the integrity and confidentiality of the data.


### Workflow

- **Login**: Users access the system through a secure login page. Once authenticated, they are directed to the main page where they can view and manage inventory.
- **Inventory Management**: Users can record new inventory entries and exits, adjust stock levels, and generate reports. The interface will provide a clear and up-to-date view of inventory levels and alerts about potential issues.
- **Report Generation**: The system will allow the generation of detailed reports on inventory status, including movement history and trend analysis. Reports can be exported in various formats for review and analysis.
- **Synchronization with Other Systems**: The application will be integrated with other factory modules, such as the purchasing system, to ensure that inventory data is always up-to-date and synchronized.


## Alternative Solutions

### Third-Party Solution

We considered the option of acquiring a stock management system from an external provider. These solutions often offer advanced functionalities and ongoing support. Examples include systems like SAP Business One or NetSuite.

**Pros**:

- Faster implementation due to the immediate availability of the software.
- Continuous support and updates provided by the vendor.
- Proven and reliable functionalities.

**Cons**:

- High cost for licensing and subscription.
- Less flexibility to customize according to the specific needs of the factory.
- May require complex integration with existing systems.


### Open Source Solution

We evaluated the use of open-source inventory management solutions, such as Odoo or ERPNext. These platforms offer a robust foundation that can be adapted and extended according to needs.

**Pros**:

- Reduced or zero initial costs.
- Flexibility to customize and adapt the software.
- Active community that can provide support and improvements.

**Cons**:

- Requires technical knowledge for customization and maintenance.
- Limited support compared to commercial solutions.
- Possible need for additional development to integrate with other systems.

### Internal Development

Developing a custom internal solution, such as the proposed Blazor WebAssembly application, tailored to the specific needs of the factory.

**Pros**:

- Complete alignment with the factory’s requirements and processes.
- Flexibility to modify and scale the system as needed.
- Full control over design and functionalities.

**Cons**:

- Longer development time.
- Requires internal resources for development and maintenance.
- Higher initial investment compared to pre-existing solutions.


## Testability, Monitoring and Alerting

**Testing**

The solution will undergo unit, integration, and end-to-end (E2E) testing to ensure proper functionality before deployment. This will include usability testing to verify that users can interact with the system smoothly, and integration testing to ensure all functions operate correctly with other systems. Performance testing will also be conducted to ensure the system handles the expected data volume without delays.

**Monitoring**

Once implemented, the system will be continuously monitored to ensure stability and performance. Monitoring tools will be used to oversee system status, resource usage, and response times. This will help detect and resolve issues before they impact users.

**Alerts**

Automatic alerts will be set up to notify the support team of any anomalies or failures in the system, such as performance issues, critical errors, or system outages. Alerts will help respond quickly to any incidents and minimize impact on factory operations.


## Cross-Team Impact

**Impact on Support and Operations:**
The new system will require more attention from the operations team initially, as it will be crucial to ensure everything functions correctly during the transition. However, once the system is up and running, the number of issues should be lower compared to the old system.

**Cost:**
Creating and implementing the new system will incur costs, especially initially. However, in the long run, it should save money because it will be easier to manage and will keep inventory better controlled.

**System Speed:**
As a web application, the new system might perform slightly slower in areas with poor internet connectivity. Still, it is designed to ensure that this difference is not too noticeable.

**Security:**
Being a web application, it may be exposed to new security risks, such as unauthorized access attempts. Therefore, measures will be taken to ensure data protection and that only authorized personnel can access it.

**Possible Drawbacks:**
Users might need time to get used to the new system, which could cause some initial inconvenience. Additionally, during the transition, some temporary issues in operations might arise if not planned properly.

**Communication with Clients:**
The support team will need to clearly explain to clients why the change is being made and how it will benefit them. It will also be important to provide assistance and training to make the transition as smooth as possible.


## Open Question

**Integration with Existing Systems**

What level of compatibility is required with the factory’s current systems? Should we consider a complete migration or a gradual integration?

**User Training**

What is the best way to train users on the new system? Are online tutorials sufficient, or will in-person training be necessary?

**Future Scalability**

How should we plan for the system’s scalability for future factory expansions? Are there critical areas that require more attention from the beginning?

**Customization Options**

To what extent should the system be customizable to adapt to changes in the factory’s processes? Is it better to offer a basic set of options or allow for more extensive customization?

**Historical Data Management**

How will we handle the transition of historical data from the old system to the new one? Is it necessary to import all data or only those relevant to current operations?


## Detailed Scoping and Timeline

### Detailed Scope:

**Phase 1: Requirements Analysis and Planning (Date: 1st week)**

- Meetings with stakeholders to define specific system requirements.
- Preparation of the final requirements document.

**Phase 2: System Design (Date: 2nd-3rd week)**

- Design of the system architecture, including data flows and database structure.
- Creation of mockups for the user interface.

**Phase 3: Initial Development (Date: 4th-8th week)**

- Implementation of the basic system structure.
- Development of critical functionalities, such as inventory management and stock tracking.

**Phase 4: Integration and Testing (Date: 9th-11th week)**

- Integration with existing systems.
- Conducting unit and integration tests to ensure system quality.

**Phase 5: Pilot Implementation (Date: 12th week)**

- Initial deployment in a controlled environment.
- Collection of feedback and adjustments based on user experience.

**Phase 6: Full Deployment and Training (Date: 13th-14th week)**

- Deployment of the system throughout the factory.
- Training of end-users to ensure a smooth transition.
