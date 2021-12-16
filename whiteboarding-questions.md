# White Board Exercises

We introduce white boarding during the second week of the class.

- [ Intro to White Boarding ](./intro-to-whiteboarding.md#white-boarding)
- [ Week 2: JavaScript ](#week-2-intro-to-javascript)
- [ Week 3: JavaScript and React ](#week-3-javascript-and-react)
- [ Week 4: Ruby ](#week-4-ruby)
- [ Week 5: SQL and Rails ](#week-5-sql-and-rails)
- [ Week 6: Full-stack Rails ](#week-6-full-stack-rails)
- [ Week 7: PD Week Technical Interviews ](./pd-week-tech-interviews.md/#pd-week-technical-interviews)
- [ Week 8: Cat Tinder ](#week-8-cat-tinder)
- [ Week 9: Apartment App ](#week-9-apartment-app)
- [ Great Resource ](https://www.interviewcake.com/coding-interview-tips) for technical interviews

### Process
Students will be divided into groups and paired with one instructor or resident (the interviewer). During each weekly session two students will be interviewed. The students who are not being interviewed should follow along and attempt each question on their own.

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
- review all questions at the end of each interview expanding on the topics so they have the opportunity to learn.
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

### Week 2: Intro to JavaScript

**Student 1**  
TECH QUESTIONS:  
1) What excites you about coding?  
2) What is the difference between an array's value and index? As a developer, why is it important to distinguish between the two?  
3) What is iteration?

CODE PROMPT:  
As a developer, you are given an array of mixed data. Create a function that takes the array and returns an array with only the the values that that are strings.

INSTRUCTOR'S NOTES:
```javascript
let testArray = [3, 4, 5, true, false, true, "hello", "hey", "yo"]

const filterArray = (array) => {
  // can use filter and typeof "string"
}
console.log(filterArray(testArray, "string"))
// Output: ["hello", "hey", "yo"]
```

**Student 2:**  
TECH QUESTIONS:  
1) Why did you decide to learn development?  
2) What is a function? Why would you use one?  
3) If your function logs undefined, what can you do to troubleshoot this problem?

CODE PROMPT:  
As a developer, you are given an array of english words. Create a function that returns an array with the words in all uppercase letters.

INSTRUCTOR'S NOTES:
```javascript
let arrayOfWOrds = ["i", "am", "so", "excited"]

const makeEmCaps = (array) => {
  // can use map and .toUpperCase
}
console.log(makeEmCaps(arrayOfWOrds))
// Output: ["I", "AM", "SO", "EXCITED"]
```

[ Back to the Top ](#white-board-exercises)

### Week 3: JavaScript and React

**Student 1:**  
TECH QUESTIONS:  
1) What are your strengths as a developer?  
2) What is the difference between a `+` when dealing with numbers and a `+` when dealing with strings?
3) Compare and contrast equality operators and relational operators.    

PROMPT:  
As a developer you are tasked with calculating some information for a farmer. The farmer has chickens (2 legs), goats (4 legs) and horses (4 legs). Create a function that takes in the three animal quantities and returns the total number of legs on the farm.

INSTRUCTOR'S NOTES:
```javascript
const totalLegs = (chicks, goats, horses) => {
  return chicks * 2 + goats * 4 + horses * 4
}
// Most people will overthink and over code this one!
```

**Student 2:**  
TECH QUESTIONS:  
1) What are your weaknesses as a developer?  
2) What is the difference between null and undefined?  
3) Compare and contrast arrays and objects.  

PROMPT:  
A group of friends have decided to start a secret society. The name will be the first letter of each of their names. Create a function that takes in an array of names and returns the name of the secret society. (Optional stretch: The secret society's name should be sorted in alphabetical order.)

INSTRUCTOR'S NOTES:
```javascript
--> example input: ["austin", "sarah", "mina"]

secretSociety = (array) => {
  // can use substring, charAt, [0], etc
  // note that .sort() will treat lower and uppercase letters differently
}
--> "asm"
--> (STRETCH) "ams"
```

[ Back to the Top ](#white-board-exercises)

### Week 4: Ruby

**Student 1:**  
TECH QUESTIONS:  
1) What text editor do you use and why?  
2) What is a DOM event?  
3) What is the difference between React state and props?

