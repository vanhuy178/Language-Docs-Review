# Language-Docs-Review
Reveiw Important Point in programming language

1. Create a file with the name is: ```MyException.cs```
```
using System;
namespace MyException
{
    public class NoNameException : Exception
    {
        public NoNameException() : base("No name!!!")
        {

        }
    }
    public class AgeException : Exception
    {
        public AgeException() : base("Too old or Unold!!!")
        {

        }
    }
}
```

2. use it in ```Program.cs```

```
 static void Register(string name, int age)
    {
        if (string.IsNullOrEmpty(name))
        {
            throw new NoNameException();
        }
        else if (age < 18 || age > 35)
        {
            throw new AgeException();
        }

        WriteLine("Register successfully!!");
    }
```
