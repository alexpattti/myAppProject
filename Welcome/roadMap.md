# Roadmap 

This project is structured into a 6-week plan, divided into 2-week phases. Each phase focuses on a key aspect of development. Within each phase, tasks are broken down by day, with specific goals and subtasks.

There are notes at the very bottom.

# **Week 1-2: Deep Foundations (Feb 15 - Feb 28)**

####  **React Native Basics – Feb 16**

📌 This involves learning React Native fundamentals
✅  Hooks
✅  Navigation
✅  Styling  
✅  **Mini Goal:** Build a few small test screens to get familiar with the frameworks.

---

####  **Set up Supabase & Auth – Feb 17** 

📌 Get authentication working using Supabase (setting up authentication, fetching/saving data).
-  Create a Supabase project  
-  Set up email/password authentication  
-  Test sign-up and login flow in Postman  
-  Connect authentication to a basic React Native UI (sign-in screen)  
-  Mini Goal: User should be able to sign up, log in, and see their profile.

---

####  **Create basic PostgreSQL database – Feb 18**

📌 Build the database structure to store users & memberships
-  Create a users table (ID, email, name, role)  
-  Create a memberships table (userID, status, start_date, expiry_date)  
-  Connect Supabase authentication with the users table  
-  Write a test query to fetch a user's membership status  
-  Mini Goal: A user should be able to log in and have their membership status retrieved.

---

####  **Test real-time syncing – Feb 19** 

📌 Learn how Supabase handles real-time updates
-  Enable real-time updates on the check_ins table  
-  Create a listener in React Native for live updates  
-  Test inserting new check-ins manually in the database  
-  Verify if the front-end updates automatically  
-  Mini Goal: Check-ins should appear instantly without needing a refresh.

---

####  **Build simple sign-in/sign-up – Feb 20** 

📌 Create a user-friendly authentication screen
-  Create a sign-up form (email, password, confirm password)  
-  Implement validation (password strength, email format)  
-  Add error handling (invalid credentials, network issues)  
-  Display user details after login  
-  Mini Goal: Fully working authentication flow.

---

####  **Set up and manage membership data – Feb 21**

📌 Store and manage membership data
-  Define columns: ID, userID, plan type, start_date, expiry_date  
-  Add foreign key linking users and memberships  
-  Test inserting sample memberships via Supabase dashboard  
-  Write a query to check a user's active membership status  
-  Mini Goal: Users should have a membership associated with them.

---

####  **Buffer Day (Catch-Up & Debugging) – Feb 22**

📌 Use this day to review, debug, and reinforce what you've learned so far.
-  Double-check authentication flow (login, signup, session persistence)
-  Test real-time updates and database syncing
-  Debug any issues with user creation or membership retrieval
-  If ahead: Start sketching the check-in UI

---

####  **Buffer Day (Refinement & UI Adjustments) – Feb 23**

📌 Fine-tune what you’ve built and ensure everything is working smoothly.
- Improve form validation for signup/login (better error messages)
- Make sure Supabase authentication roles are properly assigned
- Add UI polish (adjust button sizes, colors, loading indicators)
- If ahead: Begin planning database integration for check-ins

---

#### **Create basic check-in/out flow (dummy data) – Feb 24**

📌 Prototype the check-in/out system using temporary (dummy) data

- Create a button for "Check In" and "Check Out"  
- Store check-ins in temporary state (not yet connected to the database)  
- Display a simple list of check-ins (e.g., "Checked in at 10:00 AM")  
- Allow users to toggle between checked in and checked out  
- Mini Goal: The UI should feel functional, even if it's not yet connected to the backend.

---

#### **Buffer Days (Refinement, Debugging, and Prep for Database Integration) – Feb 25-27**

📌 These are flex days—you can debug, refine, or move ahead!

- Test and tweak the check-in UI to ensure a smooth experience  
- Make sure role-based access (admin vs. user) is working correctly  
- Optimize performance (reduce unnecessary API calls)  
- If ahead: Start connecting the check-in feature to the database  