PROMPT:  
As a developer, you are given a string containing multiple words. Create a function that capitalizes all the words in the string.

INSTRUCTOR'S NOTES:
```javascript
const capitalizer = (string) => {
  // split string, map
  // get first value with charAt or [0] and apply toUpperCase
  // add the rest of the word with substring or splice
  // join
}
console.log(capitalizer("hey there learn student"))
--> 'Hey There Learn Student'
```

**Student 2:**  
TECH QUESTIONS:  
1) What operating system do you use and why?  
2) What is a virtual DOM?  
3) What is the difference between a function and a method? Does the distinction matter?  

PROMPT:  
As a developer, you are given a multi digit number. Write a function that takes the number and returns an array with a single integer at each index.

INSTRUCTOR'S NOTES:
```javascript
// the main challenge is tracking data types and knowing which methods can be applied to which data types
const splitNum = (number) => {
  return number.toString().split("").map(value => {
    return parseInt(value)
  })
}

splitNum(34832)
--> [3, 4, 8, 3, 2]
```

[ Back to the Top ](#white-board-exercises)

### Week 5: SQL and Rails

**Student 1:**  
TECH QUESTIONS:  
1) What makes you a good teammate?  
2) What is the difference between a JavaScript function using the keyword function and a function using the arrow syntax?  
3) Verbally psuedocode the procees of determining if a number is prime. (A prime number is one divisible only by one and itself. Ex: 3, 5, 7, 11, 13)

PROMPT:  
Write a function that takes in a string and checks if the string is a palindrome. (Can be done in JavaScript or Ruby)

INSTRUCTOR'S NOTES:
```javascript
const palindrome = (string) => {
  if(string === string.toLowerCase().split("").reverse().join("")){
    return `${string} is a palindrome!`
  } else {
    return `${string} is NOT a palindrome!`
  }
}
```

**Student 2:**  
TECH QUESTION:  
1) What do you value in a mentor?  
2) What is a stack overflow?  
3) What would you get if you add the string "hello" to the number 3? (In JavaScript vs Ruby?)

PROMPT:  
Create a function that takes in a string with multiple words and returns a string with the letters in each word reversed. The words should remain in the same order. (Can be done in JavaScript or Ruby)

INSTRUCTOR'S NOTES:  
```javascript
console.log("hello" + 3)
--> "hello3"

const reverser = (string) => {
  return string.split(" ").map(value => {
    return value.split("").reverse().join("")
  }).join(" ")
}

console.log(reverser("oh hey there you"))

--> "ho yeh ereht uoy"
```
```ruby
p 'hello' + 3
--> TypeError

def reverser string
  reversed_array = string.split(' ').map do |value|
    value.reverse
  end
  reversed_array.join(' ')
end

p reverser 'oh hey there you'

--> "ho yeh ereht uoy"
```

[ Back to the Top ](#white-board-exercises)

### Week 6: Full-stack Rails

**Student 1:**  
TECH QUESTIONS:  
1) When working in a group, what role do you find yourself naturally gravitate towards?  
2) What is a relational database?  
3) What is an example of a domaine specific language?

PROMPT:  
(Part 1) As a developer, you have been tasked with creating a database table for a client who sells cookies online. What columns would you recommend to your client to have in the cookie table? (Open to interpretation - just an exercise in thinking through a problem. Optional stretch: What data type would each column have?)

(Part 2) Write a SQL query that will return the type and price of the most expensive cookie in the table.

INSTRUCTOR'S NOTES:  
Possible columns include type of cookie, price, size, cost of materials, calories, delivery date, delivery location, special instructions... The goal is to get them asking questions and doing some creative thinking.
```sql
SELECT type of cookie, price
FROM cookie
ORDER BY price DESC
LIMIT 1
```

