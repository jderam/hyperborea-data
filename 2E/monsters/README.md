# Monsters
Monsters are being processed in the following way:
* 00: Copy/paste raw monster text from PDF
* 01: For monsters that are presented in a group in the book, split them into an individual file for each monster
* 02: Generate a unique ID for each monster
* 03: First-pass parsing of data into a dictionary. Each field from the table gets parsed into a field. Description goes into a field.
* 04: Additional parsing. For example, attack rate contains both the number of attacks and the type of attack, That should be split, and it can be reassembled later for presentation. Number encountered has an additional value for in-lair, etc. Ascending AC can be added here.
* 04: Cleaning of description field. Save it as an HTML string. Replacement of certain weird characters will likely need to occur here.


## Output Data Goals
* file of JSON objects for each monster
* sqlite3 database with monsters table populated
