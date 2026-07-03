# FOCUS Analyst Reviewer 


Key Competencies: 
- Be prepared to build a common language for finance and technology teams
- Be prepared to make data more accessible within the organization
- Have confidence in using data correctly
- Be qualified to leverage the FOCUS Use Case Library
- Know how to run queries on FOCUS datasets using the Use Case Library
- Apply best practices to filter and validate queries

FinOps Landscape - https://www.finops.org/landscape/?prod_TOOLS_SERVICES%5Btoggle%5D%5Bis_focus_adopter%5D=true 

FOCUS Specification - https://focus.finops.org/focus-specification/
FOCUS Columns - https://focus.finops.org/focus-columns/ 
FOCUS Sandbox - https://focus.finops.org/sandbox/#uc-14652 
FOCUS Use Cases - https://focus.finops.org/use-cases/?version=v1-3&use_case=allocate-multi-currency-charges-per-application-2
FOCUS Adoption - https://www.finops.org/wg/adopting-focus-the-finops-open-cost-and-usage-specification/ 
FOCUS Adoption Pitch Deck - https://docs.google.com/presentation/d/1c41cgWcurYRMPN1hxAmvMS6VbRXJNKNs3LTqCUjm9qI/edit 

FOCUS Adoption Success Stories: 
1. European Union - https://www.youtube.com/watch?v=aB9toFmQdZo&list=PLUSCToibAswnhNotqiR8SzxkoRhzJn79j&index=20
2. ST Microelectronics - https://www.youtube.com/watch?v=5WIzx_bixSQ&t=2104s
3. GitLab - https://www.youtube.com/watch?v=8r7J0N6_rls&list=PLUSCToibAswmIoGwT-MuclEmfnSIg6h45&index=7 
4. Zoom - https://www.youtube.com/watch?feature=shared&t=551&v=VLGxlSJQFHE 



"To best enable distributed decision-making regarding technology use, getting consistent and well-understood billing data into the path of the decision-makers is crucial. For example, aim to put billing data in the path of your engineers, early and often. Ideally before they deploy infrastructure... FOCUS datasets enable self-service reporting and can surface insights that native billing data formats may obscure. Leadership reports should integrate FOCUS billing data with business metrics like KPIs(opens in a new tab) and unit economics. Business leaders need to be able to evaluate their technology spend, savings, and opportunities in their standard dashboards."

FOCUS 1.3 Data Model https://docs.google.com/spreadsheets/d/1V9DO1bgr4HWgsYcrZIfFATm3pUb6AN_3QpwSwgqz2_8/edit?gid=0#gid=0 

FOCUS Requirements Model Analyzer - https://finops-open-cost-and-usage-spec.github.io/focus_requirements_model_analyzer/ 

FOCUS Converter https://github.com/finopsfoundation/focus_converters 

How to Export FOCUS Data from Different Cloud Providers: 
- Azure https://focus.finops.org/get-started/microsoft/ https://learn.microsoft.com/en-us/azure/cost-management-billing/costs/tutorial-improved-exports
- Alibaba Cloud https://www.alibabacloud.com/help/en/user-center/export-alibaba-cloud-standard-billing-focus 
- Huawei Cloud https://support.huaweicloud.com/intl/en-us/usermanual-cost/costcenter_000002_03_07.html 

Validator Uses

The FOCUS Validator can be used in the following ways: 

1 As a command-line validator (CLI): Validate a FOCUS dataset and generate a clear conformance report that identifies rule failures.

2 As a machine-readable rule set (YAML(opens in a new tab)): Consume the authoritative FOCUS validation rules to understand or implement conformance logic in your own tooling.

The FOCUS datasets are the real-life implementations of billing data in FOCUS-aligned format. These datasets are ideally acquired directly from the billing data generator. 

The FinOps Open Cost and Usage Specification (FOCUS) is an open technical specification for technology-related billing data that defines clear requirements for vendors to produce uniform cost and usage datasets. The goal of the specification is to provide a common vocabulary to explain vendors' consumption-based billing models. This will help FinOps Practitioners analyze billing data from disparate sources, and it will also help prospective FOCUS data generators by offering a reference format for their consumption-based billing models.

