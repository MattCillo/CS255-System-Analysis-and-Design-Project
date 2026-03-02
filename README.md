# CS255-System-Analysis-and-Design-Project
CS255 System Analysis and Design


Briefly summarize the DriverPass project. Who was the client? What type of system did they want you to design?

The client was DriverPass, a driving school business. They required a centralized, cloud-based driver education management system to address a problem where approximately 65% of students fail their licensing exams due to a lack of proper training. The system was designed to facilitate a hybrid learning environment, combining online practice tests with a scheduling platform for in-car driving lessons. It needed to handle package management (6, 8, and 12-hour options), automated scheduling to prevent double-booking of cars and drivers, and role-based access for students, instructors, secretaries, the IT officer, and the owner.


What did you do particularly well?

I effectively mapped the complex interactions between different user roles and the system using UML diagrams. The sequence and activity diagrams clearly outlined the logic required for asynchronous tasks, such as modifying appointments and sending notifications to instructors via a Notification Service without making the student wait for real-time acceptance. Additionally, the nonfunctional requirements were well-defined, specifically detailing the need for cloud infrastructure, strict role-based access control (RBAC), and secure handling of Personally Identifiable Information (PII) using TLS and AES-256 encryption.


If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?

I would revise the system's adaptability limitations regarding package management. Currently, the design restricts the owner from dynamically creating new packages without developer assistance, meaning packages must be hard-coded or developer-managed. I would improve the class diagram and backend architecture to include a dynamic package creation module. This would allow administrators to define custom hour blocks and pricing through the user interface, improving long-term adaptability.


How did you interpret the user’s needs and implement them into your system design? Why is it so important to consider the user’s needs when designing?

I interpreted the users' needs by segmenting the interface requirements based on their distinct operational roles. For instance, the student dashboard was designed as a self-service hub featuring an online test progress widget and driver notes, while the secretary view focused on scheduling support, and the owner view centered on generating Excel-compatible reports. Considering user needs is critical because a system that fails to align with the end-users' daily workflows such as the requirement for mobile responsiveness for students versus desktop monitor optimization for office staff will suffer from low adoption and fail to solve the underlying business problem.


How do you approach designing software? What techniques or strategies would you use in the future to analyze and design a system?

My approach begins with a thorough requirements gathering phase to establish both functional and nonfunctional needs before any technical architecture is drafted. In the future, I will continue utilizing object-oriented design principles and UML modeling (Use Case, Class, Activity, and Sequence diagrams) to visualize system components, state changes, and data flow.  I will also prioritize building cloud-native, modular architectures to ensure scalability and ease of integration with external APIs, similar to the external DMV System integration planned for DriverPass to receive regulatory updates.
