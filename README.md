# canYou
import java.util.*;


public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */

        Scanner keyboard = new Scanner(System.in);

        final int num= keyboard.nextInt();

        Solution.Inner.powerof2(num);

    }


    private static class Inner{

        public static void powerof2(int num){
            int[] temp=new int[31];
            for(int i=0;i<=30;i++){
                temp[i]= (int) Math.pow(2,i);
            }
            int flag=0;
            for(int j=0;j<=30;j++){

                if (temp[j] == num ){
                    flag=1;
                }
            }
            if (flag==1){
                System.out.println(num+" is power of 2");
                System.out.println("An instance of class: Solution.Inner.Private has been created");
            }else{
                System.out.println(num+" is not a power of 2");
                System.out.println("An instance of class: Solution.Inner.Private has been created");
            }


        }



    }
}
