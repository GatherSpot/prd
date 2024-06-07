# Timeline/Resource Planning


The MVP development is planned to be executed over a 14-week time period. We will also define milestones so that we make sure we are on time and to evaluate our progress better.

We will need to have 1 front end dev, 1 UI designer, 1 backend developer and 1 software tester.
We decided to start with working with EPFL.


**Milestone 1:** Documentation and Design completion


- Reading documentation about EPFL APIs, in particular related to authentication (backend developer).
- Tequila registration and integration (backend developer).
- Tests to check EPFL API status (software tester).
- Create proper UI for private chats, including the creation of the channel by a user with another one they follow and the inner messages (UI designer + front-end developer).

| Sprint/Week Number | Objective        | Outcomes                            |
| :----------------- | :--------------- | :---------------------------------- |
| Week 1             | Documentation    | EPFL API Investigation              |
| Week 2             | Technical Setup  | Configure Tequila Auth              |
|                    |                  | Setup mock version of EPFL's        |
|                    |                  | authentication system for tesing    |
| Week 3             | Design for chats | Chat UI components ready to be used |


**Milestone 2** Finish authentication testing and Features development


- With EPFL mock integration in place, everything related to authentification will have to be extensively tested (software tester).
- Integration of private chats within the application by using components previously defined. Use the already defined functions / create to link the UI and Firebase (front end developer).
- Reading documentation about PayPal and paying attention to RESTful APIs for processing payments, managing accounts, and handling transactions (backend developer).

| Sprint/Week Number | Objective              | Outcomes                           |
| :----------------- | :--------------------- | :--------------------------------- |
| Week 4             | Testing authentication | Integration of authentication done |
| Week 5             | Chats integration      | Private chats integration done     |
| Week 6             | Documentation          | Good understanding of PayPal's API |


**Milestone 3** Features development continued


- Design payment flow with proper UI to prepare payment integration (UI designer + front-end developper).
- Use PayPal SDKs or API endpoints to implement payment processing.
- Set up a PayPal developer account and create sandbox (test) accounts for simulating transactions without involving real money. Also, generate API credentials (Client ID and Secret) for authenticating the app with PayPal's servers.


| Sprint/Week Number | Objective             | Outcomes                           |
| :----------------- | :-------------------- | :--------------------------------- |
| Week 7             | UI design for payment | Integration of authentication done |
| Week 8             | Payment integration   | Payment feature integrated         |
| Week 9             | Testing               | Fully-functional payment feature   |


**Milestone 4** Initial Rollout and Feature Iterations for PMF


- Rollout app to alpha testers.
- Polish product and deliver it.


| Sprint/Week Number | Objective         | Outcomes                         |
| :----------------- | :---------------- | :------------------------------- |
| Week 10/11         | Alpha Testing     | Deployed app to production       |
|                    |                   | Monitored app performance        |
|                    |                   | Gathered user insights/analytics |
|                    |                   | Fix small issues if needed       |
| Week 12            | Feature Iteration | Optimize user experience         |
| Week 13            | Beta Testing      | Initiate marketing               |
|                    |                   | Getting users on the app         |
| Week 14            | Full Rollout      | Promote the app widely           |

