# Phone-Plans
This program calculates the monthly phone bill based on the plan chosen.

import java.util.Scanner;
//list the plans offered
public class PhonePlans {
    public static void main(String[] arg) {
        System.out.println("There are three cell phone plans available." + "\n" + "Option One offers unlimited calling and texting " +
                "for $64.99 per month" + "\n" + "Option Two offers unlimited calling and pay per text with a base price of $59.00 " +
                "per month and an additional 5 cents per text." + "\n" + "Option Three offers a $35.00 base price for up to 50 min " +
                "of calling and and then 3 cents per minute. This option does not allow texting." + "\n");


        double choice;
        System.out.println("Enter your choice: ");
        Scanner sc = new Scanner(System.in);
        choice = sc.nextDouble();

        {    //Introduce option one. The bill here will always be $64.99
            if (choice == 1)
                System.out.println("You have chosen option one. Your monthly bill will be $64.99. ");
        }


             //Introduce option two. The cost will be $59 with an additional 5 cents per text.
            if(choice == 2) {
                System.out.println("You have chosen option two." + "\n" + "Please enter the number of texts sent: ");

            int texts;
            texts = sc.nextInt();
            double secondPlanPrice = 59.00 + (0.05 * texts);
            System.out.println("Your monthly bill is " + "$" + secondPlanPrice);
        }


            //Introduce option three. The cost will be $35 with an additional 3 cents per minute when exceeding 50 minutes.
           if(choice == 3) {
               System.out.println("You have chosen option three." + "\n" + "Please enter the number of minutes used: ");

           int minutes;
           minutes = sc.nextInt();
           double thirdPlanPrice = 35.00 + (0.03 * minutes);
                if (minutes <= 50)
                    System.out.println("Your monthly bill is $35.00");
                else
                    System.out.println("Your monthly bill is "  + "$" + thirdPlanPrice);

        }
        //In case of invalid user input.
            if(choice != 1) if(choice!= 2) if(choice != 3)
                System.out.println("There is no such plan in existence. Please enter another plan.");





    }
}