## FOCUS Specification 
0 Specification Details (License and Specs, Members of Steer Co, Document Status) 
1 Introduction (how specs were created, language used: background, intended audience, scope, design principles, design notes, tyopgraphic conventions, FOCUS feature levels, conformance checkers or validators)
2 Supported Features (core capabilities for FinOps practitioners - each feature has a description, dependent column, support column and example SQL query)
3 Columns (overview, ID, name, description, constraints, version)
4 Attributes (high level requirements for data granularity and formatting standards, formatting for each column)
5 Metadata (metadata structure that must be supplied by data providers)
6 Use Case Library (commonly performed FinOps scenarios used as basis for the specification: context, columns, copyable SQL queries)
7 Glossary
8 Appendix - grouping constructs for resources/services and origination of cost data 

FOCUS 1.0 was the first production release of the specification, announced in June 2024.  It defined a baseline of metrics and dimensions to fulfill common and basic FinOps use cases, focusing chiefly on billing models carried by Cloud Service Providers (CSPs).  It also introduced semantics to describe billing data in a provider-agnostic manner. FOCUS 1.1 advanced the specification by adding new columns that give Practitioners deeper, more granular insight into multi-cloud billing data, including capacity reservations, commitment discounts, service subcategories, and SKU details. It also improved metadata to support more reliable ETL pipelines and automation. With major cloud providers already publishing FOCUS exports and conformance reports, this release marked a key step toward truly unified multi-cloud reporting and set the stage for future expansion into SaaS and broader Cloud+ scopes. FOCUS 1.2 moves FinOps into the Cloud+ era by unifying Cloud, SaaS, and PaaS billing data under one schema, giving Practitioners a single way to report, analyze, and allocate costs across all their providers. This release adds the Invoice ID column to streamline reconciliation and chargeback, introduces new billing account dimensions for sharper cost allocation, and expands support for virtual and national currencies so teams can track credits, tokens, and multi-currency spend with clarity. With three new data generators adopting the standard (Alibaba Cloud, Databricks, and Grafana), FOCUS 1.2 strengthens industry alignment and prepares teams for a world where Cloud+ reporting is the norm.  With version 1.3, Practitioners gain more transparency in how data generators allocate costs, a dedicated dataset for tracking contract terms, and new metadata signals that confirm recency and completeness of data generator exports. The update also clarifies the difference between Service Providers and Host Providers, introduces the first planned column deprecations, and lays the groundwork for future conformance programs that help ensure dataset reliability across vendors. FOCUS 1.3 delivers meaningful improvements that remove friction from everyday FinOps work and strengthens the shared language the community depends on.

## Specification Test 
When reading the specification, all audiences will need to know the following aspects: 

Normative text - the rules that make up the specification

Non-normative text - the context of the specification

Supporting content - examples to help understand the application of the specification

The FOCUS specification includes over six hundred requirements. The Requirements Analyzer makes it searchable. With the Analyzer, you can filter by function type—composite, format, nullability, presence, and filter by keyword—MUST, SHOULD, MAY. Drill into specific columns or attributes to see exactly what's required.

https://github.com/FinOps-Open-Cost-and-Usage-Spec/FOCUS_Spec/tree/working_draft/supporting_content

### Specification Attributes


Attributes are requirements that apply across a FOCUS dataset instead of an individual column level. Requirements on data content can include naming conventions, data types, formatting standardizations, etc. Attributes may introduce high-level requirements for data granularity, recency, frequency, etc. Requirements defined in attributes are necessary for servicing FinOps Capabilities accurately using a standard set of instructions, regardless of the origin of the data.

Attributes define formatting for all columns in the specification, providing consistency across FOCUS datasets, making the data easier to use. Attributes define the rules for formatting and validating FOCUS datasets.

Core Attributes - column naming, how missing values appear, number and date formatting, date/time format, null handling, column handling
Standard Attributes - currency format, string handling, discount handling
Specialized Attributes - key-value format, unit format


### Column Handling 
Column Handling defines the naming and ordering conventions for columns appearing in a FOCUS dataset. Consistent column names eliminate the need for data generator-specific query logic and enable portable SQL across all FOCUS data sources. Column Handling helps you answer questions about:

• Who is responsible for incurring or delivering the service?

• What the charge is for?

• When the charge was incurred?

• Where the service was delivered?

• Why the charge was incurred for a specific price?

• How much the charge is, and how that cost is calculated?

All columns defined by FOCUS MUST follow the following rules:

