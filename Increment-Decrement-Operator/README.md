# Increment Decrement Operator

## Increment Operator
This operator is represented as ++. It is used to add 1 to the existing value of a variable. It can be used in two ways:-

### Prefix Form
In this form, the increment operator is placed before the operand. It adds one to the existing value of variable then takes the incremented value of variable.
#### Example: `++a`

### Postfix Form
In this form, the increment operator is placed after the operand. It takes the existing value of variable and then adds one to the existing value of variable in the next statement.
#### Example: `a++`

## Decrement Operator
This operator is represented as -–. This operator is used to subtract one from the existing value of a variable.

### Prefix Form
In this form, the increment operator is placed before the operand. It subtracts one from the existing value of variable then takes the decremented value of variable.
#### Example: `--a`

### Postfix Form
In this form, the decrement operator is placed after the operand. It first takes the existing value of variable and then subtracts one from the existing value of variable in the next statement.
#### Example: `a--`

## Program to demonstrate increment/decrement operator.	Output (Line Wise)

```C

    #include<stdio.h>
    int main(){
      int a=10; 
      printf(“\na=%d”,++a);	// a=11
      printf(“\na=%d”,a++);	// a=11
      printf(“\na=%d”,a);	  // a=12
      printf(“\na=%d”,a–);	// a=12
      printf(“\na=%d”,–a);	// a=10
      return (0);
    }
    
```

