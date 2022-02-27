# wordle
This is a complete hack for Wordle.
The following is what you need to do to solve a Wordle challenge.
We assume that in every Wordle challenge, the secret word is one among the 5757 5-letter English words given here: https://www-cs-faculty.stanford.edu/~knuth/sgb-words.txt

We have a file Worlde.txt given in this project. 
Each line in the file contains a sequence of words used to solve a single word in the dictionary.
For example, for the word "teams" you can see a line "tares 21012 alack 10200 abate 10211 teams".
This means that you answer the challenge by asking the word "tares". Then, if the secret word is teams, the answer by the Wordle server will be 21012 - 2 stands for Green, 1 stands for Yellow, and 0 stands for Grey. Then your question must be alack for which the answer from the server will be 10200, and so on.
Now to solve a secret word, you just ask "tares" and then search with the answer given by the Server.

An example is given below:
I ask "tares"
The system replies "02000" (Grey, Green, Grey, Grey, Grey)
I search "tares 02000" in the file wordle.txt. Then I can see that the next word is "pylon", then I ask "pylon".
The system replies "00011".
Then I search "tares 02000 pylon 00011". I see that "aargh" is the next word, I ask it.
The system replies "12020"
Then I search "tares 02000 pylon 00011 aargh 12020". Then I see that the word is "mango"
The system replies "22222" and I win.
