# Exp.No:34  
## PREFIX EVALUATION

---

### AIM  
To write a Python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction.

---

### ALGORITHM

1. **Start the program.**
2. Define a set of valid operators: `*, -, +, %, /, **`.
3. Initialize an empty stack.
4. Traverse the prefix expression from **right to left**:
   - If the character is a **digit**, convert it to an integer and push it onto the stack.
   - If the character is an **operator**, pop two elements from the stack.
     - Apply the operator on the two popped operands.
     - Push the result back onto the stack.
   - If an invalid character is encountered, raise an error.
5. After traversal, the stack should contain only **one element**.
6. Return the **single element** as the evaluation result.
7. **End the program.**

---

### PROGRAM
NAME: SENTHIL KANAGAVEL BALASUNDARAM
REG NO: 212223060254

```
OPERATORS=set(['*','-','+','/'])
stack=[] 
def prefix_Eval(x):
    for i in x[::-1]:
        if i not in OPERATORS:
            stack.append(int(i))
        else:
            op1=stack.pop()
            op2=stack.pop()
            if i == "+":
                stack.append(op1+op2)
            elif i=="*":
                stack.append(op1*op2)
            elif i=="-":
                stack.append(op1-op2)
    return stack[0]
test_expression =input()
print("Prefix Expression :",test_expression)
print("Evaluation result :",prefix_Eval(test_expression))
    
    
```


### OUTPUT

![image](https://github.com/user-attachments/assets/b24ff70d-2531-40bc-9133-9c13f7a7d89d)

### RESULT 

Thus, the Python program for evaluating a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction is executed successfully.
