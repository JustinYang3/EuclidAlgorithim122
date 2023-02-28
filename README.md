# EuclidAlgorithim122
import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		int num1 = scan.nextInt();
		int num2 = scan.nextInt();

		System.out.println(DivisorCalc.gcd(num1, num2));

	}

}

# DivisorCalc class

public class DivisorCalc {
	public static int gcd(int num1,int num2){
        try{
            if(num2%num1!=0){
                return gcd(num2, num1%num2);
            }
            else{
                return num1;
            }
        }
        catch(ArithmeticException ex){
            System.out.println("division by zero");
            return 0;
        }
    }
}


