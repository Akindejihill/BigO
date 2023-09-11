Step One: Simplifying Expressions
Simplify the following big O expressions as much as possible:

# Step 1

## O(n + 10)
* O(n)
## O(100 * n)
* O(n)
## O(25)
* O(1)
## O(n^2 + n^3)
* O(n^3)
## O(n + n + n + n)
* o(n)
## O(1000 * log(n) + n)
* O(log(n))
## O(1000 * n * log(n) + n)
* O( n log n)
## O(2^n + n^2)
* O(n^2)
## O(5 + 3 + 1)
* O(1)
## O(n + n^(1/2) + n^2 + n * log(n)^10)
* O(n log(n)^10)


# Step 2

### #1
```
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
```
* O(n)

### #2

```
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
```

* O(n + n) simplifies to  O(n)


### #3

```
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
```

* Worst case senario n = 10 so it's constant. O(1)
  (But what if instead of 10 the minimum was one hundred million billion trillion?)

### #4

```
function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
```

* O(n)

### #5

```
function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
```

* O(n^2)

### #6

```
function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
```
* O(n)


# Part 3

1) true
2) true
3) false
4) O(n)
5) O(n)
6) o(n)
7) o(n log(n))
8) O(n)
9) O(1)
10) 0(n)
11) 0(1)
12) 0(n)
13) 0(n)
