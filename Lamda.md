# Language-Docs-Review
Reveiw Important Point in programming language

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

}

```
