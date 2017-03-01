# java-project-file

public class SingleThread extends Thread {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
Thread t1= new Thread(new RunnableThread());
Thread t2=new Thread(new RunnableThread());
SingleThread t3=new SingleThread();	
t1.start();
t2.start();	
try{	
t2.join();	
}
catch(InterruptedException e)
{	
System.out.println(e.getMessage());
}
t3.start();	
	}
}
