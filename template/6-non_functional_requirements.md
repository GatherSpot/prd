# Non-Functional Requirements

## Security, privacy, and data retention policies

1. **Applicable Laws and Regulations:**
   - **Swiss Data Protection Act (DPA):** Compliance with the Swiss DPA is paramount as it governs the processing of personal data in Switzerland, necessitating that user data is collected and processed lawfully and transparently, even within a Firebase environment.
   - **Federal Act on Data Protection (FADP):** Adherence to FADP regulations is crucial for data protection at the federal level in Switzerland, emphasizing principles such as data minimization, purpose limitation, and data security, which should extend to Firebase data storage and processing.
   - **Swiss Financial Market Supervisory Authority (FINMA) Regulations:** If the app involves financial transactions, such as for paid events (implemented as a future feature), compliance with FINMA regulations is necessary to ensure data security and confidentiality, even within Firebase's ecosystem.
   - **Swiss Federal Act on Banks and Savings Banks:** For banking or financial services within the app, compliance with this act is obligatory to safeguard customer data and ensure the confidentiality of financial transactions, extending to Firebase's data handling procedures.

2. **Internal Policies:**
   - **Data Encryption:** All sensitive user data stored in Firebase should be encrypted using robust encryption mechanisms provided by Firebase or additional encryption layers to ensure data confidentiality and integrity.
   - **Access Control:** Implement Firebase Authentication and Firebase Security Rules to enforce strict access control measures, restricting access to sensitive data based on user roles and permissions.
   - **Data Localization:** Ensure that user data stored in Firebase is hosted in servers located within Switzerland or in jurisdictions with equivalent data protection laws, adhering to Swiss data protection regulations.
   - **Data Retention:** Define clear data retention policies within Firebase, specifying the duration for which data will be stored and establishing procedures for securely deleting data in compliance with Swiss data protection laws.

3. **Privacy Features Needed from the Phone:**
   - **Explicit Consent Mechanisms:** The app should incorporate features to obtain explicit consent from users before accessing personal data (such as location) or device features, aligning with Firebase's authentication and permission management capabilities.
   - **Data Access Controls:** Leverage Firebase Authentication and Firebase Security Rules to enable users to control data access permissions and manage their data privacy settings effectively.
   - **Secure Communication:** Utilize Firebase's built-in security features and SSL/TLS encryption to ensure secure communication between the app and Firebase servers, safeguarding user privacy against unauthorized interception or eavesdropping.

#### Authentication for Users, Confirmation by Mail
   - **Google Authentication:** Offer Google authentication as an authentication option for users, integrating Firebase Authentication with Google Sign-In to provide a convenient and secure registration process.
   - **Email Confirmation:** Implement email confirmation for user registration using Firebase Authentication's email verification feature to validate email addresses and prevent unauthorized account creation.


## Adoptions, Scalability and Availability

1. **Traffic Patterns:**
   - **Regular Traffic:** Expect consistent traffic patterns with fluctuations during peak hours or periods of increased event activity, requiring Firebase to handle varying loads efficiently.
   - **Bursty Traffic:** Prepare for bursts of traffic during promotional campaigns, major event announcements, or registration deadlines, necessitating Firebase's scalability features to accommodate sudden spikes in user activity seamlessly.

2. **Design Considerations for Burst Traffic:**
   - **Auto-scaling:** Leverage Firebase's auto-scaling capabilities to dynamically adjust resources based on real-time traffic demands, ensuring optimal performance during peak periods without manual intervention.
   - **Load Balancing:** Utilize Firebase Hosting's load balancing capabilities to distribute incoming traffic across multiple servers, preventing overloading of individual servers and maintaining high availability.
   - **Caching Mechanisms:** Implement Firebase's caching mechanisms to cache frequently accessed data and improve overall system responsiveness during periods of high traffic, reducing the load on Firebase servers.
   - **Fault Tolerance:** Implement Firebase's redundancy and failover mechanisms to minimize downtime and ensure uninterrupted service availability in the event of server failures or network disruptions.

By aligning Firebase with these non-functional requirements and incorporating appropriate security, privacy, and scalability measures, the event app will be well-equipped to comply with Swiss regulations, protect user data, and deliver a reliable and secure user experience within Firebase's environment.
