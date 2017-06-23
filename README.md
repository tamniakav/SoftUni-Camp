# SoftUni-Camp
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace SoftUni_Camp
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int car = 0;
            int microbus = 0;
            int minibus = 0;
            int bus = 0;
            int train = 0;
            int allGroups = 0;

            for (int i = 1; i <= n; i++)
            {
                int groups = int.Parse(Console.ReadLine());

                allGroups += groups;

                if (groups < 6)
                {
                    car += groups;
                }
                else if (groups < 13)
                {
                    microbus += groups;
                }
                else if (groups < 26)
                {
                    minibus += groups;
                }
                else if (groups < 41)
                {
                    bus += groups;
                }
                else
                {
                    train += groups;
                }
            }

            double carPercentage = ((double)car / (double)allGroups) * 100;
            double microbusPercentage = ((double)microbus / (double)allGroups) * 100;
            double minibusPercentage = ((double)minibus / (double)allGroups) * 100;
            double busPercentage = ((double)bus / (double)allGroups) * 100;
            double trainPercentage = ((double)train / (double)allGroups) * 100;

            Console.WriteLine($"{carPercentage:f2}%");
            Console.WriteLine($"{microbusPercentage:f2}%");
            Console.WriteLine($"{minibusPercentage:f2}%");
            Console.WriteLine($"{busPercentage:f2}%");
            Console.WriteLine($"{trainPercentage:f2}%");
        }
    }
}
