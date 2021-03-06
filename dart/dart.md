# DART _cheat-sheet_
## Table of Contents
* [Type of values](#type-of-values)   
    * [Get type value](#get-type-value)
    * [Type test](#type-test)
    * [Convert Types](#convert-types)
* [Quotes](#quotes)
* [Operators](#operators)
* [Conditionals](#conditionals)
* [Loops](#loops)
* [Collection](#collection)
* [Functions](#functions)

## Types of Values
```dart
int amount = 100;   
double amount = 100,11;   
String name = 'John';   
bool isDone = true;    
dynamic noTypeFixed = 'true';   
var likeDynamic = 'true';
```
### Get type value
```dart   
const aConstNum = 0;   
print(aConstNum.runtimeType);
```
>int
### Type test
```dart
if ( x is int ) {
  print('integrer);
}
```  
### Convert Types
```dart   
var newInt = int.parse('2022');
assert(newInt == 2022);

var newDouble = double.parse('12.34');
assert(newDouble == 12.34);

String intToString = 1.toString();
assert(intToString == '1');

String doubleToString = 3.14159.toStringAsFixed(2);
assert(doubleToString == '3.14');
```
## Quotes
```dart
var s1 = 'Single quotes';   
var s2 = "Double quates";   
var s3 = 'It\'s easy to scape';   
var s4 = "It's easy too"

var rawString = r'No special \n treatment';

var s5 = '''   
Multi-line   
string   
'''   
var s4 = """   
Also multi-line   
string   
"""

String name = 'John';   
var templateLiterals = 'My name is $name'
```
## Operators
```dart
int num = 20;
num + 2;
num - 2;

// modulus operator
num % 2;

// relational ==, !=, >=, <=
if(num == 0) {
  print('zero')
}

num = 100;
num *= 2; //num = num * 2

//unary operator
++num;
num++;
num += 1;
num -= 1;

//logical && and logical ||
if (num > 200 && num < 202) {
    print('201');
}

//Null Aware Operator
// (?.), (??), (??=)

number = n?.num ?? 0;

//ternary operator

void main() {
    int x = 101;
    var result = x % 2 == 0 ? 'Even' : 'Odd;
    print(result); 
}
```
## Conditionals
```dart
int number = 100;

if ( number % 2 == 0 ) {
    print('Even');
} 
else if ( number % 2 != 0 ) {
    print('Odd');
} else {
    print('Danzed and Confused')
};
```
```dart
int number = 1;

switch ( number ) {
    case 0:
        print('Even');
        break;
    case 1:
        print('Odd');
        break;
    default:
    print('Not 0 or 1')
}
```
## Loops
```dart
for ( var i = 0 ; 1 <= 10; ++i ) {
    print('Number: $i')
};
```
>For in
```dart
var numbers = [1, 2, 3];

for ( var n in numbers ) {
    print(n)
};
```
>.forEach() method
```dart
numbers.forEach((num) => print(num));
```
>while
```dart
int num = 5;

while (num > 0) {
    print(num);
    num-= 1;
}
```
>do while
```dart
int num = 5;

do {
    print(num);
    num -=1;
} while (num > 0);
```
>break
```dart
for (var i = 0; i <= 10; ++i) {
    if( i > 5 ) break;
    print(i);
}
```
>continue
```dart
for ( var i = 0; i <= 0; ++i ) {
    if( i % 2 == 0 ) continue;
    print('Odd: $i')
}
```
## Collection
>List
```dart
List names = [ 'John', 'Brown' ];

List <String> users = const [ 'Mario', 'Luigi']

var users2 = [...users]
```
>Set
```dart
var object = <String>{};

Set <Strings> names = {}
```
>Map
```dart
var object = {
    //Key:   Value:
    'user': 'Spiderman',
    'name': 'Peter',
    'surname': 'Parker',
}

print(object['user'])

var newObject = Map();
```
## Functions
>void before declaration if expects that the function returns some value. 
```dart
dynamic sum ( var num1, var num2 ) => num1 + num2;

dynamic square (var num) {
    return num * num;
}

void showOutput (var msg) {
    print(msg);
}
```
>anonymous function
```dart
dynamic square ( var num ) => num * num;
```
>Apply null aware operator 
```dart
void main () {
    print(sum(10));
}

dynamic sum ( var num1, { var num2 }) => num1 + (num2 ?? 0);

dynamic sum ( var num1, { var num2=0}) => num1 + num2;
```
## Class
```dart
class Person {
    String name;
    int age;

    Person(this.name, [this.age = 18]);

    //named constructor

    Person.guest() {
        name = 'Maria';
        age = 41;
    }

    void showOutput() {
        print(name);
        print(age)
    }
}

void main() {
    Person person1 = Person('John');
    person1.showOutout();

    var person2 = Person('Laia', 50);
    person2.showOutout();

    var person3 = Person.guest()
    person3.showOutput();
}
```
```dart
class X {
    final name;   // Object property
    static const int age = 22;  // Class property

    X(this.name);
}
```
```dart
class Vehicle {
    String model;
    int year;
    Vehicle(this.model, this.year) {
        print(this.model);
        print(this.year);
    }
}

class Car extends Vehicle {
    double price;

    Car(String model, int year, this.price) : super(model, year);

    void showOutput() {
        super.showoutput();
        print(this.price);
    }
}

void main() {
    var car1 = Car('Accord', 2014, 150000);
    car1.showOutput();
}
```

```dart

```
## Excption Handling
```dart

```
```dart

```
```dart

```
```dart

```
```dart

```
```dart

```
