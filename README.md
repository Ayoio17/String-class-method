Overview

The Datetime Converter is a C++ program that transforms datetime strings from the format "YYYY-MM-DD HH:MM:SS" into a more human-readable format: "DDth of MonthName, YYYY at HH:MM AM/PM". This program validates input, converts time formats, and replaces numeric months with their corresponding names.

Features

Input Validation:

Ensures the input string matches the expected "YYYY-MM-DD HH:MM:SS" format.

24-Hour to 12-Hour Conversion: Converts the hour component from 24-hour to 12-hour format with appropriate AM/PM suffixes.

Numeric Month Replacement: Converts numeric month values to their corresponding names (e.g., "04" to "April").

Day Suffix Formatting: Adds the correct suffix to the day (e.g., "1" to "1st", "2" to "2nd").

Installation

Compile the Program:

Use a C++ compiler to compile the program. For example, using g++:

    g++ -o datetime_converter datetime_converter.cpp

Usage

Run the Program:

Execute the compiled program:

    ./datetime_converter

Input Format:

Provide the datetime string in the format "YYYY-MM-DD HH:MM:SS". 

For example:

    [2023-01-08 14:05:09]

Output:

The program will output the converted datetime string. 

For example:

    08th of January, 2023 at 2:05 PM

Error Handling:

If the input format is invalid, the program will return:

    Invalid datetime format

Example

    #include <iostream>
    #include "datetime_converter.h"

    int main() {
    std::string input = "2023-01-08 14:05:09";
    std::cout << convertDatetime(input) << std::endl; // Outputs: 08th of January, 2023 at 2:05 PM
    return 0;
    }