Column IDs MUST use Pascal case.

Column IDs MUST NOT use abbreviations.

Column IDs MUST be alphanumeric with no special characters.

Column IDs SHOULD NOT use acronyms.

Column IDs SHOULD NOT exceed 50 characters to accommodate column length restrictions of various data repositories.

Columns that have an ID and a Name MUST have the Id or Name suffix in the Column ID.

Column display names MAY avoid the Name suffix if there are no other columns with the same name prefix.

Columns with the Category suffix MUST be normalized.

All FOCUS columns SHOULD be first in the provided dataset.

Custom columns SHOULD be listed after all FOCUS columns and SHOULD NOT be intermixed.

Columns MAY be sorted alphabetically, but custom columns SHOULD be after all FOCUS columns.

Identifiers will use the “Id” abbreviation since this is a standard pattern across the industry.

Product offerings that incur charges will use the “Sku” abbreviation because it is a well-understood term both within and outside the industry.

Column naming inconsistencies will break every query and integration. If one provider uses "ResourceID" and another uses "resource_id," your queries fail or require constant case-sensitivity handling. The Pascal case requirement (ResourceId) means your SQL works across all FOCUS providers without modification.


Best Practices in Columns Querying: 
- Always use exact Pascal case column names
- Reference columns by name, never by position
- Use table aliases to avoid ambiguity in joins

Best Practices When Validating Data: 
- Compare actual column names against FOCUS specification
- Check that all mandatory columns exist with correct names
- Verify custom columns also follow naming conventions

Best Practices When Building Integrations: 
- Design tools to expect FOCUS-standard column names
- Reject data with non-compliant column names early
- Document any custom columns added beyond FOCUS requirements

### Null Handling

Cost data rows that don't have a value for a column must be handled consistently to reduce friction for FinOps Practitioners who consume the data for analysis, reporting, and other use cases. Null Handling defines how FOCUS datasets represent missing or unavailable values. This consistency ensures that queries behave predictably across all FOCUS data generators.

Columns MUST use NULL when there isn't a value that can be specified for a nullable column.

Columns MUST NOT use empty strings or placeholder values such as 0, "Not Applicable", "N/A", or "None", or empty strings ("") for any column type. Without consistent null handling, queries fail silently. For example, a provider using empty strings ("") instead of nulls means a SQL query like: WHERE ResourceId IS NULL misses records, and a query like COUNT(DISTINCT ResourceId) includes blanks as values.

There is always a Nullable and Not Nullable "Content Constraints" per column that will be True or False on "Allows nulls:"

Best Practices for Queries: 
1. Always use IS NULL and IS NOT NULL for null checks
2. Never use = '' or = 0 to check for missing values
3. USE COALESCE() or IFNULL to handle nulls in calculations

Best Practices for Validating Data: 
1. Check nullable columns for empty strings and placeholders
2. Verify that not-nullable columns never contain NULL
3. Test aggregations to ensure nulls don't skew results
4. Check for values like "N/A" and "0" used as a placeholder

Best Practices when Building Reports: 
1. Decide how to display nulls (for example: blank, "Unknown", or dash)
2. Document null handling in report definitions for clarity
3. Test reports with data containing nulls to verify how that data will display

### Numeric Format

Numeric Format defines the rules and formatting requirements for numeric columns appearing in a FOCUS dataset. Consistent numeric formatting ensures clarity, accuracy, and ease of interpretation for both humans and systems.

The FOCUS specification does not require a specific level of precision for numeric values. The level of precision required for a given column is determined by the provider and should be part of the data definition published by the data generator.

- Single Numeric Value Only 
- Integer, decimal and scientific notation are allowed.
- No fractional notation
- Clean numbers only (No thousands separators (commas, such as 1,234) No currency symbols (such as $, €, £) No units of measure (such as GB, hours, %) No positive signs (+))

Improper numeric formatting causes calculation errors and data type mismatches. Values like "1,234.56" (with commas), "$45.00" (with currency symbols), or "5 GB" (with units) break SUM and AVG functions. 

Best Practices When Writing Queries: 
Assume numeric columns are proper numbers (no parsing needed)

Use standard arithmetic operators (+,-,*,/)

Apply aggregate functions (SUM, AVG, MIN, MAX) without concern

Scientific notation values work in calculations automatically