**Student 2:**  
TECH QUESTIONS:  
1) Do you consider your personality more outgoing or more reserved?  
2) What is the difference between a scripting language and a markup language?  
3) What is SQL?

PROMPT:  
(Part 1) As a developer, you have been tasked with creating a database table for a client who works in a greenhouse and needs to keep track of the plants for sale. What columns would you recommend to your client to have in the plant table? (Open to interpretation - just an exercise in thinking through a problem. Optional stretch: What data type would each column have?)

(Part 2) Write a SQL query that will return all the plants that start with the letter p.

INSTRUCTOR'S NOTES:  
Possible columns include plant species name, category, sunlight needs, price, pot size, projected growth, humidity needs, recommended watering/fertilizer schedule... The goal is to get them asking questions and doing some creative thinking.

```sql
SELECT plant_species
FROM plant
WHERE plant_species LIKE 'P%'
```

[ Back to the Top ](#white-board-exercises)

### Week 8: Cat Tinder

**Student 1:**    
TECH QUESTION:  
1) Tell me about something you enjoy doing outside of coding.   
2) What does the term asynchronous mean in programming?  
3) What is a Promise? What are the possible states of a Promise?


PROMPT:  
What is this code doing?
```javascript
markTask = (e) => {
  let task = this.state.batch.tasks.find(v => v.id === e.target.id)
  markTaskDone(task)
  this.props.completeTask(task)
}
```

INSTRUCTOR'S NOTES:  
The markTask function is finding one task from the state object by an id that is coming from an input of some kind, then passing task to a local method and a method in the parent component.   

**Student 2:**  
TECH QUESTION:  
1) Tell me about a project you are working on.    
2) What is the Virtual DOM?
3) What is a recursive function? How would you avoid an infinite loop in a recursive function?

PROMPT:   
What is this code doing?
```javascript
cards = (array) => {
  array.sort(() => Math.random() - 0.5)
  this.setState({ flashcards: array })
}
```

INSTRUCTOR'S NOTES:   
The cards function is shuffling an array based on the random number being positive or negative.

[ Back to the Top ](#white-board-exercises)

### Week 9: Apartment App

**Student 1:**    
TECH QUESTION:  
1) What does being a full-stack developer mean to you?
2) What is your favorite thing about JavaScript?
3) What does the difference between authorization and authentication?  


PROMPT:  
Create a function that takes in an array of numbers and returns an array of the numbers squared and in ascending order. (Can be done in JavaScript or Ruby)

INSTRUCTOR'S NOTES:  
```javascript
const squaredAscending = (array) => {
  return array.map(value => value**2).sort((a, b) => a - b)
}
```

```ruby
def square_ascending array
    new_array = array.map! do |value|
    value * value
    end
    new_array.sort
end
```
Big - O Notation

```javascript
const sortedSquaredArray = (array) => {
	const sortedSquares = new Array(array.length).fill(0)
	let smallerValueIndex = 0;
	let largerValueIndex = array.length - 1;
	for (let index = array.length - 1; index >= 0; index--){
		const smallerValue = array[smallerValueIndex];
		const largerValue = array[largerValueIndex]
		if (Math.abs(smallerValue) > Math.abs(largerValue)) {
			sortedSquares[index] = smallerValue * smallerValue;
			smallerValueIndex++;
		} else {
			sortedSquares[index] = largerValue * largerValue;
			largerValueIndex--;
		}
	}
	return sortedSquares
}
```



**Student 2:**  
TECH QUESTION:  
1) What does being a life-long learner mean to you?   
2) What does it mean to have a full-stack application?
3) What is your least favorite thing about JavaScript?

PROMPT:   
Create a function that takes in a string of a single word and returns the middle letter. (Can be done in JavaScript or Ruby)

INSTRUCTOR'S NOTES:   
The code prompt can be made simplier by giving the student either an even or odd length string.

```javascript
const getMiddle = (string) => {
  let mid = string.length / 2
  if(string.length%2 === 0){
    return string[mid - 1] + string[mid]
  } else {
    return string[Math.floor(mid)]
  }
}
```

[ Back to the Top ](#white-board-exercises)
