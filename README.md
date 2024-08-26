# Program 7

## Program Description:  
>In the heyday of the Dunder Mifflin empire, Scranton used a monetary system based on schrute-bucks, stanley-nickels, and klevins.
>
>There were 20 klevins to a schrute-buck, and 12 stanley-nickels to a klevin.
>
>The notation for this old system used two decimal points, so that, for example, $5.2.8 meant 5 schrute-bucks, 2 klevins and 8 stanley-nickels.
>
>The new monetary system introduced after Kevin was deposed, consists of only schrute-bucks and stanley-nickels, with 100 stanley-nickels to a schrute-buck.  We'll call this new system decimal schrute-buck.
>
>Thus $5.2.8 in the old notation is $5.13 in decimal schrute-bucks (actually $5.1333333).  

- Write a program to convert the old schrute-bucks stanley-nickels klevins format to decimal schrute-bucks.
  - Use final variables for each conversion rate
- Choose variable names which are meaningful for this problem.

## Program Data:
N/A

## Statements Required: 
- Input
- Output
- Variable Assignment
- Final Variables

## Sample Output:
>Enter schrute-bucks:  7
>
>Enter klevins:  17
>
>Enter stanley-nickels:  9
>
> ----------------------------
>
>Decimal schrute-bucks = $7.89
>
>My Code:
>
>import java.util.Scanner;

public class Program{
    public static void main(String[] args){
        Scanner input = new Scanner(System.in);
        
        System.out.println("Enter schrute-bucks: ");
        int schruteBucks = input.nextInt();
        System.out.println("Enter klevins: ");
        int klevins = input.nextInt();
        System.out.println("Enter stanley-nickels: ");
        int stanleyNickels = input.nextInt();
        
        System.out.println("Decimal schrute-bucks = $" + convertMoney(schruteBucks, klevins, stanleyNickels));
    }
    
    public static double convertMoney(int schruteBucks, int klevins, int stanleyNickels){
        
        double total = schruteBucks;
        double newKlevins = klevins;
        newKlevins += (double) stanleyNickels / 12;
        total += newKlevins / 20;
        total *= 100;
        total = (int) (total + 0.5);
        total /= 100;
        return total;
    }
}//import stuff here

//Your code here

//Paste console output below:
/*
Enter schrute-bucks: 
7
Enter klevins: 
17
Enter stanley-nickels: 
9
Decimal schrute-bucks = $7.89

*/

