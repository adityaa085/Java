1.Write a program to print factorial of N ( without using any loop)

import java.util.Scanner;

public class factorial {

	public static void main(String[] args) {
	
	
	
		System.out.println("Enter the number");
     
   Scanner sc=new Scanner(System.in);
	
	int a =sc.nextInt();
	
	System.out.println("Factorial of "+a+" = "+fact(a));


	}
	
 
   static int fact(int a )
   
 {
    	if(a==0)
    
	{
    	
	return 1;
    	}
    
	else
    	{
    
		return a*fact(a-1);
    	}
 
   }

}

2.	There is an animal class which has the common characteristics of all animals.
 Dog, Horse, Cat are animals(sub-class). Each can shout, but each shout is different.
 Use polymorphism to create objects of same and using an animal variable, make each of the animals shout.
 
 public class TestingClass {
	

	public static void main(String args[]) throwsIOExceptions {
		
animal a;
		a=new dog();
		a.shout();
		
	
	a=new cat();
		a.shout();
	
	
		a=new horse();
		a.shout();
	
}

}


public class animal {
	

	public void shout()
	{

		System.out.println("animal shout");

	}

}
public class horse extends animal
 {

	public void shout()
	
{
	
	System.out.println("Horse shout");
	
}
}
public class cat extends animal{

	
	public void shout()
	
{
		System.out.println("cat meows");
	
}

}
public class dog extends animal{


	public void shout()

	{
		System.out.println("Dogs barks");

	}
}
3.	Create an abstract class Instrument which is having the abstract function play.  
Create three more sub classes from Instrument which is Piano, Flute, Guitar.
 Override the play method inside all three classes printing a message 
             “Piano is playing  tan tan tan tan  ”  for Piano class
              “Flute is playing  toot toot toot toot”  for Flute class
              “Guitar is playing  tin  tin  tin ”  for Guitar class 
      Create an array of 10 Instruments.
      Assign different type of instrument to Instrument reference.
     Check for the polymorphic behavior of  play method.
	 
	 public class Testingclass {

	
public static void main(String[] args)
 {

		instrument []a=new instrument[10];
		
for(int i=0;i<10;i++)
		{

			a[i]=new flute();

			a[i].play();
	
		
			a[i]=new guitar();

			a[i].play();
			
		
	a[i]=new piano();
		
	a[i].play();
		}

	
}

}
public class flute extends instrument{
	public void play()
	
{
	
	System.out.println("Flute is playing toot toot toot toot");
	
}

}


public class guitar extends instrument{
	
	public void play()
	{

		System.out.println("Guitar is playing  tin  tin  tin");
	}

}

public class piano extends instrument {

	public void play()
	{
	
	System.out.println("Piano is playing  tan tan tan tan");

	}
}

4.	Write an interface called Playable, with a method void play();
Let this interface be placed in a package called music.Write a class called Veena which implements Playable interface. 
Let this class be placed in a package music.string.Write a class called Saxophone which implements Playable interface. 
Let this class be placed in a package music.wind.Write another class Test in a package called live. Then,
a. Create an instance of Veena and call play() method
b. Create an instance of Saxophone and call play() method
c. Place the above instances in a variable of type Playable and then call play().

package live;

import music.Playable;
import music.wind.*;
import music.string.*;
public class Test {

	public static void main(String[] args) {
		Playable p;
		
		p=new Veena();
		p.play();
		

		p=new Saxophone();
		p.play();

	}
	}

package music.string;

import music.Playable;
public 
class Veena  implements Playable{

	public void play()

	
{
		
System.out.println("Veena is played");
	}
}

package music.wind;
import music.Playable;
public class Saxophone implements Playable{

	public void play() {
		System.out.println("Saxophone is played");
	
	
	}

}
5.	Write a program to accept name and age of a person from the command            
        prompt(passed as arguments when you execute the class) and ensure that the age entered is >=18 and < 60. 
		Display proper error messages. The program must exit gracefully after displaying the error message in case the arguments passed are not proper.
 (Hint : Create a user defined exception class for handling errors.)
 
 public class person {

	public static void main (String[] args) throws IOException{
		
		
		String name=args[0];
		int age=Integer.parseInt(args[1]);
		
		if(age>=18 && age<60)
		{
			System.out.println(name+"'s age is "+age);
		}
		else
		
{
		
	throw new userdefined();
	
	}

	
}

}

public class userdefined extends Exception{
	
	public String toString()
	
{
		return  "Age should be above 18 and less than 60";
	
}

}



6.	Write  a  program  to  assign  the  current  thread  to  t1.  Change  the  name  of  the  thread  to  MyThread. 
 Display  the  changed  name  of  the  thread. Also  it  should  display  the  current  time. 
  Put  the  thread  to  sleep  for  10  seconds  and  display  the  time  again.
  public static void main(String[] args) throws InterruptedException, InterruptedIOException {

		
		
Thread t=Thread.currentThread();

		System.out.println("old name of the thread is "+t);

		SimpleDateFormat sdf=new SimpleDateFormat("HH:mm:ss");

		currenttime time1=new currenttime();
	
	
		
		 
		System.out.println("current time :"+sdf.format(time1.now()
)
);
	
	t.setName("MyThread");
	
	System.out.println("new name of the thread is "+t);

		
		
		
		t.sleep(10000);

		
		
		System.out.println("current time again  :"+sdf.format(time1.now()));


	}
	
	

}
7.Create an ArrayList of Employee( id,name,address,sal) objects and search for particular Employee object based on id number and name.
	 public class Employee{
  
	String id,name,address;
	int salary;
	public String getId() {
		return id;
	}
	public void setId(String id) {
		this.id = id;
	}
	public String getName() {
		return name;
	}
	public void setName(String name) {
		this.name = name;
	}
	public String getAddress() {
		return address;
	}
	public void setAddress(String address) {
		this.address = address;
	}
	public int getSalary() {
	
	return salary;
	}
	public void setSalary(int salary) {
		this.salary = salary;
	}
	
}


import java.util.*;

public class TestingEmp {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		ArrayList<Employee> test=new ArrayList<Employee> ();
		Employee [] emp1=new Employee[5];
		
		for(int i=0;i<3;i++)
		{
			emp1[i]=new Employee();
			
			System.out.println("Enter the name of the employee");
			String a=sc.next();
			emp1[i].setName(a);
			
			System.out.println("Enter the ID of the employee");
			String b=sc.next();
			emp1[i].setId(b);
			
			System.out.println("Enter the address of the employee");
			String c=sc.next();
			emp1[i].setAddress(c);
			
			System.out.println("enter the salary of the employee");
			emp1[i].setSalary(sc.nextInt());
			
		    test.add(i, emp1[i]);	
			
					
		}
		
		System.out.println("Enter the name and Id of the Employee to be searched");
	    String name=sc.next();
	    String id=sc.next();
	    
	    int j=0;
	    int flag=0;
	    Iterator i=test.iterator();
	    Employee e;
	    while(i.hasNext())
	    {
	    	e=(Employee) i.next();
	    	if(e.getName().equals(name) && e.getId().equals(id))
	    	{
	    		flag=1;
	    		System.out.println("Found object ");
	    		break;
	    	}
	   }
	    	
	    
	    if(flag==0)
	    {
	    	System.out.println("Employee details not found");
	    	
	    }
	    if(flag==1)
	    {
	    	System.out.println("other details of the employee which is searched "+emp1[j].getAddress()+"\n"+emp1[j].getSalary());
	    }
	}
