      # .NET
       1)Write a C# program to print Fibonacci series using Recursion and without using Recursion. 
       using System;
      public class Fibonacci
      {
    public static void Main(string[] args)
    {
        int n1 = 0, n2 = 1, n3, i, number;
        Console.WriteLine("Enter the number of elements:");
        number = int.Parse(Console.ReadLine());
        Console.Write(n1 + " " + n2 + " ");
        for(i = 2; i < number; i++)
        {
            n3 = n1 + n2;
            Console.Write(n3 + " ");
            n1 = n2;
            n2 = n3;
        }
    }
    OUTPUT:
   ![image](https://user-images.githubusercontent.com/97939356/156504948-929f41d8-6a09-46a0-80a0-13c2d4e46985.png)

    
       2)Write a C# program to check whether the given number is Prime or not. 3. Write a C# program to check whether the given element is Palindrome or not. 4. Write a C# program to print factorial of a number. 

      using System;

      namespace Exercise
      {
    public class Prime 
    {
        static void Main(string[] args)
        {
            int n, i, m = 0, flag = 0;
            Console.WriteLine("Enter the number to check the prime");
            n = int.Parse(Console.ReadLine());
            m = n / 2;
            for (i = 2; i <= m; i++)
            {
                if (n % i == 0)
                {
                    Console.Write("Number is not a Prime");
                    flag = 1;
                    break;
                }
            }
            if (flag == 0)
                Console.Write("Number is Prime");
        }
    }
      }

      OUTPUT:

   ![image](https://user-images.githubusercontent.com/97939356/156502267-c7cbc30f-d17b-4527-a867-96a75ce41ffe.png)
      
   ![image](https://user-images.githubusercontent.com/97939356/156502324-5fca5b5d-b330-4d87-bf8e-8a5dd68075ac.png)
      
      3)Write a C# program to check whether the given element is Palindrome or not.
      using System;

      namespace Exercise
      {
    public class palindrome
    {
        public static void Main(string[] args)
        {
            int n, r, sum = 0, temp;
            Console.Write("Enter the number : ");
            n = int.Parse(Console.ReadLine());
            temp = n;
            while (n > 0)
            {
                r = n % 10;
                sum = (sum * 10) + r;
                n = n / 10;
            }
            if (temp == sum)
                Console.Write("Number is Palindrome");
            else
                Console.Write("Number is not Palindrome");
        }
    }
      }
      
        OUTPUT:
      
   ![image](https://user-images.githubusercontent.com/97939356/156502537-0776efd1-4f95-46f0-b311-09917b29d95d.png)

   ![image](https://user-images.githubusercontent.com/97939356/156502608-f4473aa6-8f29-44bc-b790-4ea21c57a390.png)

      4)
      using System;

      namespace Exercise
      {
        public class Factorial
    {
        public static void Main(string[] args)
        {
            int i, fact = 1, number;
            Console.WriteLine("Enter any number:");
            number = int.Parse(Console.ReadLine());
            for(i=1;i<=number;i++)
            {
                fact = fact * i;
            }
            Console.Write("Factorial of" + number + "is:" + fact);
        }
    }
      }

       OUTPUT:
       
   ![image](https://user-images.githubusercontent.com/97939356/156502786-476253c6-530b-4039-9038-8fb18ec8c5f2.png)

         5)
      using System;
      namespace Exercise
      {

    public class Armstrong
    {
        public static void Main(string[] args)
        {
            int n, r, sum = 0, temp;
            Console.WriteLine("Enter the number");
            n = int.Parse(Console.ReadLine());
            temp = n;
            while(n>0)
            {
                r = n % 10;
                sum = sum + (r * r * r);
                n = n / 10;
            }
            if (temp == sum)
                Console.Write("Armstrong Number");
            else
                Console.Write("Not Armstrong number");
        }
    }
      }
      OUTPUT:
      
   ![image](https://user-images.githubusercontent.com/97939356/156503900-eef859e6-77a4-4a44-89e0-44edac8e7a4b.png)
      
   ![image](https://user-images.githubusercontent.com/97939356/156503971-86794299-c691-49c5-8d39-b26f39758d81.png)
      
      6)
      using System;

      namespace Exersice
      {
    public class Sum
    {
        public static void Main(string[] args)
        {
            int n, sum = 0, m;
            Console.WriteLine("Enter a number");
            n = int.Parse(Console.ReadLine());
            while(n>0)
            {
                m = n % 10;
                sum = sum + m;
                n = n / 10;
            }
            Console.Write("Sum is=" + sum);
        }
    }
      }
      
    OUTPUT:
    
   ![image](https://user-images.githubusercontent.com/97939356/156504430-c483bd90-5db7-4190-a7a2-ffce3b1cb354.png)
   
   ![image](https://user-images.githubusercontent.com/97939356/156504517-5d2def11-1ba4-4289-86a5-671475b59390.png)

      7)
      using System;

      namespace Exercise
      {
     public class reverse
    {
        public static void Main(string[] args)
        {
            int n, reverse = 0, rem;
            Console.WriteLine("enter a number:");
            n = int.Parse(Console.ReadLine());
            while (n != 0)
            {
                rem = n % 10;
                reverse = reverse * 10 + rem;
                n /= 10;
            }
            Console.Write("Reverse number:" + reverse);
        }
    }
      }
      OUTPUT:
      
   ![image](https://user-images.githubusercontent.com/97939356/156504717-fb18951c-41a3-49f3-ac87-f7df8443710a.png)

      8)C# Program to Print a Binary Triangle
      using System;

      namespace _2program_B.T_
      {
  
       class BinaryTriangle
    {
    
        static void Main(string[] args)
        {
            int number, digit = 1;
            Console.WriteLine("\nEnter the number of lines:");
            number = Convert.ToInt32(Console.ReadLine());
            for (int i = 1; i <= number; i++)
            {
                for (int space = number - i; space > 0; space--)
                    {
                    Console.Write(" ");
                }
                for (int j = 0;j < i; j++)
                {
                    Console.Write(digit + " ");
                    digit = (digit == 1) ? 0 : 1;
                }
                Console.Write("\n");
            }
        }
    }
}
OUTPUT:

   ![image](https://user-images.githubusercontent.com/97939356/154633529-599810a6-b91f-4bd6-bd39-eb75f08ecff8.png)
     
     9)
      using System
      namespace Exercises
      {
    class AmicableNumber
    {
        static void Main(string[] args)
        {
            int num1, num2, sum1 = 0, sum2 = 0;
            Console.WriteLine("\n--------AMICABLE NUMBERS-----------\n"); Console.Write("\nEnter the first number: ");
            num1 = Convert.ToInt32(Console.ReadLine());
            Console.Write("\nEnter the second number: ");
            num2 = Convert.ToInt32(Console.ReadLine());
            for (int i = 1; i < num1; i++)
            {
                if (num1 % i == 0)
                {
                    sum1 += i;
                }
            }
            for (int i = 1; i < num2; i++)
            {
                if (num2 % i == 0)
                {
                    sum2 += i;
                }
            }
            if (sum1 == num2 && sum2 == num1)
            {
                Console.WriteLine("\nThe numbers {0} and {1} are amiciable.", num1, num2);
            }
            else
            {
                Console.WriteLine("\nThe numbers {0} and {1} are not amiciable.", num1, num2);
            }
        }
    }
      }
      OUTPUT:
      
   ![image](https://user-images.githubusercontent.com/97939356/156505452-330358af-fdbb-4bf6-90a7-96ea120d4a05.png)

      10)C# Program to Illustrate Multilevel Inheritance with Virtual Method(displaying students details)
      using System;

    namespace Exercises
     using System;

    namespace Exercises
    {
     class PersonalDetails
    {
        string name;
        int age;
        string gender;
        public PersonalDetails(string name, int age, string gender)
        {
            this.name = name;
            this.age = age;
            this.gender = gender;
        }
        public virtual void Display()
        {
            Console.WriteLine("\n------PERSONAL DETAILS-----\n");
            Console.WriteLine("Name:" + name);
            Console.WriteLine("Age:" + age);
            Console.WriteLine("Gender:" + gender);
        }
    }
    class CourseDetails : PersonalDetails
    {
        int regNo;
        string course;
        int semester;
        public CourseDetails(string name, int age, string gender,int regNo, string course, int semester):base(name,age,gender)
        {
            this.regNo = regNo;
            this.course = course;
            this.semester = semester;
        }
        public override void Display()
        {
            base.Display();
            Console.WriteLine("\n------COURSE DETAILS-----\n");
            Console.WriteLine("RegisterNumber:" + regNo);
            Console.WriteLine("Course:" + course);
            Console.WriteLine("Semester:" + semester);
        }
    }
    class MarksDetails : CourseDetails
    {
        int[] marks = new int[5];
        int total;
        float average;
        string grade;
        int flagFail;
        public MarksDetails(string name, int age, string gender, int regNo, string course, int semester, int[] marks) : base(name, age, gender, regNo, course, semester)
        {
            total = 0;
            for (int i = 0; i < 5; i++)
            {
                this.marks[i] = marks[i];
                total += marks[i];
                if (marks[i] < 35)
                {
                    flagFail = 1;
                }
            }
            Calculate();
        }
        private void Calculate()
        {
            average = total / 5;
            if (flagFail == 1 || average < 40)
                grade = "Fail";
            else if (average >= 70)
                grade = "Distinction";
            else if (average >= 60)
                grade = "First class";
            else if (average >= 50)
                grade = "Second class";
            else
                grade = "Pass class";
        }
         public override void Display()
        { 
                base.Display();
                Console.WriteLine("\n------Marks DETAILS-----\n");
                Console.WriteLine("Marks in 5 Subject:");
                for (int i = 0; i < 5; i++)
                    Console.WriteLine(marks[i] + "   ");
                Console.WriteLine();
                Console.WriteLine("Total:" + total);
                Console.WriteLine("Average:" + average);
                Console.WriteLine("Grade:" + grade);
            
        }
        class MultiLevel
        {
            public static void Main(string[]args)
            {
                MarksDetails student1 =new MarksDetails ("Abhijith", 22, "Male", 20190001, "MSC", 5, new int[] { 77, 80, 98, 95, 98 });
                student1.Display();

            }
        }
    }
}
OUTPUT:

![image](https://user-images.githubusercontent.com/97939356/154634672-9f4cee12-94c1-4c80-a8bb-2b49670b1ae2.png)

      11)C# Program to Create a Gray Code
     using System;

     namespace Exercises
    {
     class GrayCode
    {
        static int getGray(int n)
        {
            return n ^ (n >> 1);
        }
        static void Main(string[]args)
        {
            int InputNum, GrayNum;
            Console.Write("\n Enter the decimal number:");
            InputNum = Convert.ToInt32(Console.ReadLine());
            Console.Write("\n Binary Equivalent of {0}:{1}", InputNum, Convert.ToString(InputNum, 2));
            GrayNum = getGray(InputNum);
            Console.Write("\n GrayCode Equivalent of {0}:{1}", InputNum, Convert.ToString(GrayNum, 2));
        }
    }
      }
      OUTPUT:

![image](https://user-images.githubusercontent.com/97939356/154635001-ed95122c-4bd6-4d4d-9e7d-238f6df9ef7a.png)

      12)C# Program to calculate volume of 2 boxes and find the resultant volume after addition of 2 boxes by implementing operator overloading
      using System;

     namespace Exercises
    {
    class Box
    {
        float width;
        float height;
        float length;
        public float Volume
        {
            get { return width * height * length; }
        }
        public Box(float width, float height, float length)
        {
            this.width = width;
            this.height = height;
            this.length = length;
        }
        public static float operator +(Box box1, Box box2)
        {
            return box1.Volume + box2.Volume;
        }
        public override string ToString()
        {
            return "box with width" + width + "height" + height + "and length" + length;
        }
    }
    class OperatorOverloading
    {
        public static void Main()
        {
            Box box1 = new Box(10, 20, 30);
            Box box2 = new Box(25, 32, 15);
            Console.WriteLine("Volume of {0} is: {1}", box1, box1.Volume);
            Console.WriteLine("Volume of {0} is: {1}", box2, box2.Volume);
            Console.WriteLine("Volume after adding boxes: {0}", box1 + box2);
        }
    }
      }
      OUTPUT:

![image](https://user-images.githubusercontent.com/97939356/154635488-8c001601-0eb0-46a3-8256-e798796ff5f2.png)

      13)C# Program to Implement Principles of Delegate(converting input string to uppercase first,last and entire string)
      using System;

    namespace Exercises
    {
    class Delegate
    {
        delegate string UppercaseDelegate(string input);
        static string UppercaseFirst(string input)
        {
            char[] buffer = input.ToCharArray();
            buffer[0] = char.ToUpper(buffer[0]);
            return new string(buffer);
        }
        static string UppercaseLast(string input)
        {
            char[] buffer = input.ToCharArray();
            buffer[buffer.Length - 1] = char.ToUpper(buffer[buffer.Length - 1]);
            return new string(buffer);
        }
        static string UppercaseAll(string input)
        {
            return input.ToUpper();
        }
        static void WriteOutput(string input, UppercaseDelegate del)
        {
            Console.WriteLine("INPUT String:{0}", input);
            Console.WriteLine("Output String:{0}", del(input));
        }
        static void Main()
        {
            WriteOutput("tom",new UppercaseDelegate(UppercaseFirst));
            WriteOutput("tom", new UppercaseDelegate(UppercaseLast));
            WriteOutput("tom", new UppercaseDelegate(UppercaseAll));
        }

    }
      }
      OUTPUT:

![image](https://user-images.githubusercontent.com/97939356/154635954-242f946c-5cd4-46d9-a11e-029e341768c1.png)

      14)C# Program to generate register number automatically for 100 students usinf=g static constructer
      using System;

    namespace Exercises
    {
    class RegisterNum
    {
        int regNo;
        static int startNum;
        static RegisterNum()
        {
            startNum = 20210000;
        }
        RegisterNum()
        {
            regNo = ++startNum;
        }
        public static void Main(string[]args)
        {
            for(int i=0;i<100;i++)
            {
                RegisterNum Student = new RegisterNum();
                Console.WriteLine("Student{0}:{1}", i + 1, Student.regNo);
            }
        }
    }
      }

            Output:

![image](https://user-images.githubusercontent.com/97939356/154636723-85d06d20-b231-4c5e-a85e-a83cea51d2d2.png)
![image](https://user-images.githubusercontent.com/97939356/154636847-9f14a558-ba5b-48ae-a349-9d24b5eaf609.png)
![image](https://user-images.githubusercontent.com/97939356/154636918-e3b9daa0-d1c1-4ce0-8f88-1731d2fe5157.png)

7)C# Program 

      15)C# Program to find the frequency of the word "is" in agiven sentence
      using System;

    namespace Exercises
     {
    class FrequencyIS
    {
        static void Main(string[] args)
        {
            int count = 0;
            string inputString;
            Console.WriteLine("\n----FREQUENCY OF WORD IS-----");
            Console.Write("\nEnter the input string:");
            inputString = Console.ReadLine();
            char[] separator = { ',', ' ', '.', '!', '\n' };
            string testString = inputString.ToLower();
            String[] outcomes = testString.Split(separator);
            foreach (String s in outcomes)
            {
                Console.WriteLine(s);
                if (s == "is")
                    count++;
            }
            Console.WriteLine("\n Number of 'is' in'"+ inputString +"'is:"  + count);
        }
    }
}

OUTPUT:

![image](https://user-images.githubusercontent.com/97939356/154637445-dc06633b-861b-4a59-ac6f-6036c27031cb.png)


      16)C# program that bench mark 2D,Jagged array allocation 
      using System;
      using System.Diagnostics;

      namespace Exercises
      {
    class BenchmarkAllocation
    {
        const int max = 100000;
        static void Main(string[] args)
        {
            var Arr2D = new int[100, 100];
            var ArrJagged = new int[100][];
            for (int i = 0; i < 100; i++)
            {
                ArrJagged[i] = new int[100];
            }
            var Stopwatch2D = Stopwatch.StartNew();
            for (int i = 0; i < max; i++)
            {
                for (int j = 0; j < 100; j++)
                {
                    for (int k = 0; k < 100; k++)
                    {
                        Arr2D[j, k] = k;
                    }
                }
            }
            Stopwatch2D.Stop();
            var StopwatchJagged = Stopwatch.StartNew();
            for (int i = 0; i < max; i++)
            {
                for (int j = 0; j < 100; j++)
                {
                    for (int k = 0; k < 100; k++)
                    {
                        Arr2D[j, k] = k;
                    }
                }
            }
            StopwatchJagged.Stop();
            Console.Write("\n Time Taken for Allocation in case of 2D array:");
            Console.WriteLine(Stopwatch2D.Elapsed.TotalMilliseconds + "millisecond");
            Console.Write("\n Time Taken for Allocation in case of Jagged array:");
            Console.WriteLine(StopwatchJagged.Elapsed.TotalMilliseconds + "millisecond");
        }
    }
      }

      OUTPUT:
      
   ![image](https://user-images.githubusercontent.com/97939356/156500325-e0d82e4c-335a-486f-8b14-9be3d585000a.png)

      17)C# Program to find the sum of the values on diagonal of the matrix
             using System;
            namespace Exercises
            {
            class SumOfDiagonal
            {
        static void Main(string[] args)
        {
            int MaxRow, MaxCol, Sum = 0;
            int[,] Matrix;
            Console.WriteLine("\n-----SUM OF DIAGONAL OF A MATRIX------\n");
            Console.Write("\n enter the number of rows:");
            MaxRow = Convert.ToInt32(Console.ReadLine());
            Console.Write("\n enter the number of columns:");
            MaxCol = Convert.ToInt32(Console.ReadLine());
            if (MaxRow != MaxCol)
            {
                Console.WriteLine("\n the dimension entered are not a square matrix");
                Console.WriteLine("\n exiting the program");
                return;
            }
            Matrix = new int[MaxRow, MaxCol];
            for (int i = 0; i < MaxRow; i++)
            {
                for (int j = 0; j < MaxCol; j++)
                {
                    Console.Write("\n Enter the ({0},{1} the element of matrix:", (i + 1), (j + 1));
                    Matrix[i, j] = Convert.ToInt32(Console.ReadLine());
                }
            }
            Console.WriteLine("\n the entered matrix is:");
            for (int i = 0; i < MaxRow; i++)
            {
                for (int j = 0; i < MaxCol; j++)
                {
                    Console.Write("  " + Matrix[i, j]);
                    if (i == j)
                    {
                        Sum += Matrix[i, j];
                    }
                }
                Console.WriteLine();
            }
           Console.WriteLine("\n the sum of diagonal is:" + Sum);
        }
    }
      }
      
      OUTPUT:
      
      
      
         11)C# Program to create a file to check the existence of a file and read the content of the file
      using System;
      using System.IO;

      namespace Exercises
      {
    class FileRead
    {
        public static void Main()
        {
            string fileName;
            while (true)
            {
                Console.WriteLine("\n 1.CREATE A FILE:");
                Console.WriteLine("\n 2.Existence of the file:");
                Console.WriteLine("\n 3.Read the content of the file:");
                Console.WriteLine("\n 4.Exit:");
                Console.WriteLine("\n ENTER YOUR CHOICE:");
                int ch = int.Parse(Console.ReadLine());
                switch (ch)
                {
                    case 1:
                        Console.Write("\n Enter the file name to create:");
                        fileName = Console.ReadLine();
                        Console.WriteLine("\nWrite the content to the file:");
                        string r = Console.ReadLine();
                        using (StreamWriter fileStr = File.CreateText(fileName)) 
                            {
                            fileStr.WriteLine(r);
                             }
                        Console.WriteLine("File is Created"); 
                        break;
                    case 2:
                        Console.Write("\n enter the file name:");
                        fileName = Console.ReadLine();
                        if (File.Exists(fileName))
                        {
                            Console.WriteLine("File exist");
                        }
                        else
                        {
                            Console.WriteLine("\n file does not exist in current director");
                        }
                        break;
                        case 3:
                        Console.Write("Enter the file name to read the content:");
                        fileName = Console.ReadLine();
                        if (File.Exists(fileName))
                        {
                            using (StreamReader sr= File.OpenText(fileName))
                            {
                                string s = "  ";
                                Console.WriteLine("\n here the content of the file:");
                                while ((s = sr.ReadLine()) != null)
                                {
                                    Console.WriteLine(s);
                                }
                                Console.WriteLine(" ");
                            }
                        }
                        else
                        {
                            Console.WriteLine("\n File does not exist");
                        }
                        break;
                        case 4:
                        Console.WriteLine("\n Exiting");
                        return;
                        default:
                        Console.WriteLine("\n Invalid choice");
                        break;
                } 
            }
        }
    }
      }
      OUTPUT:
      
   ![image](https://user-images.githubusercontent.com/97939356/156507495-33a7644d-043f-42b9-936c-ba239343a781.png)
   
   ![image](https://user-images.githubusercontent.com/97939356/156507583-c36d4822-9bfd-4251-b049-42f6f3e9d749.png)
   
   ![image](https://user-images.githubusercontent.com/97939356/156507653-4c9c5c6b-b02e-497b-86cc-3c8c2cb111f1.png)
  
       12)C# program to perform the file comparison
      using System;
      using System.IO;

      namespace Exercises
      {
    class FileRead
    {
        public static void Main()
        {
            string file1;
            string file2;
            Console.Write("Enter the first file path:");
            file1 = Console.ReadLine();
            Console.Write("Enter the first file path:");
            file2 = Console.ReadLine();
            if (!File.Exists(file1))
            {
                Console.WriteLine("Frist file does not exist!");
            }
            else if (!File.Exists(file2))
            {
                Console.WriteLine("Second file does not exist!");
            }
            else if (File.ReadAllText(file1) == File.ReadAllText(file2))
            {
                Console.WriteLine("Both file contain the same content");
            }
            else
            {
                Console.WriteLine("Content of the file are not same");
            }
        }
    }
      }
      
      OUTPUT:
   ![image](https://user-images.githubusercontent.com/97939356/156508728-1ea685ee-e1d9-417c-bbb5-78b6f5c5e015.png)
  
  ![image](https://user-images.githubusercontent.com/97939356/156509069-5aad416d-c478-42c1-8217-eb3f4ed3279e.png)

      13)C# program to implement Icomparable Interface
      using System;
      namespace  Exercises
      {
    class Fraction:IComparable
    {
        int z, n;
        public Fraction(int z,int n)
        {
            this.z = z;
            this.n = n;
        }
        public static Fraction operator +(Fraction a, Fraction b)
        {
            return new Fraction(a.z * b.n + a.n * b.z, a.n * b.n);
        }
        public int CompareTo(object obj)
        {
            Fraction f = (Fraction)obj;
            if ((float)z / n < (float)f.z / f.n)
                return -1;
            else if ((float)z / n > (float)f.z / f.n)
                return 1;
            else
                return 0;
        }
        public override string ToString()
        {
            return z + "/" + n;
        }

    }
    class ICompInterface
    {
        public static void Main()
        {
            Fraction[] a =
            {
                new Fraction(5,2),
                new Fraction(29,6),
                new Fraction(4,5),
                new Fraction(10,8),
                new Fraction(34,7)
            };
            Array.Sort(a);
            Console.WriteLine("Implementing the IComparable Interface in" + "Displaying Fraction:");
            foreach (Fraction f in a)
            {
                Console.WriteLine(f + " ");
            }
            Console.WriteLine();
            Console.ReadLine();
        }
    }
      }
                
    OUTPUT:                
![image](https://user-images.githubusercontent.com/97939356/156509792-93cd2960-5495-4f10-bf1c-cf279df0e4c2.png)

14)C# program to create thread pool

      using System;
      using System.Threading;

      namespace Exercises
      {
      class ThreadPoolProg
    {
        public void ThreadFun1(object obj)
        {
        
            int loop = 0;
            for(loop=0;loop<=4;loop++)
            {
              Console.WriteLine("Thread 1 is executing");
            }
        }
        public void ThreadFun2(object obj)
        {

            int loop = 0;
            for (loop = 0; loop <= 4; loop++)
            {
                Console.WriteLine("Thread 2 is executing");
            }
        }
        public static void Main()
        {
            ThreadPoolProg TP = new ThreadPoolProg();
            for (int i = 0; i < 2; i++)
            {
                   ThreadPool.QueueUserWorkItem(new WaitCallback(TP.ThreadFun1));
                   ThreadPool.QueueUserWorkItem(new WaitCallback(TP.ThreadFun2));
            }
            Console.ReadKey();
        }          
    }
      }
      OUTPUT:
   ![image](https://user-images.githubusercontent.com/97939356/156510404-ebd774f4-90e0-476e-b241-3e95f2710185.png)
   
      15)C# program to demonstrate error handling using Try,Catch and Finally Block
      using System;
      namespace p15_d.e
      {
    class Exceptionhandling
    {
        static void Main(string[] args)
        {
            Age a = new Age();
            try
            {
                a.displayAge();
            }
            catch(AgeIsNegativeException e)
            { 
                Console.WriteLine("AgeIsNegativeException:{0}", e.Message);
            }
            finally
            {
                Console.WriteLine("Exception of Finallyblock is done");
            }
        }
    }
      }
      public class AgeIsNegativeException : Exception
      {
    public AgeIsNegativeException(string message) : base(message)
    {
    }
      }
      public class Age
      {
    int age = -5;
    public void displayAge()
    {
        if (age < 0)
        {
            throw (new AgeIsNegativeException("Age cannot be negative"));
        }
        else
        {
            Console.WriteLine("Age is:{0}", age);
        }
    }
      }
      
      OUTPUT:
      
   ![image](https://user-images.githubusercontent.com/97939356/156511176-53f2edd7-50ab-4cfa-97c5-04798657684d.png)
   
        1)C# Program to Convert Digits to Words.    
        using System;
      using System.Collections.Generic;
      using System.ComponentModel;
      using System.Data;
      using System.Drawing;
      using System.Linq;
      using System.Text;
      using System.Threading;
      using System.Windows.Forms;

      namespace prgm44
      {
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            backgroundWorker1.WorkerReportsProgress = true;
            backgroundWorker1.RunWorkerAsync();
        }

        private void backgroundWorker1_DoWork(object sender, DoWorkEventArgs e)
        {
            for (int i = 1; i <= 100; i++)
            {
                Thread.Sleep(50);
                backgroundWorker1.ReportProgress(i);
            }
        }

        private void backgroundWorker1_ProgressChanged(object sender, ProgressChangedEventArgs e)
        {
            progressBar1.Value = e.ProgressPercentage;
            this.Text = "Progress: " + e.ProgressPercentage.ToString() + "%";
        }

    }
      }
      
      OUTPUT:
      
![image](https://user-images.githubusercontent.com/97939356/158940789-c1872d91-c34b-4d81-be83-343440e93929.png)

        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        3) C# Program to Perform Reversal, Padding and Trimming Operations on  string. 
            using System;
      using System.Collections.Generic;
      using System.ComponentModel;
      using System.Data;
      using System.Drawing;
      using System.Linq;
      using System.Text;
      using System.Threading.Tasks;
      using System.Windows.Forms;

      namespace prgm555
      {
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            System.Timers.Timer timer = new System.Timers.Timer();
            timer.Interval = 1000;//1s 
            timer.Elapsed += Timer_Elapsed;
            timer.Start();
        }
        private void Timer_Elapsed(object sender, System.Timers.ElapsedEventArgs e)
        {
            circularProgressBar1.Invoke((MethodInvoker)delegate
            {
                circularProgressBar1.Text = DateTime.Now.ToString("hh:mm:ss"); circularProgressBar1.SubscriptText = DateTime.Now.ToString("tt");//AM or PM
             });
        }
    }
      }
      
      OUTPUT:
   ![image](https://user-images.githubusercontent.com/97939356/158940499-85791966-2dad-441f-bb85-35d22c0c687f.png)
       
      21. C# Program to perform a number guessing game. 
        using System;
      using System.Collections.Generic;
      using System.ComponentModel;
      using System.Data;
      using System.Drawing;
      using System.Linq;
      using System.Text;
      using System.Threading.Tasks;
      using System.Windows.Forms;

      namespace guesses2
      {
    public partial class Form1 : Form
    {
        // Intialising component  
        static Random r = new Random();
        int value;
        int guessnum;
        int win = 10;
        int guess = 1;
        public Form1()
        {
            InitializeComponent();
        
            value = r.Next(10);
            this.Controls.Clear();
            this.BackColor = Color.SkyBlue;
            this.AutoSize = true;
            this.Padding = new Padding(16);
            Label label = new Label();
            label.Text = "Pick a number between 1 and 100";
            label.Bounds = new Rectangle(10, 20, 340, 40); 
            label.Font = new Font("Arial", 16);
            textBox1 = new TextBox();
            textBox1.Bounds = new Rectangle(20, 50, 120, 80);
            textBox1.Font = new Font("Arial", 24);

            button1 = new Button();
            button1.Text = " Check Your Guess ";
            button1.Bounds = new Rectangle(160, 50, 120, 40);
            button1.BackColor = Color.LightGray;
            button1.Click += new EventHandler(button1_Click);
            Label label2 = new Label();
            label2.Text = "Low Guess";
            label2.Bounds = new Rectangle(20, 150, 160, 40); label2.Font = new Font("Arial", 18);
            richTextBox1 = new RichTextBox();
            richTextBox1.Bounds = new Rectangle(20, 190, 160, 300); richTextBox1.Font = new Font("Arial", 16);
            Label label3 = new Label();
            label3.Text = "High Guess";
            label3.Bounds = new Rectangle(180, 150, 160, 40); label3.Font = new Font("Arial", 18);
            richTextBox2 = new RichTextBox();
            richTextBox2.Bounds = new Rectangle(180, 190, 160, 300); richTextBox2.Font = new Font("Arial", 16);
            label4 = new Label();
            label4.Bounds = new Rectangle(20, 100, 340, 40); label4.Font = new Font("Arial", 16);
            this.Controls.Add(label);
            this.Controls.Add(textBox1);
            this.Controls.Add(button1);
            this.Controls.Add(label4);
            this.Controls.Add(label2);
            this.Controls.Add(label3);
            this.Controls.Add(richTextBox1);
            this.Controls.Add(richTextBox2);
        }
        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
            // Coding of game  
            if (textBox1.Text == "")
            {
                return;
            }
            guessnum = Convert.ToInt32(textBox1.Text);
            textBox1.Text = String.Empty;
            if (win >= 0)
            {
                if (guessnum == value)
                {
                    MessageBox.Show("You have guessed the number! \n The number was " + value); 
                    InitializeComponent();
                }
                else if (guessnum < value)
                {
                    richTextBox1.Text += guessnum + "\n";
                    MessageBox.Show("wrong Guess and number of guesses left are " + (10 - guess));
                }
                else if (guessnum > value)
                {
                    richTextBox2.Text += guessnum + "\n";
                    MessageBox.Show("wrong Guess and number of guesses left are " + (10 - guess));
                }
                guess++;
                win--;
            }
            if (guess == 11)
            {
                MessageBox.Show( "You loose,Correct Guess is " + value);
            }
        }

        private void label3_Click(object sender, EventArgs e)
        {

        }
        /*static void Main()
      {
       Application.Run(new Form1());
      }*/
    }
      }
      OUTPUT:
      
![image](https://user-images.githubusercontent.com/97939356/158955978-048dc95d-1090-4e4a-837d-ae20b8caf75e.png)
![image](https://user-images.githubusercontent.com/97939356/158956309-e6b77d91-1fdb-4b1e-82e7-9d22d3d37701.png)
![image](https://user-images.githubusercontent.com/97939356/158956430-eda699e6-beca-4c03-846b-0b6fdd8b98e5.png)




   
   


   


      
