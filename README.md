using System;

namespace _8.BeerKegs
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());
            double volume = 0;
            double biggestKeg = double.MinValue;
            string biggestKegModel ="";
            for (int i =0; i<n; i++)
            {
                string model = Console.ReadLine();
                float radius = float.Parse(Console.ReadLine());
                int height =int.Parse(Console.ReadLine());
                volume = (Math.PI * (radius *radius )* height);
                if (volume > biggestKeg)
                {
                    biggestKeg = volume;
                    biggestKegModel = model;
                }


            }
            Console.WriteLine(biggestKegModel);
        }
    }
}
