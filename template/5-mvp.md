# The MVP

Concretely, we aim to integrate the following services into GatherSpot, which are ordered by their priority:

- **Self-Hosting and Custom Databases:** Crucial for large entities to manage their data securely.

- **Extended authorization mechanism:** Ensuring proper access control and making sure people accessing events from a certain organization are allowed to do so.

- **Payment integration:** Currently, our app does not support financial transactions for events that require attendee participation fees. We plan to integrate services like PayPal to facilitate these payments.

- **Private conversations:** Being able to chat with other users privately and not as part of event chatting groups can be a significant improvement.

- **Version for iOS devices:** Important to reach a broader audience.

## Personas and Scenarios

The target personas for the product are the following:

- **Hobbyists/Social Butterflies**: Socially dynamic people who enjoy attending and organizing social events related to what they like.

- **Large Entities**: Universities, clubs, organizations that manage large-scale events and need tailored solutions for event management.

Event Organizers are the key personas because they will use GatherSpot's comprehensive features for event creation, management, and feedback. The app development and feature prioritization should heavily insist on their usage patterns and feedback.

**High Level Scenarios**

We expect the typical patterns and scenarios to happen like this:

- **Adoption**: An individual discovers GatherSpot through a friend or online promotion, downloads the app, and registers. Upon successfully attending an event that they hopefully liked, they keep on using the app and browse upcoming events, registering to the ones they are interested in.

- **Use**: An event organizer creates a new event, sets the date, location, and details, and promotes it within the app. Participants register, and they communicate through the integrated chat.

- **Sharing**: After a successful event, participants leave positive feedback, share their experiences on social media, and follow the organizer for future events. Universities and clubs promote the app for their internal events.

## User Stories and Key Features

1. **User Story for university citizens:**
    - “As an university citizen, I want to be informed of all social events organized inside my university so that I can register if I am interested.” 

2. **User Story for event organizers:**
    - “As an event organizer inside a university, I want to be able to post events so that students can stay informed about all social activities without relying on physical flyers or other outdated methods.”

3. **User Story for participants:**
    - "As a participant, I want to be able to pay the registration fee directly through the app to avoid having to bring money to the event."

4. **User story for all users:**
    - "As a user, I want to be able to privately contact any organizer or participant so that I can express my questions or concerns comfortably."

5. **User story for iOS users:**
    - “As the owner of an iOS device, I want to be able to use the app so that I can also benefit from the app features.”

## Success Criteria
The success of the MVP for the event application will be evaluated based on several key metrics and qualitative assessments specific to the event management and participation context:

1. **User Penetration:**

   - **Active Users:** Measure the number of active users on the app, focusing on daily and monthly active user metrics, particularly tracking how many users regularly create or join events.

   - **User Growth Rate:** Track the growth rate of new user registrations over time, with particular attention to spikes around event promotions.

   - **Retention Rate:** Analyze user retention rates by monitoring how many users continue to use the app for event creation and participation after their initial registration over specified periods (e.g., 1 week, 1 month, 3 months).

2. **Quality / Satisfaction:**
   - **User Satisfaction:** Collect user feedback through post-event surveys, app ratings, and reviews to gauge overall user satisfaction with event management features.

   - **Net Promoter Score (NPS):** Utilize the NPS metric to understand how likely users are to recommend the app to others for event creation and participation.

   - **Customer Support Requests:** Monitor the number and nature of customer support requests related to event creation, management, and participation to identify and address common issues or pain points.

   - **Error Rates:** Track the frequency and types of errors encountered by users, particularly during event registration and management processes, to improve app stability and performance.

3. **Engagement Metrics:**
   - **Session Length:** Measure the average duration of user sessions, focusing on time spent on event creation, management, and browsing/joining events.

   - **Event Participation:** Monitor the number of events created and the participation rates in these events, including metrics like RSVPs, check-ins, and active participation during events.

   - **Feature Usage:** Analyze which event management features (e.g., calendar integration, reminders, ticketing) are most frequently used to understand user preferences and improve less-used features.

4. **Business Metrics:**

   - **Revenue:** Track revenue generated through app features such as event fees, ticket sales, or premium subscriptions for advanced event management tools.

   - **Customer Acquisition Cost (CAC):** Calculate the cost to acquire each new user who creates or joins events and compare it to industry benchmarks.

   - **Customer Lifetime Value (CLV):** Estimate the total revenue expected from a user over their entire relationship with the app, focusing on repeated event creators and frequent event participants.

