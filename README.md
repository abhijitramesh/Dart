# Dart

## Intro to Dart

When you create a dart file and start wirting a program, there is no need to use any access specifiers. Everything is `public` by default. Dart does not support any access specifiers.

The main function is really simple.
In java:

`public static void main(String[]args)`

In Dart:

`void main()`

Or if you need command line arguments:

`void main(List<String> args)`

It pretty clear from these examples that the syntax of Dart is way more simple and compact than in Java.
In Dart, code can be defined inside, as well as outside the classes.

Another difference in Dart and Java is indentation. Dart uses 2-character indentation, instead of 4.

## Constructors in Dart

In Dart, declaration of constructors takes just a line. For exammple a constructor for a Bicycle class is:

`Bicycle(this.var1, this.var2, this.var3 );`

Keep in mind:
1) Constructors with out bodies are valid in Dart.
2) A semicolin(;) at the end of the constructor is really important.
3) Using `this` in the construcotr is a shortcut. The constructor mentioned above is equivalent to:

`Bicycle(int var1, int var2, int var3) {`

  `this.var1 = var1;`  
  
  `this.var2 = var2;`
  
  `this.var3 = var3;`  
  
`}`

In the main function, you can directly assign the values to a variable as well as call the constructor at the same time. Following are two examples which show how to print the data stored in a variable:

### Example 1:

`var bike = new Bicycle(3,6,7)

print(bike);`

Output:

`Instance of 'Bicycle'`

### Example 2:

Now we will use toString() function to give us the value stored in bike.
In the class, override toString() to get the output.

`@override
String toString() => 'Bicycle: $var2 kmph'`

Then write the same main method as above.

Output:

`6 kmph`

If you do `$var1` instead of `$var2`, you will get `3 kmph` as output.

If you want to print more than one variable:

`@override
String toString() => 'Bicycle: $var2 kmph $var1 $var3'`


You can find the entire program which demonstrates these concepts [here](https://github.com/yashk2000/Dart/blob/master/Bicycle.dart)
