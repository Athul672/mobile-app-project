 

Development Framework – React Native 

Status 

Accepted 

Decision 

We will develop a mobile weather application using React Native. 

Context 

We are creating a weather app for Android. Our team already has experience with JavaScript, React, and Expo from previous SAIT courses. Because React Native also uses JavaScript, the team can build the app more quickly without learning a completely new framework. This helps us stay productive and meet the project timeline. 

Options Considered 

React Native 
Ionic 
Cordova 
Native Script 
Framework7 

 

Rationale 

React Native is a strong choice for a weather app because it allows fast development and provides smooth performance like native Android apps. It supports essential weather app features like GPS for location, API requests for weather data, and animated UI components for weather visuals. 
 React Native also has a large ecosystem of libraries such as Expo, which makes it easier to handle permissions, fetch API data, and design UI screens. Many online tutorials and community resources are available, making this a convenient choice. 

Consequences  

We can build the weather app faster because we already know JavaScript and React. 
It is easy to use GPS and location services, which are important for showing local weather. 
Many libraries help us fetch real-time weather data from APIs. 
Lots of tutorials and community support make building weather features easier. 
Some advanced Android features might need extra setup, but they are not required for our weather app. 

 

 

 
Navigation strategy 

 
Hardware: GPS, Speaker, Fingerprint scanner, etc.  
Decision 

Our weather app will not use any device hardware. 

Context 

The weather app only needs to show weather information from an online API. It does not need the camera, microphone, GPS, or any other hardware to work. Keeping the app simple helps us finish it faster. 

Options Considered 

Use GPS 
Use sensors 
Use camera or microphone 
Use no hardware (chosen) 

Rationale 

We are not using hardware because: 

The app works well without it. 
It keeps the project easy and simple. 
No permission is needed. 
Faster development and fewer errors. 

Consequences 

Easy to build 
No need to ask for permissions 
Fewer problems and faster testing 
Users must type in the location instead of it being detected automatically 

 

 

 

Database storage: Local (encrypted or unencrypted), remote, or none.  

Status 

Decided not to use database storage. Open to using database storage if 100% needed. 

Decision 

Decided not to use database storage for our mobile weather app. 

Assumptions 

We want to make an app that will show the current temperature and a 5-day forecast. 

All of the information will be displayed on the same page. 






Navigation Strategy - Tab Navigation

Context
 Our team is building a Weather Forecast mobile app for Android using React Native. The app will present:

  Current weather conditions


  A 5-day forecast


  Settings page (e.g., temperature units, user location preferences, light/dark mode)


 The navigation structure must allow users to move between these core features quickly. As a student team operating under a short project timeline, our architectural decisions need to:
  Match our skill level (mostly familiar with React/React Native)


  Keep complexity low


  Avoid unnecessary features that go beyond the scope of the course.


 We considered several navigation patterns commonly used in mobile apps:
Stack Navigation


  Drawer Navigation


  Tab Navigation


 Each option supports different user interface expectations.
Decision
 We will use Bottom Tab Navigation as our primary navigation strategy, implemented using React Navigation.
Rationale
 Our decision is based on the following factors:
 Business Priorities
  Users must quickly switch between weather views (today vs. 5-day forecast).


  Navigation should be simple and consistent across Android devices.


  The app should feel familiar to typical weather-app users, who expect tabs.


 Team Skillset
  The team is already experienced with React and basic React Navigation.


  Tab navigation has a smaller learning curve compared to drawers or stacks.


  Faster to implement, which supports our limited timeline.


 Pros
  Highly effective for apps with 2–4 primary screens.


  Always-visible tabs make switching between weather views effortless.


  Faster development due to simple configuration.


  Supports icons and labels, improving accessibility and usability.


  Works well for mobile apps that do not require deep navigation flows.


 Cons
  Tabs appear on all main screens, even when content is scroll-heavy.


  Not suitable if the app grows to contain many feature screens (would require stacking or drawers later).



  Despite these minor drawbacks, tab navigation aligns best with our user needs and course scope.

Consequences
 Effects of This Decision
  Users can move between the three main screens with a single tap.


  We must design screens with enough vertical space to account for the tab bar.


  All core screens will remain at the top level of the app’s navigation structure.


Outputs / Follow-Ups
 Future ADRs may be required only if we add nested screens (e.g., detailed weather info, saved locations).


 We must create a clear icon set for each tab (e.g., home, calendar, settings).


 Team members need to configure React Navigation dependencies early in the development cycle.


After-Action Review Plan
 One month after implementation (or near project end), we will review whether tab navigation:


  Supports user needs


  Works well with the final UI


  Needs extension with nested stack screens





 
