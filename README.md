# c-.net

Write a c# code to show even numbers between 1 to 10:
using System;
namespace looping
{
    class Program
    {
        static void Main(string[] args)
            
        {
            int i = 1;
            for (i = 1; i <= 10; i++)
            {
                if (i % 2 == 0)
                {
                    Console.WriteLine(i);
                }
            }
            Console.ReadLine();
        }
    }
}

using System;
namespace looping
{
    class Program
    {
        static void Main(string[] args)
            
        {
            int i = 1, a;
            Console.WriteLine("Enter the last integer upto the even numbers you want: ");
            a=int.Parse(Console.ReadLine());
            for (i = 1; i <= a; i++)
            {
                if (i % 2 == 0)
                {
                    Console.WriteLine(i);
                }
            }
            Console.ReadLine();
        }
    }
}

Using break:
using System;
namespace looping
{
    class Program
    {
        static void Main(string[] args)
            
        {
            int i = 1, a;
            Console.WriteLine("Enter the last integer upto the even numbers you want: ");
            a=int.Parse(Console.ReadLine());
            for (i = 1; i <= a; i++)
            {
                if (i % 2 == 0)
                {
                    if (i > 6)
                    {
                        break;
                    }
                    Console.WriteLine(i);
                }
            }
            Console.ReadLine();
        }
    }
}

Continue:
using System;
namespace looping
{
    class Program
    {
        static void Main(string[] args)
            
        {
            int i = 1, a;
            Console.WriteLine("Enter the last integer upto the even numbers you want: ");
            a=int.Parse(Console.ReadLine());
            for (i = 1; i <= a; i++)
            {
                if (i % 2 == 0)
                {
                    if (i <= 6)
                    {
                        continue;
                    }
                    Console.WriteLine(i);
                }
            }
            Console.ReadLine();
        }
    }
}

Break in while loop:
using System;
namespace whileloop
{
    class Program
    {
        static void Main(string[] args)
        {
            int i = 1, a;
            Console.WriteLine("Enter the last integer upto the even numbers you want: ");
            a = int.Parse(Console.ReadLine());
            while (i <= a)
            {
                if (i % 2 == 0)
                {
                    if (i > 6)
                    {
                        break;
                    }
                    Console.WriteLine(i);
                }
                i++;
            }
            Console.ReadLine();
        }
    }
}


Function and object:
using System;
namespace functionarr
{
    class Program
    {
        void show()
        {
            Console.WriteLine("new function is invoked!");
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            Program msg = new Program();
            msg.show();
        }
    }
}

Array:
using System;
namespace functionarr
{
    class Program
    {
        void show()
        {
            int[] a = {1,2,3,4,5};
            Console.WriteLine("new function is invoked!");
            Console.WriteLine(a[3]);
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            Program msg = new Program();
            msg.show();
        }
    }
}
 Addition of array elements:
using System;
namespace functionarr
{
    class Program
    {
        int sum;
        void show()
        {
            
            int[] a = {4,7,9,6,2};
            for (int i = 0; i < 5; i++)
            {
                sum = sum + a[i];    
            }
            Console.WriteLine(sum);
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            Program msg = new Program();
            msg.show();
        }
    }
}
Max value from array:
using System;
namespace functionarr
{
    class Program
    {
        int sum,maximum,i,j;
        int[] a = {4,7,9,6,2};
        void show()
        {
           for (i = 0; i < 5; i++)
            {
                sum = sum + a[i];    
            }
            Console.WriteLine("sum= "+sum);
        }
        void maxi()
        { 
         for (j = 0; j < 5; j++)
            {
               //maximum=a[j];
               if (a[j] > maximum)
               {
                   maximum = a[j];
               }
               else 
               {
                   Console.WriteLine("max= " + maximum);  
               }
            }
        
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            Program msg = new Program();
            msg.show();
            msg.maxi();
        }
    }
}


Default Constructor:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace constructor
{
    class defconstructor
    {
        defconstructor()
        {
            Console.WriteLine("Constructor called");
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            defconstructor con = new defconstructor();
        }
    }
}

 Constructor accessing private member:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace constructor
{
    class defconstructor
    {
        int age;
        defconstructor()
        {
            age = 29;
            Console.WriteLine(age);
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            defconstructor con = new defconstructor();
        }
    }
}

Parameterized Constructor:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace constructor
{
    class paraconstructor
    {
        paraconstructor(int age, String name)
        {
            Console.WriteLine("Name is: "+name);
            Console.WriteLine("Age is: "+age);
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            paraconstructor con = new paraconstructor(23,"Mayur");
        }
    }
}

