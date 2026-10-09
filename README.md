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
