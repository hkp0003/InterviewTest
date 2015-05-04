interview-take-home-test
========================
## First Things First
Hello and welcome! This 'take home' is a way for us to evaluate your skills as a developer. 

Please follow
[these instructions](https://help.github.com/articles/duplicating-a-repository)
for creating a place to work on this test. More explicitly please do not use the built-in GitHub fork functionality. Make your repo private in the github settings, and add users @DevonGleeson
and @DavidWhitlock as contributors, so we can see your results. If you don't have a GitHub account that allows you to create private repositories, and are a recent graduate, or are still in school consider [this](https://education.github.com/discount_requests/new). If none of these are options, please make your commits in a local repository, then email us with a copy of the repository.

### Running
From the command line start the server by running this command:
```bash
./gradlew runServer
```
Once the server us running, in another terminal window, you can start the client with this command and the client will begin accepting user input from the keyboard:
```bash
./gradlew run
```
You can run the unit tests in the system by running this command:
```bash
./gradlew test
```
If you'd prefer to use Intellij IDEA, you could generate the project files using this command line:
```bash
./gradlew idea
```
### The problem
The server accepts arbitrary strings from the client. Currently the strings are just echoed back. I'd like you to add a feature to this system: When the server recieves a string it should return the starting location and length of the longest contigous repeated character. Please add more unit tests for the feature you are writing. 

Example ```aaabbbbbbcccc``` will output ```(3, 6)```.

Bonus points! Make the server multi-threaded.

### Metrics for evaluation
We will be evaluating this project on:
* comprehension (how well you filled out the below questions) 
* unit tests are all passing
* code review of design, comments, maintainability.

### Describe the System
My code takes the user input and converts it into a char array. Arfter which I sort the array and store the longest char repetition and it's "counter" as I iterate through the array while checking equalities. If another char has a longer sequence, I swap the longest stored char, and add 1 to it's "counter". As for the number of chars, I just add to my charCounter whenever I iterate the array and find an inequality.

### Test Plan
I used a TDD method for my test cases. For my test cases I wanted to cover extremities as well as basic functionality and special characters.
