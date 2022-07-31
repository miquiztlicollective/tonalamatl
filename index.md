---
title: "Tonalamatl"
draft: false
image: //via.placeholder.com/640x150
alt_text: "Tonalamatl screenshot"
summary: "Summary of the Tonalamatl project"
tech_used:
- JavaScript
- CSS
- HTML
keywords:
- tonalamatl
---

Analog time keeping in the digital age.

**tl;dr**

```cpp
int date_requested
int date_remainder = getRemainder(date.year, 52);

function int getRemainder(int date_divisor, int date_divider) {
	int date_quotient = date_divisor / date_divider;
	int date_remainder = date_divisor * date_quotient - date_quotient;
	
	return date_remainder;
};

	int year_remainder = getRemainder(date_remainder, 4);
	string TYPE_OF_YEAR[] = ["Tecpatl", "Calli", "Tochtli", "Acatl"];

funtion string getTypeOfYear(int year_reminder){
	return TYPE_OF_YEAR[year_remainder];
};

	int y_number_remainder = getRemainder(date_remainder, 13);
	
	function getYearNumber(int y_number_remainder) {
		int year_number = y_number_remainder + 3;
		
		if (year_number > 13) {
			year_number =- 13;
			return year_number;
		} else { return year_number; };
	};
	
	// to find the *veintena* i still need to find a way to read from a table more complicated
	
	int diff_of_days = date.day() - first_day_of veintena;
	string symbol_of_day = getSymbolOfDay(diff_of_days);
	
	string SYMBOLS_OF_DAYS[] = [
		Cipactli,
		Ehecatl,
		Calli,
		Cuetzapllin,
		Coatl,
		Miquiztli,
		Mazatl,
		Tochtli,
		Alt,
		Itzcuintli,
		Ozomatli,
		Malinalli,
		Acatl,
		Ocelotl,
		Cuauhtli,
		Cozcacuauhtli,
		Ollin,
		Tecpatl,
		Quiahuitl,
		Xochitl
	]
	
	string function getSymbolOfDay(int symbol_of_day) {
		return SYMBOLS_OF_DAYS[symbol_of_day];
	}
	
	int FIRST_DAY_NUM[] = [1, 10, 6, 2, 11, 7, 3, 12, 8, 4, 13, 9, 5]
	
	int function getFirstDayNum(int y_number_remainder) {
		return FIRST_DAY_NUM[y_number_remainder];
	}

```

This is the common way of translating the *Gregorian* calendar dates to the *Mexican* calendar.

Table 1
/tabla-01.csv

Table 1 has 7 rows.
- Row 1: the number of the Mexican years in successive sequence.
- Row 2--5: sussesion of the 52 years in the *Xiuhmolpilli* based on type of year.
- Row 2: *Calli* year
- Row 3: *Tochtli* year
- Row 4: *Acatl* year
- Row 5: *Tecpatl* year
- Row 6: number belonging to *Cipactli*---the first day of the set of 20 days---of the first *veintena* of the year---*Atlacahualo*.
- Row 7: used to find the number attached to the first day of every *veintena* of the year.
- Row 8: used to find the number of the first *Nemontemi*---which has its own count.

| 1 | 2 | 3 |  |
|:--|:--|:--|:--|
|  |  |	|
|  |  |			|
|  |  | 03-Tecpatl = 0 |

Table 2
/table-02.csv

Table 2 has the time of the day to which each day starts based on type of year.


Table 3
/table-03.csv

Table 3 the order to which the days of the Mexican calendar start based on the groups of the days in the *Nemontemi* based on type of year.

Table 4
/table-04.csv

Table 4 is the order that the days are inscribed in the *Mexican Calendar* in each *veintena* of the year.

Table 5
/table-05.csv

Table 5 serves as a guide to match the number of the belonging to the *Señores de la Noche* system for each day.

## Steps to find a date

### Example January 31, 1997

1. The year is divided by 52---number of the years in the cycle of *Mexican Calendar* system. Use the remainder with the first 5 rows in *Table 1*. The cell is the corresponding type of year.
	- 1997 / 52 = 38 with remainder of 21
	- `date_remainder = getRemainder(1997, 52);`
	- `year_remainder = getRemainder(21, 4);`
	- `type_of_year = getTypeOfYear(year_remainder = 1);`
	- `y_number_remainder = getRemainder(21, 13);`
	
	- 10-Tecpatl, 17. Atlacahualo (18:43 / Mar 11)
	- 10-Tecpatl, 17. Tititl (18:43 / Jan 25)
	- 11-Calli, 01. Atlacahualo (0:43 / Mar 12)
	- 11-Calli, 17. Tititl (0:43 / Jan 26)
	- 	31 - 26 + 1 = 6 for Table 3 = Miquiztli
	- 	31 - 26 = 5 for array in program = Miquiztli
2. 