5. **Progress in Discussions with Ecosystem Partners / Investors / Customers:**

   - **Partnerships:** Monitor progress in forming strategic partnerships with event organizers, venues, and service providers that can enhance the app’s functionality or market reach.

   - **Investor Engagement:** Track interest and engagement from potential investors, including meetings held, feedback received, and investment commitments, particularly focusing on investors with a background in event management technologies.

   - **Customer Acquisition:** Evaluate the effectiveness of marketing and sales efforts in acquiring early customers, especially key target groups such as professional event organizers and influential community leaders.

6. **Technical Performance:**

    - **Uptime and Reliability:** Ensure high levels of app uptime and reliability, aiming for minimal downtime and quick recovery from any issue, especially during peak event registration periods.

   - **Scalability:** Assess the app’s ability to handle increased traffic and user load, particularly during event promotion periods and on the days of major events.

   - **Response Time:** Measure the app’s response times, striving to maintain low latency for an optimal user experience, especially during critical actions like event registration and check-in.

By systematically tracking and analyzing these metrics, we can determine the success of the MVP, identify areas for improvement, and make data-driven decisions to enhance the app’s functionality and user experience in the event management domain.

## Features Outside the Scope

- **Gamification** Gamification involves incorporating game-like elements such as badges, points, leaderboards, and rewards to increase user engagement and make the app more enjoyable. Users can earn badges for participating in events, accumulate points for certain actions, and see their rankings on leaderboards. Currently, we only rate organizers and we believe it is enough for the product to be viable.
      Building a gamification system requires designing and implementing various elements such as point tracking, badge awarding mechanisms, and leaderboards. This adds complexity and time to the development process. Introducing gamification too early may shift focus from the core functionalities.


- **Integration strategy**:
  - Step 1: Start with a basic rewards system where users can earn points for specific actions like attending events or providing feedback.
    
    - Step 2: Introduce badges and achievements for reaching milestones, such as attending a certain number of events or organizing popular events.
   
      - Step 3: Add leaderboards to foster friendly competition among users, showing top event organizers or most active participants.

   - **Recommendation system**


      A recommendation system is designed to suggest events to users based on their past behavior. It leverages algorithms to analyze user data and provide personalized event suggestions, enhancing user engagement and satisfaction. Even though it would be a nice feature for the app, building an effective recommendation system involves developing complex algorithms, collecting and processing large amounts of data, and continuously fine-tuning the recommendations based on user feedback. This requires significant resources and time.


      - **Integration strategy**:


         We have already implemented basic filtering based on interests and location. 


         - Step 1: Gradually collect data on user behavior, such as the types of events they attend, their interactions, and their preferences, keeping in mind that we have to ensure data privacy and compliance with regulations.


         - Step 2: Start with collaborative filtering which is easier to implement and based on the construction of a user-interaction matrix using data previously collected. For user-based collaborative filtering, recommend events that similar users have attended or shown interest in. For item-based collaborative filtering, recommend events similar to those a user has interacted with. 


         - Step 3: Evaluate the performance of the collaborative filtering system using appropriate metrics such as precision, recall, or Mean Average Precision (MAP). Repeat all this sequence until having satisfactory results (MAP score > 0.5 would be great).


   - **Event Sponsorship:**


      Event sponsorship feature would enable organizers to guarantee visibility for the events they create. It would also be a way for the app to generate revenues. We decided to exclude it from the MVP because implementing a robust system for managing sponsorships requires significant development effort. It involves the creation of a backend infrastructure to handle sponsorship agreements as well as designing a user-friendly interface for organizers to manage their sponsorship deals.


      - **Integration strategy**:


      - Step 1: Conduct market research to identify potential sponsors who align with the nature of events hosted or promoted through GatherSpot. This can only be done after the product has reached a certain level of success related to engagement metrics and user penetration.

   
      - Step 2: Develop sponsorship proposal packages outlining the benefits and opportunities available to sponsors.


      - Step 3: Reach out to potential sponsors to discuss partnership opportunities and negotiate sponsorship agreements.
      

Starting with gamification, then incorporating a recommendation system, and finally introducing event sponsorship makes sense, as we aim to create the best possible product to attract potential sponsors. By prioritizing these features in this sequence, we ensure that GatherSpot evolves into a comprehensive and compelling platform that not only delights users but also offers tangible benefits to potential sponsors, thereby increasing our chances of securing valuable sponsorship deals.
