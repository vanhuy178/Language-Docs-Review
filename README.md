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
