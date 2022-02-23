# White Board Exercises

We introduce white boarding during the second week of the class.

- [Student's Intro to White Boarding](./intro-to-whiteboarding.md#white-boarding)
- [Interviewer's Intro to White Boarding](#process)
- [Week 2: JavaScript](#week-2-intro-to-javascript)
- [Week 3: JavaScript and React](#week-3-javascript-and-react)
- [Week 4: React and Ruby](#week-4-react-and-ruby)
- [Week 5: Ruby and SQL](#week-5-ruby-and-sql)
- [Week 6: Ruby on Rails](#week-6-rails)
- [Week 7: PD Week Technical Interviews](./pd-week-tech-interviews.md/#pd-week-technical-interviews)
- [Week 8: Cat Tinder](#week-8-cat-tinder)
- [Great Resource](https://www.interviewcake.com/coding-interview-tips) for technical interviews

### Process
Students will be divided into groups and matched with one instructor or resident (the interviewer). During each weekly session two students will be interviewed. The students who are not being interviewed should follow along and attempt each question silently on their own.

Each interview should take 20-30 minutes. The interviewer will ask the student three questions and give one code prompt.

The questions consist of one generic interview question and two technical questions. The difficulty of these questions varies. Some topics are covered in class and others have not been covered. This is for the purpose of creating a real-world interview experience allowing the students to work through nerves and practice answering questions they don't know.

The code prompt should mimic a "real life" white boarding session. The student can use a text medium such as the notes app or a markdown file to code out the prompt.  

During the coding portion of the interview the student should:
- write down the prompt and confirm the accuracy with the interviewer.
- establish an example input and output and confirm the accuracy with the interviewer.
- list out their plan in regular words before beginning to code.
- communicate constantly and think out loud.

The interviewer should:
- be engaged.
- remember the students are VERY nervous.
- allow the students to struggle but NOT fail.
- provide constructive feedback at the end of each interview.
- review all questions at the end of each interview expanding on the topics so all students have the opportunity to learn.
- manage the time spent on each interview so the total session takes about one hour.
- send the students back to the main room at the end of the session.
- provide feedback on each student to the instructors.

### Feedback
At the end of the session, each interview should provide feedback to the instruction team via Slack.

Feedback for each interviewee should include:
- the student's first name.
- a brief impression of the student's ability to communicate.
- a brief over all impression of the student's current technical ability.
- any questions the student failed to answer.
- whether the student followed the code prompt expectations as noted above.

---

### Week 2: Intro to JavaScript

**Student 1**  
TECH QUESTIONS:  
1. What excites you about coding?  
2. What is the difference between an array's index and value? As a developer, why is it important to distinguish between the two?  
3. What is iteration?

CODE PROMPT:  
As a developer, you are given an array of mixed data. Create a function that takes in the array and returns an array with only the values that are strings.

INTERVIEWER'S NOTES:
- 1 - The goal here is to get the student to start to formulate a very common soft-skills interview question. Encourage the student to come up with a solid, well-practiced answer.
- 2 - An index in an array is the location of each item. Arrays are zero-indexed. The value is the content that is at each index. The value must be a data type recognized by JavaScript. Knowing the difference between the two is important to be able to successfully access the data in an array.
- 3 - Iteration is repeating a specific action until a condition is met.
```javascript
// Example input:
let mixedDataArray = [3, 4, "yo", true, false, "hey"]

const onlyStrings = (array) => {
  // will need to iterate over the array - can use a for loop or filter
  // will need to make an evaluation of each value in the array - can use typeof
  return array.filter(value => typeof value === "string")
}
console.log(onlyStrings(mixedDataArray))
// Output: ["yo", "hey"]
```

**Student 2:**  
TECH QUESTIONS:  
1. Why did you decide to learn development?  
2. What is a function? Why would you use one?  
3. If a JavaScript function logs undefined what can you do to troubleshoot this problem?

CODE PROMPT:  
As a developer, you are given an array of English words. Create a function that returns an array with the words in all uppercase letters.

INTERVIEWER'S NOTES:
- 1 - A softball-style question that is common for career transitioners. It is a great opportunity for connecting with the interviewer. Encourage the student to come up with a solid, well-practiced answer.
- 2 - A function is an encapsulated piece of code functionality. It makes code logic reusable.
- 3 - If a JavaScript function logs undefined ensure your function has a return.
```javascript
// A common miscommunication will happen here on the difference between capitalization and all uppercase letters. This prompt is looking for the latter.

// Example input:
let arrayOfWOrds = ["i", "am", "so", "excited"]

const yelling = (array) => {
  // will need to iterate over the array - can use a for loop or map
  // will need to use .toUpperCase()
  return array.map(value => value.toUpperCase())
}
console.log(yelling(arrayOfWOrds))
// Output: ["I", "AM", "SO", "EXCITED"]
```

[Back to the Top](#white-board-exercises)

---

### Week 3: JavaScript and React

**Student 1:**  
TECH QUESTIONS:  
1. What are your strengths as a developer?  
2. What is the difference between a `+` when dealing with numbers and a `+` when dealing with strings?
3. Compare and contrast equality operators and relational operators.    

PROMPT:  
As a developer, you are tasked with calculating some information for a farmer. The farmer has chickens, goats, and horses. Create a function that takes in the three quantities of each animal and returns the total number of legs on the farm.

INTERVIEWER'S NOTES:
- 1 - A classic interview question. Encourage the student to be humble and honest.
- 2 - A plus sign applied to the JavaScript number data type will perform a mathematical operation. The plus sign applied to the JavaScript string data type will perform concatenation.
- 3 - The similarities between equality (==, ===) and relational (<, >, <=, >=) operators are they both are used for comparisons and both return a Boolean value. The differences are relational operators only compare numbers where equality operators can be used on any data type.
```javascript
// We can assume all animals have the expected number of legs for their given species.
// Most people will overthink and over code this one!

const totalLegs = (chickens, goats, horses) => {
  return chickens * 2 + goats * 4 + horses * 4
}
console.log(totalLegs(3, 4, 5))
// Output: 42
```

**Student 2:**  
TECH QUESTIONS:  
1. What are your weaknesses as a developer?  
2. What is the difference between null and undefined in JavaScript?  
3. Compare and contrast JavaScript arrays and objects.  

PROMPT:  
A group of friends have decided to start a secret society. The name will be the first letter of each of their names. Create a function that takes in an array of names and returns the name of the secret society.

INTERVIEWER'S NOTES:
- 1 - This is a spin on the classic "trap" interview question. Encourage the student to be humble and honest but turn the question into an opportunity to talk about learning, growth, and goals.
- 2 - Null is a data type that represents the intentional absence of value while undefined is the value of a variable that has been declared but not assigned a value.
- 3 - The similarities between JavaScript objects and arrays are they are both non-primitive data types and collections of data. The differences are arrays are wrapped in square braces and the values are referenced by index whereas objects are wrapped in curly braces and.the values are referenced by keys.
```javascript
// Example input:
let names = ["elyse", "austin", "sarah"]

const secretSociety = (array) => {
  // will need to iterate over the array - can use map or for loop
  // will need to extract the first letter of each string - can use substring, slice, charAt, [0], etc
  // will need to convert the array into a string - can use join
  return array.map(name => name[0]).join("")
}
console.log(secretSociety(names))
// Output: "eas"
```

[Back to the Top](#white-board-exercises)

---

### Week 4: React and Ruby

**Student 1:**  
TECH QUESTIONS:  
1. What text editor do you use and why?  
2. What is the DOM?  
3. What is the difference between React state and props?

PROMPT:  
As a developer, you are given an array of numbers. Create a function that takes in the array and returns an array with the numbers in ascending order.

INTERVIEWER'S NOTES:
- 1 - Looking for a bit of self-reflection here. Looking for the student to have a reason for their choice other than "it is what we used in class." Encourage them to talk about why they like the interface as well as any plugins, themes, or snippets they use.
- 2 - DOM stands for Document Object Model which is a visual representation of the markup and code logic that makes up a website.
- 3 - React state is a specialized object used for data storage in a class-based component. Props are a specialized object that allows data to flow between components. State can be modified while props are read-only.
```javascript
// Example input:
let exampleNumbersArray = [42, 100, 9, 0, 27]

const ascendingOrder = (array) => {
  // will need to iterate over the array
  // sort is passed an optional function to account for multi digit numbers
  // if the student is not familiar with sort, they may want to use map or for loop
  return array.sort((a, b) => a - b)
}
console.log(ascendingOrder(exampleNumbersArray))
// Output: [0, 9, 27, 42, 100]
```

**Student 2:**  
TECH QUESTIONS:  
1. What operating system do you use and why?
2. What is a virtual DOM?  
3. What is the difference between a function and a method? Does the distinction matter?  

PROMPT:  
As a developer, you are given a multi digit number. Write a function that takes the number and returns an array with a single integer at each index.

INTERVIEWER'S NOTES:
- 1 - Looking to see if the student can navigate a potentially loaded interview question. Encourage the student to defend their choice while still being open minded about other technologies.
- 2 - The virtual DOM is light-weight representation, or preview layer of the DOM that listens for any diff created by user interactions. The diff can be reconciled more efficiently than regular DOM updates since only the nodes that have changes are updated.
- 3 - A function is a stand-alone snippet of code functionality. A method is a function that belongs to a class. Methods do not have independent existence. The distinction matters in knowing what data can be accessed by the function/method and how they are invoked.
```javascript
// The main challenge is tracking data types and knowing which methods can be applied to which data types.

// Example input:
let multiDigitNumber = 142

const splitNum = (number) => {
  // will need to convert number to string in order to split the string to an array
  // will need to iterate to convert the string back to a number
  return number.toString().split("").map(value => parseInt(value))
}
console.log(splitNum(multiDigitNumber))
// Output: [1, 4, 2]
```

[Back to the Top](#white-board-exercises)

---

### Week 5: Ruby and SQL

**Student 1:**  
TECH QUESTIONS:  
1. What makes you a good teammate?  
2. What is the difference between a JavaScript function using the keyword function and a function using the arrow syntax?  
3. Verbally pseudocode the process of determining if a number is prime. (A prime number is one divisible only by one and itself. Ex: 3, 5, 7, 11, 13)

PROMPT:  
Write a function that takes in a string and checks if the string is a palindrome. (Can be done in JavaScript or Ruby.)

INTERVIEWER'S NOTES:
- 1 - This is a spin on the classic "what are your strengths" question. Looking for the ability to speak confidently about their experiences. Encourage the student to find a short anecdote they can keep handy. Using pair programming as an example is a great option.
- 2 - Arrow functions have a shorter syntax and can be written without curly braces, parentheses, or the keyword return as long as there is only one expression. Arrow expressions use the scope of their parent where the function keyword creates its own internal scope.
- 3 - Using iteration like a for loop, with the iteration starting from 2 and incrementing one each time, ending one before the given number, use the modulo operator to see if any numbers return no remainder. NOTE: The student may not be familiar with prime numbers. In that case have them reason through the concept of a prime number. The goal is to get them problem solving out loud.
```javascript
const palindrome = (string) => {
  // JavaScript reverse method only works on arrays
  // STRETCH: consider casing
  if(string === string.split("").reverse().join("")){
    return `${string} is a palindrome!`
  } else {
    return `${string} is NOT a palindrome!`
  }
}
console.log(palindrome("racecar"))
// Output: "racecar is a palindrome!"
console.log(palindrome("hello"))
// Output: "hello is NOT a palindrome!"
```
```ruby
def palindrome(string)
  # Ruby reverse method works on strings and arrays
  # STRETCH: consider casing  
  if string.reverse == string
    return "#{string} is a palindrome!"
  else
    return "#{string} is NOT a palindrome!"
  end
end
p palindrome('racecar')
# Output: 'racecar is a palindrome!'
p palindrome('hello')
# Output: 'hello is NOT a palindrome!'
```

**Student 2:**  
TECH QUESTION:  
1. What do you value in a mentor?  
2. What is a stack overflow?  
3. What would you get if you add the string "hello" to the number 3? (In JavaScript vs Ruby?)

PROMPT:  
As a developer, you are given a string of a single word. Create a function that takes in the string and returns the middle letter(s). (Can be done in JavaScript or Ruby.)

INTERVIEWER'S NOTES:  
- 1 - Looking for a bit of self-reflection here. Encourage the student to think about their individual priorities and learning needs.
- 2 - A stack overflow is a when a program tries to execute more actions than it has memory to perform.  
- 3 - When adding a string and a number JavaScript will perform type coercion and concatenate the two items returning the string "hello3". Ruby will return an error as the data types are not compatible for either addition or concatenation.

```javascript
console.log("hello" + 3)
--> "hello3"

const getMiddle = (string) => {
  // even length strings will return two letters and odd length strings will return one letter
  let mid = string.length / 2
  if(string.length % 2 === 0){
    return string[mid - 1] + string[mid]
  } else {
    return string[Math.floor(mid)]
  }
}

console.log(getMiddle("hootenanny"))
// Output: "en"
console.log(getMiddle("lollygagger"))
// Output: "g"

// If the student is struggling, the code prompt can be made simpler by with this modification: As a developer, you are given a string of a single word that is an odd number of characters.

const getMiddleOfOddLength = (string) => {
  let mid = string.length / 2
  return string[Math.floor(mid)]
}
console.log(getMiddleOfOddLength("world"))
// Output: "r"
```
```ruby
p 'hello' + 3
=> TypeError (no implicit conversion of Integer into String)

def get_middle(string)
  middle = string.length / 2
  if string.length % 2 == 0
    string[middle - 1] + string[middle]
  else
    string[middle.round]
  end
end

p get_middle('hootenanny')
# Output: 'en'
p get_middle('lollygagger')
# Output: 'g'
```

[Back to the Top](#white-board-exercises)

---

### Week 6: Rails

**Student 1:**  
TECH QUESTIONS:  
1. When working in a group, what role do you find yourself naturally gravitate towards?  
2. What is a relational database?  
3. What is an example of a domaine specific language?

PROMPT:  
(Part 1) As a developer, you have been tasked with creating a database table for a client who sells cookies online. What columns would you recommend to your client to have in the cookie table? (Open to interpretation - just an exercise in thinking through a problem. Optional stretch: What data type would each column have?)

(Part 2) Write a SQL query that will return the type and price of the most expensive cookie in the table.

INTERVIEWER'S NOTES:
- 1 - This question is partially self-reflection on whether the student feels more comfortable in a leader role or a support role. Many students will discuss whether they prefer "driving" or "navigating" during a pairing session. Encourage them to think bigger and broader than just pair programming.  
- 2 - A relational database organizes information into tables that have columns which define the data and rows that are instances of the data.
- 3 - A domaine specific language is specified to one particular task. Examples are RSpec, HTML, SQL.
- Part 1: The goal of this section to get them asking questions and doing some creative thinking. Possible columns include type of cookie, price, size, cost of materials, calories, delivery date, delivery location, special instructions, etc. Encourage them to share a screen and write down their ideas.
```sql
SELECT type of cookie, price
FROM cookie
ORDER BY price DESC
LIMIT 1
```

**Student 2:**  
TECH QUESTIONS:  
1. Do you consider your personality more outgoing or more reserved?  
2. What is the difference between a scripting language and a markup language?  
3. What is SQL?

PROMPT:  
(Part 1) As a developer, you have been tasked with creating a database table for a client who works in a greenhouse and needs to keep track of the plants for sale. What columns would you recommend to your client to have in the plant table? (Open to interpretation - just an exercise in thinking through a problem. Optional stretch: What data type would each column have?)

(Part 2) Write a SQL query that will return all the plants that start with the letter p.

INTERVIEWER'S NOTES:  
- 1 - This is a spin on asking if the student considers themselves more introverted or extroverted. Encourage the student to have confidence in their answer no matter which they identify with.
- 2 - Scripting language performs logic and a markup language creates the presentation or visual aspect of the app.
- 3 - SQL stands for Structure Query Language and is a domaine specific language for querying relational databases.
- Part 1: The goal of this section to get them asking questions and doing some creative thinking. Possible columns include plant species name, category, sunlight needs, price, pot size, projected growth, humidity needs, recommended watering/fertilizer schedule, etc. Encourage them to share a screen and write down their ideas.
```sql
SELECT plant_species
FROM plant
WHERE plant_species LIKE 'P%'
```

[Back to the Top](#white-board-exercises)

---

### Week 8: Cat Tinder

**Student 1:**    
TECH QUESTION:  
1. Tell me about something you enjoy doing outside of coding.   
2. What is your least favorite thing about JavaScript?
3. What is a Promise? What are the possible states of a Promise?

PROMPT:  
What is this code doing?
```javascript
markTask = (e) => {
  let task = this.state.batch.tasks.find(v => v.id === e.target.id)
  markTaskDone(task)
  this.props.completeTask(task)
}
```

INTERVIEWER'S NOTES:
- 1 - This is one of those generic interview questions that, if answered thoughtfully, will allow the student to show their personality and make a human connection with the interviewer. Encourage the student to give a well-rounded answer and not look at this question as a throw away.
- 2 - Plenty of options here. :) Encourage the student to take this question as a thoughtful critique not an opportunity to language-bash.
- 3 - A Promise is a proxy value used to handle asynchronous actions. The possible states of a Promise can be in one of three states: pending, rejected, or fulfilled.
- Prompt - Share this code snippet on your screen. Have the student tell you everything they can about the code. This is from a previous LEARN capstone project that tracked fermentation. The markTask method is from a class-based component in React. It is finding one task from the state object by an id that is coming from an input of some kind, then passing the task variable to a method in the same class and a method in the parent component.   

**Student 2:**  
TECH QUESTION:  
1. What does being a full-stack developer mean to you?   
2. What is your favorite thing about JavaScript?
3. What is asynchronous programming?

PROMPT:   
What is this code doing?
```javascript
cards = (array) => {
  array.sort(() => Math.random() - 0.5)
  this.setState({flashcards: array})
}
```

INTERVIEWER'S NOTES:  
- 1 - This question can be interpreted as a technical question or as a personal question. Maybe both.
- 2 - Encourage the student to come up with specific examples.   
- 3 - Asynchronous programming is allowing your code to have good time management. JavaScript is single threaded meaning that it does one thing at a time. Asynchronous actions allow a process to run separately from the single thread.
- Prompt: Share this code snippet on your screen. Have the student tell you everything they can about the code. This is from a previous LEARN capstone project that created randomized flashcards. The cards method is in a class-based React component that holds state. Shuffling an array based on the random number being positive or negative. State is then updated with the newly randomized array.

[Back to the Top](#white-board-exercises)
