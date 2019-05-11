## WP4 Markovian Haiku Generator
***
#### Final Product
<img src="dem1.png"      alt="icon"
 style="float: left; margin-right: 10px;" />
##### Generated with keyword: clean water
<img src="dem2.png"      alt="icon"
 style="float: left; margin-right: 10px;" />
##### Generated with keyword: economic china
<img src="dem3.png"      alt="icon"
 style="float: left; margin-right: 10px;" />
###### Generated with keyword: trump
<img src="dem4.png"      alt="icon"
 style="float: left; margin-right: 10px;" />
###### Generated with keyword: scandal
***
#### HTML parsing
The html parsing was done using the requests library which extracts the complete html and associated scripts from a given url. The url was constructed using the keyword, a story filter, and the Los Angeles Times website. Once that was extracted, the BeautifulSoup library was used to extract relevent information embedded within the html code. 
***
#### Markov chain generation
The markov chain is a way to probabilistically determine the most likely word to follow a given word. When the article is read into the program, a dictionary is generated to keep track of every word that follows a given word (a key) and the frequency. This allows for the random selection of a starting word and a weighted distribution that selects the next word. As such, this can generate an infinitely long, but at some point repetitive, string.
***
#### Syllable counter
The syllable counter was implemented as a simplistic function that could capture a majority of the words provided. A major shortcoming is its inability to account for abbreviations, numerals, and contractions. Such an effort would require breaking down words into their component phonemes and analyzing those for syllabic properties. 
***
#### Poem generator
The poem generator attempts a Haiku under the traditional, but not strict, structure of the 5-7-5 syllable count. When generating the string from the markov chain, if there is no word in the probability distribution that has the right amount of syllables to make it fit into either the five or seven syllable count, then the program will keep selecting new keys (source words) until it finds a match. Before moving on to a new key however, it will iterate over the key's values a maximimum of 10 times. 
***
#### Graphical User Interface
The GUI was made using the tkinter library which interfaces well with python. While the end product appears rather simplistic in terms of design, the GUI is meant to capture the essence of the project and make navigating the program self-explanatory. 
***
#### Key takeaways
Overall, this project has allowed me to branch out and explore different libraries. I also created a virtual environment to encapsulate all the package requirements to allow for better portability. The code is well-commented where it is complex and the rest is intuitive (as seen in variable and function names). 
