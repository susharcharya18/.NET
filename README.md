# .NET
1)C# Program to Print a Binary Triangle
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

2)C# Program to Illustrate Multilevel Inheritance with Virtual Method(displaying students details)
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

4)C# Program to Create a Gray Code
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

6)C# Program to calculate volume of 2 boxes and find the resultant volume after addition of 2 boxes by implementing operator overloading
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

7)C# Program to Implement Principles of Delegate(converting input string to uppercase first,last and entire string)
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