---
#### **Buffer Days (Refinement, Debugging, and Prep for Database Integration) – Feb 26**

📌 These are flex days—you can debug, refine, or move ahead!

- Test and tweak the check-in UI to ensure a smooth experience  
- Make sure role-based access (admin vs. user) is working correctly  
- Optimize performance (reduce unnecessary API calls)  
- If ahead: Start connecting the check-in feature to the database  

---
#### **Buffer Days (Refinement, Debugging, and Prep for Database Integration) – Feb 27**

📌 These are flex days—you can debug, refine, or move ahead!

- Test and tweak the check-in UI to ensure a smooth experience  
- Make sure role-based access (admin vs. user) is working correctly  
- Optimize performance (reduce unnecessary API calls)  
- If ahead: Start connecting the check-in feature to the database  

---

#### **Mini Goal: Basic auth & data storage working – Feb 28**

📌 By today, the foundation should be complete!

- Users can sign up, log in, and be authenticated  
- Membership data is stored and retrieved properly  
- Users can check in, and their check-ins are saved in the database  
- Everything should work without manual database edits!  
- 🎯 Mini Goal Achieved! You’re now ready for Week 2 🚀  

---




# **Week 3-4: Core Feature Development (Mar 1 - Mar 13)**

---

#### **Build Check-In/Out system – Mar 1**

📌 Implement the core check-in/out functionality

- Create check-in and check-out buttons  
- Store check-ins in the check_ins table (userID, timestamp)  
- Prevent duplicate check-ins on the same day  
- Display a list of recent check-ins for the user  
- Mini Goal: Users can check in/out, and the data is saved persistently.  

---

#### **Implement real-time user count display – Mar 2**

📌 Show the number of currently checked-in users

- Set up a real-time listener on the check_ins table  
- Query for users who are checked in (status = active)  
- Display the count dynamically on the dashboard  
- Mini Goal: Live count updates instantly as users check in/out.  

---

#### **Buffer Day (Refine Live Count & Debug) – Mar 3**

📌 Review and test real-time features

- Ensure live count updates instantly across all devices  
- Optimize database queries for efficiency  
- Fix UI glitches related to check-ins  

---

#### **Add role-based access (admin vs. customer) – Mar 4**

📌 Set up permissions so admins and customers see different views

- Define user roles in the database (role: admin/customer)  
- Restrict certain pages based on role  
- Admins can see all check-ins and users; customers only see their own  
- Mini Goal: The app should recognize admins and customers correctly.  

---

#### **Buffer Day (Testing & Refinement) – Mar 5**

📌 Use this time to refine user roles & real-time features

- Ensure customers can't access admin functions  
- Improve UI for admin/customer views  
- If ahead: Start setting up the membership management system  

---

#### **Buffer Day (Testing & Refinement) – Mar 6**

📌 Use this time to refine user roles & real-time features

- Ensure customers can't access admin functions  
- Improve UI for admin/customer views  
- If ahead: Start setting up the membership management system 

---

#### **Create membership management system – Mar 7**

📌 Allow users to sign up, renew, or cancel memberships

- Implement a UI for managing membership plans  
- Connect membership changes to the database  
- Ensure that expired memberships prevent check-ins  
- Mini Goal: Users can fully manage their memberships.  

---

#### **Buffer Day (Membership System Debugging) – Mar 8**

📌 Use this day to test and refine the membership system

- Ensure renewals update expiration dates correctly  
- Test UI for different membership states (active, expired, pending)  
- Fix potential bugs  

---

#### **Admin dashboard setup – Mar 9**

📌 Build an admin panel for gym employees to manage users

- Display a list of all active members  
- Show check-in history in real time  
- Provide an interface for canceling/renewing memberships  
- Mini Goal: Admins can oversee memberships and check-ins easily.  

---

#### **Buffer Day (Final Testing & Polishing) – Mar 10**

📌 Use this day to debug and improve overall app functionality