Best Practices When Validating Data: 
Test that all numeric columns cast successfully to numeric types

Look for string-like patterns in numeric columns

Verify precision matches provider documentation

Check for negative values only where appropriate

Best Practices When Building Reports: 
Format numbers for display (add add commas, currency symbols) in presentation layer

Store raw numeric values in databases

Document precision and rounding rules

Be aware of scientific notation with large/small numbers

### Date/Time Format

Date/time values MUST be in UTC (Coordinated Universal Time), which helps to avoid ambiguity across different time zones, and ensure consistency for global operations.

Date/Time values MUST align with ISO 8601 standard, which is the globally recognized format for representing dates and times.

ISO 8601-1:2019: https://www.iso.org/obp/ui/?__cf_chl_f_tk=SNz3eMLoDKbEpUZfBBdbxGlVOCwFFCJ3eP0YsFYhmeA-1783047099-1.0.1.1-DL0Gw6Rnk1ANo7YhP26nhedipwGtcJ14GETv4LkvghM#iso:std:iso:8601:-1:ed-1:v1:en 

Values providing information about a specific moment in time MUST use:

Format: YYYY-MM-DDTHH:mm:ssZ

Include date and time components separated by T

Use two-digit hours (HH), minutes (mm), and seconds (ss)

End with Z indicator to denote UTC

Query to Convert to Local Time if Needed: 
SELECT 
  ChargePeriodStart,
  ChargePeriodStart AT TIME ZONE 'America/Los_Angeles' AS PacificTime
FROM 
  focus_data;

### Currency Format 

Currency Format defines the formatting requirements for currency columns appearing in a FOCUS dataset. Consistent currency representation enables accurate cost aggregations, currency conversions, and financial reporting across providers and regions. A currency may be one of the following currency types:

National currency (e.g. USD, EUR)

Virtual currency (e.g. tokens, credits)

Currency columns MUST be represented as a three letter alphabetic code dictated by ISO 4217:2015 https://www.iso.org/standard/64758.html (Ref of Alphabetic Currency Codes: https://en.wikipedia.org/wiki/ISO_4217)

Currency-related columns MUST conform to StringHandling(opens in a new tab) requirements when the value is presented in virtual currency (e.g. credits, tokens).

Billing Currency has mandatory currency format and Pricing Currency has conditional currency format. 

National currency is government-issued legal tender within a recognized monetary system used for real financial transactions (for example: Indian Rupee, Australian Dollar, and the Euro). Virtual currency is a provider-specific credit or token, which is not legal tender. 

Virtual currency typically shows in Pricing Currency when:

Provider uses internal credit system

Commitment discounts denominated in tokens

Prepaid units purchased and consumed

Virtual currency follows String Handling rules:

Must maintain original casing and spacing

Should be descriptive (e.g., "credits", not "cr")

Consistently formatted across all records

Examples of valid virtual currency values in Pricing Currency include 'credits' and 'tokens', such as Databricks DBUs (Databricks Units), MongoDB Atlas Credits, and OpenAI GPT tokens

Validation: 
Check for virtual currency in Billing Currency (which is not allowed) using SQL:

SELECT DISTINCT BillingCurrency

FROM focus_data

WHERE BillingCurrency NOT IN (

   SELECT code
   FROM iso_4217_codes
);

Best Practices when Writing Queries: 
Always use uppercase three-letter ISO codes in filters

Group by currency before aggregating costs

Never assume single currency without checking

Use currency conversion tables with ISO codes as keys

Best Practices When Validating Data: 
Verify all national currency uses ISO 4217 codes

Check that Billing Currency never contains virtual currency

Ensure Pricing Currency correctly identifies type (national vs. virtual)

Validate case consistency (uppercase for ISO codes)

Best Practices when Building Reports: 
Display currency codes alongside amounts (e.g., "1,234.56 USD")

Provide currency conversion when consolidating muti-currency costs

Document which currency is used for totals

Handle virtual currency separately from national currency

Best Practices when Performing Currency Conversions: 
Use ISO codes as lookup keys in exchange rate tables

Apply conversions at the exchange date

Document conversion rates and dates used

Never convert virtual currency to national currency

### String Handling

String Handling defines the requirements for text-based columns appearing in a FOCUS dataset. Proper string handling fosters data integrity, interoperability, and consistency, improving data analysis and supporting reliable data-driven decision-making.

