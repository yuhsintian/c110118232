### hw8_C110118232

請新增一個CShape的子類別CTriangle，其constructor 共有三個double的參數 a,b,c (為直角三角形的三個邊長)，其面積為0.5*a*b，請寫出CTriangle的類別程式與產生其物件的main 程式(顏色為紅色，a=3, b=4, c=5)

```
import java.awt.Color;

class CShape {
    private Color color;

    public CShape(Color color) {
        this.color = color;
    }

    public Color getColor() {
        return color;
    }

    public void setColor(Color color) {
        this.color = color;
    }
}

class CTriangle extends CShape {
    private double a;
    private double b;
    private double c;

    public CTriangle(Color color, double a, double b, double c) {
        super(color);
        this.a = a;
        this.b = b;
        this.c = c;
    }

    public double getArea() {
        return 0.5 * a * b;
    }
}

public class Main {
    public static void main(String[] args) {
        double a = 3;
        double b = 4;
        double c = 5;
        Color color = Color.RED;

        CTriangle triangle = new CTriangle(color, a, b, c);
        System.out.println("Triangle Color: " + triangle.getColor());
        System.out.println("Triangle Area: " + triangle.getArea());
    }
}
```