- Test all features together (check-ins, user roles, memberships)  
- Fix UI inconsistencies and optimize database performance  
- Ensure admin actions (canceling, renewing) work correctly  

---

#### **Buffer Day (Final Testing & Polishing) – Mar 11**

📌 Use this day to debug and improve overall app functionality

- Test all features together (check-ins, user roles, memberships)  
- Fix UI inconsistencies and optimize database performance  
- Ensure admin actions (canceling, renewing) work correctly  

---

#### **Buffer Day (Final Testing & Polishing) – Mar 12**

📌 Use this day to debug and improve overall app functionality

- Test all features together (check-ins, user roles, memberships)  
- Fix UI inconsistencies and optimize database performance  
- Ensure admin actions (canceling, renewing) work correctly  

---

#### **Mini Goal: Functional check-in system & membership features – Mar 13**

📌 By today, all major features should be working!

- Users can check in/out and see live updates  
- Memberships are managed properly (sign-up, renewal, expiration)  
- Admins have control over users and check-ins  
- The core app is now fully functional!  
- 🎯 Mini Goal Achieved! Ready for Week 5 (Testing & Refinements).  

---




# **Week 5-6: Testing & Refinements (Mar 14 - Mar 20)**

#### **Test UI and fix layout bugs – Mar 14**

📌 Refine the UI/UX to improve usability and aesthetics

- Test app on different screen sizes and devices  
- Fix layout inconsistencies (buttons, spacing, fonts)  
- Improve loading states and error messages for better user experience  
- Ensure smooth navigation between screens  
- Mini Goal: The UI should feel clean, intuitive, and responsive.  

--

#### **Buffer Day (UI Debugging & Refinement) – Mar 15**

📌 Use this day to polish the UI further based on testing feedback

- Optimize animations and transitions (reduce lag)  
- Test dark mode compatibility (if applicable)  
- Fix any remaining UI glitches  

---

#### **Optimize database performance – Mar 16**

📌 Ensure the app runs efficiently without lag or unnecessary load

- Add database indexes to speed up queries  
- Optimize real-time sync to reduce unnecessary API calls  
- Review and improve SQL queries for better efficiency  
- Test database load under multiple users checking in/out  
- Mini Goal: The app should feel fast and responsive under load.  

---

#### **Buffer Day (Database Optimization & Security Review) – Mar 17**

📌 Use this day to refine database efficiency & security

- Ensure Supabase rules properly restrict unauthorized access  
- Test performance under stress (simulate multiple check-ins)  
- Optimize membership renewal logic  

---

#### **Implement push notifications (optional) – Mar 18**

📌 Add notifications for check-in reminders & membership expiration

- Set up Firebase Cloud Messaging (FCM) or Expo Notifications  
- Send test notifications when users check in/out  
- Notify users before their membership expires  
- Ensure notifications work on both iOS and Android  
- Mini Goal: Users should receive timely, useful notifications.  

---

#### **Buffer Day (Final Testing & Tweaks) – Mar 19**

📌 Run a full test of the app to catch last-minute issues  
- Test all features together (check-ins, admin panel, memberships)  
- Fix minor bugs related to UI, data storage, or logic  
- Ensure notifications are triggered at the right time  

---

#### **Mini Goal: App should feel smooth & reliable – Mar 20**

📌 By today, the app should be fully functional and polished!  
 UI is clean and bug-free  
 Database performance is optimized for real-time usage  
- Push notifications (if enabled) work reliably  
- The app should feel ready for real-world use!  
- 🎯 Mini Goal Achieved! Now, you're ready for final deployment & testing.  

---




# **Finish Deployment & Polish (Mar 21 - Mar 31)**

#### **Final bug fixes & optimizations – Mar 21**

📌 Ensure everything runs smoothly before beta testing  
- Fix any outstanding minor bugs from Week 5-6  
- Optimize API calls to reduce unnecessary requests  
- Review app performance (loading times, animations)  
- Ensure Supabase security rules prevent unauthorized access  
- Mini Goal: App should be fully functional with no major issues.  

