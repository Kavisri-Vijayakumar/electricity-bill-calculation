import java.util.Scanner;
public class ElectricityBill {
    public static void main(String[] args) { 
        Scanner scanner = new Scanner(System.in); 
        System.out.print("Enter the number of units consumed: ");
        int units = scanner.nextInt();     
        double billAmount = 0;
        if (units <= 100) {
            billAmount = units * 5; // ₹5 per unit for first 100 units
        } else if (units <= 300) {
            billAmount = 100 * 5 + (units - 100) * 7; 
        } else {
            billAmount = 100 * 5 + 200 * 7 + (units - 300) * 10;
        }
        billAmount += 50;
        System.out.println("Total Electricity Bill: ₹" + billAmount);
        scanner.close();
    }
}
output
Enter the number of units consumed: 350
Total Electricity Bill: ₹2450.0

