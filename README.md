# ExtractClinHxFromCCD
Extract clinical history from CCD in XML format

## Objective
As part of a data migration from Centricity to Epic, a text summary of the patient's clinical history was requested by clinicians since it cannot be converted as discrete data.

## Function
The process starts with the consumption of a CSV file containing patient demographics. The consuming process (CallAPIForCCD) extracts patient identifiers needed to call the Centricity SOAP API with the needed authentication and parameters to retrieve all discrete data points documented in the patient's chart. The resulting XML-formatted document is passed onto the next consumer (ExtractHxFromCCD) that is responsible for extracting the data points containing the patient's clinical history. After extraction, the process formats the data into a user-friendly text format as requested by clinicians.
