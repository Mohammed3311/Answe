# Answe
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        double medicareMedicaidRate =0.0275 ; //2.75% --> 0.0275   Dividing by 100
        double pensionPlanRate =  0.06;  //6%  -->0.06  Dividing by 100
        double healthInsurance = 75.0; //75 BD
        double  grossAmount,NetPay;
        double pensionPlanDeduction , medicareMedicaidDeduction,totalDeductions;

        System.out.print("Enter gross amount (BD): ");
        grossAmount = scanner.nextDouble();
        medicareMedicaidDeduction=grossAmount*medicareMedicaidRate;
        pensionPlanDeduction=grossAmount*pensionPlanRate;

        totalDeductions=pensionPlanDeduction+medicareMedicaidDeduction+healthInsurance;
        NetPay=grossAmount-totalDeductions;

        System.out.println("Gross amount: "+grossAmount);
        System.out.println("Medicare/Medicaid Tax: "+medicareMedicaidDeduction);
        System.out.println("Pension Plan: "+pensionPlanDeduction);
        System.out.println("Health Insurance: "+totalDeductions);
        System.out.println("Net Pay: "+NetPay);
    }
}
