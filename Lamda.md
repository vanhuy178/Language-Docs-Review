# Language-Docs-Review
Reveiw Important Point in programming language

1. Lamda expression can assign to delegate.

```
    static void Main(string[] args)
    {
        // how to write lamda expression and how can we use it;
        Action<string> message;
        message = (string a) => WriteLine(a); // ~ delegate void name(string s) ~ Action<string>
        message("Delegate with lamda expression");

        Func<int, int, int> calculator;


        calculator = (int a, int b) =>
         {
             int sum = a + b;
             return sum;
         };

        calculator(10, 10);
        
        
        Action hi;
        hi = () => WriteLine("Hi fen");
        hi?.Invoke(); 
        
        /*
            This is the same with above
            if(hi != null) {
                hi.Invoke();
            };
        */

        Action<string, string> welcome;
        welcome = (mgs, name) =>
        {
            ForegroundColor = ConsoleColor.Yellow;
            WriteLine($"{mgs} {name}");
            ResetColor();
        };
        welcome("Welcome to my Home", "Hien");
        
        
        // Lamda expression in ASP.NET core

        // Example;

        int[] arrayNumber = { 1, 3, 4, 5, 6, 7, 9, 10 };
        WriteLine("arrayNumber.ToList().ForEach");
        arrayNumber.ToList().ForEach((x) =>
        {
            if (x % 2 == 0)
            {
                WriteLine(x);
            }
        });

        var divideFour = arrayNumber.Where((a) =>
         {
             return a % 4 == 0;
         }
         );

        // var result = arrayNumber.Select((int item) =>
        // { // must have return value
        //     return Math.Sqrt(item);

        // }); // select is same with map JavaScript;
        // foreach (var item in result)
        // {
        //     WriteLine("The result of arrayNumber with Select method: " + item);
        // }

}

```
