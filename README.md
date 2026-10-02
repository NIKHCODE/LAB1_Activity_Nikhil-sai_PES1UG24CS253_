Lab 1 — Requirements Engineering & UML Use-Case Modelling
Course: Software Engineering
Lab: Lab 1
Problem Statement: #08 — Campus & Academic Operations
System: Digital Campus Library Reservation Gateway  
Overview
This repository contains the deliverables for Lab 1 on Requirements Engineering and UML Use-Case Modelling.
The system scenario focuses on a digital university library gateway that supports:
- Searching the physical ISBN catalog
- Managing hold requests and FIFO waitlists
- Providing hold notifications
- Managing book availability
- Tracking overdue fine transactions
Deliverables
File	Description
8_SE_Lab1_SE_Problem_Statements.pdf	Provided problem statement for the lab
Requirement_table.pdf	Requirements table containing 5 Functional Requirements and 2 Non-Functional Requirements
Uml.drawio.pdf	UML Use-Case Diagram for the Digital Campus Library Reservation Gateway
Architectural_diagram/Digital_Campus_Library_Architecture.png	System architecture diagram showing the layered architecture and major system components


Requirements
The requirements table contains:
- FR-001 to FR-005 — Functional Requirements
- NFR-001 to NFR-002 — Non-Functional Requirements
- Requirement ID
- Type
- Description
- Priority
- Acceptance Criteria
- Rationale
UML Use-Case Model
The UML diagram models the interaction between the system and its actors, including:
- Student Member
- Head Librarian
- Payment Gateway
The diagram includes the required «include» and «extend» relationships between use cases.
System Architecture
The architecture diagram represents the Digital Campus Library Reservation Gateway using a layered architecture.
The architecture consists of:
- Presentation Layer — Provides the web/mobile interface through which students and librarians interact with the system.
- Application Layer — Contains the API Gateway and core services such as Catalog Search, Reservation/Hold Queue, Notification, Loan & Return, and Fine Management.
- Data Layer — Stores catalog information, library records, loan/return transactions, fine transactions, and reservation queue data.
- External Services — Supports external email/SMS services for sending notifications to library members.
Architecture Method
A Layered Architecture was selected to separate the user interface, application/business logic, and data management responsibilities. The API Gateway acts as the entry point between the presentation layer and application services.
The reservation service manages FIFO hold queues, while the catalog service handles ISBN-based searching. Separate services are used for notifications, loan/return operations, and fine management.
Why This Architecture?
This architecture was chosen because it provides:
- Modularity — Each major library operation is handled by a dedicated service.
- Maintainability — Changes to one layer or service can be made with minimal impact on other components.
- Scalability — Services such as catalog search can be optimized independently for large numbers of titles.
- Security — Authentication and authorization can be handled through the API Gateway.
- Clear separation of responsibilities — Presentation, application logic, and data storage are kept separate.
- Requirement alignment — The architecture directly supports catalog search, FIFO reservation queues, automated notifications, book availability, and overdue fine management.
