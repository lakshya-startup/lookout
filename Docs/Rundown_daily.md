# Rundown Day 1
<p>
Foundation & Clarity

- Brainstormed and locked in the Look Out concept
- Decided on tech stack: FlutterFlow + Firebase (using Google credits)
- Created official GitHub account and repo under company name
- Learned Git basics — commits, pushes, version control mindset
- Researched AI tools: when to use what and why
- Decided MVP build order: Login/Signup → Beginner Guide → Visa Countdown → Dashboard
- Day was mostly theory and setup but the foundation is solid
4 hrs : 30 mins
</p>

# Rundown Day 2
- Firebase Research
    A deep research on how Fire Base works why we need Firebase and what portion of our prod will it be contributing, so finally it would be integral as it is the backend of the prod.
    From User Auth, Storage, cloud functions(Functions which stays idle until called and performs, and th server quickly launches man instances to support this if there is many triggers) 
- Firebase Auth, FireStore and Firebase storage = Leanrt the theory and base of it.
- Created Firebase project 
- <b>Application security measures to keep in mind: </b>
    1. Trusting Front end blindly
    2. Broken Access Control 
    3. Business Logic Issue 
    4. External APIs (something as a service)
4hr : 00 mins 

# Rundown Day 3
<b>Foundation</b>
Created lookout-dev Firebase project. Created FlutterFlow project. Linked them together by registering Android and iOS apps in Firebase, downloading both config files (google-services.json + GoogleService-Info.plist) and uploading them to FlutterFlow. That handshake means FlutterFlow now knows exactly which Firebase kitchen to talk to.

<b>Database</b>
Created Firestore database — region set to australia-southeast1 (Sydney) meaning my users' data lives on servers closest to New Zealand, keeping the app fast for your target market.
Created the users collection with the right fields — email, full_name, visa_expiry_date, university, plan, created_at. Every international student who signs up to Look Out will become one document inside that collection.

<b>Security</b>
Wrote and deployed Firestore Security Rules. 

Anyone can create an account (signup works without being logged in yet)
Only logged in users can read data
Only the owner can write or delete their own document
Everything else in the database is locked by default

<b>Where Firestore and Auth are right now:</b>
Firestore is sitting there like a clean empty filing cabinet. Structure is defined, rules are live, Sydney servers are ready. But zero documents inside because zero users have signed up yet.
Auth is enabled in Firebase — Email/Password is live. But it hasn't been tested yet because the Login and Signup screens in FlutterFlow aren't fully wired up yet.

# What's left to finish Day 3:
Wire up Auth in FlutterFlow properly → test signup with the my email → see myself appear in Firebase Auth !!

# Rundown Day 4:
Restarted Auth in Firebase.
Hit run.
Created my own account.
Checked Firebase — my email and UID are sitting 
in the database on Sydney servers.
Look Out has its first user. It's me.
The app is alive.
<b>So the Login and sign up is ready For now </b>

# Rundown Day 5:
<p> Scaffolding, gave alot of thought into how to tackle this Everest the best possible way.</p><br>
<P>Because at first I was about to build the beginner guide first all the backend stuff too but I could not quite visualize how <br>the backend and frontend was going to shape so i though of just focusing on making UI and leaving it as a placeholder and working on it after all of it is completed I will then start working on backend properly I mean this is how I am going to tackle it</P>

# Rundown Day 6:
<p>Build succesfully the visa dynamic island it is very MVP atm haha, But I do believe that it's better than the prior plan I had in mind <br> so Visa Countodwn Feature initial Phase UI Done <br>
Also I have started working on Feature which deadass new, because This new feature is called the TV and it will stay at the main homepage so I thought It should be the one to be made first.
</p>
