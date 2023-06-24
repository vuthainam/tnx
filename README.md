My solution is pretty simple, while generating TNX data in a loop, also create/update dictionary for each requirement/function, i.e:
- TsDict: the key is a unique TS value and the value of each key is correspondence corresponding list of TNX objects
- UserPointDict: the key is a unique Username and the value of each key is the total point of the corresponding User
- DateDict: Calculate date value base TS value and return as a string, then add it into DateDict within the calculation Total Point of that date and init/update UserDict (key is Username, value is a list of TNX objects of the user in that date).
Then store all the Dictionaries in IndexedDb.
In the end, every time you want the result for each requirement/function, just need to query the corresponding dictionary within input data as the dictionary key.

Because the time complexity to query data from IndexedDb for each dictionary is really simple so I decided just to share the context/description of the solution without the actual implementation, time complexity documentations and benchmark results.
