---
toc: true
layout: post
description: Unit 1: Primitives
categories: [markdown,test prep]
title: Primitives Class Notes
---
# Primitives


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

### FRQ 2006

#### 1 Part A

``` java
public boolean conflictsWith(Appointment other){
  if (getTime().overlapsWith(other.getTime())){
    return true;
  else {
    return false;
  }
}

```

#### 1 Part B

``` java
public void clearConflicts(Appointment appt){
  for (int i = 0; i < apptList.size(); i++){
    if (appt.conflictsWith(apptList(i))){
      appList.remove(i);
    }
  }
}
```

#### 1 Part C

``` java
public boolean addAppt(Appointment appt, boolean emergency){
  if (emergency) {
    clearConflicts(appt);
    }
  else {
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
