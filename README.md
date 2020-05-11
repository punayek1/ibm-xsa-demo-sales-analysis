# ibm-xsa-demo-sales-analysis

## coredb module 
This is the base module where cds is used to create table and data loaded from CSV. Roles are created for using the tables from this HDI container to other containers.

## mashup module
This module is developed to show HDI cross container aceess and classic schema access in HDI container.

For usage of another HDI container, steps to be followed are,
1. Create service reference of HDI container.
2. Create hdbgrants file to assign roles of the source container to current container's owner and user.
3. Create synonyms and use synonyms to refer to the objects of source container.

For usage of classic schema objects, steps to be followed are,
1. Create service reference of Classic schema and use that to add reference to HDI container.
2. HDI users are now needs to be assigned to the role that provides DML access to classic schema. Create HDI contianer for that. 
3. Create synonyms and use synonyms to refer to the objects of source classic schema.

## reports module
Reference was created to mashup module and views are reused in this model to create new models.
