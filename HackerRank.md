# Algorithms

## 1. Grading

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