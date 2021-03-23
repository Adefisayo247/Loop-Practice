# # 1 Explain Infinite Loops with Example
An infinite loop, as the name suggests, is a loop that will keep running forever. If you accidentally make an infinite loop, it could crash your browser or computer. It is important to be aware of infinite loops so you can avoid them. An infinite loop will run forever, but the program can be terminated with the break keyword.
A common infinite loop occurs when the condition of the while statement is set to true. Below is an example of code that will run forever. It is not necessary to test any infinite loops.

# # # Example
```
// Set a condition to true
const iceCapsAreMelting = true;
let polarBears = 5;

// Initiate infinite loop
while (iceCapsAreMelting) {
  console.log(`There are ${polarBears} polar bears.`);
  polarBears++;
  // Terminate infinite loop when following condition is true
  if (polarBears === 0) {
    console.log("There are no polar bears left.");
    break;
  }
}
```

# # 2 Explain For loops with Example
A for loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop.
When a for loop executes, the following occurs:

The initializing expression initialExpression, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.
The conditionExpression expression is evaluated. If the value of conditionExpression is true, the loop statements execute. If the value of condition is false, the for loop terminates. (If the condition expression is omitted entirely, the condition is assumed to be true.)
The statement executes. To execute multiple statements, use a block statement ({ ... }) to group those statements.
If present, the update expression incrementExpression is executed.
Control returns to Step 2.
A for statement looks as follows:

for ([initialExpression]; [conditionExpression]; [incrementExpression])
  statement

# # # Example
```
for (i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}
```

# # 3 Explain For each loops with Example
The forEach() method calls a function (a callback function) once for each array element. ForEach() is useful to iterate over all array items, without breaking, involving simultaneously some side-effects.

Note that the function takes 3 arguments:
The item value
The item index
The array itself

# # # Example
```
//don't use the for each if the order of the array is important
var txt = "";
var numbers = [45, 4, 9, 16, 25];
numbers.forEach(myFunction);

function myFunction(value) {
  txt = txt + value + "<br>";
}
```

# # 4 Explain For of loops with example
The JavaScript for/of statement loops through the values of an iterable object. It lets you loop over iterable data structures such as Arrays, Strings, Maps, NodeLists, and more:

# # # Example
```
let cars = ["BMW", "Volvo", "Mini"];
let text = "";

for (let x of cars) {
  text += x + "<br>";
}
```
# # Use the ForEach loop to loop through an array of objects and log the second property of each object to the console

```
const Currency = [
  {
    name: 'Dollar',
    country: 'USA',
    renewalYear: 1860,
  },
  {
    name: 'Cedis',
    country: 'Ghana',
    renewalYear: 1958,
  },

  {
    name: 'Naira',
    country: 'Nigeria',
    nickname: 1960,
  },
];
// to get the second property of each object for each object in the Currency array defined above
// const secondProperty = Currency[2].country;
// console.log(secondProperty);

Currency.forEach((objectInCurrencyArray) => {
  let secondProperty = objectInCurrencyArray.country;
  console.log('the second property in each of the object is ', secondProperty);
});
```