Parameterized Constructor at Runtime:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
namespace constructor
{
    class paraconstructor
    {
        int a;
        String n;
        paraconstructor(int age, String name)
        {
            a = age;
            n = name;
        }
        static void Main(string[] args)
        {
            paraconstructor con = new paraconstructor(23,"Mayur");
            Console.WriteLine("Age is: "+ con.a);
            Console.WriteLine("Name is: "+con.n);
            Console.ReadLine();
        }
    }
}

Write a c#.Net program to accept user Define number and print table of given number. Value should be accept as early class objects created.
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
namespace table
{
    class table
    {
        int num;
        table(int a)
        {
            Console.WriteLine("table of "+a+" is: \n");
            for (int i = 1; i <= 10; i++)
            {
                Console.WriteLine(a*i);
            }
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            int num;
            Console.WriteLine("Enter a number to print it's table: ");
            num = int.Parse(Console.ReadLine());
            table t1 = new table(num);    
        }
    }
}

Write a c#.Net program to accept user Define number and print table of given number. Value should be accept as early class objects created. And object should free memory spaces after program execution completed. (Destructor)
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
namespace table
{
    class table
    {
        int num;
        table(int a)
        {
            Console.WriteLine("table of "+a+" is: \n");
            for (int i = 1; i <= 10; i++)
            {
                Console.WriteLine(a*i);
            }
            Console.ReadLine();
        }
        ~table()
        {
            Console.WriteLine("Destructor called.");
            Console.ReadLine();
        }
        static void Main(string[] args)
        {
            int num;
            Console.WriteLine("Enter a number to print it's table: ");
            num = int.Parse(Console.ReadLine());
            table t1 = new table(num);    
        }
    }
}

Single inheritance
using System;
namespace inheritance
{
    public class stud
    {
        public string name="Mayur";
        public string class1="SYBCA";
        void showinfo()
        {
            Console.WriteLine("Name= " + name + " Class= " + class1);
  
        }
    }
    public class exam: stud
    {
        public void showsub()
        {
        string sub="C#.Net";
        Console.WriteLine("" Subject= "+sub);
        Console.ReadLine();
        }
    }

    class Program
    {
        static void Main(string[] args)
        { 
            exam ex=new exam();
            ex.showinfo();
            ex.showsub();
        }
    }
}

Multilevel Inheritance
using System;
namespace inheritance
{
    public class stud
    {
        public string name="Mayur";
        public string class1="SYBCA";
        public void showinfo()
        {
            Console.WriteLine("Name= " + name + " Class= " + class1);
  
        }
    }
    public class exam: stud
    {
        public void showsub()
        {
        string sub="C#.Net";
        Console.WriteLine("Subject= "+sub);
        }
    }
    public class mark : exam
    {
        public void showmarks()
        {
            int marks = 50;
            Console.WriteLine("Marks= " + marks);
            Console.ReadLine();
        }
    }

    class Program
    {
        static void Main(string[] args)
        { 
            mark mk=new mark();
            mk.showinfo();
            mk.showsub();
            mk.showmarks();
        }
    }
}

Interface
using System;
namespace interfacedemo
{
   public class student
    {
        public string name;
        public string class1;
        
    }
    interface exam
    {
       void showsub();
    }
    class result:student,exam
    {
        public void showinfo()
        {
            name = "Mayur";
            class1 = "SYBCA";
            Console.WriteLine(name);
            Console.WriteLine(class1);
        }

        public void showsub()
        {
            Console.WriteLine("C#.net");
            Console.ReadLine();
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            result r = new result();
            r.showinfo();
            r.showsub();
        }
    }
}
                                                                                                                                                                                                                                                          
 Method Overloading:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace methodoverloading
{
    class methodover
    {
        public void add(int a,int b)
        {
            Console.WriteLine(a+b);
        }
        public void add(int a,int b,int c)
        {
            Console.WriteLine(a+b+c);
            Console.ReadLine();
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            methodover mo = new methodover();
            mo.add(5,6);
            mo.add(7, 3, 9);
        }
    }
}

Method Overriding: 
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace meoverriding
{
    class A
    {
        public void add(int a, int b)
        {
            Console.WriteLine("Addition: "+ a + b);
        }
    }
    class B:A
    {
        public void add(int a, int b)
        {
            Console.WriteLine("Addition: " + a + b);
            Console.ReadLine();
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            B b = new B();
            b.add(5,5);
            b.add(6,6);
        }
    }
}


