# Write-a-program-to-convert-a-natural-number-in-base-10-to-any-number-in-base-b-1-b-36-.
Write a program to convert a natural number in base 10 to any number in base b (1&lt; b≤ 36).
package bai02;
import java.util.Scanner;
public class Main {
 
    public static void doiCoSo(int n,int base){
        if(n>=base) doiCoSo(n / base, base);
        if(n % base>9) System.out.printf("%c",n%base+55);
        else
        System.out.print((n % base));
    }
    public static int enter(){
        Scanner input= new Scanner(System.in);
        boolean check= false;
        int n=0;
        while(!check){
            System.out.print(" ");
            try{
                n= input.nextInt();
                check= true;
            }catch(Exception e){
                System.out.println("You must log in! or log in again...");
                input.nextLine();
            }
        }
        return(n);
    }
    public static void main(String[] args) {
                System.out.println("Tap n");
        int n= enter();
        System.out.println("Input can be converted to b");
        int b= enter();
        System.out.println("So " +n+ " converts to " +b+ " bar: ");
        doiCoSo(n,b);
    }
 
}
