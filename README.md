# classes and objects in java
class Student {
    int roll=3; // intialization and declaration
    String name;
    
    public static void main(String[] args) {
        Student s1=new Student();  // creating object for s1
        s1.roll=9; // accessing through refernece varaible s1 
        System.out.println(s1.roll);
    }
}
# parametrized constructor
class Student {
    String institute;
    int enroll;
    int dob;
Student(String name,int enroll, int dob){
    this.institute=institute;
    this.enroll=enroll;
    this.dob=dob;
}
    public static void main(String[] args) {
      Student surya=new Student("piet",22,143);
      Student naresh=new Student("piet",2,2);
        System.out.println(surya.dob);
        System.out.println(naresh.dob);
    }
}
# exmple
class Main {
    int roll;
    String name;
Main(){
    this(32,"surya"); // calling constructor using this keyword
}
Main(int roll,String name){ // two constuctors
    this.roll=roll;
    this.name = name;
}
    

void changeROll(int newroll){ // method having differnet parameter names
    roll=newroll;
    System.out.println(roll);
}
    public static void main(String[] args) {
        Main s1=new Main(); // calling empty constructor
        Main s2=s1;   // s2 points to s1 memory location
        s1.name="naresh";//changes made in s1 effects s2
        System.out.println(s2.name);
        
        s1.changeROll(3);
        
    }
}
# method using object

class Main {
    public int add(int n1,int n2){
        return n1+n2;
    }
    public static void main(String[] args) {
      Main c1=new Main();
        System.out.println(c1.add(2,5));
    }
} 
# java pass by value using swapping
import java.util.Arrays;
class Main {
    int temp;
    public int[] swap(int n1,int n2){
        int temp;
        temp=n1;
        n1=n2;
        n2=temp;
    return new int[]{n1,n2};
    }
    public static void main(String[] args) {
      Main c1=new Main();
        int a=10;
        int b=12;
        int[]result=c1.swap(a,b);  // pass by value
        System.out.println(Arrays.toString(result)); 
        System.out.println(a+" "+b);//does not change original values
    }
} 
# using final keyword
import java.util.Arrays;
class Main {
    final int n=10;//perment value
    String name;
Main(String name){
    this.name=name;
}
public static void main(String[]args){
    final Main s1=new Main("surya");
    System.out.println(s1.n);
    s1.name="naresh";       // we can object even if it is final 
    System.out.println(s1.name);
}
}
# re assigning cannot be done in final object variable 
class Main {
    final int n=10;//perment value
    String name;
Main(String name){
    this.name=name;
}
public static void main(String[]args){
    final Main s1=new Main("surya");
    System.out.println(s1.n);
    s1.name="naresh"; // we can object even if it is final 
    (!) s1=new Main("suresh"); // we cannor re assign the final obbject
    System.out.println(s1.name);
}
}
