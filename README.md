# JavaMessi
import java.util.*;

class ElectricityBill {

   public static void main(String [] args) {
   Units s = new Units();
   s.consumed();
   s.cost();
   }

}  

class Units {

   Scanner s = new Scanner(System.in);
   double bill, newBill, price, unit, newUnit;
   
   public void consumed() {
   System.out.println("Enter the unit consumed = ");
   unit = s.nextInt();
   }
   
   public void cost() {
      
      if (unit > 0 && unit <= 100) {
         price = 0.50;
         bill = unit * price;
         System.out.println("Price per unit = Rs. 0.50");
         System.out.println("Bill = Rs." + bill);         
         
      } else if (unit > 100 && unit <= 300) {
         price = 3.00;
         newUnit = unit - 100;
         newBill = (newUnit * price) + 50.0;
         System.out.println("Price per unit = Rs. 3.00");
         System.out.println("Bill = Rs." + newBill);
         
      } else if (unit > 300 && unit <= 600) {
         price = 10.00;
         newUnit = unit - 300;
         newBill = (newUnit * price) + 950.0;
         System.out.println("Price per unit = Rs. 10.00");
         System.out.println("Bill = Rs." + newBill);          
         
      } else {
         price = 15.00;
         newUnit = unit - 600;
         newBill = (newUnit * price) + 7000.0;         
         System.out.println("Price per unit = Rs. 15.00");
         System.out.println("Bill = Rs." + newBill);
                   
      }
   }
}

