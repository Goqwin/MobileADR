# MobileADR - Assignment
## Scenario 2
### Anton Koulikov, Godwin Mercado

### Overview

This README outlines the technology stack and key decisions made by Anton K. and Godwin M. (The Development Duo) responsible for building a social networking mobile app for a university. (Scenario 2).

The key points of the app's design were focused on connecting students and professors, allowing students to share information across fellow students with class-related content and managing their schedules, while also keeping in mind with Professors and their abilities to host announcements and update grades. This app was with the intent of being a hybrid app and therefore we have considered the following requirements in making our decisions:

- **Cross-Platform Support**: The app should be available on both iOS and Android platforms.
- **Offline Support**: Users should be able to access certain features and data even when offline, with data synchronization mechanisms.
- **Performance Optimization**: The app should be optimized for various smartphone specifications and minimize data usage.
- **Integration with Active Directory**: The app should securely integrate with the university's Active Directory system for user authentication and permissions.
- **Push Notifications**: The app should integrate with a push notification service supporting both iOS and Android.
- **Data Privacy and Security**: Strong data encryption and secure transmission protocols should be implemented to protect sensitive user information.
- **Accessibility Features**: The app should be designed with accessibility features, including text-to-speech and support for assistive technologies.

### Summary of our Tech Stacks

**Technology Stack**

- **Hybrid App Development**: We have chosen to develop a hybrid mobile app to efficiently support both iOS and Android platforms with a single codebase. This decision was made to save development time and resources.

- **React Native UI Framework**: For the app's user interface, we have opted for the React Native framework. React Native allows us to build a native-like user experience while reusing a significant portion of the codebase across platforms. It's a popular choice for hybrid mobile app development.

- **AWS for Hosting**: To ensure scalability and reliability, we will host the app on Amazon Web Services (AWS). AWS provides a robust infrastructure that can accommodate the app's potential growth and high demand.

- **Java for Backend**: We have chosen Java as the backend programming language. Java offers excellent performance, security, and scalability for handling user data, notifications, and integrations with other systems.

- **PostgreSQL for Database**: PostgreSQL is selected as the database management system due to its reliability, data integrity, and scalability. It will securely store and manage user data, including grades, profiles, and app content.

- **Role-Based Access Control (RBAC) for Permissions**: To implement secure access control and permissions, we will utilize a Role-Based Access Control (RBAC) system. This ensures that students and professors have appropriate roles and permissions enforced when using the app.

**Additional Considerations**

- **Offline Capabilities**: For offline support, we will implement data synchronization mechanisms using technologies like Redux Offline or React Native's AsyncStorage. This allows users to access essential features and data even without an internet connection.

- **Push Notification Provider**: We will choose a suitable push notification provider, such as Firebase Cloud Messaging (FCM) or Amazon Simple Notification Service (SNS), to ensure that users receive timely updates and notifications on both iOS and Android platforms.

- **Data Privacy and Security**: Our team will implement strong encryption, secure data transmission protocols (e.g., HTTPS), and adhere to relevant data protection regulations (e.g., GDPR) to safeguard user data and privacy.

- **Accessibility Features**: In line with accessibility guidelines, we will design and develop the app with features like text-to-speech, high contrast modes, and support for assistive technologies to ensure inclusivity and usability for all users.