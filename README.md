XSD 1.1 Validator
=================

Command line XML Schema 1.1 validator written in Java.

This JAR also contains Xerces2 Java with all of its dependencies.

You can run the JAR with the command java -jar xsd11-validator.jar to display usage information:
usage: java hu.unideb.inf.validator.SchemaValidator -if <file> | -iu <url>
       [-sf <file> | -su <url>]
 -if,--instanceFile <file>   read instance from the file specified
 -iu,--instanceUrl <url>     read instance from the URL specified
 -sf,--schemaFile <file>     read schema from the file specified
 -su,--schemaUrl <url>       read schema from the URL specified

You most provide an instance document to be validated using either the -if or the -iu option. (Option -if requires a file path as an argument, option -iu requires an URL.) Similarly, you can specify a schema document using either the -sf or -su option. The -sf and -su options are not mandatory, if they are omitted the value of the xsi:schemaLocation attribute is considered in the instance. The following is an example of how to use the program:
java -jar xsd11-validator.jar -sf schema.xsd -if instance.xml
