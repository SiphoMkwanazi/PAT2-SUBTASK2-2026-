# PAT2-SUBTASK2-2026-
Translation of a short message into morse code
#include <iostream>
#include <string>
#include <cctype>

using namespace std;

// Function to translate English letters into Morse code
string getMorseCode(char ch)
{
switch (toupper(ch))
{
case 'A': return ".-";
case 'B': return "-...";
case 'C': return "-.-.";
case 'D': return "-..";
case 'E': return ".";
case 'F': return "..-.";
case 'G': return "--.";
case 'H': return "....";
case 'I': return "..";
case 'J': return ".---";
case 'K': return "-.-";
case 'L': return ".-..";
case 'M': return "--";
case 'N': return "-.";
case 'O': return "---";
case 'P': return ".--.";
case 'Q': return "--.-";
case 'R': return ".-.";
case 'S': return "...";
case 'T': return "-";
case 'U': return "..-";
case 'V': return "...-";
case 'W': return ".--";
case 'X': return "-..-";
case 'Y': return "-.--";
case 'Z': return "--..";

// Space between words
case ' ': return "/";

// Numbers
case '0': return "-----";
case '1': return ".----";
case '2': return "..---";
case '3': return "...--";
case '4': return "....-";
case '5': return ".....";
case '6': return "-....";
case '7': return "--...";
case '8': return "---..";
case '9': return "----.";

// Invalid characters
default: return "[UNKNOWN]";
}
}

int main()
{
string message;

// Program heading
cout << "======================================" << endl;
cout << " MORSE CODE TRANSLATOR " << endl;
cout << "======================================" << endl;

// Background information
cout << "\nAbout Morse Code:" << endl;
cout << "Morse code is a communication method" << endl;
cout << "that uses dots (.) and dashes (-) to" << endl;
cout << "represent letters, numbers, and symbols." << endl;
cout << "It was developed in the early 1830s." << endl;

// Examples
cout << "\nExamples of Morse Code:" << endl;
cout << "A = .-" << endl;
cout << "B = -..." << endl;
cout << "C = -.-." << endl;
cout << "D = -.." << endl;
cout << "E = ." << endl;

// User enters message
cout << "\nEnter a short message in English:" << endl;
getline(cin, message);

// Display Morse code translation
cout << "\nTranslated Morse Code:" << endl;

for (int i = 0; i < message.length(); i++)
{
cout << getMorseCode(message[i]) << " ";
}

cout << endl;

// End of program
cout << "\nTranslation completed successfully." << endl;

return 0;
}
. 