---

#### **Buffer Day (Final Testing & Debugging) – Mar 22**
📌 Use this day for extra testing & minor refinements  
- Run a final walkthrough of all features  
- Ensure role-based access works as expected  
- Fix any UI glitches or inconsistencies  

---

#### **Beta test with a friend – Mar 23**

📌 Have a real user test the app and provide feedback  
- Observe where they struggle or get confused  
- Collect feedback on UI, performance, and usability  
- Mini Goal: Identify any usability issues before deployment.  
- Mini Goal: Identify any usability issues before deployment.  

---

#### **Buffer Day (Fix Beta Feedback) – Mar 24**

📌 Implement feedback from beta testing  
- Adjust UI elements based on user confusion  
- Fix any issues found during testing  
 Ensure database updates are seamless  

---

#### **Deploy to test environment – Mar 25**

📌 Push the app to a real-world testing environment  
- Deploy to an internal test environment (Expo TestFlight or Android Beta)  
- Ensure all backend services (Supabase, notifications) are stable  
- Test app behavior in a real-world setting  
- Mini Goal: The app should function as expected outside the development environment.  

---

#### **Buffer Day (Monitor Deployment & Fix Bugs) – Mar 26**

📌 Use this day to observe & tweak anything that isn’t working  
- Check for crashes or unexpected errors in test environment  
- Debug any deployment-specific issues  
- Optimize any laggy areas of the app  

---

#### **Final UI/UX polish – Mar 27**

📌 Make last-minute UI refinements before launch  
- Ensure app theme, colors, and fonts are consistent  
- Fine-tune animations, transitions, and loading states  
- Double-check spacing, button sizes, and responsiveness  
- Mini Goal: The app should feel professional and polished.  

---

#### **MVP Launch! 🎉 – Mar 28**

📌 Officially launch the first version of your app!  
- Announce availability (if applicable)  
- Ensure onboarding is smooth for new users  
- Monitor database and real-time functionality under real users  
- Mini Goal: The MVP version is fully live and working! 🚀  

---

#### **Buffer Day (Monitor & Gather Feedback) – Mar 29**

📌 Observe how users interact with the live app  
- Track real-time check-ins and ensure no crashes  
- Look for edge cases that weren’t tested before  
- Collect initial user feedback  

---

#### **Emergency fixes (if needed) – Mar 30**

📌 Fix any unexpected post-launch issues  
- Resolve major bugs affecting functionality  
- Patch minor UI or database problems  
- Ensure push notifications and check-ins are stable  
- Mini Goal: The app should run without critical issues.  

---

#### **Final Buffer Day (Last Review & Prep for Deadline) – Mar 31**

📌 Make final adjustments before the April 1 deadline  
- Run one last full test of all features  
- Ensure all services (Supabase, authentication, check-ins) are stable  
- Prepare documentation (if needed for future improvements)  

---

#### **Final deadline – April 1**

📌 By today, the app should be 100% done!  
- All features fully working (check-ins, memberships, real-time updates)  
- No major bugs or performance issues  
- Project Successfully Completed! 🎉  




---

Notes:

You'll see in the roadmap that there are a lot of buffer days. Ideally I'd like to not use all of them, but this is my first project, and I'm new to the entire coding world. But I gave myself a cushion so that way I just move on a day ahead. Doing that will also help me stay motivated, as it will trick my brain into thinking I'm ahead of schedule which will keep me the momentum high. 

When I complete things I will mark them with a ✅.


- Mark critical tasks as High Priority (e.g., Check-In System, Membership Management).
- Set reminders for deadlines, especially mini goals.
- Use subtasks where necessary (e.g., “Build Check-In System” could have subtasks for “QR Code Scan” and “Manual Check-In”).
- Every Sunday, review progress and adjust tasks if needed.
- Every morning, check your Today’s Tasks in TickTick to stay on track.