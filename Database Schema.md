# Database Schema

This document serves to outline the layout of data for each Chronica article entry. This schema is universal and should be referenced when interacting with any of the articles stored in the database to understand its structure.

## Chronica Article

### Article ID

**<u>Attribute name</u>**: article-id

**<u>Description</u>**: ID of the chronica article. Represents when the article was inserted into the database.

* <u>**Field Type**</u>: Integer

### Article Name

<u>**Attribute name**</u>: article-name

**<u>Description</u>**: Name of the Chronica article.

* <u>**Field Type**</u>: String
* <u>**Restraints**</u>: Alphanumeric characters

### Short Description

<u>**Attribute name**</u>: short-desc

**<u>Description</u>**: Description of the Chronica article.

* <u>**Field Type**</u>: String
* <u>**Restraints**</u>: Max 150 characters

### Author
<u>**Attribute name**</u>: author

**<u>Description</u>**: Name of the article's author.

* <u>**Field Type**</u>: String
* <u>**Restraints**</u>: Alphanumeric characters

### Chronicle

### Year Published
<u>**Attribute name**</u>: year-pub

**<u>Description</u>**: Year the article was published.

* <u>**Field Type**</u>: Integer


### Location
<u>**Attribute name**</u>: location

**<u>Description</u>**: Where the article is physically located.

* <u>**Field Type**</u>: String
* <u>**Restraints**</u>: Max 150 characters

