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

Cost Columns

Cost Columns represent monetary values at different stages of the pricing lifecycle: Billed Cost, Effective Cost, List Price (List Unit Price times Pricing Quantity), Contracted Cost (Contracted Unity Price times Pricing quantity). 

Unit Price Columns Capture Rate Information

List Unit Price (single pricing unit of associated SKU of data generator exclusive of any discounts)
Contracted Unit Price (agreed upon unit price for a single pricing unit of the associated SKU inclusive of negotiated discounts while excluding commitment based discounts)

Consumption Columns track resource usage independent of pricing. 

Consumed Quantity - volume of usage based on provider measurement
Consumed Unit - unit of measurement for consumption


Currency Column (Billing Currency Column) identifies the monetary denomination

Different FinOps Personas need different cost views. Finance needs Billed Cost for invoice reconciliation. Engineering needs Effective Cost for true resource attribution. Procurement needs List Cost and Contracted Cost to measure negotiation effectiveness.

Billed Cost and Effective Cost serve fundamentally different purposes. Billed Cost matches invoices. Effective Cost distributes prepaid purchases across the resources that consumed them. Summing Effective Cost for a billing period will not match your invoice.

Savings calculations require the right comparison. Comparing Effective Cost to List Cost overstates savings by including negotiated discounts. To measure commitment discount value specifically, compare Effective Cost to Contracted Cost.

Consumed Quantity differs from Pricing Quantity. Consumed Quantity reflects actual resource usage at provider-measured granularity. Pricing Quantity reflects the billable units after pricing rules like block pricing. A 500-token consumption might be priced as 1 block of 1,000 tokens.

Unit prices enable rate verification. List Unit Price and Contracted Unit Price let analysts validate that providers are applying correct rates. The formulas are deterministic: List Unit Price × Pricing Quantity = List Cost; Contracted Unit Price × Pricing Quantity = Contracted Cost.

Multi-currency environments require explicit currency handling. Organizations with global deployments may have charges in multiple currencies. Billing Currency identifies the denomination for each charge, enabling proper aggregation and currency conversion when needed. All cost columns are denominated in the Billing Currency.

Aggregations

When aggregating for savings calculations, it's important to exclude one-time or recurring charges that are paid to cover future eligible charges or the covered charges themselves. This exclusion helps prevent double counting of these charges in the aggregation.

When looking at List Cost or Contracted Cost, apply a filter to the Charge Category (purchase or usage) before summing the column to prevent double counting of charges. 

Analyst Application

You can use the Billing columns to reconcile invoices, calculate savings, track spending trends, and validate pricing.

SAVINGS CALCULATION: 
SELECT SUM(ContractedCost) - SUM(EffectiveCost) AS CommitmentSavings,
SUM(ListCost) - SUM(ContractedCost) AS NegotiatedSavings 
FROM focus_data 
WHERE BillingPeriodStart >= '2026-01-01' 
AND BillingPeriodEnd < '2026-02-01'

Effective Cost versus Contracted Cost Example

Let's say you pre-purchase a $1 per hour virtual machine (VM) instance with a commitment discount that provides a 30% and is paid all upfront. Since the VM was pre-purchased, 100%, you will pay for it now, and next month's Billed Cost will be $0 because it was paid last month. Once you apply the amortized rate, you end up with an Effective Cost of $0.70 per hour.

Now let's talk about negotiated discounts. You have a negotiated discount with the CSP of 5% for all purchases. Therefore, you will never pay the List Cost ($1). You will always pay (List Cost * 95%) for OnDemand usage. This becomes the Contracted Cost ($0.95). 

It is important to understand that the full effective cost is $0.70, but the savings is not $0.30. A savings of $0.30 would be comparing the List Cost to the Effective Cost. However, you will never pay the List Cost because of the 5% negotiated discount. To figure out the savings for the commitment-based discount, you will need to compare Effective Cost and Contrated Cost to eliminate the 5% negotiated discount. This answers the question, "How much did I save by purchasing this commitment-based discount compared to not buying the discount?" The comparison needed is between Effective Cost and Contracted Cost. In this example, the savings for the commitment-based discount would be $0.25. 

Best Practices for Billing Cost Columns: 
Use Billed Cost for invoice reconciliation only
Billed Cost matches what appears on invoices. Do not use it for resource attribution or trend analysis involving commitment discounts.
Use Effective Cost for spend analysis and allocation
Effective Cost distributes prepaid purchases to consuming resources. Use it for chargeback, showback, and cost optimization analysis.
Validate unit price math on sample rows
Confirm that List Unit Price × Pricing Quantity = List Cost and Contracted Unit Price × Pricing Quantity = Contracted Cost. Discrepancies indicate data quality issues.
Separate negotiated and commitment savings
List Cost vs. Contracted Cost measures negotiation effectiveness. Contracted Cost vs. Effective Cost measures commitment discount value.
Track Consumed Quantity for usage optimization
Consumed Quantity reflects actual resource usage independent of pricing. Use it to identify optimization opportunities without rate fluctuations distorting the picture.
Handle multi-currency data explicitly
Group or filter by Billing Currency before aggregating costs. Summing USD and EUR charges without conversion produces incorrect totals.

### Pricing

Pricing metrics answer, "What are we being billed for?", not "What did we use?" The columns related to pricing provide details about how a service provider has priced each resource and help analysts understand how each line item is priced. Cost is calculated using this basic formula: 

Time or Usage * Rate = Cost
Pricing Quantity * Unit Price = Cost 

The Pricing Quantity column provides the time or usage side. List Unit Price, Contracted Unit Price, or calculated variations of these columns provide the Rate information. Pricing Category identifies the pricing model (Standard, Committed, Dynamic, Other). Unit prices (List Unit Price, Contracted Unit Price, derived Billed Unit Price, and Effective Unit Price) show rates at different discount stages. Together, these enable unit economics, savings calculations, and optimizations analysis. Learn more about the columns in this category below:

PRICING CATEGORY

Describes the pricing model used for a charge at the time of use or purchase. Pricing Category can be useful for distinguishing between charges incurred at the list unit price or a reduced price and exposing optimization opportunities, like increasing commitment-based discount coverage.

Normalized Column with Allowed Values: 

Standard: Charges priced at the agreed upon rate for the billing account, including negotiated discounts. This pricing includes any flat rate and volume/tiered pricing but does not include dynamic pricing or reduced pricing due to the application of a commitment discount. This does include the purchase of a commitment discount at agreed upon rates.

Dynamic: Charges priced at a variable rate determined by the provider. This includes any product or service with a unit price the provider can change without notice, like interruptible or low priority resources.

Committed: Charges with reduced pricing due to the application of the commitment discount specified by the Commitment Discount ID.

Other: Charges priced in a way not covered by another pricing category.

PRICING QUANTITY

The volume of a given SKU associated with a resource or service used or purchased, based on the Pricing Unit. This is distinct from Consumed Quantity, as it focuses on pricing and cost, not resource and service consumption.

