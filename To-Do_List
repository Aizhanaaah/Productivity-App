namespace ToDoList
{
    internal class Program
    {
        static void Main(string[] args)
        {
            DateTime currentTime = DateTime.Now;
            Console.WriteLine("Date and time: {0}", currentTime.ToString());
            Console.WriteLine(" ");
            Console.WriteLine("Your Daily To-Do List");
            Console.WriteLine(" ");
            Console.Write("How many tasks will you accomplish today? ");
            int n = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine(" ");
            Console.WriteLine("Write your tasks below:");
            string priority;
            List<int> priorityList = new List<int>();
            int priorityPercentage = 0;
            for (int i = 0; i < n; i++)
            {
                Console.Write("{0}. ", i+1);
                string tasks = Console.ReadLine();
                Console.Write("Priority (high, medium, low): ");
                priority = Console.ReadLine();
                if (priority == "high")
                {
                    priorityPercentage += 100;
                }
                else if (priority == "medium")
                {
                    priorityPercentage += 50;
                }
                else if (priority == "low")
                {
                    priorityPercentage += 10;
                }
                priorityList.Add(priorityPercentage);
            }
            Console.WriteLine(" ");
            Console.WriteLine(" ");
            int did = 0;
            int didnt = 0;
            for (int i = 0; i < n; i++)
            {
                Console.Write("Did you accomplish the Task {0}? (y/n):", i+1);
                char done = Convert.ToChar(Console.ReadLine());
                if (done == 'y')
                {
                    did++;
                }
                else
                {
                    didnt++;
                    priorityPercentage -= priorityList[i];  
                }
            }
            Console.WriteLine(" ");
            Console.WriteLine("You have accomplished {0} tasks today!", did);
            Console.WriteLine("You have not accomplished {0} tasks today!", didnt);
            Console.WriteLine("Your productivity level for today is: {0} percent!", priorityPercentage);
        }
    }
}
