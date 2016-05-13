# capstone-ideas

### Interior Design App

- Ability to select furniture items from a dropdown list, with included LxWxH measurements.
- Select the size of the room,
- add windows, doors, heating vents, etc.
- drag and drop furniture items onto the room
- save room layouts as JSON (possibly Mongo?)

  - Potentially, when you select the length and width of the room, it will create an array of arrays, with each index of the array representing one square foot.  Therefore, if you have a bed that is 6 feet long, it would take up 6 indexes in the array, potentially one per array (representing a row/column in the room).
- Possibly use ionic framework and mongo for storage.


### Social Media App

- Reddit type forum posts, but have a custom profile.  The "news feed" is topics or posts from forums that you watch/like, or similar things.
- Not sure how to implement this, would need lots of seed data for a forum.
- Angular front end, Express/Node back end, probably Mongo storage, so that there can be an array of posts, and each post can have comments, and they can basically nest from there.


### Code Challenge w/ Sockets

- Build an app with sockets that shows you a coding challenge and lets you get into a room with your friends to solve it.  You can have a personal profile, which tracks the number of challenges you've taken part in, the number you've won, and the number of points you have total.  Finishing the challenge first (with correct answer) gets you 5 points, second gets 3 points, and third gets 1 point.  You can still finish the challenge even if you're not the first 3, you just don't get points.
- Use social auth to log in (Satellizer), and maybe have access to your friends list to invite people?  also to start could just have a randomly generated url that connects the people into the room.
- Users can upload a photo of themselves, or it can pull the facebook profile pic as their personal profile photo
- the profile will track the number of points they have.
- maybe have a global leaderboard showing the top 5 people by points.
- Need to come up with a way to score the answer, or just focus on speed.
- probably use mongo to store scores as an array on the user object, otherwise could use psql to have a users table, and then a scores table with a user ID associated, and then just grab all the rows with that user ID to sum the points and such.
  - need to figure out a way to validate that the code is correct
    - could possibly use either hackerrank API or hackerearth run API.
      - Pass the typed code to the API along with what the desired output is, it runs the code and then tells if the output that it comes back with matches the desired output.
        - not sure about if there's a way to run tests on the functions, or what the structure of the programming challenges would have to be.
  - also need to figure out how to write angular end to end and unit tests in order to build the API that saves and sets the scores.
  - the project will use Angular for the front end, Sockets.io for communication, Node/Express backend, and either Mongo or Psql for the database.  Probably Sattelizer or OAuth for social authentication also.
    - Could also sort of change this up to be a study app that asks you questions and you have to tell what the output should be, sort of like our in-class trivia.

#### User Stories
1. As a user, I want to be able to go to a home page without being logged in.
1. As a user, I want to be able to have a sign up button/page to register
1. As a user, I want to be able to sign up with social authentication
1. As a user, I want to have a sign in button with social authentication
1. As a user, I want to see an example problem/solution on the landing page.
1. As a user, I want to have a navigation bar with multiple features.
  - Create a game
  - Invite a friend to a game
  - Join a friends game
1. As a user, I want to be able to have a code block section to type my solution into
1. As a user, I want to be able to see when my friends have finished the challenge, but not their answer.
1. As a user, I want to have a show hint button that gives me some help with the challenge.
1. As a user, I want to be able to have a user profile.
1. As a user, I want my user profile to track my points earned.
1. As a user, I want my user profile to track how many challenges I've completed.
1. As a user, I want my user profile to track how many challenges I've been the first to complete.
1. As a user, I want to be able to challenge friends via email invite.
1. As a user, I want to be able to compete in challenges with online players.



### Something LoL API based

- maybe a stats site where you can go on and track your friends and your stats, and compare them?


### Social media analytics dashboard

- possibly a mobile app
  - using ionic framework
  - this would allow you to set fan goals for pages, like goals, etc, and let you know how close you are to achieving these goals.


### Electron based Desktop Application in Javascript

- Possibly a media server, or a streaming API for movies on your hard drive or on your network
  - Wrapper for VLC to create embedded video player?


### Movie database iPhone app

- Can use the camera to take pictures of barcodes and look up the movies
- Have a database of your own movies
- Going to use Guidebox API to find streaming sources for each movie that you search for
- Use ionic framework to wrap the app natively.
  - ngBarcodeScanner is an Ionic tool to use the camera to be a barcode scanner.
- Users will have the ability to search for movies via barcode or search box.
  - The search will query the OMDB API for movie info and image, and then will query the guidebox API for streaming sources.
  - Users can add movies to their collection, ideally would be like, DVDs they own, or movies they have access to.
  - Could also have a tab in the app for movies they've seen, and could pull data on how many times in a year they've watched certain movies?
- Going to use Mongo for the backend, each user will have an object, and users can have an array of movies in their collection,
  - and each movie in the collection array will be an object with all the OMDB api info.
- Users can randomly generate a movie from their collection
- Users can filter the collection, or can search the collection.
- Using Angular.JS for the front end, with Ionic.
- Using Node.js, Express, and Mongo for the back end.  The back end will be a separate Repo and will basically just be building the API for my project, which queries the other two APIs as well as my DB.
- This API will be hosted probably on Heroku, and then my angular app will just make $http calls to my own API.
