# Kotlin Functions And Lamdas

A function is a named block of code that performs a particular task.
In Kotlin, a function always returns a value.

# Declaring functions
Functions in Kotlin are declared as follows

fun <function name>(<param1:Type>,<param2:Type>,...<paramN:Type>):<returntype>{ func body}


Let us get a quick example of a function
```kotlin
fun sayHello()
{
    println("Hello from Kotlin")
}

```

The above function takes no parameters and returns type Unit.Unit is corresponds to void on the JVM.

Now a function that takes two parameters and returns a value demonstrated thus

```kotlin
fun welomeStudent(name:String,id:String):String{

    return "Welcome $name. Your student id is $id"

}

```
## Calling functions
Functions in Kotlin are called the same way like most languages

```
<function name>(arg1,arg2,..argn)
```
Calling the above functions can be done as follows

```kotlin
sayHello()  //Prints Hello
welcomeStudent("Ngenge Senior","SC!1B373")
```

Now the beauty of Kotlin in functions come in when we can call functions using named parameters.

```kotlin
wecomeStudent(id="SX13A123","John Doe")
```

As you might have noticed, calling functions with named arguments, you can pass the arguments in any order. 
You might be asking how this helps us. Now imagine a function that you have just writtent that takes 20 parameters. Now, in a language like Java, you are compelled to know the order in which the parameters are passed to the function. But here with Kotlin, that order is not necessary.

## Functions with Single expressions
We can write the function to add two integers as follows
```kotlin
fun add(a:Int,b:Int):Int{
    return a + b
}
```

The function has just a single expression. With Kotlin, we can simplify the function as follows

```kotlin
    fun add(a:Int,b:Int) = a+b
```
In this new version, we omit the return type as Kotlin will infer the type for us.

## Functions with default values
Another awesome part of Kotlin is that it gives you the ability to give default values to your parameters. Let us take a real example. Say you are developing an app with two types of users, when user provides name, he/she is a regular user, but if not, they are anonymous

```kotlin
    fun greetUser(name:String = "Anonymous user",userId:Int = 0)
    {
        println("Welcome $name. Your user id is $userId")
    }

```
This function can be called in the following ways.

```kotlin
    greetUser() // prints Welcome Anonymous user. Your userid is 0
    ("Ngenge Senior")// Prints , Welcome Ngenge Senior. Your user id is 0
    greetUser(name="Romeo", userId=3) //Works as expected
    greetUser(userId=2,name="Julliet")

```
