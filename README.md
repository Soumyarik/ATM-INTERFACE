# ATM-INTERFACE

import java.util.*;
class Main
{
    static void AtmDisplay( double balance,int option)
    {


          switch (option) 
          {
            case 1:
                System.out.println(" Your Current Balance : " + balance);
                   break;
            case 2:
                 double deposite = 0;
                 Scanner sc = new Scanner(System.in);
                 System.out.println("Balance : " + balance); 
                  System.out.print("Enter Your Deposit Amount : ");
                   deposite = sc.nextDouble(); 

                   deposite = deposite + balance;

                   System.out.print("Your Current Balance is: " + deposite);
                    break;
            case 3:
                 double Widrawl = 0;
                 Scanner sb = new Scanner(System.in); 
                 System.out.println("Balance : " + balance);
                 System.out.print("Enter  the amount you want to withdrawal : ");
                 Widrawl = sb.nextDouble();

                 if(balance>Widrawl)
                 {
                    Widrawl = balance - Widrawl;
                    System.out.println(" Your balance After Widrawl is  : " + Widrawl);
                 }
                 else
                 {
                    System.out.println("Sorry! You  don't have enough money in your account" );
                 }
                    break;
            case 4 :
                 System.out.println("Thank you for visisting The ATM!"); 
                 break; 

            default  : 
                  System.out.println("press Invalid option!");       

          }

    }

    static void AtmOption()
    {
        System.out.println("press 1 for Balance Enquiry");
        System.out.println("Press 2 for deposite ");
        System.out.println("press 3 for Widrawl");
        System.out.println("Press 4 for Exit");
    }

    public static void main(String[] args) 
    {
        double balance = 1000.00;  //Initial Balance in the account 
        System.out.println("Wellcome  to ATM");
       AtmOption();
       Scanner sc=new Scanner(System.in);
       int option = sc.nextInt();
       AtmDisplay(balance, option);


    }
}
