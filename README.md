# iOSPlayground

## Property attributes

Here are some examples of the main behaviors of OOP in Kotlin and Objective-C:

**Classes**

**Kotlin:**

```kotlin
class Person(val name: String, val age: Int) {
    fun greet() {
        println("Hello, my name is $name and I am $age years old.")
    }
}
```

**Objective-C:**

```objectivec
@interface Person
@property (nonatomic, copy) NSString *name;
@property (nonatomic, assign) NSInteger age;

- (void)greet;
@end

@implementation Person

- (void)greet {
    NSLog(@"Hello, my name is %@ and I am %ld years old.", self.name, self.age);
}

@end
```

In both Kotlin and Objective-C, classes are used to define blueprints for creating objects. Classes can have properties, which store the state of the object, and methods, which define the behavior of the object.

**Interfaces**

**Kotlin:**

```kotlin
interface Animal {
    fun makeSound()
}

class Dog : Animal {
    override fun makeSound() {
        println("Woof!")
    }
}

class Cat : Animal {
    override fun makeSound() {
        println("Meow!")
    }
}
```

**Objective-C:**

```objectivec
@protocol Animal
@optional
- (void)makeSound;
@end

@implementation Dog
- (void)makeSound {
    NSLog(@"Woof!");
}
@end

@implementation Cat
- (void)makeSound {
    NSLog(@"Meow!");
}
@end
```

In both Kotlin and Objective-C, interfaces are used to define contracts that classes can implement. Interfaces can have methods, but they cannot have properties or implementations. This makes interfaces a good way to define common behavior for different classes.

**Objects**

**Kotlin:**

```kotlin
val person = Person("Alice", 25)
person.greet()
```

**Objective-C:**

```objectivec
Person *person = [[Person alloc] initWithName:@"Alice" age:25];
[person greet];
```

In both Kotlin and Objective-C, objects are instances of classes. Objects have their own unique state and behavior, which is defined by the class that they are instances of.

**Other OOP behaviors**

Other OOP behaviors that are supported in both Kotlin and Objective-C include:

* **Inheritance:** Classes can inherit from other classes, inheriting their fields and methods. This allows for code reuse and specialization.
* **Polymorphism:** Objects can be treated as if they were instances of their parent classes. This allows for writing more flexible and dynamic code.
* **Abstraction:** OOP allows you to hide the implementation details of objects and expose only the functionality that is needed. This makes code more reusable and maintainable.

**Conclusion**

Kotlin and Objective-C are both powerful object-oriented programming languages. They both support the core features of OOP, such as classes, interfaces, objects, inheritance, polymorphism, and abstraction. However, there are some key differences between the two languages, such as optional typing, null safety, and extension functions.

Which language is better for you depends on your specific needs and requirements. If you are developing applications for Apple platforms, then Objective-C is the language that you need to learn. If you are developing applications for other platforms, or if you are looking for a more modern and expressive language, then Kotlin is a good option.

<img width="856" alt="image" src="https://github.com/santosmgbh/iOSPlayground/assets/5347606/095b11f5-9264-4fb4-b47c-0206c89fa219">



**nonatomic**

The `nonatomic` property attribute tells the compiler that the property can be read and written to concurrently by multiple threads. This can improve performance, but it also introduces the risk of data races.

In Kotlin, there is no direct equivalent to the `nonatomic` property attribute. However, Kotlin does support concurrent programming, and you can use Kotlin's threading features to achieve the same effect.

**copy**

The `copy` property attribute tells the compiler that the property should be copied when it is assigned to a new variable. This is useful for properties that contain mutable objects, such as `NSString`.

In Kotlin, the equivalent to the `copy` property attribute is the `val` keyword. `val` variables are immutable, which means that they cannot be changed once they have been initialized.

**assign**

The `assign` property attribute tells the compiler that the property should be assigned to a new variable without copying it. This is useful for properties that contain immutable objects, such as `NSInteger`.

In Kotlin, the equivalent to the `assign` property attribute is the `var` keyword. `var` variables are mutable, which means that they can be changed after they have been initialized.

**Example**

Here is an example of how to use the `nonatomic`, `copy`, and `assign` property attributes in Objective-C:

```objectivec
@interface Person
@property (nonatomic, copy) NSString *name;
@property (nonatomic, assign) NSInteger age;
@end

@implementation Person

@end
```

The `name` property is copied when it is assigned to a new variable. This is because `NSString` is a mutable object. The `age` property is not copied when it is assigned to a new variable. This is because `NSInteger` is an immutable object.

Here is an example of how to use the `val` and `var` keywords in Kotlin:

```kotlin
class Person(val name: String, var age: Int) {
    fun greet() {
        println("Hello, my name is $name and I am $age years old.")
    }
}
```

The `name` property is immutable, which means that it cannot be changed once it has been initialized. The `age` property is mutable, which means that it can be changed after it has been initialized.

**Conclusion**

The `nonatomic`, `copy`, and `assign` property attributes in Objective-C are used to control how properties are read and written to, and whether they are copied when they are assigned to new variables. The `val` and `var` keywords in Kotlin are used to control whether variables are immutable or mutable.

Kotlin does not have a direct equivalent to the `nonatomic` property attribute, but it does support concurrent programming, and you can use Kotlin's threading features to achieve the same effect.
