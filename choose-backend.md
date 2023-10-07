# ADR (Architecture Decision Record): Using Java for Backend Infrastructures and Interconnectivity

## Status

**Status:** Accepted

## Content

The development of a university social networking mobile app requires careful consideration of various factors, including user authentication, data storage and retrieval, offline capabilities, push notifications, data security, and accessibility/API features. The decision to use Java as the backend language addresses these requirements effectively.

Important Highlights:

- Distinction between classes: The app differentiates between students and professors, with each having specific functionalities and requirements. Professors handle announcements, assignments, and grades, while students focus on connecting with peers, managing schedules, and accessing events and clubs.
- Data security: The app's handling of sensitive information necessitates robust security measures, including encryption algorithms and secure data management to ensure data privacy and security.

## Decision 
**Reasoning** 

- **Cross-platform compatibility:** Java's ability to be compiled on any platform with a Java Virtual Machine (JVM) makes it suitable for both Android and iOS development. This ensures widespread adoption and accessibility for users on various devices.
- **Robust security and libraries:** Java offers robust security features and libraries for implementing encryption algorithms and middleware interactions, such as HTTP requests and user control. This allows for the secure handling of sensitive data and efficient integration with existing security systems.
- **Object-Oriented Programming (OOP) principles:** Java's foundation in OOP principles facilitates code reusability, scalable software design, and streamlined maintenance. This enables versatile functionality and extensibility for different user types and future applications.
- **Accessibility to features:** Java provides easy accessibility to various features, such as push notifications using Firebase or integration with AWS. This ensures timely updates and notifications for users.
- **Networking capabilities:** Java has built-in networking capabilities, making it well-suited for handling interconnectivity between devices. This enables seamless data synchronization in offline mode and enhances the app's overall performance.

## Constraints

- **JVM Implementation:** It is necessary to implement Java Virtual Machine (JVM) on all systems that will be using this app.
- **Limited Frontend Development:** Java is primarily for back-end development, so other frontend technologies will be required depending on the complexity of the UI.
- **Research for Libraries:** Additional research is needed to find and implement the appropriate libraries to meet other functionalities.

## Conclusion

Despite some limitations, Java is an excellent choice for the backend infrastructure of the university social networking mobile app. It effectively addresses requirements for cross-platform compatibility, robust security, scalability, maintainability, and interconnectivity. The ability to compile Java on different platforms ensures accessibility for both Android and iOS users. Java's security features and libraries enable the implementation of encryption algorithms and seamless integration with existing security systems. Its adherence to OOP principles promotes code reusability, scalability, and extensibility. The networking capabilities of Java facilitate offline data synchronization and enhance the app's performance.

Additionally, Java offers various APIs and GUI options, such as Text-to-Speech (TTS) capabilities through open source libraries like Java.FreeTTS and Java.MaryTTS. It also supports UI customization with Java Swing for switching between light and dark modes.

In conclusion, Java provides a comprehensive solution for building a reliable, secure, and feature-rich backend infrastructure for the university social networking mobile app.

---

**References:**

- [Java.FreeTTS](https://freetts.sourceforge.io/docs/index.php)
- [Java.MaryTTS](https://marytts.github.io/)
- [Java Swing](https://docs.oracle.com/javase/8/docs/technotes/guides/swing/)
