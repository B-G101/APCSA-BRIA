---
toc: true
layout: post
description: Primitives class notes
categories: [markdown]
title: Primitives Class Notes
---
# Primitives Class Notes

#### Why Java
- Has simple syntax
- Allows for automatic garage collection
- More flexible and efficient because its OO
- It can be run on any platform
    - First compose with Java
    - Then into byte code
    - Then runs on a jvm
- It allows for multi threading
- Secure
#### Primitives vs. Non primitives
- Primitives
    - Predefined 
    - Lowercase
    - “Primitives”
    - Cannot call methods
    - Value
    - Different sizes based on which primitive it is
- Non primitives
    - Done by you
    - Uppercase
    - “Reference types”
    - Can call methods
    - Can be null
    - All same size
Primitives Types
- Boolean
    - One bit
- Int
    - 2-3 bits
- Double 
    - Decimals
    - 64 bits
- Char, float, long, etc
#### Review Cont
- Variable naming conventions
    - Letters, numbers, or underscores — nothing else
    - Typically starts with lowercase and then a capital
    - The ***final*** keyword means that the value cannot be changed later
- Casting 
    - Manual casting vs automatic
    - Widening happens automatically and you go from small data type to bigger data type
        - Ex: int to double
    - Narrowing is going from bigger data type to a smaller one and you have to declare it


### Hacks 
1. 10/4 is equal to 2.5 which will round down to 2 or round up to 3 depending on the rounding since it is an integer data type. --> 2
``` java
int x = 10;
int y = 4; 
int z = x/y;
/// What is the value of z?
```
<br>

3. val is 205 and its going to be looped 5 total times. 2 to the power of 5 is 32. 205/32 is equal to 6. -->
``` java 
int val = 205;
for(int i=0; i<5; i++>) {
  val/=2;
}
// At the end of its executition, what is the value of the variable val in the code above?
```
<br>

2. A is not a valid assignment statement because the variable is not on the left side of the assignment sign. D is not a valid assignment statement because the equation is on the left side and not the right side of the assignment sign. --? a, d
<br>

4. I is being added to itself and the loop executes 5 times. So 3+3>6+6>12+12>24+24>48+48=96 --> 96 
``` java
int i = 3;
for(int j=5;j>0;j--){
  i += i;
}
// What will be the value of i at the end of this loop's iteration
```
<br>

6. The loop iterates 4 times. 5*1>5*2>10*3>30*4 = 120 --> 120
``` java
int i =5, p=27;
for(int l=23;l<p;l++>){
  i *= (l-22);
}
// What is the value for I at the end of the code above?
```
<br>

5. This is an example of casting that converts the doubles into int. This is narrowing casting since the data type is getting smaller. 455 + 3.75 = 458.75 rounded up is 459 or rounded down is 458 --> 458
``` java
int i = 100;
double d = 4.55, d2 = 3.75;
int j = (int)(d*100 + d2);
// What is the value of j at the end of the code's execution?
```


### FRQ 2006

#### 1 Part A

``` java
// boolean meaning return type true or false
public boolean conflictsWith(Appointment other){
  // getting the time of two different appointments and checking if they overlap with one another using given method
  if (getTime().overlapsWith(other.getTime())){
    return true;
    // returning true if there is an overlap otherwise false is returned
  else {
    return false;
  }
}
}

```

#### 1 Part B

``` java
public void clearConflicts(Appointment appt){
  // Looping through each appointment in the appointment list array list
  for (int i = 0; i < apptList.size(); i++){
    // Using given methods to check if the paramater appointment conflists with any appointments already in the appointment arraylist
    if (appt.conflictsWith(apptList(i))){
      // if the appointments overlap then the appointment at the given index will be removed from the array list
      appList.remove(i);
    }
  }
}
```

#### 1 Part C

``` java
public boolean addAppt(Appointment appt, boolean emergency){
  // if there is an emergency then the appointment will clear
  if (emergency) {
    clearConflicts(appt);
    }
  else {
    // otherwise it loops through the appointment list and checks if that appointment conflicts with another appointment using the get method
    for (int i = 0; i < apptList.size(); i++) {
      if (appt.conflictsWith((Appointment)apptList.get(i))) {
        return false;
      }
    }
  }
 return apptList.add(appt);
  
}
```

#### 2 Part A

``` java
public double purchasePrice(){
  return ((1 + taxrate) * getListPrice());
  
}
```

#### 3 Part A

``` java
public int compareCustomer(Customer other){
 int nameCompare = getName().compareTo(other.getName());
 if (nameCompare != 0) {
  return nameCompare;
 }
 else {
  return getID() - other.getID();
 } 
}
```
