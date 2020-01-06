WeWalk (Web App)

There is so much complexity lol. Disguuuuuustingg.
Actually u can delete alot of the extra cases I've brought up. Unless u trynna go big with this XD.
Feel Free to make changes and updates over here as you build your project.
Gave you the gist. I try :'(
U should have asked them snobs :'(
Haven't finalized on backend for you.
Not sure abt which backend and database are the best tools rn.
firebase SDk is ghetto for spring boot. You could just use firebase for backend tbh. 
Bcz it has REST functionality to make calls to APIs. 
I'm srry I couldn't finalize your backend and database. I havent worked with spring boot or firebase.
You shld dig around some more
to decide what is best for project. But yeah I think you could just use firebase to connect everything.
It has a lot of extensions ig. 
I can update and assist with the design for backend, APIs, Databases. Still need to finalize these three.
Will wait on your edits.

Delete these texts :')

So,

back-end-> 

firebase, spring ()

or 

firebase for back-end too? (Simpler)

Ideas:
-----

Have search bar and time selection on different page than map page.
We could require users to give a specifc format like how they input destination and time. (Any other way u want to do?)
Collect those and store in database.
Use backend logic to figure out user matching and party notification.
Here three pages in web app. 

Basic Gist

1) Login
2) search bar for user destination & time selection . Extract user response & store in database (criteria for matching? Anything else?) 
3) Map Page with user live location and Buddy live location shared once match is approved.
   

or 

Have search bar and time slection and map on same page. 

Basic Gist

1) Login
2) Map Page with search bar & time selection. Extract user response & store in database. Map 
Page with user live location and Buddy live location shared once match is approved.


Basic Idea:
------
Pairs you with other people walking in same direction.

2 Page Application (Login Page & App Activity Page)


Front-End:
------

-> Login Page(Swift)

-> App Activity Page(HTML,CSS,Javascript, Use of backend to render map on page through API)
      1. Search bar and rest of page could be Map
      2. Refer to API Section.


Back-End:
------

Goal: 
Generates new information to front end to display to user. 
Communication layer between front end and (APIs or databases).

For Example:

Login Activity 
1.  Taking registration information from UI and putting in database
2.  Retrieving information from database to authenticate user on UI
      If login right,
        open App Activity Page
      else
        redirect to "Try Again" text appearing on Login Page.

App Activity
1. Connect to API endpoint url to get user live location data. Return info to UI App Activity Page and show marker.
2. Save live user location data in database under users id in database. 
#2 Do we need to keep track of user location in database?
Yes.. what if they never check out keep updating user location in database... 
If checked out, delete record of user location.


Logic:

  find all the users walking in same direction around the same time
    - User destination and time selection input in the search bar.
      Will be verified by some location API and saved in database.
      
  show all the options(people matched)
    - People matched on criteria of their input for time and destination. 
    - use backend to retrieve this info from database and make list of all possible matches
      from matching criterias of user Ids.
      
      If no available exact matches in database, 
      Can Make Exception for returning "No walking buddies in the Area" (Up to u? )
      
  user can choose person/people to walk with
    - Backend forwards list of matches to UI. 
      Decide how its gonna be displayed on maps page. 
      User chooses person.
      
  
  all the perties are notified
    - once user selects person.

hmmm r we trynn have multiple people walking together or only pairs.??


Spring & Swift & firebase or swift & Firebase??????


API:
------
Good Resource

Code for App Activity Page (Customize if you dont want
whole layout of page to be map) -> https://medium.com/risan/track-users-location-and-display-it-on-google-maps-41d1f850786e 

You have to register for Google API key. Link -> https://developers.google.com/maps/documentation/javascript/get-api-key

Have another copy of your project. Never upload your api key to github. Cuz there are dumb bots looking to scrape that key.
Others will steal your key and use it for themselves and u get billed. 
200$ credit is way more than enough and u dont have to worry cuz its free every month if u provide ur billing account.
I used for my scraper project. I got 100,000 requests free credit that resets. DW.
API key is just a string. In your git repo, keep my_api_key but in your other copy on computer keep the string so you can
connect to api.
Test ur web app locally with the api functionalities in the other copy. 

 Recommended

1) Google Maps Javascript API to display map on App Activity Page.
2) Geolocation API to retrieve user's live location.
3) Gonna sleep I'll come back to this.

Not sure if it supports as many browsers as Google. Prob less.  
Instead if you wanna embed maps into App Acitivity Page using Apple's API (shld be no problem) -> https://developer.apple.com/documentation/mapkitjs
1) MapKit JS


Databases:
------

Goal: To Authenticate user after registration (& select time??)

1. Storing Login Information 
2. Storing user live location in real time through firebase.
3. Database lookup?? Hmm IDEK
4. I have no experience.. Varshika🙄 this is ur domain … jk did some research. 
5. Firebase NoSQL Database? This lets you store and sync data between users in real time.
Will be perfect for matches which is dependent on destination of user and their preferred time.

Web App Hosting:
------

1. First, Test web functionality locally on computer.
2. If successful, deploy on Varshika's GitHub Pages Account.
3. Next step, maybe learn how to deploy on AWS (S3).


Potential IOS App?? 
------
Convert web app to mobile app.
Let's worry abt this later :'(

