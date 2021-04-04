# Data Model Design

## Summary

A quick summary of the different data modeling methodologies historically include :
* Flat Model — single, two-dimensional array of data elements
* Hierarchical Model — records containing fields and sets defining a parent/child hierarchy
* Network Model — similar to hierarchical model allowing one-to-many relationships using a junction ‘link’ table mapping
* Relational Model — collection of predicates over finite set of predicate variables defined with constraints on the possible values and combination of values
* Star Schema Model — normalized fact and dimension tables removing low cardinality attributes for data aggregations
* Data Vault Model — records long term historical data from multiple data sources using hub, satellite, and link tables

## Database Development Life Cycle

Some criteria that the data model must meet :
* Adaptability — creating schemas that withstand enhancement or correction
* Expandability — creating schemas that grow beyond expectations
* Fundamentality — creating schemas that deliver on features and functionality
* Portability — creating schemas that can be hosted on disparate systems
* Exploitation — creating schemas that maximize a host technology
* Efficient Storage — creating optimized schema disk footprint
* High Performance — creating optimized schemas that excel

The 3 stages in the life of a data model :
* A fresh install — based upon the current version of the schema
* Apply an upgrade — drop/create/alter dB objects upgrading one version to the next
* Data migration — where a disruptive "upgrade" occurs (like splitting tables or platform)

The main flaws that we encounter in a data model :
* Composite Primary Keys avoid them, rarely effective or appropriate; there are some exceptions depending upon the data model
* Bad Primary Keys usually datetime and/or strings (except a GUID or Hash) are inappropriate
* Bad Indexing either too few or too many
* Column Datatypes when you only need an Integer don’t use a Long (or Big Integer), especially on a primary key
* Storage Allocation inconsiderate of data size and growth potential
* Circular References where a table A has a relationship with table B, table B has a relationship with table C, and table C has a relationship with table A

How to evolve a data model ?
1. Understand the data
2. Model the data (if that doesn't work, we go back to step 1)
3. Validate the model (if that doesn't work, we go back to step 2)
4. Build the model
5. Deploy the model
6. Test the model (if that doesn't work, we go back to step 1 or 2)
7. Release

Schema changes can be an expensive proposition so understanding the database life cycle and its role becomes very important. Versioning your database model is critical. Use graphical diagrams to illustrate the designs. Create a "Data Dictionary" or "Glossary" and track lineage for historical changes.

## The Data Modeling Process Layers

| Data Model Aspect | Holistic | Conceptual | Logical | Physical |
|-------------------|----------|------------|---------|----------|
|Data Silos|X| | | |
|Data Silo Relationships|X| | | |
|Element Names| |X| | |
|Element Relationships| |X| | |
|Element Generalizations| |X| | |
|Element Items| |X| | |
|Entity Names| | |X| |
|Entity Relationships| | |X| |
|Entity Keys| | |X| |
|Entity Attributes| | |X| |
|Entity Constraints| | |X| |
|Table / View Names| | ||X|
|Column Names| | | |X|
|Column Data Types| | | |X|
|Column Default Values| | | |X|
|Primary / Foreign Keys| | | |X|
|Index Names| | | |X|
|Index Properties| | | |X|
|Storage Configurations| | | |X|