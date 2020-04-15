Абстрактная форма суперкласса и реализация в подклассах
Реализуйте суперкласс Shape и его подклассы Circle, Rectangle и Square, как показано на диаграмме классов.
***
<http://online.platforma.institute/asset-v1:digitalspirit.ru+1+1+type@asset+block@ExerciseOOP_ShapeAbstract.png>
***
В этом задании Shape должен быть определен как абстрактный класс, который содержит:
***
* Две переменные экземпляра с модификатором доступа protected: color (String) и filled(логический). Protected переменные могут быть доступны для его подклассов и классов в одном пакете. Они обозначены знаком «#» на диаграмме классов.
* Getter и setter для всех переменных экземпляра, а также метод toString().
* Два абстрактных метода getArea() и getPerimeter() (показаны курсивом на диаграмме классов).
Подклассы Circle и Rectangle должны переопределять абстрактные методы getArea() и getPerimeter() и обеспечивать правильную реализацию. Они также переопределяют метод toString ().
***
Напишите класс c методом main для проверки следующих вопросов, связанных с полиморфизмом, и объясните результаты. Некоторые операторы могут вызвать ошибки компиляции. Объясните ошибки, если таковые имеются.
***
```
Shape s1 = new Circle(5.5, "red", false);   // Upcast (приведение типов от более конкретного к более общему)
                                            // Circle к Shape
System.out.println(s1);                    // метод какого класса срабатывает?
System.out.println(s1.getArea());          // метод какого класса срабатывает?
System.out.println(s1.getPerimeter());     // метод какого класса срабатывает?
System.out.println(s1.getColor());
System.out.println(s1.isFilled());
System.out.println(s1.getRadius());

Circle c1 = (Circle)s1; // Downcast (приведение типа от более общего к более конкретному)
                        // преобразование обратно к Circle
System.out.println(c1);
System.out.println(c1.getArea());
System.out.println(c1.getPerimeter());
System.out.println(c1.getColor());
System.out.println(c1.isFilled());
System.out.println(c1.getRadius());

Shape s2 = new Shape();

Shape s3 = new Rectangle(1.0, 2.0, "red", false);   // Upcast
System.out.println(s3);
System.out.println(s3.getArea());
System.out.println(s3.getPerimeter());
System.out.println(s3.getColor());
System.out.println(s3.getLength());

Rectangle r1 = (Rectangle)s3;   // downcast
System.out.println(r1);
System.out.println(r1.getArea());
System.out.println(r1.getColor());
System.out.println(r1.getLength());

Shape s4 = new Square(6.6);     // Upcast
System.out.println(s4);
System.out.println(s4.getArea());
System.out.println(s4.getColor());
System.out.println(s4.getSide());

// Обратите внимание, что мы понижаем (downcast) Shape s4 до Rectangle,
//  который является суперклассом для Square, вместо преобразования к Square
Rectangle r2 = (Rectangle)s4;
System.out.println(r2);
System.out.println(r2.getArea());
System.out.println(r2.getColor());
System.out.println(r2.getSide());
System.out.println(r2.getLength());

// Downcast Rectangle r2 к Square
Square sq1 = (Square)r2;
System.out.println(sq1);
System.out.println(sq1.getArea());
System.out.println(sq1.getColor());
System.out.println(sq1.getSide());
System.out.println(sq1.getLength());
```
***
Что такое реализация абстрактного метода и абстрактного класса?

