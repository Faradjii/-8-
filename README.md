class zachet
{
    static void Main(string[] args)
    {
        Console.Write("Длина массива: ");
        int a = Convert.ToInt32(Console.ReadLine());

        Random random = new Random();
        int[] array = new int[a];

        Console.Write("Минимальное число массива: ");
        int min = Convert.ToInt32(Console.ReadLine());

        Console.Write("Максимальное число массива: ");
        int max = Convert.ToInt32(Console.ReadLine());

        for (int i = 0; i < a; i++)
        {
            array[i] = random.Next(min, max);
        }

        Console.WriteLine("массив: ");

        foreach (var number in array)
        {
            Console.Write(number + " ");
        }
        Console.WriteLine();

        double sum = 0;
        int count = 0;

        foreach (var number in array)
        {
            if (number % 2 != 0)
            {
                sum += number;
                count++;
            }
        }

        double sredneeArefm = sum / count;
        Console.WriteLine("Среднее арифметическое нечетных чисел: " + sredneeArefm);


    }
}
