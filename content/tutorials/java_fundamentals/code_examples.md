---
title: Code Examples
linktitle: Code Examples
toc: true
type: docs
date: 2019-11-21T12:57:49-07:00
lastmod: 2020-07-05T12:57:49-07:00
draft: false
menu:
  java_fundamentals:
    parent: Java
    weight: 2

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---


## Tip Calculator

```java
public class Main {

// Create the Function
	public static double calculateTotalMealPrice(double listedMealPrice, 
												 double tipRate, 
												 double taxRate) {
		double tip = tipRate * listedMealPrice;
		double tax = taxRate * listedMealPrice;
		double result = listedMealPrice + tip + tax;
		return result;

	}

	public static void main(String[] args) {
// Call the Function
		double groupTotalMealPrice = calculateTotalMealPrice(100, 0.20, 0.08);
		System.out.println("Total meal price for group: $" + groupTotalMealPrice);

		double individualMealPrice = groupTotalMealPrice / 5;
		System.out.println("Total meal price per individual: $" + individualMealPrice);

	}
}

```

```terminal
> Total meal price per individual: $25.6
```
---
## Salary Calculator

```java
public class Main {

// Create the Function
		public static double salaryCalculator(double hoursPerWeek,
											  double amountPerHour, 
											  int vacationDays) {

			if (hoursPerWeek < 0) {
				return -1;
			}
			
			if (amountPerHour < 0) {
				return -1;
			}
			
			double weeklyPaycheck = hoursPerWeek * amountPerHour;
			double unpaidTime = vacationDays * amountPerHour * 8;
			return (weeklyPaycheck * 52) - unpaidTime;
			
		}
		
// Call the Function
		public static void main(String[] args) {
			double salary = salaryCalculator(40, 15, 8);
			System.out.println("Your annual salary is $" + salary);

		}
}

```

```terminal
> Your annual salary is $30240.0
```
---
