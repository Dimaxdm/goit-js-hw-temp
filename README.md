# Homework. Module 2. Branching & Loops

## Overview

Complete each task in its corresponding JavaScript file:

- `task-1.js`
- `task-2.js`
- `task-3.js`
- `task-4.js`

After implementing each solution, paste the provided test code below your function and leave it unchanged so your mentor can verify the results.

---

# Task 1. Droid Order

Complete this task in **`task-1.js`**.

A repair droid sales station is ready to launch, but the sales department still needs software to process customer orders.

## Requirements

Declare a function named `makeTransaction(quantity, pricePerDroid, customerCredits)`.

The function accepts three parameters:

- `quantity` — the number of droids ordered.
- `pricePerDroid` — the price of a single droid.
- `customerCredits` — the customer's available balance.

Complete the function as follows:

1. Declare a variable that stores the total order cost.
2. Calculate the total price of the order.
3. Check whether the customer has enough credits to complete the purchase:
   - If the total cost exceeds the available balance, return:

```text
Insufficient funds!
```

- Otherwise, return:

```text
You ordered <quantity> droids worth <totalPrice> credits!
```

Where:

- `<quantity>` is the number of ordered droids.
- `<totalPrice>` is the total order cost.

### Test your solution

```javascript
console.log(makeTransaction(5, 3000, 23000));
// "You ordered 5 droids worth 15000 credits!"

console.log(makeTransaction(3, 1000, 15000));
// "You ordered 3 droids worth 3000 credits!"

console.log(makeTransaction(10, 5000, 8000));
// "Insufficient funds!"

console.log(makeTransaction(8, 2000, 10000));
// "Insufficient funds!"

console.log(makeTransaction(10, 500, 5000));
// "You ordered 10 droids worth 5000 credits!"
```

> **Do not remove these test cases.** Leave them in your solution for your mentor to review.

## Review Checklist

- [x] - The `makeTransaction(quantity, pricePerDroid, customerCredits)` function is declared.
- [x] - `makeTransaction(5, 3000, 23000)` returns `"You ordered 5 droids worth 15000 credits!"`.
- [x] - `makeTransaction(3, 1000, 15000)` returns `"You ordered 3 droids worth 3000 credits!"`.
- [x] - `makeTransaction(10, 5000, 8000)` returns `"Insufficient funds!"`.
- [x] - `makeTransaction(8, 2000, 10000)` returns `"Insufficient funds!"`.
- [x] - `makeTransaction(10, 500, 5000)` returns `"You ordered 10 droids worth 5000 credits!"`.

---

# Task 2. Message Formatting

Complete this task in **`task-2.js`**.

## Requirements

Declare a function named `formatMessage(message, maxLength)`.

The function accepts:

- `message` — the input string.
- `maxLength` — the maximum allowed string length.

Complete the function so that:

- If the message length is less than or equal to `maxLength`, return the original string unchanged.
- Otherwise, truncate the string to `maxLength` characters, append `"..."`, and return the shortened version.

### Test your solution

```javascript
console.log(formatMessage("Curabitur ligula sapien", 16));
// "Curabitur ligula..."

console.log(formatMessage("Curabitur ligula sapien", 23));
// "Curabitur ligula sapien"

console.log(formatMessage("Vestibulum facilisis purus nec", 20));
// "Vestibulum facilisis..."

console.log(formatMessage("Vestibulum facilisis purus nec", 30));
// "Vestibulum facilisis purus nec"

console.log(formatMessage("Nunc sed turpis a felis in nunc fringilla", 15));
// "Nunc sed turpis..."

console.log(formatMessage("Nunc sed turpis a felis in nunc fringilla", 41));
// "Nunc sed turpis a felis in nunc fringilla"
```

> **Do not remove these test cases.** Leave them in your solution for your mentor to review.

## Review Checklist

