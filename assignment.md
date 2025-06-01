
# JAVA PROGRAMS

## 1. Factorial of n
```java
import java.util.Scanner;
public class Factorial {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();
        long fact = 1;
        for(int i = 1; i <= n; i++) {
            fact *= i;
        }
        System.out.println("Factorial: " + fact);
    }
}
```

## 2. Fibonacci Series
```java
import java.util.Scanner;
public class Fibonacci {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter number of terms: ");
        int n = sc.nextInt();
        int a = 0, b = 1;
        System.out.print("Fibonacci Series: " + a + " " + b);
        for(int i = 2; i < n; i++) {
            int c = a + b;
            System.out.print(" " + c);
            a = b;
            b = c;
        }
    }
}
```

## 3. HCF of two Numbers
```java
import java.util.Scanner;
public class HCF {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first number: ");
        int a = sc.nextInt();
        System.out.print("Enter second number: ");
        int b = sc.nextInt();
        int hcf = 1;
        for(int i = 1; i <= a && i <= b; i++) {
            if(a % i == 0 && b % i == 0)
                hcf = i;
        }
        System.out.println("HCF: " + hcf);
    }
}
```

## 4. LCM of two Numbers
```java
import java.util.Scanner;
public class LCM {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter first number: ");
        int a = sc.nextInt();
        System.out.print("Enter second number: ");
        int b = sc.nextInt();
        int max = Math.max(a, b);
        int lcm = max;
        while(true) {
            if(lcm % a == 0 && lcm % b == 0) {
                break;
            }
            lcm++;
        }
        System.out.println("LCM: " + lcm);
    }
}
```

## 5. Count the number of digits of an integer
```java
import java.util.Scanner;
public class CountDigits {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();
        int count = 0;
        if(n == 0) count = 1;
        else {
            while(n != 0) {
                n /= 10;
                count++;
            }
        }
        System.out.println("Number of digits: " + count);
    }
}
```

## 6. Check whether a number is palindrome or not
```java
import java.util.Scanner;
public class Palindrome {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();
        int temp = n, rev = 0;
        while(n != 0) {
            rev = rev * 10 + n % 10;
            n /= 10;
        }
        if(temp == rev)
            System.out.println("Palindrome");
        else
            System.out.println("Not Palindrome");
    }
}
```

## 7. Check whether a number is prime or not
```java
import java.util.Scanner;
public class Prime {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int n = sc.nextInt();
        boolean isPrime = n > 1;
        for(int i = 2; i <= Math.sqrt(n); i++) {
            if(n % i == 0) {
                isPrime = false;
                break;
            }
        }
        if(isPrime)
            System.out.println("Prime");
        else
            System.out.println("Not Prime");
    }
}
```

## 8. Method Overloading
```java
public class Overload {
    void show(int a) {
        System.out.println("a: " + a);
    }
    void show(double a) {
        System.out.println("double a: " + a);
    }
    public static void main(String[] args) {
        Overload obj = new Overload();
        obj.show(5);
        obj.show(5.5);
    }
}
```

## 9. Default Constructor (0-argument)
```java
public class DefaultConstructor {
    DefaultConstructor() {
        System.out.println("Default Constructor called");
    }
    public static void main(String[] args) {
        DefaultConstructor obj = new DefaultConstructor();
    }
}
```

## 10. Parameterized Constructor
```java
public class ParameterizedConstructor {
    int x;
    ParameterizedConstructor(int a) {
        x = a;
    }
    public static void main(String[] args) {
        ParameterizedConstructor obj = new ParameterizedConstructor(10);
        System.out.println("x = " + obj.x);
    }
}
```

## 11. Constructor Overloading
```java
public class ConstructorOverload {
    int x;
    ConstructorOverload() {
        x = 0;
    }
    ConstructorOverload(int a) {
        x = a;
    }
    public static void main(String[] args) {
        ConstructorOverload obj1 = new ConstructorOverload();
        ConstructorOverload obj2 = new ConstructorOverload(5);
        System.out.println("x in obj1 = " + obj1.x);
        System.out.println("x in obj2 = " + obj2.x);
    }
}
```