All columns capturing a string value defined in the FOCUS specification MUST follow these requirements. Custom string columns SHOULD adopt the same requirements:

String values MUST maintain the original casing, spacing, and other relevant consistency factors as specified by data generators and end-users. 

Charges to mutable entities (e.g., resource names) MUST be accurately reflected in corresponding charges incurred after the change and will not alter charges incurred before the change, preserving data integrity and auditability for all charge records.

Immutable string values that refer to the same entity (e.g., resource identifiers, region identifiers, etc.) MUST remain consistent and unchanged across all billing periods.

Empty strings and strings consisting solely of spaces SHOULD NOT be used in not-nullable string columns.

Typically Mutable 
Resource Name
Name
Sub Account Name
Tags (values)

Typically Immutable
Resource ID
Billing Account ID
Sub Account ID
Region ID
Invoice ID
SKU ID
Provider

Mutable strings (like resource names) that change retroactively corrupt historical analysis. If renaming "prod-server" to "production-server" updates past charges, your year-over-year trending breaks because you're comparing different entities. Case sensitivity matters: "Production" and "production" should remain distinct when the data generators set them that way.

Best Practices When Writing Queries: 
Use exact case matching for string comparisons

Account for mutable strings changing over time

Join on immutable IDs, not mutable names

Use Resource ID for long-term tracking, and Resource Name for display

Best Practices When Validating Data: 
Compare successive data extracts for retroactive changes

Verify that immutable values never change

Check for empty strings in not-nullable columns

Ensure that original casing and spacing are preserved

Best Practices when Building Reports: 
Use immutable IDs for grouping and aggregation
Display mutable names for readability
Document that names may change over time
Include both ID and name in detailed exports

### Discount Handling

Discount Handling indicates how to include and apply discounts to usage charges or rows in a FOCUS dataset. A discount is a pricing construct where providers offer a reduced price for services. Providers may have many types of discounts, including:

Commercially negotiated discounts: Volume pricing, contract terms

Commitment discounts: Reduced rates when committing to usage or spend

Bundled discounts: Free or reduced usage of one product based on usage of another

Discount Handling is commonly used in scenarios like verifying discounts were applied and calculating cost savings.

All applicable discounts SHOULD be applied to each row they pertain to and SHOULD NOT be negated in a separate row.

All discounts applied to a row MUST apply to the entire charge.

Purchased discounts (e.g., commitment-based discounts) MUST be amortized.

Credits that are applied after the fact use a ChargeCategory of “Credit”.

Discount methods directly impact savings calculations and can inflate ROI reports by 2-10x. Some providers show list price usage rows, then subtract discounts in separate rows (leading to double-counting savings). Others apply discounts directly to usage rows. Misunderstanding this creates incorrect "we saved $X" executive reports.

Best Practices When Analyzing Discounts: 
First identify which discount method your provider uses
Use List Cost vs Billed Cost for inline discounts
Carefully pair usage and discount rows for separate row method
Always validate savings calculations against invoices

Best Practices When Calculating Savings: 
Never sum both price differences AND discount rows
Account for commitment purchases separately from usage
Include unused commitment costs in total commitment analysis
Calculate savings as: (List Cost - Billed Cost) for committed usage

Best Practices When Building Reports: 
Document which discount method applies to each provider
Show both gross (before discount) and net (after discount) costs
Separate commitment purchases from commitment usage
Flag unused commitment amounts as waste/opportunity

### Key-Value Format 

Key-Value Format defines the rules and formatting requirements for columns that convey data as key-value pairs. This structured approach consolidates related information and provides consistency in the schema.

Key-value pairs are also referred to as:

Name-value pairs

Attribute-value pairs

Field-value pairs

The most common use of Key-Value Format in FOCUS is the Tags column, where resource tags are stored as structured data.

Key-Value Format columns MUST contain a serialized JSON string, consistent with the ECMA 404(opens in a new tab) definition of an object. Remember: This specification intentionally uses existing reference standards to define attributes when possible. 

Keys in a key-value pair MUST be unique within an object.

Values in a key-value pair MUST be one of the following types: number, string, true, false, or null. 

Values in a key-value pair MUST NOT be an object nor an array.

Valid key-value format demonstrating all five valid values: {"KeyString":"Value1", "KeyNumber":42, "KeyBool":true, "KeyBool2":false, "KeyEmpty":"", "KeyNull":null}

