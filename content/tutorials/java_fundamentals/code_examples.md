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

## Code Examples

Example #1

```java
public class Main {

	public static double calculateTotalMealPrice(double listedMealPrice, double tipRate, double taxRate) {
		double tip = tipRate * listedMealPrice;
		double tax = taxRate * listedMealPrice;
		double result = listedMealPrice + tip + tax;
		return result;

	}

	public static void main(String[] args) {
		double groupTotalMealPrice = calculateTotalMealPrice(100, .2, .08);
		System.out.println("Total meal price for group: $" + groupTotalMealPrice);

		double individualMealPrice = groupTotalMealPrice / 5;
		System.out.println("Total meal price per individual: $" + individualMealPrice);

	}
}
```