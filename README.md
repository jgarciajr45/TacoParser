
Project Overview
The goal of this project is to parse a CSV file containing Taco Bell locations, determine the two Taco Bells that are the farthest apart, and display their details.

Key Components
Data Parsing:

TacoParser class is responsible for parsing each line of the CSV file to create Taco Bell location objects.
Location Representation:

Point struct holds latitude and longitude values.
TacoBell class implements the ITrackable interface and represents a Taco Bell location.
Distance Calculation:

The main program uses the GeoCoordinate class from the GeoCoordinatePortable library to calculate distances between locations.
Testing:

TacoParserTests class contains unit tests to ensure the parsing logic works correctly.
Detailed Breakdown
TacoParser.cs
Namespace: LoggingKata
Class: TacoParser
Method: Parse(string line)
Splits the input line into an array of strings.
Parses latitude, longitude, and name from the array.
Creates and returns a TacoBell object.

Program.cs
Namespace: LoggingKata
Main Method:
Reads lines from the CSV file.
Parses each line into TacoBell objects using TacoParser.
Uses nested loops and GeoCoordinate.GetDistanceTo to find the two farthest locations.
Displays the names and distance of the two farthest Taco Bells.
TacoParserTests.cs
Namespace: LoggingKata.Test
Tests:
ShouldReturnNonNullObject: Verifies that the parser returns a non-null object.
ShouldParseLongitude: Verifies that the parser correctly extracts the longitude.
ShouldParseLatitude: Verifies that the parser correctly extracts the latitude.




Summary

This project involves parsing a CSV file to create Taco Bell location objects, calculating the distances between these locations to find the farthest pair, and testing the parsing logic to ensure accuracy. The TacoParser class handles the parsing, the main program handles the distance calculation, and unit tests verify the correctness of the parsing logic.




