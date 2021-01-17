# PracticeWeek9



Q1:--------


// Java program to find a triplet 
class FindTriplet { 
  
    // returns true if there is triplet with sum equal 
    // to 'sum' present in A[]. Also, prints the triplet 
    boolean find3Numbers(int A[], int arr_size, int sum) 
    { 
        int l, r; 
  
        // Fix the first element as A[i] 
        for (int i = 0; i < arr_size - 2; i++) { 
  
            // Fix the second element as A[j] 
            for (int j = i + 1; j < arr_size - 1; j++) { 
  
                // Now look for the third number 
                for (int k = j + 1; k < arr_size; k++) { 
                    if (A[i] + A[j] + A[k] == sum) { 
                        System.out.print("Triplet is " + A[i] + ", " + A[j] + ", " + A[k]); 
                        return true; 
                    } 
                } 
            } 
        } 
  
        // If we reach here, then no triplet was found 
        return false; 
    } 
  
    // Driver program to test above functions 
    public static void main(String[] args) 
    { 
        FindTriplet triplet = new FindTriplet(); 
        int A[] = { 1, 4, 45, 6, 10, 8 }; 
        int sum = 22; 
        int arr_size = A.length; 
  
        triplet.find3Numbers(A, arr_size, sum); 
    } 
} 



Q2:--------

#include <stdio.h>
#include <string.h>
#include <stdlib.h>
 
int main ()
{
    char str1[100], str2[100], str_rem[100];
    int i = 0, j = 0, k = 0;
 
    printf ("Enter the First string:\n");
    fflush (stdin);
    gets (str1);
 
    printf ("Enter the Second string:\n");
    gets (str2);
 
    for (i = 0; str1[i]!= '\0'; i++)
    {
        for (j = 0; str2[j] != '\0'; j++)
        {
            if (str1[i] == str2[j])
            {
                continue;
            }
            else
            {
                str_rem[k] = str2[j];
                k ++;
            }
        }
        str_rem[k] = '\0';
        strcpy (str2, str_rem);
        k = 0;
    }
 
    printf ("On removing characters from second string we get: %s\n", str_rem);
 
    return 0;
}




Q3 ----------


public static String IntegerToRomanNumeral(int input) {
    if (input < 1 || input > 3999)
        return "Invalid Roman Number Value";
    String s = "";
    while (input >= 1000) {
        s += "M";
        input -= 1000;        }
    while (input >= 900) {
        s += "CM";
        input -= 900;
    }
    while (input >= 500) {
        s += "D";
        input -= 500;
    }
    while (input >= 400) {
        s += "CD";
        input -= 400;
    }
    while (input >= 100) {
        s += "C";
        input -= 100;
    }
    while (input >= 90) {
        s += "XC";
        input -= 90;
    }
    while (input >= 50) {
        s += "L";
        input -= 50;
    }
    while (input >= 40) {
        s += "XL";
        input -= 40;
    }
    while (input >= 10) {
        s += "X";
        input -= 10;
    }
    while (input >= 9) {
        s += "IX";
        input -= 9;
    }
    while (input >= 5) {
        s += "V";
        input -= 5;
    }
    while (input >= 4) {
        s += "IV";
        input -= 4;
    }
    while (input >= 1) {
        s += "I";
        input -= 1;
    }    
    return s;
}


Q4:--------------




// Java program to print diamond pattern 
import java.util.Scanner; 
  
class Pattern { 
    void display(int n) 
    { 
        // sp stands for space 
        // st stands for number 
        int sp = n / 2, st = 1; 
  
        // Outer for loop for number of lines 
        for (int i = 1; i <= n; i++) { 
  
            // Inner for loop for printing space 
            for (int j = 1; j <= sp; j++) 
                System.out.print(" "); 
  
            // Inner for loop for printing number 
            int count = st / 2 + 1; 
            for (int k = 1; k <= st; k++) { 
                System.out.print(count); 
                if (k <= st / 2) 
                    count--; 
                else
                    count++; 
            } 
  
            // To goto next line 
            System.out.println(); 
            if (i <= n / 2) { 
  
                // sp decreased by 1 
                // st increased by 2 
                sp = sp - 1; 
                st = st + 2; 
            } 
  
            else { 
  
                // sp increased by 1 
                // st decreased by 2 
                sp = sp + 1; 
                st = st - 2; 
            } 
        } 
    } 
  
    // Driver code 
    public static void main(String[] args) 
    { 
        Pattern p = new Pattern(); 
        int n = 7; 
        p.display(n); 
    } 
} 



