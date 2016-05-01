# capstone-ideas

Interior Design App

- Ability to select furniture items from a dropdown list, with included LxWxH measurements.
- Select the size of the room,
- add windows, doors, heating vents, etc.
- drag and drop furniture items onto the room
- save room layouts as JSON (possibly Mongo?)

  - Potentially, when you select the length and width of the room, it will create an array of arrays, with each index of the array representing one square foot.  Therefore, if you have a bed that is 6 feet long, it would take up 6 indexes in the array, potentially one per array (representing a row/column in the room).
- Possibly use ionic framework and mongo for storage.


Social Media App

- Reddit type forum posts, but have a custom profile.  The "news feed" is topics or posts from forums that you watch/like, or similar things.
- Not sure how to implement this, would need lots of seed data for a forum.
- Angular front end, Express/Node back end, probably Mongo storage, so that there can be an array of posts, and each post can have comments, and they can basically nest from there.


Code Challenge w/ Sockets

- Build an app with sockets that shows you a coding challenge and lets you get into a room with your friends to solve it.  You can have a personal profile, which tracks the number of challenges you've taken part in, the number you've won, and the number of points you have total.  Finishing the challenge first (with correct answer) gets you 5 points, second gets 3 points, and third gets 1 point.  You can still finish the challenge even if you're not the first 3, you just don't get points.
  - need to figure out a way to validate that the code is correct
    - could possibly use either hackerrank API or hackerearth run API.
      - Pass the typed code to the API along with what the desired output is, it runs the code and then tells if the output that it comes back with matches the desired output.
        - not sure about if there's a way to run tests on the functions, or what the structure of the programming challenges would have to be.
        - Could also sort of change this up to be a study app that asks you questions and you have to tell what the output should be, sort of like our in-class trivia.
        
