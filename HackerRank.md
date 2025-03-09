# Algorithms

## 1. Simple array sum

### Problem:
Given an array of integers, find the sum of its elements.

### Solution:

```
function simpleArraySum(arr) {
    return arr.reduce((acc, curr) => acc + curr);
}
```

## 2. Compare the Triplets

### Background:
- Alice and Bob each created one problem.
- A reviewer rates the two challenges, awarding points on a scale from 1 to 100 for three categories: problem clarity, originality, and difficulty.

### Problem:
The task is to calculate their comparison points by comparing each category:
- If a[i] > b[i], then Alice is awarded 1 point.
- If a[i] < b[i], then Bob is awarded 1 point.
- If a[i] = b[i], then neither person receives a point.

### Solution:

```
function compareTriplets(a, b) {
    let result = [0, 0];
    for(let i=0; i<a.length; i++){
        if(a[i] > b[i]){
            result[0] += 1
        } else if(a[i] < b[i]){
            result[1] += 1
        }
    }
    return result;
}
```

## 3. Diagonal Difference

### Problem:
Given a square matrix, calculate the absolute difference between the sums of its diagonals.

### Solution:

```
function diagonalDifference(arr) {
    let diagonal1 = 0;
    let diagonal2 = 0;
    for(let i=0; i<arr.length; i++){
        diagonal1 += arr[i][i];
        diagonal2 += arr[i][arr.length - i - 1];
    }
    return Math.abs(diagonal1 - diagonal2);
}
```

## 4. Grading

### Background:
- Every student receives a grade in the inclusive range from 0 to 100.
- Any grade less than 40 is a failing grade.

### Problem:
Sam is a professor at the university and likes to round each student's  according to these rules:
- If the difference between the grade and the next multiple of 5 is less than 3, round grade up to the next multiple of 5.
- If the value of grade is less than 38, no rounding occurs as the result will still be a failing grade.

### Solution:

```
function gradingStudents(grades) {
    let result = [];
    for (const elem of grades){
        if (elem < 38 || elem % 5 < 3){
            result.push(elem);
        } else if(elem % 5 >= 3){
            result.push(elem +  5 - elem % 5);
        }
    }
    return result;
}
```

## 2. Apple and Orange