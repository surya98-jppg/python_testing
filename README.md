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