Disambiguating keys using a prefix: {"parent/key1":"Value1", "child/key1":"Value2"}

Tags are the foundation of showback, chargeback, and cost allocation strategies. Without consistent JSON formatting, tag queries break across providers, and custom parsers fail. A common mistake is treating tags as simple text when they're structured data requiring specific parsing. Inconsistent tag formats prevent automated allocation rules and cost center assignments.

Best Practices When Designing Tag Strategies: 
Use consistent key naming across all resources

Standardize value formats (e.g., "production" not "prod" or "PRODUCTION")

Document required vs. optional tags

Implement tag governance to enforce standards

Keep tag keys simple and descriptive

Best Practices When Writing Queries: 
Use JSON extraction functions, not LIKE on raw JSON

Handle missing tags with COALESCE or IFNULL

Test queries with both tagged and untagged resources

Cache extracted tag values in CTEs for complex queries

Best Practices when Validating Data: 
Verify Tags column contains valid JSON
Check for prohibited structures (such as arrays or nested objects)
Validate that tag keys follow naming conventions
Ensure there are no duplicate keys within the same record

### Unit Format

Unit Format indicates standards for expressing measurement units in columns appearing in a FOCUS dataset. Billing data frequently captures data measured in units related to data size, count, time, and other dimensions.

Unit inconsistencies will break unit economics calculations and usage trending. Mixing "GB" and "GiB" (which differ by ~7%) causes inaccurate storage cost analysis. Without standardized units, comparing "cost per GB" across providers requires complex conversion logic. A common mistake is assuming all data units are base-10 when some are base-2.

Units are expressed as a single unit of measure adhering to one of the following three formats:

<plural-units> - “GB” (unit abbreviations represent plural and singular form), “Seconds”

<singular-units>-<plural-time-units> - “GB-Hours”, “MB-Days”

<plural-units>/<singular-time-unit> - “GB/Hour”, “PB/Day”

Units can be expressed with a unit quantity or time interval. If a unit quantity or time interval is used, the unit quantity or time interval is expressed as a whole number. The following formats are valid:

<quantity> <plural-units> - “1000 Tokens”, “1000 Characters”

<plural-units>/<interval> <plural-time-units> - “Units/3 Months”

Unit values and components of columns using the Unit Format follow a capitalization scheme consistent with the capitalization scheme. 

Data Size Unit Name

Data size unit names are abbreviated using one of the abbreviations in the following table. For example, a unit name of "TB" is a valid unit name, and a unit name of "terabyte" is an invalid unit name. Data size abbreviations can be considered both the singular and plural forms of the unit. For example, "GB" is both the singular and plural form of the unit "gigabyte", and "GBs" would be an invalid unit name.

The following table lists the valid abbreviations for data size units up to 10^18 bits or bytes. For values exceeding this, please refer to the specification(opens in a new tab). 

Count-Based Unit Names

A count-based unit is a noun that represents a discrete number of items, events, or actions. For example, a count-based unit can be used to represent the number of requests, instances, tokens, or connections. 

If the following list of recommended values does not cover a count-based unit, a provider can introduce a new noun representing a count-based unit. All nouns appearing in units that are not listed in the recommended values table will be considered count-based units. A new count-based unit value will be capitalized.

List: Count, Unit, Request, Token, Connection, Certificate, Domain, Core

Time-Based Unit Names

A time-based unit is a noun that represents a time interval. Time-based units can be used to measure consumption over a time interval or in combination with another unit to capture a rate of consumption. Time-based units will match one of the values listed in the following table.

Year, Month, Day, Hour, Minute, Second 

Composite Units

If the unit value is a composite value made from combinations of one or more units, each component will also align with the set of recommended values.

Instead of "per" or "-" to denote a Composite Unit, slash ("/") and space (" ") will be used as a common convention. Count-based units like requests, instances, and tokens can be expressed using a value listed in the count dimension. For example, if a usage unit is measured as a rate of requests or instances over a period of time, the unit can be listed as "Requests/Day" to signify the number of requests per day.

Best Practices when Writing Queries: 
Always include Consumed Unit in results alongside Consumed Quantity

Normalize units before aggregating across different unit types

Document conversion factors used in calculations

Filter by specific units to avoid mixing incompatible types

