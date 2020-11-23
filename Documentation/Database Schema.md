# Database Schema

This document serves to outline the layout of data for each Chronica article entry. This schema is universal and should be referenced when interacting with any of the articles stored in the database to understand its structure.

## Chronicle

### Chronicle ID

**<u>Attribute name</u>**: chronicle-id

**<u>Description</u>**: ID of the chronicle. Represents when the chronicle was inserted into the database.

* <u>**Field Type**</u>: Integer

### Chronicle Name

<u>**Attribute name**</u>: chronicle-name

**<u>Description</u>**: Name of the chronicle article.

* <u>**Field Type**</u>: String
* <u>**Restraints**</u>: Alphanumeric characters

### Short Description

<u>**Attribute name**</u>: short-desc

**<u>Description</u>**: Description of the chronicle.

* <u>**Field Type**</u>: String
* <u>**Restraints**</u>: Max 150 characters

### Author
<u>**Attribute name**</u>: author

**<u>Description</u>**: Name of the chronicle's author.

* <u>**Field Type**</u>: String
* <u>**Restraints**</u>: Alphanumeric characters

### Year Published
<u>**Attribute name**</u>: year-pub

**<u>Description</u>**: Year the chronicle was published.

* <u>**Field Type**</u>: Integer


### Location
<u>**Attribute name**</u>: location

**<u>Description</u>**: Where the chronicle is physically located.

* <u>**Field Type**</u>: String
* <u>**Restraints**</u>: Max 150 characters

