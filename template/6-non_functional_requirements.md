# Non-Functional Requirements

## Security, privacy, and data retention policies

*Which are the applicable laws and regulations?*

*What are your internal policies?*

*Which privacy features do you need from the phone?*

We will be working with very sensitive data about location and health so we will have to comply to different laws linked to the protection of data.

In Switzerland :
Swiss Federal Act on Data Protection (FADP): The app must comply with the Swiss FADP, which governs the processing of personal data to protect the privacy and rights of individuals.

Revised FADP (revFADP): As of September 2023, the revised FADP introduces stricter requirements for data protection, including enhanced user rights and stricter penalties for non-compliance.

In Europe : 
GDPR (General Data Protection Regulation): For deployment within the European Union, compliance with GDPR is mandatory. GDPR sets strict guidelines for the collection, processing, and storage of personal data, emphasizing user consent, data minimization, and the right to be forgotten.

In the USA : 
CCPA (California Consumer Privacy Act): In the United States, particularly in California, CCPA protects consumer privacy rights and mandates transparency in data handling practices.
COPPA (Children's Online Privacy Protection Act): If the app is intended for children under 13 in the USA, compliance with COPPA is necessary to protect their personal information.
HIPAA (Health Insurance Portability and Accountability Act): In the USA, if the app handles health-related data, adherence to HIPAA regulations is essential to ensure the confidentiality and security of medical information.

The internal policies that we aim to comply with are the following :

Data Encryption: All user data, both at rest and in transit, will be encrypted using industry-standard protocols (e.g., AES-256, TLS).

Access Control: Implement strict access control measures to ensure that only authorized personnel can access sensitive user data.

Regular Audits: Conduct regular security audits and vulnerability assessments to identify and mitigate potential risks.

Data Minimization: Collect only the data necessary for the app’s functionality and ensure it is anonymized whenever possible.

User Consent: Obtain explicit user consent before collecting or processing any personal data, and provide clear information on how their data will be used.

Data Retention: Establish clear data retention policies, specifying how long user data will be stored and the process for securely deleting it once it is no longer needed.

On the phone we will require 3 privacy features :

Permission Management: Utilize the phone's permission management system to request user consent for accessing location data, step count, and other personal information.

Location Services: Implement privacy-respecting location services, ensuring that location data is only collected when necessary and with user consent.

Background Data Access: Minimize the use of background data collection, and clearly inform users when and why their data is being collected in the background.

## Adoptions, Scalability and Availability

*What kind of traffic patterns do you expect to see?*

Daily Usage Peaks: Expect increased traffic during early morning and late evening hours when users are most likely to check their step counts and engage with the app’s features.

Weekly Peaks: Higher traffic on weekends as users participate in challenges and social activities.

Event-Driven Spikes: Anticipate spikes in traffic during special events, challenges, or promotions.

*Are there known periods of bursty traffic that the MVP must be designed to support?*

Challenge Deadlines: Increased activity towards the end of challenge periods as users try to complete their goals.

Seasonal Trends: Higher usage during certain seasons, such as summer and new year, when people are more likely to set fitness goals.

Marketing Campaigns: Traffic surges following marketing campaigns, app updates, or collaborations with renowned IPs.

*Scalability and Availability*

Cloud Infrastructure: Use scalable cloud infrastructure (e.g., AWS, Google Cloud) to handle varying traffic loads and ensure high availability.

Load Balancing: Implement load balancing to distribute traffic evenly across servers and prevent any single server from becoming a bottleneck.

Auto-Scaling: Enable auto-scaling features to automatically adjust the number of active servers based on current traffic, ensuring optimal performance during peak times.

Redundancy and Failover: Set up redundant systems and failover mechanisms to maintain service availability during hardware failures or other disruptions.

Monitoring and Alerts: Use monitoring tools and set up alerts to detect and respond to performance issues or unusual traffic patterns in real-time.

By addressing these non-functional requirements, StepQuest can ensure a secure, reliable, and scalable application that meets user expectations and complies with relevant regulations.