Best Practices when Calculating Unit Economics: 

Use the correct per-unit calculation. 

Sample Query: 
SELECT
          ServiceName,

          ConsumedUnit,

          SUM(BilledCost) / NULLIF(SUM(ConsumedQuantity), 0) AS CostPerUnit,

          SUM(ConsumedQuantity) AS TotalQuantity,

          COUNT(DISTINCT ResourceId) AS ResourceCount

FROM focus_data

WHERE ConsumedQuantity > 0

AND ConsumedUnit IS NOT NULL

GROUP BY ServiceName,
                ConsumedUnit

ORDER BY CostPerUnit DESC;

Best Practices when Validating Data: 
Check for consistent unit usage across similar services

Verify units match provider documentation

Look for unexpected unit variations over time

Validate unit conversions against known values

Best Practices when Building Reports: 
Display unit alongside quantity (e.g., "1,234 GB" not just "1,234")

Normalize to common units for cross-resource comparison

Document which units are used for each metric

Provide unit conversion factors in report definitions

### Metadata

FOCUS metadata(opens in a new tab) tells you how to work with billing data before you load it. It answers three questions: who generated this data, what structure it has, and when the structure changed.

Data generators supply metadata programmatically via files, APIs, or tables, and SHOULD provide documentation on their implementation of the FOCUS metadata.

Metadata is important because FOCUS is a billing specification that is more evolutionary than a traditional billing specification. Metadata allows providers to communicate explicitly to providers what is actually contained within the data that is provided: level of granularity, when it was last delivered, what version of FOCUS is available. The metadata gives a structured way for providers to communicate to Practitioners, not only what is being provided but also the history.

The primary value of metadata is to enable analysts to consistently load data into a datastore. When combining FOCUS datasets of different versions, knowing what version and schema applies to the data will help you load data. You can plan and build with confidence knowing what is being provided.


Metadata ensures less chaos, fewer broken dashboards, fewer surprises, and more predictable FinOps work.

The specification defines two metadata entities: Data Generator (identifies the source) and Schema (defines the structure).

Data Generator

Included in the metadata is the Data Generator. This is the human-readable name of the entity that is generating the data. For example, if Acme is generating the data, the updated data generator related metadata could look like this: { "DataGenerator": "Acme" }.

Schema

Each FOCUS dataset must have metadata about the schema associated with it. The schema metadata provides information about the structure of the data provided. Within the schema is the following information:

Schema ID: this will provide a way to reference the datasets' providers' version of the schema in the form of a unique identifier.

Creation Date: this provides the date the schema was created.

FOCUS Version: the version of FOCUS utilized for building the dataset.

Column Definition: this provides a list of the columns present in the FOCUS dataset along with metadata about the columns. Below are the attributes that make up a column definition.

Core Attributes: 
Included in the metadata schema column definition are these core parts:

Column Name: The name of the column provided in the FOCUS dataset.
Data Type: The data type of the column provided in the FOCUS dataset.

Clarifying Attributes: 
In addition to the core attributes of the column definition, there are additional attributes that may be available depending on the datatype. 



Numeric Precision & Scale
Numeric precision is the maximum number of digits for the values in the column and numeric scale is the maximum number of digits after the decimal point in decimal numbers. 
For example, the number 123.45 has a precision of 5 and a scale of 2. In cloud billing data, consider a precision of 30 with a scale of 15 because you'll be working with lots of little numbers that make up really big numbers.
Provider Tag Prefixes: this defines the list of prefixes used in the tag name of provider-defined tags. This metadata is useful for the consumer to identify which tags are provider-defined vs user-defined.
String Encoding: The string encoding scheme of the column provided in the FOCUS dataset.
String Max Length: The string max length of the data that can be stored in the column.

Schema changes trigger new metadata. When providers add columns, remove columns, change datatypes, or adopt new FOCUS versions, they create new Schema objects with unique Schema IDs. Data exports reference their Schema ID so you know which structure to expect.

Column definitions prevent load failures. Each column lists its datatype, constraints, and format requirements. Decimal columns specify precision and scale. String columns specify max length and encoding. Without this, database loads fail on datatype mismatches.

Version tracking enables multi-version queries. FOCUS Version tells you which columns exist. Data Generator Version tracks provider-specific logic changes that don't alter schema structure.


Metadata locations and formats vary by provider. Check your provider's FOCUS implementation documentation for:

