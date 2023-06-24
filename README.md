My solution is pretty simple, while generating TNX data in a loop, also creating/updating dictionay for each requirement/function, i.e:
  - TsDict: which the key is unique TS value and value of each key is correspondance corresponding list of TNX objects
  - UserPointDict: which the key is unique Username and value of each key is total point of corresponding User
  - DateDict: Calculate date value as a string base TS value, then add it into DateDict within the calculation Total Point of that date and init/update UserDict (key is Username, value is list of TNX objects of user in that date).
Then store all the Dictionaries in IndexedDb.
At the end, every time you want the result for each requirement/function, just need to query corresponding dictionary within input data as dictionary key.

Because of the time complexity to query data from IndexedDb for each dictionary is really simple so I decided just share the context/description of the solution without the actual implementation.
