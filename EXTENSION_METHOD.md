# Language-Docs-Review
Reveiw Important Point in programming language

## EXTENSION METHOD

1. We defined an other namespace and we start to define static methods 
```
MyExtension.cs
using System;
namespace MyLib
{
    public static class Xyz
    {
        public static double MySquare(this int x) => x * x;
        public static double MySquareRoot(this int x) => Math.Sqrt(x);

        public static double MySin(this int x) => Math.Sin(x);

        public static double MyCos(this int x) => Math.Cos(x);
    }
}
```
2. we import ```namespace MyLib``` into ```Program.cs```, so we can call static methods;
```
  // Using extension method
        int x = 105;
        WriteLine(x.MySquare());
        WriteLine(x.MySin());
        WriteLine(x.MyCos());
        WriteLine(x.MySquareRoot());
```
