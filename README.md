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
OUTPUT:![image](https://user-images.githubusercontent.com/97939356/154634672-9f4cee12-94c1-4c80-a8bb-2b49670b1ae2.png)

