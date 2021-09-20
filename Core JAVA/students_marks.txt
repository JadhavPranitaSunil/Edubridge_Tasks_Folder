import java.util.*;
public class Tests {
	public static void main(String[] args) {
		try{
	Scanner sc = new Scanner(System.in);
	System.out.println("Enter Marks of Student : ");
	int marks = sc.nextInt();
	if(marks<25){
		System.out.println("J");
	}
	else if(marks>=25 && marks<45)
		System.out.println("Z");
	else if(marks>=45 && marks<50)
		System.out.println("D");
	else if(marks>=50 && marks<60)
		System.out.println("C");
	else if(marks>=60 && marks<80)
		System.out.println("B");
	else if(marks>=80 && marks<=100)
		System.out.println("A" + marks/0);
		}
		catch(Exception e){
			System.out.println(e);
		}
}
}
