# Using a PostgreSQL Database for Data Management and Security of an Educational Platform

## Status

**Status:** Accepted

## Content

- The need for **structured data** when coming to terms with the different types of user profiles that exist, courses, messages, and announcements. Other elements include assignments and grades.
- **Data security** and privacy highlighting the demand for safe-keeping sensitive information, encryption, and role-based access control (Active Directory), including making HTTP requests and other secure transmission protocols.
- The **multiplatform capabilities** regarding whether on Android or iOS are something that is valued and considered.

All of this is expected for the development of a social networking mobile app for a university.

## Decision
**Reasoning**

- **PostgreSQL** maintains data consistency; it has the ability to support **ACID Transactions**[^1^], ensuring the highest possible data reliability and integrity in cases of emergencies. It also executes changes in a manner that doesn't create conflicts and corruption, preventing complexity, incorrect views of data, and the rework/reprocessing needed after a pipeline break.
  
- **PostgreSQL and its scalability:** PostgreSQL has the ability to partition tables or cluster tables, which are good for handling increased data loads. This can be related to when more students enroll in the university or when classes are overbooked.

- **PostgreSQL and Security:** It offers features such as encryption, role-based access control, and SSL/TLS support. This addresses the requirement for data privacy and security along with the active directory and roles. An example could include the student's grade. You can use PostgreSQL's ability to encrypt data as a way to make it more challenging for unauthorized individuals to tamper with or access this sensitive data.
  - In addition to security, we have **Role-Based Access Control (RBAC)**; PostgreSQL allows you to define roles and assign specific permissions to those roles. This addresses the perfectly aligned scenario requirement to integrate with an existing Active Directory and enforce user roles and permissions effectively. An example would be Students and Professors. You can create corresponding roles in PostgreSQL for these roles and assign appropriate permissions. Professors, for this instance, may have the permission to post announcements and assignments (as it is aligned with the relationship within the database), while students may not.

- **PostgreSQL's popularity and community support:** There is a lot of documentation and support that gives information regarding the extensions that can enhance database functionality and address specific needs.

- **Java Integration:** Since the backend integration is accepted, you can use PostgreSQL and Java to work together through JDBC, which allows a smoother interaction between the Java backend and the PostgreSQL database.

- **Relational Structure/JSONB Support:** The structured data, encompassing elements like user profiles, courses, messages, announcements, assignments, grades, and more, can be effectively organized within a well-structured database, taking full advantage of its robust relational capabilities. Additionally, it's important to consider the presence of semi-structured or somewhat flexible data that PostgreSQL can handle, such as user-generated content.

## Conclusion

In conclusion, the decision to use PostgreSQL as the database for the university social networking mobile app is highly justified and aligns effectively with the business requirements and user needs outlined in the scenario. PostgreSQL's support for ACID transactions ensures the highest level of data reliability and integrity, instilling trust and accuracy in handling sensitive information like student grades.

The database's scalability options, including partitioning and clustering capabilities, cater to the potential growth in the user base, allowing the app to accommodate more students and courses without compromising performance. Robust security features, such as encryption, RBAC, and SSL/TLS support, protect sensitive data and meet stringent data privacy and security requirements.

The integration with Active Directory simplifies user authentication and role enforcement, providing a seamless and secure user experience while leveraging existing user management systems. The strong community support and extensive documentation surrounding PostgreSQL offer valuable resources and extensions that enhance database functionality and efficiently meet specific needs.

Additionally, seamless integration with Java through JDBC optimizes performance and development efficiency. PostgreSQL's support for structured and semi-structured data effectively organizes and manages diverse data types, meeting the app's data storage requirements.

Overall, PostgreSQL provides a secure, scalable, and efficient data management solution that fulfills the app's goals and objectives, ensuring a reliable and user-friendly experience for all stakeholders involved.

**Notes:**

[^1^]: **What is ACID?**
  - Atomicity: An all or none approach in terms of execution of a singular unit of work (READ, WRITE, UPDATE, DELETE) of data.
  - Consistency: Ensures that transactions only make changes to tables in predefined and predictable ways.
  - Isolation: The ability to ensure that transactions of multiple users do not impact the transactions of another user. Each simultaneous transaction is executed one by one.
  - Durability: Ensures that the changes made to the data made by successfully executed transactions will be saved, even in the event of a system failure.

**Principles of a Good Database System:**
This is outside knowledge but when designing a database system the main 3 principles are as follows:
  - Maintainability
  - Reliability
  - Scalability
These principles were heavily considered when selecting which database language we'd use when addressing this scenario. 