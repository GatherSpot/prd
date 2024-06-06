# Functional Requirements

## Self-Hosting and Custom Databases:

### Motivation:
In the GatherSpot MVP, we decided to support self-hosting of data by different entities. The idea is to enable institutions to have their own instance of the GatherSpot app, hosted on their servers.Large organizations may require high levels of data security and control. Self-hosting ensures that sensitive information is stored within the organization’s own infrastructure, minimizing the risk of external data breaches. Moreover, many large entities have strict compliance requirements that necessitate storing and managing data within their own secure environments.

People aware of their privacy should also appreciate the self-hosting functionality. Individuals and smaller organizations often have concerns about data privacy and control. Allowing these users to self-host and manage their own databases can significantly enhance trust in the platform.They will appreciate the transparency and autonomy provided by self-hosting options.

### Proposed solution: 
In the POC, the only way to store data was on Firebase. We need to adapt and extend the app so that an organization can choose where it saves its data. The outcome should stay as simple as possible so that the organization will use GatherSpot. Our solution is to make our application compatible with various server and other database systems.

#### Self-Hosting capability:
 Develop an option within the application that enables organizations and users to host the application on their own servers. Technically instead of Firebase data storage handler, add a more abstract layer for the storage in the implementation. Ensure compatibility with various server environments, offer support for common OS

#### Custom database integration:
 Implement a flexible database integration system that allows users to connect their own preferred database solutions instead of only the database system provided by Google Firebase. This includes support for popular databases such as MySQL, PostgreSQL, Microsoft SQL Server, and others.

By implementing these solutions, we ensure that GatherSpot remains flexible and user-friendly, accommodating the diverse data storage needs of various organizations while maintaining the simplicity and reliability that users expect. We also aim to cater to the needs of large entities requiring stringent data security and privacy-conscious users seeking greater control over their data.

