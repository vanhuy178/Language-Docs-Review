# Language-Docs-Review
Reveiw Important Point in programming language

### Delegate in C#


1. Each method must be them same type and return value
```
public delegate void ShowLogg(string message); 

static void Info(string s)
    {
        Console.ForegroundColor = ConsoleColor.DarkGreen;
        Console.WriteLine(s);
        Console.ResetColor();
    }
static void Warning(string s)
    {
        Console.ForegroundColor = ConsoleColor.Red;
        Console.WriteLine(s);
        Console.ResetColor();
    }
```
2. Because delegate is reference type the value of it can be null;

```
static void Main(string[] args) {
  ShowLogg slgg = null; // delegate is reference type so it can be null, delegate can be reference to multiple method;
  
  slgg += Info;
  slgg += Info;
  slgg += Info;
  slgg += Info;
  slgg += Warning;
  slgg += Warning;

  slgg?.Invoke("Love everyone");
}

```
2. We can use delegate is defined by .NET
```
static void Main(string[] args) {
 // Next we talk about Action and Func: this is two delegate build-in by .net, It has generic.
 Action ac1;     // --> delegate void ac1(no params);
 Action<string, int> ac2;    // --> delegate void ac2(string s, int i)
 Action<string> ac3; // delegate void ac3<string s> --> because it received string, and void so we can use two method Info, Warning. 

 ac3 = Warning;
 ac3 += Info;
 Console.WriteLine("Action 3:");
 ac3.Invoke("Love baby");
  
 // Func is the same action but it must have return value
 //Func<int> f1; // -> delegate int f1();
 //Func<int, string, int> f2; // -> delegate int (int i ,  string s); // the last params is the return value

 Func<int, int, int> calulator;
 int a = 10;
 int b = 10;
 // calulator = Add;
 // WriteLine($"Sum: {calulator(a, b)}");
 calulator = Minus;
 WriteLine($"Minus: {calulator(a, b)}");
}
```

4. We can received ```ShowLogg``` as arguments
```
static void Add(int a, int b, ShowLogg logg)
{
    int result = a + b;
    logg?.Invoke($"The sum in logg is: {result}");
}

static void Main(string[] args) { 
Add(10, 20, Info) // 30 with DarkGreen text
}

```
