# Inheritance
# Area of Shapes


Coding-

package calculatearea;
//inheritance program
abstract class Shape{
    public abstract double calculateArea();
}
class Circle extends Shape{
    private double radius;
    public Circle(double radius){
        this.radius=radius;
    }
    //area of circle
    @Override
    public double calculateArea(){
        return Math.PI*radius*radius;
        
    }
   
}
//rectangle class
class Rectangle extends Shape{
    private double length,width;
    public Rectangle(double length,double width){
        this.length=length;
        this.width=width;
        
    }
    //area of rectangle override
    @Override
    public double calculateArea(){
        return length*width;
    }
}
//square class
class Square extends Shape{
    private double side;
    public Square(double side){
        this.side=side;
    }
    //area of square override
    @Override
    public double calculateArea(){
        return side*side;
    }
}
//triangle class
class Triangle extends Shape{
    private double base,height;
    public Triangle(double base,double height){
        this.base=base;
        this.height=height;


}
    //area of triangle override
    @Override
    public double calculateArea(){
        return 0.5*base*height;
    }
}
public class ShapeInheritanceExample{
    public static void main(String[]args){
        //shape objects
        Shape circle=new Circle(5);
        Shape rectangle=new Rectangle(4,5);
        Shape square = new Square(4);
        Shape triangle=new Triangle(2,3);
        //calculating areas of shapes
        System.out.println("Area of the circle is:"+circle.calculateArea());
        System.out.println("Area of rectangle is:"+rectangle.calculateArea());
        System.out.println("Area of square is:"+square.calculateArea());
        System.out.println("Area of triangl is:"+triangle.calculateArea());
    }
}

output-

Area of the circle is:78.53981633974483
Area of rectangle is:20.0
Area of square is:16.0
Area of triangle is:3.0

