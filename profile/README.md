## 👋

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

## GUI. Lecture 1  

Sławomir Aleksander Dańczak, M.Sc.

I. Without modifying the main method, make the code below work.  

Hint: Subject class can have access to students’ set (e.g. an array). Adding too many students to the set may throw an exception.  

```java
public class Main {

      public static void main(String args[]) {
      
            Person p1 = new Person("Jan" , 50);
            Student s1 = new Student("Jasiek", 20);
            Person p3 = (Person)s1;
            
            p1.sayHelloTo(p3); //Hi Jasiek! 
            p3.sayHelloTo(p1); //Hi Jan!
            
            Subject s = new Subject ("GUI"); 
            s.setTeacher(p1);
            
            try {
                s.addStudent(s1);
            } catch(TooManyStudentsException e) { 
                e.printStackTrace();
            }
            
            System.out.println(s); //GUI, teacher: Jan, students: Jasiek
      }
}
```
