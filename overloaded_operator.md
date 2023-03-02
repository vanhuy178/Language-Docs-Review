# Language-Docs-Review
Reveiw Important Point in programming language

```
class Vector // overloaded operator
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
        public static Vector operator +(Vector v1, double value)
        {
            double x = v1.x + value;
            double y = v1.y + value;
            Vector v = new Vector(x, y);
            return v;
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

```