Pricing Quantity forms the Usage part of Time or Usage x Rate = Cost. In the FinOps practice, we can impact cloud spend by paying less for what you use (rate reduction). Take advantage of cloud discount pricing models such as Savings Plans (AWS, Azure), Reserved Instances (AWS, Azure), and Committed Use Discounts (GCP) based on usage data from FOCUS conformed datasets.

PRICING UNIT

Provider-specified measurement unit for determining unit prices, indicating how the provider rates measured usage and purchase quantities after applying pricing rules like block pricing.

Examples: 

Number of hours for compute appliance runtime (e.g., Hours)

Gigabyte-hours for a storage appliance (e.g., GB-Hours)

Accumulated count of requests for a network appliance or API service (e.g., 1,000 Requests)

Why This Matters

Pricing Quantity is what you're billed for, while Consumed Quantity is what you used. Confuse them and your unit economics are wrong.

For example, let's say you're using block pricing. You pay for 1,000 hours, but only use 501 of those hours. That's Pricing Quantity = 1,000, and Consumed Quantity = 501. Calculate cost per hour using Consumed Quantity and you show $2.50/hour, when you're actually paying $5.00/hour. If Finance catches the error, then your credibility may drop. Understanding pricing mechanics is mandatory for accurate financial analysis.


There are also several currency-related columns in FOCUS specification: 

Pricing Currency
The national or virtual currency denomination that a resource or service was priced in.
Pricing Currency is commonly used in scenarios where different currencies are used for pricing and billing.

Pricing Currency Contracted Unit Price 
The Pricing Currency Contracted Unit Price represents the agreed-upon unit price for a single Pricing Unit of the associated SKU, inclusive of negotiated discounts, if present, while excluding negotiated commitment discounts or any other discounts. This price is denominated in the Pricing Currency. When negotiated discounts do not apply to unit prices and instead are applied to exchange rates, the Pricing Currency Contracted Unit Price defaults to the Pricing Currency List Unit Price. The Pricing Currency Contracted Unit Price is commonly used to calculate savings based on negotiation activities.

Pricing Currency Effective Cost
Represents the cost of the charge after applying all reduced rates, discounts, and the applicable portion of relevant, prepaid purchases (one-time or recurring) that covered this charge, as denominated in Pricing Currency.This allows the FinOps Practitioner to perform a conversion from either: a national currency to a virtual currency (e.g., tokens to USD), or
one national currency to another (e.g., EUR to USD).

Pricing Currency List Unit Price
Represents the suggested provider-published unit price for a single Pricing Unit of the associated SKU, exclusive of any discounts. This price is denominated in the Pricing Currency.
The Pricing Currency List Unit Price is commonly used for calculating savings based on various rate optimization activities.

Analyst Application

You can use the Pricing columns to validate rates, understand pricing models, analyze virtual currency scenarios, and verify cost calculations.

Sample Full Pricing Currency Analysis: A FinOps Practitioner is analyzing a SaaS provider that uses a token-based pricing model. The provider bills in USD but prices usage in tokens. The practitioner needs to understand both the token consumption rate and the dollar cost.


SELECT ServiceName, PricingCurrency, PricingUnit, 

SUM(PricingQuantity) AS TotalTokens, 

SUM(PricingCurrencyEffectiveCost) AS TokenCost, 

SUM(EffectiveCost) AS USDCost 

FROM focus_data 

WHERE ProviderName = 'Acme SaaS' 

AND BillingPeriodStart >= '2026-01-01' 

AND BillingPeriodEnd < '2026-02-01' 

GROUP BY ServiceName, PricingCurrency, PricingUnit

Best Practices

Use Pricing Quantity for all cost calculations
Pricing Quantity is the billing basis. Always divide cost by Pricing Quantity for unit economics, never by Consumed Quantity unless you want consumption efficiency metrics.

Filter Charge Category when aggregating Pricing Quantity
When aggregating Pricing Quantity for commitments, include Usage for utilization and Purchase for commitment size. Never include both together or you will double count.

Group by Pricing Unit before aggregating
Never sum across different units. Hours ≠ GB ≠ Credits. Always group by unit before aggregating Pricing Quantity or cost.

Use Pricing Category to identify optimization opportunities
Standard means potential commitment coverage. Committed is already optimized. Dynamic requires you to consider risk tolerance and volatility

Understand your pricing strategy
Understand your pricing strategy by comparing Pricing Quantity to Consumed Quantity. Large divergence between them usually signals block or stair step pricing and a potential optimization opportunity.

Report Pricing Quantity to Finance, Consumed Quantity to Engineering
Finance reconciles invoices using Pricing Quantity. Engineers optimize resources using Consumed Quantity. Provide both views so each team can work from the data they trust.

### Account Columns

Overview

Account columns establish the organizational hierarchy for billing data. FOCUS defines a two-tier structure: billing accounts (where invoices are generated) and sub accounts (where resources and services are deployed). 

Each tier includes three columns that work as a set:

ID: Provider-assigned unique identifier

Name: Human-readable display name

Type: Provider-defined classification (introduced in v1.2)

The billing account represents the financial relationship with the provider. Sub accounts represent logical groupings beneath that relationship, used for access control, cost management, or organizational structure.


Billing Account ID
An identifier assigned by the data generator for a billing account. 
Billing accounts are commonly used for scenarios like grouping based on organizational constructs, invoice reconciliation, and cost allocation strategies.

Billing Account Name
A display name assigned to a billing account. 
A friendly name, if available from your provider, that can be beneficial for display purposes and reports. 

Billing Account Type
A provider-assigned name to identify the type of billing account.
Billing Account Type is commonly used for scenarios like mapping FOCUS and provider constructs, summarizing costs across providers, or invoicing and chargeback.

