/*Eugene Vasquez
COMPSCI-ITSE
Write a program that read in arbitrary
numbers of integers that are in the range 0 to 50
inclusive and counts how many occurrence of each are entered.*/

import java.util.Scanner;
import java.util.ArrayList;
import java.util.InputMismatchException;

public class exercise18 {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        ArrayList<Integer> array = new ArrayList<Integer>();
        Integer intcount = 0;



        while(true)
        {
            System.out.println("Please enter a number (enter a non-Integer to end)");  //prompt
            try{
                Integer x = input.nextInt();
                array.add(x);
                if (x>=0 && x<=50) { //conditions
                    intcount++;
                }
            }
            catch (InputMismatchException ex) {
                break;
            }
        }

        System.out.println();
        System.out.format("The numbers you entered were: %s\n", array);
        System.out.format("The intcount of in-range numbers was: %d\n", intcount); //output
    }
}
