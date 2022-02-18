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
