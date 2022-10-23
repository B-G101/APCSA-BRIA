---
toc: true
layout: post
description: Boolean Expressions and If Statements Lesson
categories: [markdown]
title: Boolean Expressions and If Statements Class Notes + Homework
---
# Boolean Expressions and If Statements Class Notes

## FRQ 2009 3b

``` java
public class BatteryCharger {
  private int[] rateTable; 
  
  private int getChargingCost(int startHour, int chargeTime){
    int cost = 0;
    for (int x = 0; x < chargeTime; x++) {
    cost += this.rateTable[(startHour + x) % 24];
    }
    return cost;
  }
  
  public int getChargeStartTime(int chargeTime) {
   int startTime = 0;
   for (int i = 1; i < 24; i++) {
     if (this.getChargingCost(i, chargeTime) < this.getChargingCost(startTime, chargeTime)) {
     startTime = i;
     }
   }
   return startTime; 
  }
}
```

## FRQ 2017 1b

``` java
public class Digits {
  private ArrayList<Integer> digitList;
  
  public Digits(int num) {
    if (num == 0){
      digitList.add(new Integer(0));
    }
    
    while (num > 0) {
      digitList.add(0, new Integer(num % 10));
      num /= 10;
      }
  }
}
```

## FRQ 2019 3b

``` java
public boolean isBalanced(ArrayList<String> delimiters)
{ 
     int closeCount = 0;
     int openCount = 0;
     for( String s : delimiters )
     {
	if( s.equals( openDel ) )
	{
	   openCount++;
	}
	else if( s.equals( closeDel ) )
	{
	   closeCount++;	
	}
	if( closeCount > openCount )
	{
	   return false;
	}			
     }
     return closeCount ==  openCount;
}
```
