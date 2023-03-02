# Language-Docs-Review
Reveiw Important Point in programming language

```
class Vector 
    {
        double x;
        double y;
        public Vector(double _x, double _y)
        {
            x = _x;
            y = _y;
        }
        public void Info() => WriteLine($"X: {x}, Y: {y}");

        // vector --> vector + vector;
        public static Vector operator +(Vector v1, Vector v2)
        {
            double x = v1.x + v2.x;
            double y = v1.y + v2.y;
            Vector v = new Vector(x, y);
            return v;
        }
        public static Vector operator +(Vector v1, double value) // overloaded operator
        {
            double x = v1.x + value;
            double y = v1.y + value;
            Vector v = new Vector(x, y);
            return v;
        }
        
         // indexer

        public double this[int i]
        {
            set
            {
                switch (i)
                {
                    case 0:  //x
                        x = value;
                        break;
                    case 1: //x
                        y = value;
                        break;
                    default:
                        throw new Exception("Error Index");
                }
            }
            get
            {
                switch (i)
                {
                    case 0:  //x
                        return x;
                    case 1: //x
                        return y;
                    default:
                        throw new Exception("Error Index");
                }
            }
        }
        public double this[string s]
        {
            set
            {
                switch (s)
                {
                    case "x":  //x
                        x = value;
                        break;
                    case "y": //x
                        y = value;
                        break;
                    default:
                        throw new Exception("Error Index");
                }
            }
            get
            {
                switch (s)
                {
                    case "x":  //x
                        return x;
                    case "y": //y
                        return y;
                    default:
                        throw new Exception("Error Index");
                }
            }
        }
}

static void Main(string[] args) {
// overloaded operator
Vector vt1 = new Vector(10, 29);
Vector vt2 = new Vector(11, 291);

vt1.Info();
vt2.Info();
var vt3 = vt1 + vt2;
vt3.Info();

// if you + vector with a number like this var vt3 = vt1 + 10;
var vt4 = vt1 + 20;
vt4.Info();
var vt4 = vt1 + 20;
Console.WriteLine($"Tọa độ X: {vt4[0]}, Tọa độ Y: {vt4[1]} by indexer index by number");
Console.WriteLine($"Tọa độ X: {vt4["x"]}, Tọa độ Y: {vt4["y"]} by indexer index by string");

```
