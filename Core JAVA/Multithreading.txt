package Tuesday17;

public class Example1 {    
	   public static void main(String args[]){  
		  
	//creating the object for Thread class
		   NumberSystem n=new NumberSystem();
		   AlphaSystem a=new AlphaSystem();
		   
		   //starting the thread's 
	
		   //during this step thread's are moving new to runnable || running state
		   n.start();
		   a.start();
		   
		   //how to get to know the state of thread's
		   System.out.println(n.getState());
		   System.out.println(a.getState());
		   
		   //hot to get to know the priority of thread's
		   System.out.println(n.getPriority());
		   System.out.println(a.getPriority());
		   
		   //print the name of thread's
		   System.out.println(n.getName());
		   System.out.println(a.getName());

		   //set the name thread's
		   n.setName("Harshada");
		   System.out.println(n.getName());
		   a.setName("madhura");
		   System.out.println(a.getName());
		   
		   //how to find the current thread of our program
		   System.out.println("The Current Thread is :" + Thread.currentThread().getName());
		   
		 //how to get to know the state of thread's
		   System.out.println(n.getState());
		   System.out.println(a.getState());
		   
		   //finding live or alive state's

		   if(n.isAlive()){
			   System.out.println("Harshada thread is alive");
		   }
		   else{
			   System.out.println(" Number thread is Dead");
		   }
if(a.isAlive()){
			   System.out.println("Madhura Thread is alive");
		   }
		   else{
			   System.out.println("Alpha Thread is Dead");
		   }
	   }
	   
	   }

class NumberSystem extends Thread {
	public void run(){
		
		for(int i=1;i<=10;i++){
			System.out.println(i);
		}
	}
}

class AlphaSystem extends Thread{
public static char c='A';
	public void run(){
	for(int i=0;i<26;i++){
		System.out.println(c);
		c=(char)(c+1);
	}
	}
}
