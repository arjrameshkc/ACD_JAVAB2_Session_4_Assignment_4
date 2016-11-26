# ACD_JAVAB2_Session_4_Assignment_4
Super Class:
package session4_assignment;

public class ChainingSuperClass {
	int numSup,numSup1,numSup2;
 public ChainingSuperClass(){
       System.out.println("Default constructor Super Class");
  }
  public ChainingSuperClass(int numSup){
	 this.numSup = numSup; 
   }
  public ChainingSuperClass(int numSup, int numSup1){
	  this.numSup = numSup;
	  this.numSup1 = numSup1;
  }
  public ChainingSuperClass(int numSup, int numSup1, int numSup2){
	  this.numSup = numSup;
	  this.numSup1 = numSup1;
	  this.numSup2 = numSup2;
	  
  }
}

SubClass:
package session4_assignment;

public class ChainingSub extends ChainingSuperClass {
	int numSub,numSub1,numSub2;
  public ChainingSub(){
	   super();
      System.out.println("Default  sub constructor");
  }
  public ChainingSub(int numSup,int numSub){
	  super(numSup);
	  this.numSub = numSub;
   	 System.out.println("Parametrized constructor with single param");
  }
  public ChainingSub(int numSup1,int numSub,int numSub1){
//	  super(numSup,numSup1);
     super(numSup1);
	  this.numSub = numSub;
	  this.numSub1 = numSub1;
    System.out.println("Parametrized constructor with double args");
  }
  public ChainingSub(int numSup2,int numSub,int numSub1,int numSub2){
	  super(numSup2);
	  this.numSub = numSub;
	  this.numSub1 = numSub1;
	  this.numSub2 = numSub2;
     System.out.println("Parametrized constructor with three args");
  }
	
}

Main Class:

package session4_assignment;

public class ChainingMain {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		ChainingSub obj =  new ChainingSub();
    	ChainingSub obj1 =  new ChainingSub(5,5);
		ChainingSub obj2 =  new ChainingSub(5,5,5);
		ChainingSub obj3 =  new ChainingSub(5,5,15,5);
	}

}