Sub Account ID
A provider-assigned identifier assigned to a sub account that helps provide organizational hierarchy. Sub Account ID is commonly used for scenarios like grouping based on organizational constructs, access management needs, and cost allocation strategies. (for Microsoft it's resource grouping, access management and cost segregation) 

Sub Account Name
A display name assigned to a sub account. Sub Account Name is commonly used for scenarios like grouping based on organizational constructs, access management needs, and cost allocation strategies.

Sub Account Type
A provider-assigned name to identify the type of sub account. Sub Account Type is a readable display name and not a code.
Sub Account Type is commonly used for scenarios like mapping FOCUS and provider constructs, summarizing costs across providers, or invoicing and chargeback.

The billing account represents the financial relationship with the provider. Sub accounts represent logical groupings beneath that relationship, used for access control, cost management, or organizational structure.

Why This Matters

Allocation and chargeback depend on accurate account attribution. Without reliable account identifiers, you cannot assign costs to business units, departments, or cost centers. These six columns are the foundation for any organizational cost reporting.

Multi-account environments are the norm, not the exception. Large enterprises routinely operate dozens or hundreds of accounts across providers. These columns let analysts aggregate, filter, and compare costs across complex account hierarchies.

The ID/Name/Type pattern repeats throughout FOCUS. Understanding how these three elements work together here prepares you for similar patterns in other column groupings (Commitment Discount, for example).

Type columns bridge FOCUS and provider-native terminology. Billing Account Type and Sub Account Type (both conditional, added in v1.2) surface provider-specific account classifications. Analysts use these to map FOCUS data back to provider consoles and documentation.

Nullability rules enforce data integrity. When Sub Account ID is null, Sub Account Name and Sub Account Type must also be null. When Sub Account ID has a value, Name and Type must not be null. These constraints prevent orphaned or inconsistent account metadata.

Analyst Application

Analysts can use the Account columns to allocate costs across organizational boundaries, reconcile charges to invoices, and identify cost ownership.

Example: A FinOps Practitioner is building a monthly chargeback report for Finance. They query Billed Cost grouped by Billing Account ID alone. The report shows $2M in total spend, but Finance asks which departments own that spend.

SELECT BillingAccountId, BillingAccountName, SubAccountId, SubAccountName,
SUM(BilledCost)
FROM focus_data
GROUP BY BillingAccountId, BillingAccountName, SubAccountId, SubAccountName

Best Practices
1. Always include both ID and Name columns in reports.
IDs ensure uniqueness; Names provide readability. Reports need both for accuracy and usability.
2. Use Sub Account ID for granular cost allocation.
Billing account alone is too coarse for most chargeback scenarios. Sub accounts map to teams, projects, or environments.
3. Leverage Type columns for multi-provider normalization.
Billing Account Type and Sub Account Type help standardize reporting across providers with different account terminology.
4. Filter by Billing Account ID for invoice reconciliation.
Each billing account corresponds to a billable relationship. Match Billed Cost totals to invoices at this level.
5. Validate null patterns in sub account columns.
If Sub Account ID is populated, Name and Type must not be null. Violations indicate data quality issues.
6. Document account-to-owner mappings outside FOCUS.
FOCUS provides the structure; your organization provides the business context. Maintain a reference table linking Sub Account ID to cost centers


### Capacity Reservations

Overview

Capacity reservations are agreements that secure dedicated resources for a specified period, which organizations use to guarantee capacity during peak demand (like Cyber Monday, tax season, or for a product launch). Unlike commitment discounts (which provide pricing discounts), capacity reservations guarantee resource availability, and you're charged for the reserved capacity regardless of actual consumption. Common examples include AWS Capacity Reservations, GCP Reservations, and Azure Capacity Reservations.

Capacity Reservation ID
Purpose: Uniquely identify a specific capacity reservation.

Type: Dimension

Uses:

Tracking specific reservations over time

Calculating utilization per reservation

Identifying which reservations are underutilized

Grouping charges by reservation for cost allocation

Capacity Reservation Status
Purpose: Indicate whether capacity was used or unused.

Type: Dimension

Uses:

Calculating utilization percentage

Identifying waste (sum of Unused charges)

Optimization targeting (which reservations consistently show Unused rows)

Rightsizing reservations (reduce capacity of consistently unused)

Allowed Values: Used, Unused 


Why This Matters

Capacity reservations secure dedicated infrastructure, guaranteeing resource availability when you need it. This prevents "capacity not available" failures during peak demand. Unlike on-demand, you pay for reserved capacity continuously, whether you use it or not. You must be able to track utilization in order to be able to identify waste.

🔑  Key Concept
CapacityReservationStatus makes waste visible. Track it, measure it, fix it. Ignore it and you're paying for capacity you don't use.


Analyst Application

You can use the Capacity Reservations columns to determine the percentage of reserved capacity actually used, identify the dollar value of any unused reserved capacity, and find reservations with persistent low utilization for rightsizing. Below are two sample use cases and the associated queries:
a. Analyze capacity reservations on compute costs - https://focus.finops.org/use-case/analyze-capacity-reservations-on-compute-costs/ 
b. Identify unused capacity reservations - https://focus.finops.org/use-case/identify-unused-capacity-reservations/ 

Valid Utilization Calculation:
❌ Invalid Utilization Calculation:
SUM(CASE WHEN Status = 'Used' THEN ConsumedQuantity ELSE 0 END) / <br>SUM(ConsumedQuantity)

Why: Used / (Used + Unused) = utilization percentage. Separates actual usage from wasted capacity.

Best Practices:

1. Always separate Used from Unused in utilization calculations.
Used / (Used + Unused) = utilization. 
Both components are required for an accurate percentage
2. Monitor utilization trends over time.
A single snapshot can be misleading. Track daily/weekly utilization to identify patterns.
3. Calculate utilization per Capacity Reservation ID, not in aggregate.
Aggregating masks underutilization. Individual reservation tracking reveals optimization targets.Provide your feedback on BizChat
4. Filter Charge Category = 'Usage' for capacity reservations.
Capacity reservations only appear in Usage rows. Purchase rows don't exist.
5. Use Unused rows to identify rightsizing opportunities.
Consistently unused capacity represents an opportunity to reduce or cancel reservations.
6. Compare reservation cost vs. on-demand equivalent.
Calculate if reservation actually saves money. Low utilization may make on-demand cheaper.

### Charge


Overview

Charge columns classify and describe individual line items in billing data. They answer fundamental questions about each row: What type of charge is this? Is it a correction? How often does it occur? What is it for?

Charge Category
The highest-level classification of a charge based on the nature of how it is billed

Normalized Column with Allowed Values: 

Purchase: Positive or negative charges for the acquisition of a service or resource bought upfront or on a recurring basis including refunds
Tax: Positive or negative charges based on the quantity of a service or resource that was consumed over a given period of time including refunds
Usage: Charges based on the quantity of a service or resource that was consumed over a given period of time
Credit: Positive or negative charges granted by the provider for various scenarios (e.g promotional credits or corrections to promotional credits)
Adjustment: Positive or negative charges the provider applies that do not fall into other category value

Charge Class
Indicates whether the row represents a correction to a previously invoiced billing period. It will contain a value of correction when this line of the billing data is making a correction to a previous billing period. This is important for an analyst to be able to differentiate and filter between corrections and regularly incurred charges. 
Normalized Column with Allowed Values:
Correction: Correction to one or more charges invoiced in previous billing periods (e.g., refunds and credit modifications).
Null: a value of NULL represents a normal charge (i.e., a non-correction).

Charge Description
Self-contained summary of the charge's purpose and price. A Charge Description provides a high-level context of a row without requiring additional discovery. It typically covers a select group of corresponding details across a billing dataset or provides information not otherwise available

Charge Frequency
Indicates how often a charge will occur.
Normalized Column with Allowed Values:
One-Time: Charges that only happen once and will not repeat. One-time charges are typically recorded on the hour or day when the cost was incurred.
Recurring: Charges that repeat on a periodic cadence (e.g., weekly, monthly) regardless of whether the product or service was used. Recurring charges typically happen on the same day or point within every period. The charge date does not change based on how or when the service is used.
Usage-Based: Charges that repeat every time the service is used. Usage-based charges are typically recorded hourly or daily, based on the granularity of the cost data for the period when the service was used (referred to as charge period). Usage-based charges are not recorded when the service is not used.
Examples: Listed below are example scenarios with the related ChargeFrequency.
Upfront commitment purchase - One-Time
Ad-hoc usage charges - Usage-Based
Monthly commitment fee - Recurring

Charge Category and Charge Class are normalized columns with fixed allowed values. Charge Frequency is also normalized. Charge Description is free-form text provided by the provider.

Why This Matters

Charge columns are the foundation for every cost analysis. If you misclassify a $100K commitment purchase as usage, your utilization analysis breaks. If you forget to filter corrections, last month's $50K refund distorts this month's trend analysis. If you misunderstand ChargePeriod vs. BillingPeriod, your accrual-basis reporting will be wrong by thousands of dollars.

Charge Period Start and Charge Period End* define when the charge was incurred, which differs from Billing Period (when invoiced).

Charge Description provides human-readable context. Use it for initial investigation, then filter on normalized columns for aggregation.

ChargeClass MUST be null for non-corrections or same-period corrections. ChargeClass MUST be "Correction" when not null. Always filter corrections using WHERE ChargeClass IS NULL for operational analysis.

Analyst Application
An Analyst can use the Charge columns to: 
Understand costs over time to know when charges will come in
Look at a Charge Description to understand a charge itself 
Differentiate between corrections and regularly incurred charges
Group costs into different categories (e.g. these are purchases, these are usage-based billing)
Create better forecasting models based on identifying an item's Charge Frequency
Broadly categorize charges using Charge Category

Best Practices: 
1. Always filter corrections for operational analysis
Include WHERE ChargeClass IS NULL in every query analyzing current spending patterns, trends, or forecasts. Analyze corrections separately to track billing adjustments.
2. Use Charge Category before Charge Frequency
Filter by category first to narrow scope, then refine by frequency.
Example: Find recurring purchases, not purchases that are recurring
3. Don't filter by Billed Cost sign
Negative charges exist for refunds, while positive charges exist for usage.
Use Charge Category instead of assuming cost sign indicates charge type.

### Charge Origination

Overview
Charge Origination columns answer three fundamental questions about every charge: Who made it available? Who built it? Who invoiced you for it? FOCUS captures these distinct roles because modern procurement involves multiple parties.

Provider
The name of the entity that made the resources or services available for purchase.

Publisher
The name of the entity that produced the resources or services that were purchased.
This is synonymous with companies that publish books that are available for purchase at a bookstore. The company that created the book is known as the "publisher", just as the company that produced the resources you've purchased is the "publisher" of those resources.

Invoice Issuer
The name of the entity responsible for invoicing for the resources or services consumed.

Invoice ID
A provider-assigned identifier for an invoice encapsulating some or all charges in the corresponding billing period for a given billing account.

In simple scenarios, all three entities are identical. When you purchase compute directly from a provider, the provider, publisher, and invoice issuer are all the same company. But marketplace purchases, reseller arrangements, and managed service provider relationships create scenarios where these parties diverge.

Why This Matters

Procurement channels are rarely simple. Organizations purchase cloud services directly, through resellers, via marketplaces, and from Managed Service Providers (MSPs)

These columns let analysts trace spend back to its source regardless of purchasing complexity.

Invoice reconciliation requires knowing who billed you. Invoice Issuer identifies the entity that generated the invoice. When you purchase a third-party SaaS product through a cloud marketplace, the cloud provider is the Invoice Issuer even though a different company is the Publisher.

Publisher reveals the true product source. Marketplace and reseller scenarios obscure who actually built the product. Publisher cuts through that ambiguity. Use it to answer questions like "How much are we spending on software from this vendor across all procurement channels?"

Provider identifies the distribution channel. Whether you bought through a cloud provider, an MSP, or directly from a SaaS vendor, Provider tells you who made the purchase possible. Use it to analyze channel-specific spend and evaluate procurement strategies.

Invoice ID enables precise reconciliation. The sum of Billed Cost for a given Invoice ID must match the payable amount on the corresponding invoice. This column is Recommended (not Mandatory) but essential for organizations that need audit-grade reconciliation.

Best Practices
1. Use Publisher for true vendor spend analysis.
Publisher identifies who built the product. Use it to consolidate spend by vendor across procurement channels.
2. Use Invoice Issuer for payment reconciliation.
Invoice Issuer identifies who you pay. Match Billed Cost totals against invoices from this entity.
3. Expect all three to match for direct purchases.
When purchasing directly, Provider, Publisher, and Invoice Issuer are typically identical. Divergence indicates marketplace or reseller involvement.
4. Use Invoice ID for audit-grade reconciliation.
Sum Billed Cost by Invoice ID to validate against payable invoices. Note that Invoice ID is Recommended, not Mandatory, and may be null for some charges.
5. Analyze Provider to evaluate procurement channels.
Provider shows where you purchased, not who built it. Use to compare spend through MSPs versus direct procurement versus marketplaces.
6. Document scenarios where values diverge.
Marketplace purchases and MSP arrangements create complex origination patterns. Document your organization's scenarios to avoid confusion.

### Commitment Discounts

Overview

Commitment Discount columns are specifically related to the FinOps Principle: FinOps should be enabled centrally. In support of this FinOps Principle, rate, commitment, and discount optimization are centralized to take advantage of economies of scale. These columns help identify which commitment discount is being applied when you purchase an item, for example, Savings Plans and Reserved Instances. This will enable analysts to report around utilization and use of commitment discounts in your bills. 

https://www.finops.org/wg/commitment-based-discounts-overview/

Commitment Discount Category
Indicates whether the commitment discount identified in the CommitmentDiscountId column is based on usage quantity or cost (aka “spend”).

Normalized Column with Allowed Values: 

Spend: Commitment discounts that require a predetermined amount of spend.

Usage: Commitment discounts that require a predetermined amount of usage

Commitment Discount ID
The identifier assigned to a commitment discount by the provider. Commitment Discount ID is required to understand which of your commitments you've made is being applied/purchased in a charge line.

Commitment Discount Name
The display name assigned to a commitment discount

Commitment Discount Quantity
The amount of a commitment discount purchased or accounted for in commitment discount related rows that is denominated in Commitment Discount Units.

Commitment Discount Type
A provider-assigned identifier for the type of commitment discount applied to the row.

Commitment Discount Status
Indicates whether the charge corresponds with the consumption of a commitment discount identified in the CommitmentDiscountId column or the unused portion of the committed amount.

Normative Column with Allowed Values: 
Used: Charges that utilized a specific amount of a commitment-based discount. 
Unused: Charges that represent the unused portion of the commitment-based discount.

Commitment Discount Unit
Represents the provider-specified measurement unit indicating how a provider measures the Commitment Discount Quantity of a commitment discount.

Why This Matters

Commitments are complex. One purchase creates hundreds of usage rows. Aggregate wrong and utilization shows 200%. Exclude Unused rows and waste is invisible. Confuse Usage-based (hours) with Spend-based (dollars) commitments and quantity analysis is meaningless. Miss the amortization pattern and chargeback breaks. Understanding commitment structure prevents misreporting.

Analyst Application

Within a FOCUS conformed dataset, commitment discount data is beneficial to a centralized FinOps team working to manage rate commitments. These columns include the billing data needed to monitor and manage rate commitments. An analyst can use this information to look for what is and is not covered by a commitment as well as data to report performance for individual commitments or categories of commitments. 

Additionally, an analyst can use the Commitment Discount Status column to determine the amount of utilization of the commitment discount versus the portion of the commitment discount that went unutilized. It is important to note that the unused lines will only represent the portion of the commitment discount that is no longer available to be utilized (this could be a future optimization opportunity). For example, a Reserved Instance will have an amount of value to be used over time. This is often broken into time periods (windows) where each part of the discount can be applied. If a portion is not used within a specific window, it goes unused. This unused portion is what is displayed in the Commitment Discount Status column.

Best Practices

Always filter Charge Category when aggregating commitment quantities or costs
Never include both Purchase and Usage in same aggregation or you double-count. Choose based on question: utilization needs Usage, commitment size needs Purchase.

1
Exclude Purchase rows from savings calculations
Savings already in Usage rows via amortization. Including Purchase double-counts.

2
Include Commitment Discount Category in all commitment reports
Usage vs Spend determines what Commitment Discount Quantity means. Make it clear in reports.

3
Validate commitment balance over full term
Sum Purchase quantity should equal sum Usage quantity over complete commitment term. Discrepancies indicate data issues.

### Location

Location columns identify where resources are deployed and services are delivered. FOCUS provides a two-level geographic hierarchy:

Region ID
Provider-assigned identifier for an isolated geographic area where a resource is provisioned or a service is provided

Region Name
A provider-assigned display name for an isolated geographic area where a resource is provisioned or a service is provided. Region Name is commonly used for scenarios like analyzing cost and unit prices based on where resources are deployed

Availability Zone
A provider-assigned identifier for a physically separated and isolated area within a Region that provides high availability and fault tolerance.
Availability Zone is commonly used for scenarios like analyzing cross-zone data transfer usage and the corresponding cost based on where resources are deployed

Regions represent distinct geographic locations with independent infrastructure. Availability zones are isolated facilities within a region, designed to protect against localized failures while enabling low-latency connectivity between zones.

Why This Matters

Pricing varies by region. The same SKU often costs different amounts depending on where it runs. Location columns let analysts compare unit prices across regions and identify cost optimization opportunities through geographic placement.

Data residency and compliance require location tracking. Regulations often mandate where data can be stored and processed. These columns enable reporting on geographic distribution to support compliance requirements.

Cross-zone data transfer generates costs. Traffic between availability zones within a region incurs charges. Availability Zone enables analysis of cross-zone data transfer patterns and their associated costs.

Multi-region architectures need geographic cost visibility. Organizations deploying across regions for latency, redundancy, or compliance need to understand cost distribution by location. These columns support regional budget allocation and chargeback.

Null values are intentional, not errors. Some charges are not region-specific. Global services, account-level fees, and support charges may have null Region ID and Region Name values. This is expected behavior, not a data quality issue.

Analyst Application

You can use the Location columns to analyze geographic cost distribution, compare regional pricing, and identify cross-zone data transfer costs.

SELECT RegionName, AvailabilityZone, 

SUM(BilledCost) AS TransferCost 

FROM focus_data 

WHERE ServiceCategory = 'Networking' 

AND BillingPeriodStart >= '2024-01-01' 

AND BillingPeriodEnd < '2024-02-01' 

GROUP BY RegionName, AvailabilityZone

Best Practices

Use Region ID for joins and filtering
Region ID is the stable, provider-assigned identifier. Use it for programmatic operations and cross-dataset joins.

1
Use Region Name for reports and dashboards
Region Name provides human-readable context. Use it for stakeholder-facing reports where readability matters.

2
Expect null values for global services
Account-level charges, support fees, and global services are not region-specific. Null location values are valid and expected for these charges.

3
Include Availability Zone for network cost analysis
Cross-zone data transfer is a common cost driver. Include Availability Zone when analyzing networking charges to identify optimization opportunities.

4
Compare unit prices across regions
The same SKU can have different prices by region. Use Location columns with List Unit Price to identify lower-cost regions for flexible workloads.

5
Validate RegionId/RegionName consistency
When Region ID is not null, Region Name must also be not null. If you see mismatches, investigate as a potential data quality issue.


### Resource

Resource columns identify the specific technology assets that generate charges. They enable granular cost attribution, optimization analysis, and operational correlation between billing data and infrastructure.

Resource ID
Identifier assigned to a resource by the provider that uniquely identifies individual resources.
Null values are expected for non-resource charges. Tax charges, credits, adjustments, and some service-level fees are not tied to specific resources. When Resource ID is null, Resource Name and Resource Type must also be null.

Resource Name
Human-readable display name assigned to a resource.

Resource Type
The kind of resource the charge applies to.
For example, Virtual Machine, Load Balancer, or Storage Bucket

Tags
A JSON object containing key-value pairs of metadata assigned to the resource, including both user-defined and provider-defined tags.
Tags are commonly used for scenarios like adding business context to billing data to identify and accurately allocate charges. Tags may also be referred to by providers using other terms such as labels.
Tags are finalized before appearing in FOCUS data. When tags are defined at multiple levels (account, folder, resource), the provider applies inheritance rules to produce a single finalized value for each key. The Tags column contains only these finalized, deduplicated values.

Resource ID is the anchor for resource-level analysis. Resource Name provides readability. Resource Type enables grouping across similar infrastructure. Tags add business context for allocation and reporting. 

Why This Matters

Resource-level granularity enables true cost optimization. Account-level or service-level analysis cannot identify which specific virtual machine is over-provisioned or which storage bucket is growing unexpectedly. Resource ID provides the precision needed for actionable optimization.

Tags are the bridge between infrastructure and business context. Without tags, billing data lacks information about cost centers, applications, environments, or owners. Tags enable chargeback, showback, and accountability by connecting charges to organizational structures.

Resource Type normalizes across provider terminology. Different providers use different names for similar resources. Resource Type provides a consistent classification that enables cross-provider analysis of infrastructure categories.

Best Practices" 

1. Match the column to your use case

Use Resource ID for precise resource tracking.

Resource ID is unique within a provider. Use it for joins, deduplication, and correlating billing data with operational systems.

Use Resource Name for human-readable reports.

Resource ID is often opaque. Include Resource Name in reports and dashboards where humans need to identify resources quickly.

Group by Resource Type for infrastructure analysis.

Resource Type enables analysis of infrastructure categories like "all virtual machines" or "all load balancers" without knowing specific resource identifiers.

2. Handle tags well

Parse Tags as JSON, not strings.

Tags is a JSON column. Use JSON functions (JSON_EXTRACT, JSON_VALUE, etc.) to access specific tag keys. String matching on the raw column is unreliable.

Account for tag inheritance in your analysis.

Tags in FOCUS are finalized. A resource inherits tags from parent constructs unless it has its own value for that key. Understand your provider's inheritance rules.

3. Expect nulls
Expect null Resource ID for non-resource charges.
Tax, credits, adjustments, and account-level fees have null Resource ID. Filter these out for resource-level analysis, or handle them separately in allocation logic.



### Service

Service columns classify provider offerings at multiple levels of granularity. They enable analysis of what you purchased, organized from broad functional categories down to specific product names.

Service Category
The highest-level classification based on the service's core function.

Normalized column with allowed values including Compute, Storage, Networking, Databases, AI and Machine Learning, Analytics, Security, and others.

"Other" values exist for edge cases. When a service does not fit existing categories or subcategories, "Other" is used. The Service Category "Other" captures new or emerging services. Each category also has an "Other" subcategory (e.g., "Other (Compute)") for services that do not fit defined subcategories.

Service Name
The provider-specific name of the offering that was purchased.

For example: "Amazon EC2", "Azure Virtual Machines", "Cloud SQL".

Each Service Name has exactly one Service Category. A service cannot belong to multiple categories. If a database service includes compute, storage, and networking charges, those charges still have Service Category = "Databases" because that is the service's primary purpose.


Sevice Subcategory 
A secondary classification within the Service Category, providing more specific workload type information.
For example: "Virtual Machines" under Compute, "Relational Databases" under Databases.
Service Subcategory has a parent-child relationship with Service Category. Each subcategory belongs to exactly one category. For example, "Virtual Machines" is always under "Compute"; "Relational Databases" is always under "Databases". Invalid combinations indicate data quality issues.

Service Category and Service Subcategory are normalized with fixed allowed values defined by FOCUS. Service Name is provider-defined and reflects how each provider names their offerings.

Why This Matters

Service Category enables cross-provider comparison. Different providers use different names for similar offerings. Service Category normalizes these into consistent functional groups. "EC2", "Azure Virtual Machines", and "Compute Engine" all map to Service Category = "Compute", enabling multi-cloud analysis.

Service Subcategory adds workload-type precision. Service Category alone is too broad for some analyses. Knowing that costs fall under "Compute" does not distinguish between virtual machines, containers, and serverless functions. Service Subcategory provides that distinction with values like "Virtual Machines", "Containers", and "Serverless Compute".

Service Name provides provider-specific detail. When investigating anomalies or drilling into specific offerings, Service Name identifies the exact product. Use it for provider-specific analysis, trend investigation, and correlation with provider documentation.

Analyst Application

You can use the Service columns to analyze spend by functional area, compare costs across providers, and investigate service-level trends.

Best Practices for Service Columns
1. Use Service Category for cross-provider analysis.
Service Category normalizes provider offerings into consistent functional groups. Use it to compare infrastructure costs across cloud providers.
2. Use Service Subcategory for workload-type analysis.
When Service Category is too broad, Service Subcategory distinguishes between workload types like virtual machines vs. containers vs. serverless within Compute.
3. Use Service Name for provider-specific investigation.
Service Name identifies the exact provider offering. Use it when drilling into specific services, investigating anomalies, or correlating with provider-specific documentation.
4. Combine Category and Subcategory for precise filtering.
Filter by both columns for targeted analysis. For example,
ServiceCategory = 'Databases' AND ServiceSubcategory = 'Relational Databases'
isolates traditional SQL database spend.
5. Validate Subcategory-to-Category relationships.
Each subcategory has exactly one parent category. If you see "Virtual Machines" under anything other than "Compute", investigate as a potential data quality issue.
6. Expect "Other" values for emerging services.
New provider offerings may not fit existing subcategories immediately. "Other (Compute)" or "Other (Databases)" values indicate services awaiting classification.

### SKU

SKU (Stock Keeping Unit) columns provide product-level identification below the Resource level in the hierarchy. SKU Id identifies the product itself (what you're buying), and SKU Meter describes what functionality is being measured. SKU Price Id identifies the specific price point (how it's priced), and SKU Price Details provides properties as key-value pairs. Together these enable precise product identification, price verification against published lists, unit economics analysis, and SKU-specific optimization.

Think of the SKU ID as the thing that you are purchasing. For example, when you go to the supermarket and purchase a loaf of bread, that loaf of bread has a SKU that allows the retailer to track all of their offerings and item details (e.g. brand, price, weight, number of slices). In the cloud+ environment, a SKU also has details about the item being purchased.


SKU ID
A provider-specified unique identifier that represents a specific SKU. SKUs are quantifiable goods or service offerings in a FOCUS dataset that represent specific functionality and technical specifications.
SKU ID can be referenced on a catalog or price list published by a provider to look up detailed information about the SKU. The composition of the properties associated with the SKU ID may differ across providers. Some providers may not support the SKU construct and instead associate all such properties directly with the SKU Price.
SKU ID is commonly used for analyzing cost based on SKU-related properties above the pricing constructs

SKU Meter
Describes the functionality being metered or measured by a particular SKU in a charge.
Providers often have billing models in which multiple SKUs exist for a given service to describe and bill for different functionalities for that service. For example, an object storage service may have separate SKUs for functionalities such as object storage, API requests, data transfer, encryption, and object management.
This field helps Practitioners understand which functionalities are being metered by the different SKUs that appear in a FOCUS dataset.
Example: Object Storage Service
SkuMeter = "Object Storage" (storage capacity)
SkuMeter = "API requests" (read/write operations)
SkuMeter = "Data Transfer" (egress bandwidth)
SkuMeter = "Encryption" (encryption operations)

SKU Price Details
Represents a list of SKU Price properties (key-value pairs(opens in a new tab)) associated with a specific SKU Price ID.
SKU Price Details helps practitioners understand and distinguish SKU Prices, each identified by a SKU Price ID and associated with a used or purchased resource or service. It can also help determine the quantity of units for a property when it holds a numeric value (e.g., CoreCount), even when its unit differs from the one in which the SKU is priced and charged, thus supporting FinOps Capabilities like Unit Economics.
Additionally, the SKU Price Details may be used to analyze costs based on pricing properties such as terms and tiers.

SKU Price ID
A provider-specified unique identifier that represents a specific SKU Price associated with a resource or service used or purchased.
SKU Price ID can be referenced on a price list published by a provider to look up detailed information, including a corresponding list unit price. The composition of the properties associated with the SKU Price ID may differ across providers. SKU Price ID is commonly used for analyzing cost based on pricing properties such as Terms and Tiers

Why This Matters

The SKU Price ID will relate to the SKU ID and the way it is priced. There might be a few different ways to purchase the same SKU ID, so the SKU Price ID identifies which pricing model is used for the purchase (e.g., purchasing at a list price, with a discount program applied, or when the unit has tiered pricing). 

Without SKU identification, you can't verify prices against published rate cards. You can't compare costs for the same product across regions or commitment terms. You can't detect when providers change pricing. SKU columns connect billing data to price lists, enabling price verification, rate optimization, and detailed product-level analysis.

Analyst Application

Analysts can relate SKU lines to the item purchased and generally find more information about these SKUs in the price list from the provider. 

Use SKU ID for product comparison, SKU Price ID for price comparison.
SKU ID groups all pricing variations. SKU Price ID distinguishes them. Choose based on whether you're comparing products or prices.

1
Always check SKU Price Details for null before extracting properties.
SKU Price Details is optional. Use WHERE SkuPriceDetails IS NOT NULL and COALESCE for safe extraction.

2
Include SKU Meter in SKU-level reports.
SKU Meter provides context for what's being measured. Essential for explaining line items to stakeholders.

3
Use SKU Price ID as lookup key for price lists.
SKU Price ID references provider's published price list. Use it to verify rates and detect pricing errors.

4
Monitor SKU ID consistency across time.
SKU ID should be stable. If same product gets different SKU ID over time, provider changed SKU structure. Impacts time-series analysis.

5
Extract FOCUS-defined properties from SKU Price Details for standardization.
CoreCount, MemoryGB, StorageClass enable cross-SKU comparisons. Provider-specific properties (x_ prefix) vary.

6
Group by SKU Meter when analyzing service costs.
Services often have multiple SKUs metering different functionalities. SKU Meter reveals what drives cost within each service.




### Timeframe

Timeframe columns define when charges occur and when they appear on invoices. FOCUS separates these concepts into two distinct pairs:

Billing Period Start / Billing Period End: The invoice cycle boundaries. These align to your provider's invoicing cadence, typically monthly.

Charge Period Start / Charge Period End: The effective window for the charge itself. This reflects when the resource or service was actually consumed or when a purchase applies.

All four columns use inclusive start bounds and exclusive end bounds. For example, a billing period from 2026-01-01T00:00:00Z to 2026-02-01T00:00:00Z includes January charges but excludes February.

Billing Period Start
A billing period is your normal cadence of invoicing from the provider.  

Billing Period Start: represents the inclusive start bound (date and time) of a billing period.

A time period where Billing Period Start is '2024-01-01T00:00:00Z' and Billing Period End is '2024-02-01T00:00:00Z' includes charges for January, since Billing Period Start is inclusive, but does not include charges for February since Billing Period End is exclusive.

Billing Period End
Billing Period End: represents the exclusive end bound (date and time) of a billing period.

A time period where Billing Period Start is '2024-01-01T00:00:00Z' and Billing Period End is '2024-02-01T00:00:00Z' includes charges for January, since Billing Period Start is inclusive, but does not include charges for February since Billing Period End is exclusive.

Additionally, some charges may apply across multiple billing periods. Charge Period start and end will match the date boundary of the effective period (the time window for which a charge is effective, inclusive of the start date and exclusive of the end date) of the charge. For example, if a purchase is usable for 12 months, the charge will appear across billing periods from: 2024-01-01T00:00:00Z to 2025-01-01T00:00:00Z. 

Charge Period Start
Charge Period Start: represents the inclusive start bound (date and time) within a charge period.

The charge period will depend on the granularity of the billing data provided. If hourly billing data, the charge will be within the specified hour. If daily billing data, the charge will occur within the day. Note that the charge may not necessarily occur on the exact start time of the period start and may not necessarily end on the exact period end, but will most likely occur somewhere within the period.

Charge Period End
Charge Period End: represents the exclusive end bound (date and time) within a charge period.

For example, a time period where Charge Period Start is '2024-01-01T00:00:00Z' and Charge Period End is '2024-01-02T00:00:00Z' includes charges for January 1, since Charge Period Start is inclusive, but does not include charges for January 2 since Charge Period End is exclusive.

Why This Matters

Billing period and charge period are not the same thing. A 12-month commitment purchased in January has a charge period spanning the full year, but appears on the January billing period. Confusing these columns leads to incorrect amortization and forecasting.

Exclusive end bounds prevent double-counting. The end of one period equals the start of the next. For example, January's Billing Period End (2026-02-01) matches February's Billing Period Start. Queries using >= and < operators align naturally with this convention.

Charge period granularity varies by data source. Hourly data produces charge periods of one hour; daily data produces 24-hour windows. The charge may not consume the entire period, but falls somewhere within it.

Invoice reconciliation requires billing period alignment. To match FOCUS data to provider invoices, filter by Billing Period Start and Billing Period End. Charge period columns won't align to invoice totals.

Trend analysis and forecasting depend on consistent period handling. Month-over-month comparisons, budget tracking, and anomaly detection all require correct use of these columns.

Best Practices: 
Use billing period for invoice reconciliation.
Since billing period aligns to provider invoicing cycles, you can match totals against invoices using these columns.

Use charge period for consumption analysis.
Charge period reflects when usage actually occurred. Use for utilization tracking and resource optimization.

Expect charge periods to span billing periods.

Annual commitments, multi-month subscriptions, and prepaid purchases create charge periods longer than one billing cycle.

Account for data granularity in charge periods.

Hourly data produces 1-hour charge windows; daily data produces 24-hour windows. Actual consumption falls within the period, not necessarily at its boundaries.

Never mix billing and charge period in the same filter.

Combining these columns in a single WHERE clause produces unpredictable results. Choose one pair based on your analytical goal.


What's Next

As an analyst, understanding the FOCUS columns helps you to know what information is inside a FOCUS dataset. Before you even start thinking about filters, queries, and getting a certain set of information, you need to know these columns to know what data is there. A deep comprehension of the nuances of each column will lead you to make better queries and yield more accurate results for your data interpretation efforts. 


## Overall Best Practices

Overview & Data

Whether you are using SQL, a BI Tool, or a vendor solution that allows you to customize your reports, the following best practices will apply. They are intended to help you get the results from the data you are looking for.

### Start Simple
Start simply before adding complexity, especially before applying aggregations (e.g., SUM(BilledCost)). Ask yourself, "What question am I trying to answer with this report?" Think back to Gall's Law from the FinOps Certified Practitioner course:

"A complex system that works is invariably found to have evolved from a simple system that worked. A complex system designed from scratch never works and cannot be patched up to make it work. You have to start over with a working simple system." 

- John Gall (1975) Systematics: How Systems Really Work and How They Fail p. 71 

FOCUS Analysts should always start with a simple filter applied to the data. Then, verify the resulting billing lines that are included in the results. Continue to slowly step into the data by adding one filter at a time, looking at the results, and ensuring you are getting the values you expect by learning how the filters are applied in incremental steps.

### Validate Results

To build confidence in the data and in the queries you are running, it is a best practice for FOCUS Analysts to validate the results. There are multiple ways in which you can do this:

1
Validate a Small Time Range: Aligned with starting simple is the best practice to validate results over a small time range. Once you have done this, expand from there. Billing files get large—very large—so checking your work manually can be very difficult. In order to do some form of manual validation, you can restrict your query to a small time range (e.g., 1 hour) during which you may only be dealing with a few thousand rows (something your spreadsheet application can handle). Cross-checking your results in this way can provide the confidence that you have done it right. 

2
Validate Using LIMITs: In addition to validating your results over a small time range, you can also validate results with LIMITs. "LIMIT" sets the maximum number of rows that a query will return, allowing you to control the amount of data displayed or processed. For example, you could query just the first 100 lines and validate the results. If you unbounded all query results, this may produce many, many gigabytes/terabytes of data. Receiving a return result of hundreds of thousands of lines is too much for you to work with anyway. The goal is to take a peek at a portion of the data and validate the results. Setting LIMITs can also help reduce costs in situations where an organization is paying for the size of query results. 

3
Validate Against Other Tooling: If you have multiple tools (State of FinOps(opens in a new tab) data shows FinOps Practitioners use an average of 4.1 tools), you can use those tools to validate the data. If you've created a report in one tool, can you create the same report in another tool to validate? If so, then getting the same result across tools allows you to build confidence in the data and the queries you are running. For example, using a combination of FinOps tools available, like native tools + vendor solution or in-house + native tools, you can set up reports that mirror each other as a way to validate the results you are getting in one solution. Use the multiple tools at your organization to your advantage. Note that this type of validation may not yield a direct comparison unless the tools are all producing FOCUS datasets.

### Use Appropriate Filters

When applying filters, use normalized columns as a preference since these will work across billing data generators. Let's say we want to look for usage lines that are a charge. To find this information, we will need to filter out any credits. Below are two filter options: 

Non-optimal filter: FILTER (WHERE BilledCost > 0)

Optimal filter: FILTER (WHERE ChargeCategory = "Usage")

Although we could filter based on BilledCost, the most optimal filter would be to use the specific ChargeCategory column. Remember, the Charge Category is normalized, so the column will have a specified set of allowed values. Therefore, filtering for usage here will yield a more optimal result.

### Use Negated Filters

When looking at the data, use negated filters to identify what is being excluded. A negated filter is like filtering, but it's the opposite. Instead of selecting data that meets certain criteria, you're selecting data that doesn't meet that criteria. For example, if you have a list of all books and you use a negated filter to find books that are not novels, you'd end up with books that are anything but novels (like textbooks, poetry collections, etc.). 

So, if you want to look at all costs for something, you will also want to look at a negated filter to show what you are not getting. This answers the question: "What are the things in the query not being included?" Using negated filters is a way to make sure the filter applied makes sense. 

For example, if we want to look at all charges related to virtual machines, it is important to use a negated filter to see what data is being excluded when we filter for virtual machines. 

```FILTER (WHERE ServiceName DOES NOT EQUAL "VirtualMachineService")```

### Avoid SUBSTRING Matching (LIKE)

Substring matching is commonly used in queries to filter and retrieve data based on specific patterns or sequences of characters within text fields. Substring matching is essentially finding a smaller sequence of characters (substring) within a larger sequence of characters. Imagine you have a sentence like "The quick brown fox jumps over the lazy dog." If I ask you to find the word "quick" within that sentence, you would look for the sequence of characters "quick" within the larger string. 

The problem with substring matching is that it is inefficient and your results are dynamic. In other words, if a future charge doesn't match your pattern, it will not be included in the pattern. In the sentence example above, if the sentence changes to "The fast brown fox jumps over the lazy dog" then your filter will no longer be inclusive of the appropriate information. Now, there may be cases in which you use SUBSTRING (or LIKE), but if there is a more specific filter available, apply that first. 

For example, consider the filters listed below. 

Non-optimal filter: FILTER (WHERE ChargeDescription LIKE "VM Usage%") 

Note: "VM Usage%" will look for all lines in Charge Description that start with "VM Usage", including lines with additional text afterward (e.g., included: VM Usage - Size Small; excluded: Size Small - VM Usage)

Optimal filter: FILTER (WHERE ServiceName = "VirtualMachineService")

We could use the non-optimal filter; however, if the charge description changes at some point, then the filter will no longer pick up lines that start with VM Usage. The optimal filter in this case would be to filter on Service Name, which is a more stable field. 

### Use DISTINCT or GROUP BY

DISTINCT - filters out duplicate values from the results, showing only unique entries. 

GROUP BY - organizes data into groups based on specified columns, allowing for analysis and aggregation within those groups. 

Cloud billing datasets can contain hundreds of thousands of lines of data. Using DISTINCT and GROUP BY will enable you to gather a set of values with a column or columns. Additionally, using GROUP BY will allow you to gather the set of values and perform aggregations on them (e.g., sum, max, min). When possible, using GROUP BY will provide more flexibility to understand details about a specific set of values. 

### Gather Feedback

Once you have run the queries and created the reports, it is important to seek input. Collaborate with other FinOps Personas to ensure the results that are surfaced are on the right track for the reporting question(s) being asked. For example, there are many different types of 'cost' metrics. Which cost metric does the intended audience care about? 

Work with stakeholders to confirm query requirements, validate results against business expectations, and refine queries based on feedback. Start every query project with 15-minute conversation. "What are you trying to learn? What decision does this support? How will you use results?" Write down requirements before writing SQL. Share draft results early, get directional feedback and iterate.

BEFORE WRITING QUERY: 
Ask stakeholders:

What business question are we answering?

What decision depends on this answer?

What cost metric matters? (BilledCost, EffectiveCost, ListCost, ContractedCost)

What time period is relevant?

What granularity is needed? (daily, monthly, per-resource, per-service)

How will results be used? (dashboard, report, one-time analysis)

WHEN BUILDING QUERY: 
Share interim results:
"Here's what the data shows for one day. Does this align with your expectations?"
"I'm seeing these service categories. Do these groupings make sense?"
"Cost is $X for this period. Is that the right magnitude?"

WHEN PRESENTING RESULTS: 
Present results with context:
Show row counts: "Analysis includes 1.2M charges across 50 services."
Explain filters: "Excluded credits and corrections per your requirements."
Highlight surprises: "VM costs were 40% higher than expected, should we investigate?"
Ask for validation: "Does this match your understanding of our usage?"

REFINE ITERATIVELY: 
Be prepared to iterate based on feedback. Common feedback patterns include:
"Can you break this down by team?"
Add grouping: GROUP BY SubAccountName
"This number seems high."
Check filters: Are credits excluded? Are corrections included?
Verify time range: Full month vs partial month?
"We need to see commitments separately."
Add filter: WHERE PricingCategory = 'Commitment-Based'
Or create separate queries for different pricing categories

### Be Mindful of Date Ranges

When running queries, pay close attention to the date ranges being applied. Remember that start dates are inclusive and end dates are exclusive. Additionally, be aware of the data surfaced by queries across month boundaries, year boundaries, or even results surfaced for months with fewer days, like February. When it comes to cloud billing, a month is not a month. 

Put It All Together

These best practices are meant to be used not in isolation, but together to create and customize reports. For example, you might be filtering on a column and adding DISTINCT or GROUP BY as well. Whichever filters and queries you apply to the dataset, remember that it is always important to validate your results to ensure confidence in the data.