## 12. Static Members
```java
public class StaticDemo {
    static int count = 0;
    StaticDemo() {
        count++;
    }
    public static void main(String[] args) {
        StaticDemo a = new StaticDemo();
        StaticDemo b = new StaticDemo();
        System.out.println("Count: " + StaticDemo.count);
    }
}
```

## 13. Single Inheritance
```java
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}
class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
    public static void main(String[] args) {
        Dog d = new Dog();
        d.eat();
        d.bark();
    }
}
```

## 14. Method Overriding
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}
class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
    public static void main(String[] args) {
        Animal a = new Dog();
        a.sound();
    }
}
```

## 15. Multilevel Inheritance
```java
class Animal {
    void eat() {
        System.out.println("Eating...");
    }
}
class Dog extends Animal {
    void bark() {
        System.out.println("Barking...");
    }
}
class BabyDog extends Dog {
    void weep() {
        System.out.println("Weeping...");
    }
    public static void main(String[] args) {
        BabyDog bd = new BabyDog();
        bd.eat();
        bd.bark();
        bd.weep();
    }
}
```

## 16. Interface
```java
interface Drawable {
    void draw();
}
class Circle implements Drawable {
    public void draw() {
        System.out.println("Drawing Circle");
    }
    public static void main(String[] args) {
        Drawable d = new Circle();
        d.draw();
    }
}
```

## 17. Multiple Interface
```java
interface Printable {
    void print();
}
interface Showable {
    void show();
}
class Test implements Printable, Showable {
    public void print() {
        System.out.println("Hello");
    }
    public void show() {
        System.out.println("Welcome");
    }
    public static void main(String[] args) {
        Test t = new Test();
        t.print();
        t.show();
    }
}
```

# ANDROID APPLICATIONS

## 1. Display "GOOD MORNING" (Toast and TextView)
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp">
    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="GOOD MORNING"
        android:textSize="24sp" />
    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Show Toast" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.os.Bundle;
import android.widget.Button;
import android.widget.TextView;
import android.widget.Toast;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView textView = findViewById(R.id.textView);
        Button button = findViewById(R.id.button);
        button.setOnClickListener(v ->
            Toast.makeText(MainActivity.this, "GOOD MORNING", Toast.LENGTH_SHORT).show()
        );
    }
}
```

## 2. Add Two Numbers
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="number" />
    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="number" />
    <Button
        android:id="@+id/addButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Add" />
    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textSize="18sp"
        android:paddingTop="16dp" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText num1 = findViewById(R.id.num1);
        EditText num2 = findViewById(R.id.num2);
        Button addButton = findViewById(R.id.addButton);
        TextView result = findViewById(R.id.result);
        addButton.setOnClickListener(v -> {
            int n1 = Integer.parseInt(num1.getText().toString());
            int n2 = Integer.parseInt(num2.getText().toString());
            int sum = n1 + n2;
            result.setText("Sum: " + sum);
        });
    }
}
```

## 3. Average of Three Numbers
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="number" />
    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="number" />
    <EditText
        android:id="@+id/num3"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter third number"
        android:inputType="number" />
    <Button
        android:id="@+id/avgButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Compute Average" />
    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textSize="18sp"
        android:paddingTop="16dp" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText num1 = findViewById(R.id.num1);
        EditText num2 = findViewById(R.id.num2);
        EditText num3 = findViewById(R.id.num3);
        Button avgButton = findViewById(R.id.avgButton);
        TextView result = findViewById(R.id.result);
        avgButton.setOnClickListener(v -> {
            int n1 = Integer.parseInt(num1.getText().toString());
            int n2 = Integer.parseInt(num2.getText().toString());
            int n3 = Integer.parseInt(num3.getText().toString());
            double avg = (n1 + n2 + n3) / 3.0;
            result.setText("Average: " + avg);
        });
    }
}
```

