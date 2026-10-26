There are 2 main steps:
- training
- testing

# training
 1. input text
 2. assign random values for every word
 3. every time you see a word x:
    - use its node or create one if the word doesn't exist
    - look at the words around it
        - connect it to every word around it: y with connection z
        - then change the connection strength:
        - WORD IMPORTANCE ALGORITHM:
            - if there exists y already has relationships
                - look at its position
                - the less connections it has the stronger it is ( means it is specific )
        - save the strength of the connection by changing the value of connection z
        - make x and y closer by a bit based on connection strength and difference between position in the sentences
        - : Animals are good. Humans like cats
        - :   0.     1.   2.    3.     4.   5.


# Testing
- Pass "Animals are good. Humans like "
- Rank words based on importance using the same algorithm in training: WORD IMPORTANCE ALGORITHM
- Search for words that point at the same top 4-6 words
- Eg in our example: look for a word that points at: animals, humans, like, good
- and then return it


