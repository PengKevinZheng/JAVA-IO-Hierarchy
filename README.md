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
