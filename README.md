# Hackathon2
## 1. Project Description:
   
"Unexpected Encounters" is an interactive multiplayer game about relationships and making decisions. Players are involved in various settings in which they encounter the main character, Jackson.

In the game, players can select from options (Option A, B or C), each with a score that influences their relationship with Jackson. Players actively create the storyline by navigating their character's journey and changing their relationship with Jackson. Players are encouraged to invest their emotions and thoughts in the game.

Embark on this exciting journey to discover a multitude of chapters and scenes set in various locations. From the bustling basketball court to the serene library, the cosy cafe to the enchanting cinema, and the thrilling theme park, each unique setting offers a new and engaging experience. 

Immerse yourself in the interactive storyline, where your decisions throughout the game will turn into multiple possible outcomes. Every decision shapes the narrative and influences your character's relationships and ultimate destiny. This dynamic and branching storyline ensures high replay value, inviting you to explore different paths and uncover different results of the game.


## 2. Project Features:

a. Multiple Player Game 

- A two-player game in which each participant independently makes decisions.

b. Saving and loading history capabilities

- Choose options (Y or y) to continue the game or (N or n) to quit the game after each chapter. If the player chooses to quit the game, the player can save their game progress and resume where they left off at a later time for convenience and continuity. The game progress is stored into two files, each file for each player. Everytime the game starts, the two files that store players’ data will be read by the program, if there is data inside the file, the data (places and action players choose) will print out and players can continue to the chapters or places they haven’t explored, otherwise if there is no data inside, players will start the game from the beginning.

c. Diverse Chapters and Scenes Set in Several Locations

- Explore a series of diverse chapters and scenes set in several locations. Play the game's interactive storyline as you delve into settings like a basketball court, library, cafe, cinema, and theme park. Each location has different scenes and options for players to shape their relationship with our main character and influence the outcome of the game.


d. Choice-based Gameplay

- Choose options (A, B, or C) that correspond to your character's behaviours, thoughts, and emotions when making decisions at crucial points in time.

e. Establishing relationships

- Use action options to engage with Jackson and other characters in order to forge bonds and shape the dynamics of the interactions in the game.


f. Friendly User Interface

- Use an easy-to-use user interface to move through scenes, read descriptions, and make decisions.


## 3. Project Specification:

### 1. Input
   
a. From User:

i. Players choose options (Options A, B, or C) in each scene of the game.

ii. Players choose to continue (Y or y) or quit (N or n) the game after each chapter.

b. From File:

i. Previously saved game data information which are the players’ options (Options A, B, or C) for each scene

ii. Previously saved game data information which are the completed chapters for continuity.

## 2. Process
a. Calculate accumulated marks based on the players' options in each scene.

b. Compare the total marks of the players to determine the strength of their relationship with the main character.

c. Determine whether players have a stronger, weaker, or the same strength of relationship bond with the main character.


## 3.Output

a. Display the accumulated marks for each player after each chapter ends.

b. Display the total accumulated marks at the end of the game.

c. Display whether players have a stronger, weaker, or the same strength of relationship bond with the main character.


## 4.Constraints

a. Players can only choose options A, B, or C in each scene.

b. Players can only choose to continue (Y or y) or quit (N or n) after each chapter.


## 5. Assumptions
a. The game consists of 5 places or chapters, with each chapter having 2 scenes.

b. Each option has a different scoring, which can be positive or negative.

c. The total score for each player is the sum of their scores after each chapter, considering the choices made in each scene.

## 6. Formula

a. Total score = Total score + Score obtained in each scene.


## 4. Object-oriented Concept:

- The game consists of  9 classes:
  
a. FileInclusion (composition class Place) : read the two files that stores historical data, return number of places that the players has go 

b. Place: set the place name, scene1, scene2, action1 and action2 by the values that pass from class BasketballCourt, Library, Cafe, Cinema and ThemePark and pass these values to the HistoryList to append the list node.

c. PlaceList (inherited from class HistoryList and class Place) : used to link a place to the next place when the players want to continue the game.

d. HistoryList : implement a linked-list, append a list node when the players go to one place and write the data that is stored in the linked-list into the players’ history file when the game is ended by the players.

e. BasketballCourt (composition of class Place) : print out the setting and scene in basketball court and get the players’ action

f. Library (composition of class Place): print out the setting and scene in library and get the players’ action

g. Cafe (composition of class Place): print out the setting and scene in cafe and get the players’ action

h. Cinema (composition of class Place): print out the setting and scene in cinema and get the players’ action

i. ThemePark (composition of class Place): print out the setting and scene in theme park and get the players’ action


## 5. Data structures(Linked-list):

Linked list data structure is used in our game. A dynamic linked-list is implemented jin class ‘HistoryList’ so that it can grow and shrink during the program execution. Each node consists of five string data which are placeName, scene1, scene2, action1 and action2 and a pointer to the next node in the list. A default constructor initialise the head There are 4 member functions to manipulate the linked-list:

a. ‘appendListNode1’: appends new node to the end of the list for player 1

b. ‘appendListNode2’: appends new node to the end of the list for player 2

c. ‘writeListNode1’: open the file that stores historical data for player1 and write the contents of the linked list into the file

d. ‘writeListNode2’: open the file that stores historical data for player2 and write the contents of the linked list into the file


## 6. How the Game Play (put image here)
![image](https://github.com/Sjjjiie/Hackathon2/assets/118896986/e375b005-451f-4545-800e-849cd763742c)


## 7. Link of the Gameplay