## 4. Odd or Even
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <EditText
        android:id="@+id/numberInput"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter a number"
        android:inputType="number" />
    <Button
        android:id="@+id/checkButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Check" />
    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textSize="18sp"
        android:paddingTop="16dp" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText numberInput = findViewById(R.id.numberInput);
        Button checkButton = findViewById(R.id.checkButton);
        TextView result = findViewById(R.id.result);
        checkButton.setOnClickListener(v -> {
            int num = Integer.parseInt(numberInput.getText().toString());
            if (num % 2 == 0) {
                result.setText("Even Number");
            } else {
                result.setText("Odd Number");
            }
        });
    }
}
```

## 5. Kg to Pound
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <EditText
        android:id="@+id/kgInput"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter weight in Kg"
        android:inputType="numberDecimal" />
    <Button
        android:id="@+id/convertButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Convert" />
    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textSize="18sp"
        android:paddingTop="16dp" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText kgInput = findViewById(R.id.kgInput);
        Button convertButton = findViewById(R.id.convertButton);
        TextView result = findViewById(R.id.result);
        convertButton.setOnClickListener(v -> {
            double kg = Double.parseDouble(kgInput.getText().toString());
            double pound = kg * 2.205;
            result.setText("Pounds: " + pound);
        });
    }
}
```

## 6. Fahrenheit to Celsius
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <EditText
        android:id="@+id/fInput"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter temperature in Fahrenheit"
        android:inputType="numberDecimal" />
    <Button
        android:id="@+id/convertButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Convert" />
    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textSize="18sp"
        android:paddingTop="16dp" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText fInput = findViewById(R.id.fInput);
        Button convertButton = findViewById(R.id.convertButton);
        TextView result = findViewById(R.id.result);
        convertButton.setOnClickListener(v -> {
            double f = Double.parseDouble(fInput.getText().toString());
            double c = (f - 32) * 5 / 9;
            result.setText("Celsius: " + c);
        });
    }
}
```

## 7. Name & Address Layout
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Name" />
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Name" />
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Address" />
    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Address" />
</LinearLayout>
```

## 8. Calculator (+, -, *, /, %, =)
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="numberDecimal" />
    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="numberDecimal" />
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:gravity="center">
        <Button android:id="@+id/add" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="+" />
        <Button android:id="@+id/sub" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="-" />
        <Button android:id="@+id/mul" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="*" />
        <Button android:id="@+id/div" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="/" />
        <Button android:id="@+id/mod" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="%" />
    </LinearLayout>
    <TextView
        android:id="@+id/result"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textSize="18sp"
        android:paddingTop="16dp" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        EditText num1 = findViewById(R.id.num1);
        EditText num2 = findViewById(R.id.num2);
        Button add = findViewById(R.id.add);
        Button sub = findViewById(R.id.sub);
        Button mul = findViewById(R.id.mul);
        Button div = findViewById(R.id.div);
        Button mod = findViewById(R.id.mod);
        TextView result = findViewById(R.id.result);
        add.setOnClickListener(v -> {
            double n1 = Double.parseDouble(num1.getText().toString());
            double n2 = Double.parseDouble(num2.getText().toString());
            result.setText("Result: " + (n1 + n2));
        });
        sub.setOnClickListener(v -> {
            double n1 = Double.parseDouble(num1.getText().toString());
            double n2 = Double.parseDouble(num2.getText().toString());
            result.setText("Result: " + (n1 - n2));
        });
        mul.setOnClickListener(v -> {
            double n1 = Double.parseDouble(num1.getText().toString());
            double n2 = Double.parseDouble(num2.getText().toString());
            result.setText("Result: " + (n1 * n2));
        });
        div.setOnClickListener(v -> {
            double n1 = Double.parseDouble(num1.getText().toString());
            double n2 = Double.parseDouble(num2.getText().toString());
            if (n2 != 0)
                result.setText("Result: " + (n1 / n2));
            else
                result.setText("Cannot divide by zero");
        });
        mod.setOnClickListener(v -> {
            double n1 = Double.parseDouble(num1.getText().toString());
            double n2 = Double.parseDouble(num2.getText().toString());
            result.setText("Result: " + (n1 % n2));
        });
    }
}
```

## 9. Registration Form Layout
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <TextView android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="Name:" />
    <EditText android:layout_width="match_parent" android:layout_height="wrap_content" android:hint="Enter Name" />
    <TextView android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="Address:" />
    <EditText android:layout_width="match_parent" android:layout_height="wrap_content" android:hint="Enter Address" />
    <TextView android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="Phone No.:" />
    <EditText android:layout_width="match_parent" android:layout_height="wrap_content" android:hint="Enter Phone No." android:inputType="phone" />
    <TextView android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="Email Id:" />
    <EditText android:layout_width="match_parent" android:layout_height="wrap_content" android:hint="Enter Email Id" android:inputType="textEmailAddress" />
    <Button android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="SUBMIT" />
</LinearLayout>
```