- [x] - The `formatMessage(message, maxLength)` function is declared.
- [x] - `formatMessage("Curabitur ligula sapien", 16)` returns `"Curabitur ligula..."`.
- [x] - `formatMessage("Curabitur ligula sapien", 23)` returns `"Curabitur ligula sapien"`.
- [x] - `formatMessage("Vestibulum facilisis purus nec", 20)` returns `"Vestibulum facilisis..."`.
- [x] - `formatMessage("Vestibulum facilisis purus nec", 30)` returns `"Vestibulum facilisis purus nec"`.
- [x] - `formatMessage("Nunc sed turpis a felis in nunc fringilla", 15)` returns `"Nunc sed turpis..."`.
- [x] - `formatMessage("Nunc sed turpis a felis in nunc fringilla", 41)` returns `"Nunc sed turpis a felis in nunc fringilla"`.

---

# Task 3. Spam Detection

Complete this task in **`task-3.js`**.

## Requirements

Declare a function named `checkForSpam(message)`.

The function accepts a string parameter named `message`.

The words **"spam"** and **"sale"** may appear in any letter case (for example: `SPAM`, `sAlE`, etc.).

Complete the function so that:

- It returns `true` if the message contains either `"spam"` or `"sale"`.
- Otherwise, it returns `false`.

### Test your solution

```javascript
console.log(checkForSpam("Latest technology news"));
// false

console.log(checkForSpam("JavaScript weekly newsletter"));
// false

console.log(checkForSpam("Get best sale offers now!"));
// true

console.log(checkForSpam("Amazing SalE, only tonight!"));
// true

console.log(checkForSpam("Trust me, this is not a spam message"));
// true

console.log(checkForSpam("Get rid of sPaM emails. Our book in on sale!"));
// true

console.log(checkForSpam("[SPAM] How to earn fast money?"));
// true
```

> **Do not remove these test cases.** Leave them in your solution for your mentor to review.

## Review Checklist

- [x] - The `checkForSpam(message)` function is declared.
- [x] - `checkForSpam("Latest technology news")` returns `false`.
- [x] - `checkForSpam("JavaScript weekly newsletter")` returns `false`.
- [x] - `checkForSpam("Get best sale offers now!")` returns `true`.
- [x] - `checkForSpam("Amazing SalE, only tonight!")` returns `true`.
- [x] - `checkForSpam("Trust me, this is not a spam message")` returns `true`.
- [x] - `checkForSpam("Get rid of sPaM emails. Our book in on sale!")` returns `true`.
- [x] - `checkForSpam("[SPAM] How to earn fast money?")` returns `true`.

---

# Task 4. Product Shipping

Complete this task in **`task-4.js`**.

## Requirements

Declare a function named `getShippingCost(country)`.

The function should determine whether shipping is available to the specified country.

> **Use a `switch` statement** to implement this task.

Return a string in the following format:

```text
Shipping to <country> will cost <price> credits
```

Supported destinations:

| Country | Shipping Cost |
| -------- | ------------: |
| China | 100 credits |
| Chile | 250 credits |
| Australia | 170 credits |
| Jamaica | 120 credits |

If shipping is **not available**, return:

```text
Sorry, there is no delivery to your country
```

### Test your solution

```javascript
console.log(getShippingCost("Australia"));
// "Shipping to Australia will cost 170 credits"

console.log(getShippingCost("Germany"));
// "Sorry, there is no delivery to your country"

console.log(getShippingCost("China"));
// "Shipping to China will cost 100 credits"

console.log(getShippingCost("Chile"));
// "Shipping to Chile will cost 250 credits"

console.log(getShippingCost("Jamaica"));
// "Shipping to Jamaica will cost 120 credits"

console.log(getShippingCost("Sweden"));
// "Sorry, there is no delivery to your country"
```

> **Do not remove these test cases.** Leave them in your solution for your mentor to review.

## Review Checklist

- [x] - The `getShippingCost(country)` function is declared.
- [x] - A `switch` statement is used in the function implementation.
- [x] - `getShippingCost("Australia")` returns `"Shipping to Australia will cost 170 credits"`.
- [x] - `getShippingCost("Germany")` returns `"Sorry, there is no delivery to your country"`.
- [x] - `getShippingCost("China")` returns `"Shipping to China will cost 100 credits"`.
- [x] - `getShippingCost("Chile")` returns `"Shipping to Chile will cost 250 credits"`.
- [x] - `getShippingCost("Jamaica")` returns `"Shipping to Jamaica will cost 120 credits"`.
- [x] - `getShippingCost("Sweden")` returns `"Sorry, there is no delivery to your country"`.
