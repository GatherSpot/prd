# The MVP


Additional features will fall into two categories:

- 1. Extend functionalities for individuals 
- 2. Make the app usable by a broader audience


Concretely, we aim to integrate the following services into GatherSpot, which are ordered by their priority:


- **Self-Hosting and Custom Databases:** Crucial for large entities to manage their data securely.


- **Extended authentication mechanism:** Ensuring proper access control and making sure people accessing events from a certain organization are allowed to do so.


- **Payment integration:** Currently, our app does not support financial transactions for events that require attendee participation fees. We plan to integrate a service like PayPal to facilitate these payments.


- **Private conversations:** Being able to chat with other users privately and not as part of event chatting groups can be a significant improvement.


- **Version for IOS devices:** Important to reach a broader audience.

## Personas and Scenarios

*Who are the target personas for this product?*

*Which is the key persona?*

*High-level scenarios to adopt, use and share the product.*

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

*User stories about how various personas will use the product in context.*

*Identify and prioritise the key features required.*

*Justify the importance of each feature.*


1. **User Story for university citizens:**
    - “As an university citizen, I want to be informed of all social events organized inside my university so that I can register if I am interested ” 


2. **User Story for event organizers:**

    - “As an event organizer inside a university, I want to be able to post events so that students can stay informed about all social activities without relying on physical flyers or other outdated methods”


3. **User Story for participants:**

    - "As a participant, I want to be able to pay the registration fee directly through the app to avoid having to bring money to the event."


4. **User story for all users:**

    - "As a user, I want to be able to privately contact any organizer or participant so that I can express my questions or concerns comfortably."

5. **User story for IOS users:**

    - “As the owner of an IOS device, I still want to be able to use the app so that I can also benefit from the app features”


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
   - **Revenue (if applicable):** Track revenue generated through app features such as event fees, ticket sales, or premium subscriptions for advanced event management tools.
   - **Customer Acquisition Cost (CAC):** Calculate the cost to acquire each new user who creates or joins events and compare it to industry benchmarks.
   - **Customer Lifetime Value (CLV):** Estimate the total revenue expected from a user over their entire relationship with the app, focusing on repeat event creators and frequent event participants.

5. **Progress in Discussions with Ecosystem Partners / Investors / Customers:**
   - **Partnerships:** Monitor progress in forming strategic partnerships with event organizers, venues, and service providers that can enhance the app’s functionality or market reach.
   - **Investor Engagement:** Track interest and engagement from potential investors, including meetings held, feedback received, and investment commitments, particularly focusing on investors with a background in event management technologies.
   - **Customer Acquisition:** Evaluate the effectiveness of marketing and sales efforts in acquiring early customers, especially key target groups such as professional event organizers and influential community leaders.

6. **Technical Performance:**
   - **Uptime and Reliability:** Ensure high levels of app uptime and reliability, aiming for minimal downtime and quick recovery from any issues, especially during peak event registration periods.
   - **Scalability:** Assess the app’s ability to handle increased traffic and user load, particularly during event promotion periods and on the days of major events.
   - **Response Time:** Measure the app’s response times, striving to maintain low latency for an optimal user experience, especially during critical actions like event registration and check-in.

By systematically tracking and analyzing these metrics, we can determine the success of the MVP, identify areas for improvement, and make data-driven decisions to enhance the app’s functionality and user experience in the event management domain.

## Features Outside the Scope

*The MVP must be viable and minimal.*

*Which features don’t belong in it.*

*How should these be eventually integrated and in what sequence.*


 To achieve this objective, we will need to update the code such that:

 -  It enables them to have their own databases and making them self-hostable. 

 -  It implements more robust authentication methods beyond email addresses and 2FA, to ensure security and reliability (proof someone has the right to access such events from these entities).

 - It allows universities, clubs, and organizations to tailor the app to their specific needs and integrate it seamlessly into their existing systems.


