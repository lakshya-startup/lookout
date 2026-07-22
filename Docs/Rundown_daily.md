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

# Rundown Day 7: New Apporach --> Documentaion
<P> 

## 1: What & Why

What is it? The TV Feature is a place where promotional items sit, advertising like one of those big billboards. 

Why build it? All these advertisements help users find something special they are lowkey looking for or just finding the right fit. Say you want a hoodie or you're heading out for groceries using our app—mind you, this isn't the main feature, it's just something you stumble on while engaging with our service. You look and see "Hey, in Pak'nSave there is a clearance and $5 sale on most things!" So it saves you from missing out big time. These local sales don't typically appear in YouTube ads or Instagram reels. It keeps you included on what's going on in your community. Plus, so many things can generate from that, even conversation starters. If you stay at home and only go into the office for one day, you actually have something to talk about like "Hey, did you guys go to that Pak'nSave sale?" 

* Local Value: Catches real deals and community hype that big social media ads miss.
* Conversation Starter: Gives people real-world topics to connect on.
* Ambient Discovery: Something you stumble on naturally while using the app.

## 2: Obstacle & Resolution

Used PageView at first, which was weird, but because I am new to FlutterFlow I thought that would be the right fit. But it's in the name itself—PageView—so I dropped that thought, researched a bit, and found the Carousel widget. It works like an online billboard where ads stay in rotation, giving about 5-6 seconds for one ad to stay before looping to the next one with smooth animation. It also lets you add more pages for extra ads down the line.

* The Fix: Switched from PageView to the Carousel widget for smooth looping and timed rotations.
* The Structure: Created the TV inside the Stack and Column, holding a Container with the Carousel inside.

## 3: Next Action

Complete the bottom navigation bar just like any other app. If you swipe right, there's a page for that, and at the bottom there's the name or picture of that page. We're building about five pages for this. 

The main page will be the one holding the TV and Visa Countdown Feature. At the bottom, the nav bar stays stagnant—meaning if you swipe right, the page changes, but the nav stays put. The nav item's name or icon just scales up a bit with a slight margin shift if it's the current page we're in, giving it that pop effect.

* Build out all 5 pages linked to the bottom nav.
* Keep the nav bar static while background pages swipe underneath.
* Add dynamic scaling and margin shifts so the active page name/icon pops.

# Rundown Day 8: Layered Z-Stack Navigation System

## 1. What & Why

What is it? It's our custom horizontal navigation system using a layered Z-Index Stack layout in FlutterFlow. It lets users swipe naturally between 5 main app pages while keeping the bottom navigation bar permanently pinned at the bottom of the screen.

Why build it this way? Default page navigation can feel super basic or jarring when whole screens just pop in and out. By making a full-screen PageView the base layer of a Stack and pinning our custom bottom bar on top, the background pages slide seamlessly like a game canvas while the controls stay steady under your thumbs. On Index 2 (our main Homepage), we dropped in our hard-earned features from yesterday—the TV Billboard and the Visa Countdown card. Setting it up like this keeps the UI feeling ultra-fluid, modern, and sticky, giving the app a clean interactive vibe while keeping all 5 core sections easily reachable.

* Seamless Flow: Background pages swipe smoothly while the main navigation stays fixed right where you need it.
* True Layering: Puts the core interactive features like the TV Billboard and Visa Countdown right on the Homepage (Index 2) without messing up navigation.
* Clean Architecture: Keeps screen transitions fluid without relying on heavy default navigation bars that reload the whole view.

## 2: Obstacle & Resolution

The main challenge was figuring out how to keep the bottom navigation bar static while swiping through pages. If you put the navigation bar inside the PageView itself, it swipes away with the page, which completely ruins the native bottom-bar feel. 

To fix this, I made the PageView Layer 1 (the background) inside a master Stack with 5 page indexes. Then, I placed the bottom navigation layout on Layer 2 (the foreground) outside the PageView, pinning it directly at coordinates Y:1, X:0. Inside that container, I built a Row set to space elements evenly, holding 5 custom Columns that act as our tap targets. Instead of using standard buttons, each Column holds a custom Container with an On Tap action hooked up to handle state changes and jump the PageView smoothly.

* The Mistake: Realizing that putting nav controls inside the PageView causes them to swipe away with the screen content.
* The Structure: Separated the layout into a 2-layer Stack—Layer 1 holds the 5-index PageView, while Layer 2 holds the fixed navigation overlay at Y:1, X:0.
* Custom Controls: Built 5 evenly spaced Columns with custom actionable Containers instead of default FlutterFlow buttons for complete design control.

## 3: Next Action

Now that the master Z-Stack structural layout is built and the Homepage content is sitting clean on Index 2, we need to complete the two-way logic synchronization across all 5 pages.

We need to make sure tapping any of the 5 custom navigation containers updates the `currentTab` App State variable and immediately fires a `Control PageView -> Jump To` action to snap to the correct index. Once that two-way sync is locked in, we'll implement our dynamic tab sizing (`IF currentTab == index THEN height 60 / margin 12 ELSE height 44 / margin 0`) so the active tab visually pops up when you're on that page.

* Wire up On Tap actions on all 5 custom nav containers (Set `currentTab` App State + `Jump To` PageView Index).
* Verify swiping the PageView manually updates the `currentTab` state to match the bottom bar.
* Apply dynamic active-state styling (height and margin shifts) so the current tab pops out smoothly.
