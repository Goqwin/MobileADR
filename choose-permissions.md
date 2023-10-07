# Using a Role-Based Access Control for Permissions of an Educational Platform

## Status

**Status:** Accepted

## Content
There are numerous considerations when developing a social networking mobile app for a university. These requirements come in the form of: Allowing students to connect, share information, and manage their schedules. While for Professors there are features such as posting announcements, assignments, and grades. Therefore, this demands ensuring proper access control and permissions are heavily critical in terms of consideration.

## Decision
**Reasoning** 

We will implement a Role-Based Access Control (RBAC) system to manage permissions and access control. RBAC provides a flexible and scalable way to define roles and associate them with specific permissions.

### Roles

- **Student**: Students have access to features such as connecting with peers, viewing class information, and managing their schedules.
- **Professor**: Professors can post announcements, assignments, and grades in addition to accessing student features.
- **Admin**: Administrators have full control over app settings, user management, and content moderation.

**Permissions**

We will define granular permissions associated with each role to ensure fine-grained control over app functionality. For example:

- Students can view class schedules and join clubs.
- Professors can post announcements and manage their classes.
- Admins have full access to user management and content moderation.

**Integration with Active Directory**

To enforce user roles and permissions, we will integrate the app with the university's existing Active Directory system. This integration will enable secure authentication and ensure that user roles are synchronized with their Active Directory roles.

## Conclusion

In conclusion, the decision to implement Role-Based Access Control (RBAC) for managing permissions and access control in our university social networking mobile app is a crucial step toward ensuring the success and security of the application.

RBAC offers the flexibility and scalability needed to adapt to the evolving requirements of our university community. It allows us to grant appropriate access to each user category, whether they are students, professors, or administrators. This approach not only enhances usability but also enhances security by limiting access to specific functionalities based on user roles.

Furthermore, our decision to integrate the app with the university's Active Directory system adds an additional layer of security and streamlines user management. This integration ensures that user roles and permissions remain synchronized with their roles in the university's broader IT infrastructure, reducing the risk of unauthorized access and enhancing overall system integrity.

As proposed, the RBAC can be integrated with the existing active directory system, which is also to address the security and data privacy for certain users, acting as an additional layer with existing data protection protocols.
