## Getting to understand closure properly

1. Write a function called `multiplyBy` that takes a `number` as an argument and returns a function. Returned function takes another `number` as an argument and returns the multiplication of both the numbers.

```js
function multiplyBy (numA) {
  return (numB) => {
    return numA * numB;
  }
}
// Your code goes here

const double = multiplyBy(2);
const final = double(15); // final s  hould be 30
```

2. Write a function called `fullName` that takes a string `firstName` as an argument and returns a function. Returned function takes another string `lastName` as an argument and returns full name.

```js
// Your code goes here
function fullName(firstName) {
  return (lastName) => {
    return firstName + " " + lastName;
  }
}

const name = fullName('Will');
const final = name('Smith'); // final should be "Will Smith"
```

3. Write a function called `isInBetween` which takes two parameter `a` and `b` and returns a function. When you call the returned function with any number it returns `true` if the value is in between `a` and `b`.

```js
  // your code goes here
function isInBetween(a, b) {
  return (num) => {
    if (num > a && num < b) {
      return true;
    }
    else {
      return false;
    };
  }
}

const isChild = isInBetween(10, 100);
isChild(21); // true
isChild(45); // true
isChild(103); // false
```

4. Write a function call `letsWishThem` that take one parameter `string` called `greeting` and returns a function that takes another argument called `message`.

```js
function letsWishThem(greeting) {
  return (msg) => {
    return greeting + " " + msg;
  }  
}

const callWithHey = letsWishThem('Hey');
const callWithHello = letsWishThem('Hello');
callWithHey('Arya'); // Hey Arya
callWithHello('How Are You?'); // Hello How Are You?
```

5. Write a function called `addGame` which takes a string (name of the game) and the current score. It returns a function calling that will increment the score by one and print something like `Score of Basketball is 1`.

```js
function addGame(gameName, currentScore) {
  return () => {
    currentScore ++;
    return `Your score of ${gameName} is ${currentScore}`;
  }
}

// Output
const hockey = addGame('Hockey', 0);
hockey(); // Your score of Hockey is 1
hockey(); // Your score of Hockey is 2
const cricket = addGame('Cricket', 1);
cricket(); // Your score of Cricket is 2
cricket(); // Your score of Cricket is 2
```

6. Write a function called `getCard` which takes one of these options (club, spade, heart, diamond) returns a function calling that function returns random card (2,3,4,5,6,7,8,9,10,J, Q, K, A) of that suit.

```js
function getCard(suit) {
  // your code goes here
  let card = [2, 3, 4, 5, 6, 7, 8, 9, 10, 'J', 'Q', 'K', 'A'];
  return () => {
    let pick = Math.floor(Math.random() * card.length);
    return `Card is: ${card[pick]} ${suit}`;
  }
}

// Output
const randomClub = getCard('Club');
randomClub(); // Card is: 6 Club
randomClub(); // Card is: A Club
const randomSpade = getCard('Spade');
randomSpade(); // Card is: 6 Spade
randomSpade(); // Card is: A Spade
```
