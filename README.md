# JS-Class-Camping
Constructor have these 4 properties:

 - organizer - type string

 - location - type string

 - priceForTheCamp - {"child": 150, "student": 300, "collegian": 500}

 - listOfParticipants - empty array

At the initialization of the SummerCamp class, the constructor accepts the organizer and location. The priceForTheCamp is an object, the submitted values are by default and represent the price for the stay in the camp depending on the condition of the participant ("child", "student", "collegian").

Class methods: 

registerParticipant (name, condition, money):

This method register participant to the camping and accepts 3 arguments:

- name (string);
- condition (string);
- money (number);

If the given condition of participants, is not present in priceForTheCamp object with the specified default values ("child", "student", "collegian"), an error will be thrown;

If the name of the current participant is already present in listOfParticipants array, return the respective message;

If the submitted money is less than the price for the stay in the camp (the price is determined by the priceForTheCamp object, depending on the condition of the participant), return the following message:
`The money is not enough to pay the stay at the camp.`;

Otherwise, should add the participant, with properties: {name, condition, power: default 100, wins: default 0} to the listOfParticipants array and return message;

unregisterParticipant (name):

This method removes a participant from the camping and accepts 1 argument:

- name (string);

If the name of the current participant is not present in listOfParticipants array, an error with message will be thrown;

Otherwise, this function should remove the participant from the listOfParticipants array and return message;
                

timeToPlay (typeOfGame, participant1, participant2):

Method can take 2 or 3 arguments depending on the type of game:

- typeOfGame (string);
- participant1 - name (string);
- participant2 - name (string) - optional;

There are two possible types of games:

WaterBalloonFights -> you will get two players.

Note: The condition of the participants must match (Example: "Petar" - "child" and "John" - "child") 

Battleship -> you will get one player.

•	If any of the submitted participants names are not present in listOfParticipants array, an error with the following message should be thrown;
                   
•	If two names are submitted, check that the participants' condition matches, if not matched, an error with the message should be thrown;
                  
•	If the type of game is Battleship increase the power property of the participant by a value of 20, and return the message;
 

•	If the type of game is WaterBalloonFights, you must check whether the value of the power of one participant is greater than the value of the power of the other participant, and in this case increase the value of the wins property by one per winner (with the bigger power), and return the message:
       
               Note: The {name} is the name of the winner in this game.

•	Otherwise, the function returns the message:

                 `There is no winner.`

