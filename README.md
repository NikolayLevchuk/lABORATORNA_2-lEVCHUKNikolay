# lABORATORNA_2-lEVCHUKNikolay





static void Main(string[] args)
        {
            double u = 0;
            double S = 0;
            int a = 0;
            double x;
            string b;
            Console.WriteLine("Введите значение ");

            do
            {
                b = Console.ReadLine();
                x = Convert.ToDouble(b);
                if (a > x)
                {
                    Console.WriteLine("Введите другое значение ");
                }
            } while (a > x);

            for (int i = 0; i <= x; i++)
            {
                u += (Math.Pow(-1, i) * Math.Pow(i,2) + Math.Pow(-1, Math.Pow(i,2) - 1) *i) / (2*Math.Pow(i, 3) + 3);
                S *= u;
                Console.WriteLine("u" + i + "=" + u);
                u = 0;
            }
            Console.WriteLine("Добуток = " + S);
            Console.ReadKey();
        }
