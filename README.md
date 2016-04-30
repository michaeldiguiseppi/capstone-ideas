# capstone-ideas

Interior Design App

- Ability to select furniture items from a dropdown list, with included LxWxH measurements.
- Select the size of the room,
- add windows, doors, heating vents, etc.
- drag and drop furniture items onto the room
- save room layouts as JSON (possibly Mongo?)

  - Potentially, when you select the length and width of the room, it will create an array of arrays, with each index of the array representing one square foot.  Therefore, if you have a bed that is 6 feet long, it would take up 6 indexes in the array, potentially one per array (representing a row/column in the room).