## 10. Bulk Text Scrollable Vertically
**activity_main.xml:**
```xml
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Dfhkjslk kdjflds\njdnkdkjn kdlksdn\nlkdnlkl ldnls lkdflk\nldnflnl ldknfl\nldkflksd ldkfls ldkfs\nldknld nldkf\nlkdfksnndlnfnldnfk\nndsfnk fjnd m nldn\nfldn kfdnfk\nndsknfkdnfkndknfl\ndkdlknfdknknfnknk"/>
</ScrollView>
```

## 11. Multi-Activity Screen (using INTENT)
**FirstActivity.java:**
```java
import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;
import androidx.appcompat.app.AppCompatActivity;
public class FirstActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_first);
        Button goButton = findViewById(R.id.goButton);
        goButton.setOnClickListener(v -> {
            Intent intent = new Intent(FirstActivity.this, SecondActivity.class);
            startActivity(intent);
        });
    }
}
```
**activity_first.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp">
    <Button android:id="@+id/goButton" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="GO" />
</LinearLayout>
```
**SecondActivity.java:**
```java
import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;
public class SecondActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);
    }
}
```
**activity_second.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:gravity="center"
    android:orientation="vertical">
    <TextView android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="Second Activity" />
</LinearLayout>
```

## 12. Send Data (Message) from One Activity to Another
**FirstActivity.java:**
```java
import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import androidx.appcompat.app.AppCompatActivity;
public class FirstActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_first);
        EditText messageInput = findViewById(R.id.messageInput);
        Button sendButton = findViewById(R.id.sendButton);
        sendButton.setOnClickListener(v -> {
            String message = messageInput.getText().toString();
            Intent intent = new Intent(FirstActivity.this, SecondActivity.class);
            intent.putExtra("message", message);
            startActivity(intent);
        });
    }
}
```
**activity_first.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <EditText android:id="@+id/messageInput" android:layout_width="match_parent" android:layout_height="wrap_content" android:hint="Enter Message" />
    <Button android:id="@+id/sendButton" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="SEND" />
</LinearLayout>
```
**SecondActivity.java:**
```java
import android.os.Bundle;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class SecondActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);
        TextView messageView = findViewById(R.id.messageView);
        String message = getIntent().getStringExtra("message");
        messageView.setText(message);
    }
}
```
**activity_second.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <TextView android:id="@+id/messageView" android:layout_width="wrap_content" android:layout_height="wrap_content" />
</LinearLayout>
```

## 13. Send Data (Integer) from One Activity to Another
**FirstActivity.java:**
```java
import android.content.Intent;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import androidx.appcompat.app.AppCompatActivity;
public class FirstActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_first);
        EditText numberInput = findViewById(R.id.numberInput);
        Button sendButton = findViewById(R.id.sendButton);
        sendButton.setOnClickListener(v -> {
            int number = Integer.parseInt(numberInput.getText().toString());
            Intent intent = new Intent(FirstActivity.this, SecondActivity.class);
            intent.putExtra("number", number);
            startActivity(intent);
        });
    }
}
```
**activity_first.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <EditText android:id="@+id/numberInput" android:layout_width="match_parent" android:layout_height="wrap_content" android:hint="Enter a number" android:inputType="number" />
    <Button android:id="@+id/sendButton" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="SEND" />