Metadata file locations (S3 buckets, blob storage, object storage)

Metadata access methods (CLI, API, direct file access)

Metadata update notifications (when schemas change)

Current FOCUS version support

Try these common documentation search terms: "FOCUS metadata", "FOCUS schema", "billing export metadata", "cost data schema".

Metadata Best Practices: 
1. Always check Schema ID before loading data. 
Automate schema change detection. Read new column definitions. Update table structure. Prevent load failures.
2. Store metadata history.
Log each Schema ID you encounter with its Creation Date and Focus Version. Track when data generators change schemas. Debug issues by comparing metadata versions.
3. Use metadata to generate DDL.
Parse Column Definition from metadata. Generate accurate datatypes, precision, scale, and length constraints. Adapt for your database's specific requirements
4. Validate metadata against data.
After reading metadata, load sample data. Verify column names match. Check datatypes cast correctly. Catch data generator metadata errors before full load.
5. Handle deprecation proactively.
Monitor for deprecated flags. Update queries before data generators remove columns. Test with sample data missing deprecated columns.
6. Adapt patterns to your environment.
Every database handles datatypes differently. Document how metadata types map to your database types.

## Specification Columns 

Metrics and Dimensions

The FOCUS specification defines a group of columns that provide quantitative values (numeric values) categorized as "metrics" and qualitative values (such as dates, resource, and provider information) categorized as "dimensions" that can be used for performing various FinOps Capabilities(opens in a new tab).

Metrics are specification-defined columns that provide numeric values and allow for aggregation operations, such as arithmetic operations (sum, multiplication, averaging, etc.) and statistical operations. Metrics will be values used in operations such as average, median, sum, max, and min. You can also filter metrics to identify thresholds (e.g. minimum and maximum).

Dimensions are data that describe something about the row of data that allows you to categorize it (e.g. the region where the cost was incurred, the service the cost is for, and the type of usage the row describes). Typically, a FOCUS Analyst will use a combination of dimensions to filter and group what they are looking for. 

There is a design principle of the specification related to the column name: 

Category: a column name with the term category is a normalized column with a fixed set of values that can be provided. 

Type: a column with the term type is vendor-defined and often relates to that specific vendor's terms and values. 

For example, Commitment Discount Category is a column with a fixed set of values (spend or usage) and Commitment Discount Type is a column with a provider-assigned name to identify the commitment-based discount applied to the row. 

Naming Conventions

The Naming Convention Attribute previously discussed will apply to all columns appearing in the billing dataset. Remember, columns MUST use Pascal Case and MUST be alphanumeric with no special characters. Additionally, the columns MUST NOT use acronyms or abbreviations (with the exception of "Id" and "Sku"). 

Nulls

As we review each column, the columns MUST use null where there is not a value that can be specified for a nullable column. Within each column's Column Constraint section, we can see if the column allows nulls. Columns MUST NOT use empty strings or placeholder values such as 0 for numeric columns or "Not Applicable" for string columns, regardless of whether the column allows nulls or not.

Feature Levels

Within each column's Column Constraint section, we can also see a Feature Level. This designates a column as Mandatory, Conditional, Recommended, or Optional. The feature level designation is based on the following criteria:

Mandatory	A column MUST be present in the billing data with no conditions
Conditional	A column MUST be present in the billing data with conditions
Recommended	A column is RECOMMENDED to be present in the billing data
Optional	A column MAY be in the billing data


Schema

In addition to defining attributes, the specification lays out the schema (representation of a plan or theory in the form of an outline or model) for billing data. Within the specification, the schema outlines the following for each column:

Column ID – a column name that will appear at the top of a column in a FOCUS dataset

Display name – a friendly name that can be used in reports with FOCUS data

Description – a short description of the data within a specific column 

Content Constraints – a summary of the normative text about the constraints within the column, including column type, feature level, allows nulls, data type, value format, and number range

Introduced (version) – the version of the specification in which the column was introduced

This course will cover the description of each column and provide context around the intended use of the column. Refer to the specification(opens in a new tab) to better understand a column or answer specific questions. 

### Billing Columns

Billing columns capture the financial dimensions of your charges: what you owe, what you would have paid, how much you consumed, and in what currency. FOCUS organizes these into four functional groups: Cost, Unit Price, Consumption, Currency. 

