using System;
using System.Linq;

namespace Number_Wizard
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.WriteLine("Would you like to use the Armstrong Number Checker (A), the Pythagorean Triples Checker (P) or Exit (E)?\n" + "Please enter either \"A\", \"P\" or \"E\" to continue:");
                string opt = Console.ReadLine().ToUpper();

                if (opt == "A")
                {
                    Armstrong();
                }
                else
                    if (opt == "P")
                {
                    Pythagoras();
                }
                else
                    if (opt == "E")
                {
                    Environment.Exit(0);
                }
                else
                {
                    Console.WriteLine("I think you might've made a mistake...Try again\n");
                }
            }
        }



        static void Armstrong()
        {
            Console.Write("\nPlease input a number: ");
            string num = Console.ReadLine();
            double length = num.Length;
            double total = 0;
            double num2 = long.Parse(num.ToString());
            // Console.Write(num2.GetType() + "\n");




            foreach (char c in num)
            {
                double digit = int.Parse(c.ToString());
                // Console.Write(digit + "\n");
                // Console.Write(digit.GetType() + "\n");
                digit = Math.Pow(digit, length);
                // Console.Write(digit + "\n");
                total += digit;
            }
            if (num2 == total)
            {
                Console.Write(num2 + " IS an Armstrong Number\n\n");
            }
            else
            {
                Console.Write(num2 + " is NOT an Armstrong Number\n\n");
            }

        }
        static void Pythagoras()
        {
            Console.Write("\nPlease input the 3 lengths of the Triangle seperated by a space: ");
            string sides = Console.ReadLine();
            string[] indi = sides.Split(' ');

            try
            {
                int[] test = Array.ConvertAll(indi, int.Parse);
            }
            catch (FormatException)
            {
                Console.WriteLine("Input contains non-numeric characters");
                Pythagoras();
            }

            int[] numindi = Array.ConvertAll(indi, int.Parse);
            Array.Sort(numindi);
            int[] numindi_sqr = numindi.Select(x => x * x).ToArray();


            if (numindi_sqr.Length != 3)
            {
                Console.WriteLine("Input contains too many or not enough numbers");
                Pythagoras();
            }
            else
                if ((numindi_sqr[0] + numindi_sqr[1] == numindi_sqr[2]))
                {
                Console.WriteLine("Yes, " + string.Join(" ", numindi) + " are Pythagorean triples\n");
                }
            else
            {
                Console.WriteLine("No, " + string.Join(" ", numindi) + " are NOT Pythagorean triples\n");
            }





        }

    }
}