</LinearLayout>
```
**SecondActivity.java:**
```java
import android.os.Bundle;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class SecondActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);
        TextView numberView = findViewById(R.id.numberView);
        int number = getIntent().getIntExtra("number", 0);
        numberView.setText(String.valueOf(number));
    }
}
```
**activity_second.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <TextView android:id="@+id/numberView" android:layout_width="wrap_content" android:layout_height="wrap_content" />
</LinearLayout>
```

## 14. Quiz App (with Score Calculation)
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">
    <TextView android:id="@+id/question" android:layout_width="wrap_content" android:layout_height="wrap_content" android:textSize="18sp" />
    <RadioGroup android:id="@+id/options" android:layout_width="wrap_content" android:layout_height="wrap_content">
        <RadioButton android:id="@+id/yes" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="YES" />
        <RadioButton android:id="@+id/no" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="NO" />
    </RadioGroup>
    <Button android:id="@+id/nextButton" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="NEXT" />
    <Button android:id="@+id/submitButton" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="SUBMIT" />
    <TextView android:id="@+id/score" android:layout_width="wrap_content" android:layout_height="wrap_content" android:textSize="18sp" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.os.Bundle;
import android.widget.Button;
import android.widget.RadioButton;
import android.widget.RadioGroup;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    String[] questions = {
        "Is Dennis Ritchie the father of C Language?",
        "Is C object Oriented Language?",
        "Is for a keyword in C language?",
        "Is stdio.h a function in C language?"
    };
    boolean[] answers = {true, false, true, false};
    int index = 0, score = 0;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        TextView question = findViewById(R.id.question);
        RadioGroup options = findViewById(R.id.options);
        RadioButton yes = findViewById(R.id.yes);
        RadioButton no = findViewById(R.id.no);
        Button nextButton = findViewById(R.id.nextButton);
        Button submitButton = findViewById(R.id.submitButton);
        TextView scoreView = findViewById(R.id.score);
        question.setText(questions[index]);
        nextButton.setOnClickListener(v -> {
            int selected = options.getCheckedRadioButtonId();
            if ((selected == R.id.yes && answers[index]) || (selected == R.id.no && !answers[index])) {
                score++;
            }
            index++;
            if (index < questions.length) {
                question.setText(questions[index]);
                options.clearCheck();
            }
        });
        submitButton.setOnClickListener(v -> {
            int selected = options.getCheckedRadioButtonId();
            if (index < questions.length) {
                if ((selected == R.id.yes && answers[index]) || (selected == R.id.no && !answers[index])) {
                    score++;
                }
            }
            scoreView.setText("Total Score: " + score);
        });
    }
}
```

## 15. Play Music App
**activity_main.xml:**
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="16dp">
    <TextView android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="WELCOME TO MUSIC" android:textSize="24sp" />
    <Button android:id="@+id/playButton" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="PLAY" />
    <Button android:id="@+id/pauseButton" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="PAUSE" />
</LinearLayout>
```
**MainActivity.java:**
```java
import android.media.MediaPlayer;
import android.os.Bundle;
import android.widget.Button;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
    MediaPlayer mediaPlayer;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button playButton = findViewById(R.id.playButton);
        Button pauseButton = findViewById(R.id.pauseButton);
        mediaPlayer = MediaPlayer.create(this, R.raw.music); // Place music.mp3 in res/raw
        playButton.setOnClickListener(v -> mediaPlayer.start());
        pauseButton.setOnClickListener(v -> mediaPlayer.pause());
    }
    @Override
    protected void onDestroy() {
        if (mediaPlayer != null) {
            mediaPlayer.release();
            mediaPlayer = null;
        }
        super.onDestroy();
    }
}
```
