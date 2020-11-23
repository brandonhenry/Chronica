# Updating database in Drupal 8
The following sections of code will need to be placed inside of the `hook_update_N()` function. All of this information is from the Drupal documentation located at https://www.drupal.org/docs/drupal-apis/update-api/updating-database-schema-andor-data-in-drupal-8

## Add a new table
This is an example of how to add a new table to the database
```php
 $spec = [
    'description' => 'My description',
    'fields' => [
      'myfield1' => [
        'description' => 'Myfield1 description.',
        'type' => 'varchar',
        'length' => 255,
        'not null' => TRUE,
        'default' => '',
      ],
      'myfield2' => [
        'description' => 'Myfield2 description',
        'type' => 'text',
        'not null' => TRUE,
      ],
    ],
    'primary key' => ['myfield1'],
  ]; 
 $schema = Database::getConnection()->schema();
 $schema->createTable('mytable2', $spec);
```
## Add a new column
This is an example of how to add a new column to an existing table.
```php
  $spec = [
    'type' => 'varchar',
    'description' => "New Col",
    'length' => 20,
    'not null' => FALSE,
  ]; 
 $schema = Database::getConnection()->schema();
 $schema->addField('mytable1', 'newcol', $spec);
```
## Add primary keys or indexes to a table
This is an example of how to add primary keys or indexes to existing tables in the database.
```php
$spec = [
  // Example partial specification for a table:
  'fields' => [
    'myfield1' => [
      'description' => 'An example field',
      'type' => 'varchar',
      'length' => 32,
      'not null' => TRUE,
      'default' => '',
    ],
  ],
  'indexes' => [
    'myfield1_normal_index' => ['myfield1'],
  ],
 ];
 $fields = ['myfield1'];
 $schema = Database::getConnection()->schema();
 // A normal index.
 $schema->addIndex('mytable', 'myfield1_normal_index', $fields, $spec);

 // A primary key.
 $schema->addPrimaryKey('mytable', $fields);
 // A unique key.
 $schema->addUniqueKey('mytable', 'myfield1_unique_key', $fields);
```

## Updating the data within a table
This is how you would update the data within a table using an SQL query
```php
$schema = Database::getConnection()->query(  [your query goes here] );
```
