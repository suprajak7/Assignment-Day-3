# Assignment-Day-3

1.
Final :
-final is the keyword and access modifier which is used to apply restrictions on a class, method or variable.
-Final keyword is used with the classes, methods and variables.
-(1) Once declared, final variable becomes constant and cannot be modified.
 (2) final method cannot be overridden by sub class.
 (3) final class cannot be inherited.
-Final method is executed only when we call it.

Finally :
-finally is the block in Java Exception Handling to execute the important code whether the exception occurs or not.
-Finally block is always related to the try and catch block in exception handling.
-(1) finally block runs the important code even if exception occurs or not.
 (2) finally block cleans up all the resources used in try block
-Finally block is executed as soon as the try-catch block is executed.
It's execution is not dependant on the exception.

Finalize
- finalize is the method in Java which is used to perform clean up processing just before object is garbage collected.
- finalize() method is used with the objects.
-finalize method performs the cleaning activities with respect to the object before its destruction.
-finalize method is executed just before the object is destroyed

2.

import java.util.Scanner;
public class Cab{
    int fare, d, cd;
    public Cab() {
        fare=30; 
    }
    public Cab(int amt){
        fare=amt;
    }
    
}
public class CabRide{
    public static void main(String[] args){
        int cd;
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter the distance: ");
        cd=sc.nextInt();
        if(cd>3){
            Cab obj=new Cab(30+10*(cd-3));
	    System.out.print("Enter the distance travelled: ");
            obj.d=sc.nextInt();
            obj.fare+=10*obj.d;
            System.out.print("Total fare: Rs "+obj.fare);
        }
        else{
            Cab obj=new Cab();
            System.out.print("Enter the distance travelled : ");
            obj.d=sc.nextInt();
            obj.fare+=10*obj.d;
            System.out.print("Total fare: Rs "+obj.fare);
        }
        
    }
    
}
