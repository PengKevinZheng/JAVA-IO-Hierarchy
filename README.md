# JAVA-IO-Reader-vs-Writer



Reader: java.lang.Object;
        java.io.Reader;
        java.io.InputStreamReader;
        
        
An InputStreamReader is a bridge from byte streams to character streams.


Serializable: an object can be converted into binary stream and transfered over the internet.
  public class Student implemens Serializable{
  //
  }
  
String file = "xx/xx/xx";

ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(file));

Student s = new Student();

oos.writeObject();


Deserializable:

ObejectInputStream ois = new ObjectInputStream(new FileInputStream(file));

Student s = (Student)ois.readObject();

System.out.println(s);


transient: if a field in a class is transient then it cannot be serializabled.
 public Class Student{
 private transient int age;
 private String name;
 //
 ..
 }
 then the age field cannot be serializied. But the field can also do serialization and deserialization by itself.
 
 
 Deserializable and Construstor:
 
 When do deseriazable to object of child class, if its super class does not implements Serializable, the superclass's constructor will be invoked. If its super class implements Serializable, we cannot see its constructor is invoked.

