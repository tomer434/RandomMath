













using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp3
{
    class Program
    {
        static void Main(string[] args)
        {
        Start:
            Random NumberGen = new Random();
            int a = NumberGen.Next(1, 11);
            int b = NumberGen.Next(1, 11);
            Console.WriteLine("\nWhat is " + a + " + " + b);
            int Answer = Convert.ToInt32(Console.ReadLine()); // input answer

            int c = (a + b); // the right answer


            int Range = (c - Answer);   // range between numbers // 
            if (Range < 0)
            {
                Range *= -1;
            }
            if (Answer == a + b)
            {
                Console.WriteLine("Well Done!");
                goto Start;
            }
            else
            {
                int respondindex = NumberGen.Next(1, 6);
                switch (respondindex)
                {
                    case 1:
                        Console.WriteLine("Are you even trying?, You were " + Range + " numbers away from the right answer! ");
                        break;
                    case 2:
                        Console.WriteLine("Try Harder!, You were " + Range + " numbers away from the right answer! ");
                        break;
                    case 3:
                        Console.WriteLine("Wrong!, You were " + Range + " numbers away from the right answer! ");
                        break;
                    case 4:
                        Console.WriteLine("Are you joking?, You were " + Range + " numbers away from the right answer! ");
                        break;
                    default:
                        Console.WriteLine("You can do better than that!, You were " + Range + " numbers away from the right answer! ");
                        break;
                }
                goto Start;
            }
        }
    }
}

