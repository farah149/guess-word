  #include <iostream> 

 #include <string> 

  // guess word game 

 using namespace std; 

  

 int main() { 

     string word = "algorithm"; 

     int numGuesses = 15; 

     int numLetters = word.length(); 

     string guessedWord(numLetters, '_'); 

     char letter; 

  

     cout << "Welcome to the game!" << endl; 

     cout << "The word has  9 letters" <<endl; 

     cout << "You have " << numGuesses << " guesses to try to guess them." << endl; 

     cout << "The word is: " << guessedWord << endl; 

  

     while (numGuesses > 0 && guessedWord != word) { 

         cout << "Enter a letter: "; 

         cin >> letter; 

  bool correctGuess = false; 

  

  

         for (int i = 0;  i < numLetters; i++) { 

             if (word[i] == letter) { 

                 guessedWord[i] = letter; 

                 correctGuess = true; 

             } 

         } 

  

         if (correctGuess) { 

             cout << "great guess!  the letter is in the word : " << guessedWord << endl; 

         } else { 

             numGuesses--; 

             cout << "Sorry, that letter is not in the word. You have " << numGuesses << " guesses left." << endl; 

         } 

     } 

  

     if (numGuesses == 0) { 

         cout << "Sorry, you ran out of guesses. The word was " << word << "." << endl; 

     } else { 

         cout << "Congratulations! You guessed the word!" << endl; 

     } 

  

     return 0; 

 }   
