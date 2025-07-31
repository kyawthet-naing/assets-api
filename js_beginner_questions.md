# JavaScript Beginner - Top 15 Essential Questions (Mixed Format)

## Question 1 (True/False)
**True/False**: In a switch statement, if you forget to add `break`, the execution will continue to the next case.

## Question 2 (Multiple Choice)
**Multiple Choice**: What will be logged?
```javascript
var x = 1;
if (true) {
    var x = 2;
    console.log(x);
}
console.log(x);
```
- A) 1, 1
- B) 2, 1
- C) 2, 2
- D) Error

## Question 3 (Multiple Choice)
**Multiple Choice**: What's the difference between `for-of` and `for-in`?
- A) for-of gives values, for-in gives keys/indexes
- B) for-of gives keys, for-in gives values
- C) They are exactly the same
- D) for-of only works with objects

## Question 4 (Coding)
**Write code that demonstrates the difference between `for-of` and `for-in`** using the following array:
```javascript
const fruits = ["apple", "banana", "orange"];
fruits.color = "mixed"; // Adding a property to the array
```

Write two loops:
1. A for-of loop that prints each fruit
2. A for-in loop that prints each key/index

```javascript
const fruits = ["apple", "banana", "orange"];
fruits.color = "mixed";

// Your for-of loop here:

// Your for-in loop here:
```

## Question 5 (True/False)
**True/False**: Variables declared with `var` are block-scoped.

## Question 6 (True/False)
**True/False**: Static methods can be called on class instances.

## Question 7 (Multiple Choice)
**Multiple Choice**: What does the `this` keyword refer to in a class method?
- A) The class definition
- B) The global object
- C) The instance of the class
- D) The parent class

## Question 8 (True/False)
**True/False**: A child class must always call `super()` in its constructor if it extends a parent class.

## Question 9 (Coding)
**Write a class called `Rectangle`** with the following requirements:
- Constructor takes width and height
- Method `getArea()` returns width * height
- Method `getPerimeter()` returns 2 * (width + height)
- Static method `createSquare(side)` returns a new Rectangle where width = height = side

```javascript
// Your code here
class Rectangle {
    // Complete this class
}

// Test cases:
const rect = new Rectangle(5, 3);
console.log(rect.getArea()); // Should output: 15
console.log(rect.getPerimeter()); // Should output: 16

const square = Rectangle.createSquare(4);
console.log(square.getArea()); // Should output: 16
```

## Question 10 (Multiple Choice)
**Multiple Choice**: How do you call a parent class method from a child class?
- A) `parent.methodName()`
- B) `super.methodName()`
- C) `this.parent.methodName()`
- D) `base.methodName()`

## Question 11 (True/False)
**True/False**: A Promise can be in one of three states: pending, fulfilled, or rejected.

## Question 12 (Multiple Choice)
**Multiple Choice**: What does `async` function always return?
- A) undefined
- B) A value
- C) A Promise
- D) null

## Question 13 (True/False)
**True/False**: You can use `await` without being inside an `async` function.

## Question 14 (Coding)
**Create an async function called `fetchUserData`** that:
- Takes a userId as parameter
- Uses fetch to get data from `https://jsonplaceholder.typicode.com/users/${userId}`
- Returns the user's name if successful
- Returns "User not found" if there's an error
- Use async/await and try/catch

```javascript
// Your code here
async function fetchUserData(userId) {
    // Complete this function
}

// Test case:
fetchUserData(1).then(name => console.log(name)); // Should output user's name
```

## Question 15 (Coding)
**Write a function called `gradeCalculator`** that takes a numerical score (0-100) and returns the corresponding letter grade using if-else statements:
- 90-100: "A"
- 80-89: "B" 
- 70-79: "C"
- 60-69: "D"
- Below 60: "F"

```javascript
// Your code here
function gradeCalculator(score) {
    // Complete this function
}

// Test cases:
console.log(gradeCalculator(95)); // Should output: "A"
console.log(gradeCalculator(67)); // Should output: "D"
```

---

## Answer Key

### Questions 1-3, 5-8, 10-13 (Theory Questions)
1. **True** - This is the "fall-through" behavior of switch statements
2. **C** - 2, 2 (var is function-scoped, so both refer to same variable)
3. **A** - for-of gives values, for-in gives keys/indexes
5. **False** - var is function-scoped, not block-scoped
6. **False** - Static methods are called on the class, not instances
7. **C** - The instance of the class
8. **True** - Must call super() before using this in child constructor
10. **B** - super.methodName()
11. **True** - The three states of a Promise
12. **C** - Always returns a Promise
13. **False** - await must be inside an async function

### Coding Questions (4, 9, 14, 15)

**Question 4 Answer:**
```javascript
const fruits = ["apple", "banana", "orange"];
fruits.color = "mixed";

// for-of loop (gets values)
console.log("for-of loop:");
for (const fruit of fruits) {
    console.log(fruit); // apple, banana, orange
}

// for-in loop (gets keys/indexes)
console.log("for-in loop:");
for (const key in fruits) {
    console.log(key); // 0, 1, 2, color
}
```

**Question 9 Answer:**
```javascript
class Rectangle {
    constructor(width, height) {
        this.width = width;
        this.height = height;
    }
    
    getArea() {
        return this.width * this.height;
    }
    
    getPerimeter() {
        return 2 * (this.width + this.height);
    }
    
    static createSquare(side) {
        return new Rectangle(side, side);
    }
}
```

**Question 14 Answer:**
```javascript
async function fetchUserData(userId) {
    try {
        const response = await fetch(`https://jsonplaceholder.typicode.com/users/${userId}`);
        const user = await response.json();
        return user.name;
    } catch (error) {
        return "User not found";
    }
}
```

**Question 15 Answer:**
```javascript
function gradeCalculator(score) {
    if (score >= 90) {
        return "A";
    } else if (score >= 80) {
        return "B";
    } else if (score >= 70) {
        return "C";
    } else if (score >= 60) {
        return "D";
    } else {
        return "F";
    }
}
```

---

## Why These 15 Questions Are The Ultimate Selection

**Perfect Balance:**
- **7 True/False** - Test core conceptual understanding
- **4 Multiple Choice** - Test practical knowledge and code analysis
- **4 Coding** - Test hands-on programming skills

**Essential Topics Covered:**
- **Control Flow**: Switch statements, conditionals
- **Scoping**: var behavior (most critical concept)
- **Loops**: for-of vs for-in (theory + practice)
- **OOP Core**: Static methods, this keyword, inheritance, super()
- **Async Programming**: Promise states, async/await rules + real API usage
- **Practical Skills**: Grade calculator, class creation, API fetching

**Why These Are The Best 15:**
1. **High-Impact Learning** - These concepts cause the most confusion
2. **Interview Relevance** - Common technical interview topics
3. **Real-World Application** - Students will use these daily
4. **Foundation Building** - Essential for advanced JavaScript topics
5. **Comprehensive Coverage** - Spans all your key episodes efficiently