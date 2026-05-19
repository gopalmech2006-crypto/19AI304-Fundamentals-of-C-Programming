LAB RECORD
Name: Gopal B
Register Number: 212224063001
Department: ECE
Date: __________
Experiment 1
Aim

To write a C program to read a string and count the number of vowels using a separate function.

Algorithm
Read the string from the user.
Pass the string to a function.
Check each character whether it is a vowel.
Count the vowels.
Display the total number of vowels.
Program
#include <stdio.h>

int countVowels(char str[]) {
    int i, count = 0;

    for(i = 0; str[i] != '\0'; i++) {
        char ch = str[i];

        if(ch=='a' || ch=='e' || ch=='i' || ch=='o' || ch=='u' ||
           ch=='A' || ch=='E' || ch=='I' || ch=='O' || ch=='U') {
            count++;
        }
    }

    return count;
}

int main() {
    char str[100];

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    printf("Number of vowels = %d", countVowels(str));

    return 0;
}
Output
Enter a string: Saveetha College
Number of vowels = 7
Result

Thus the program to count the number of vowels in a string using function was executed successfully.

Experiment 2
Aim

To write a C program to reverse a string without using library functions like strrev().

Algorithm
Read the string.
Find the length of the string manually.
Swap the characters from beginning and end.
Print the reversed string.
Program
#include <stdio.h>

void reverseString(char str[]) {
    int i, length = 0;
    char temp;

    while(str[length] != '\0') {
        length++;
    }

    length--;

    for(i = 0; i < length / 2; i++) {
        temp = str[i];
        str[i] = str[length - i - 1];
        str[length - i - 1] = temp;
    }
}

int main() {
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    reverseString(str);

    printf("Reversed string: %s", str);

    return 0;
}
Output
Enter a string: Hello
Reversed string: olleH
Result

Thus the program to reverse a string without using strrev() was executed successfully.

Experiment 3
Aim

To write a C program to check whether a given string is palindrome or not using functions.

Algorithm
Read the string.
Find the length of the string.
Compare characters from both ends.
If all characters are equal, it is palindrome.
Otherwise, it is not palindrome.
Program
#include <stdio.h>

int isPalindrome(char str[]) {
    int i, length = 0;

    while(str[length] != '\0') {
        length++;
    }

    for(i = 0; i < length / 2; i++) {
        if(str[i] != str[length - i - 1]) {
            return 0;
        }
    }

    return 1;
}

int main() {
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    if(isPalindrome(str))
        printf("Palindrome");
    else
        printf("Not Palindrome");

    return 0;
}
Output
Enter a string: madam
Palindrome
Result

Thus the program to check whether the string is palindrome or not was executed successfully.

Experiment 4
Aim

To write a C program to calculate the length of a string manually using function.

Algorithm
Read the string.
Traverse the string until null character.
Count each character.
Display the length.
Program
#include <stdio.h>

int stringLength(char str[]) {
    int count = 0;

    while(str[count] != '\0') {
        count++;
    }

    return count;
}

int main() {
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    printf("Length of string = %d", stringLength(str));

    return 0;
}
Output
Enter a string: Computer
Length of string = 8
Result

Thus the program to find the length of a string manually was executed successfully.

Experiment 5
Aim

To write a C program to count the number of words in a sentence using function.

Algorithm
Read the sentence.
Initialize word count as 1.
Traverse the sentence.
Increment count whenever a space is found.
Display the total number of words.
Program
#include <stdio.h>

int countWords(char str[]) {
    int i, count = 1;

    for(i = 0; str[i] != '\0'; i++) {
        if(str[i] == ' ') {
            count++;
        }
    }

    return count;
}

int main() {
    char str[200];

    printf("Enter a sentence: ");
    fgets(str, sizeof(str), stdin);

    printf("Number of words = %d", countWords(str));

    return 0;
}
Output
Enter a sentence: C programming is easy
Number of words = 4
Result

Thus the program to count the number of words in a sentence was executed successfully.
