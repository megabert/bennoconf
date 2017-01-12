# bennoconf

Create XML Configuration for "Benno Mailarchiv" (www.benno-mailarchiv.de, german site)

This script creates a benno.xml configuration based on the few needed
parameters. It is a base for create more complex configurations with more 
Tenants.

## Details

It creates a configuration file /etc/benno/bennoconf/bennoconf.json if
it does not exist which can be adapted once it's created.

## Requirements

PHP, Version >= 5.6 (Lower version probably running without problems)

PHP-Libraries: xml, json

## State

Code is *Usable*

## Example usage


Create the basic Object:
```
$bennoXML = new BennoXML($C);
```

Add a Tenant/Client:
```
$bennoXML->addTenant("MyCompany",["meinedomain.de","mydomain.com"]);
```

Add another Tenant/Client:
```
$bennoXML->addTenant("AnotherCompany",["meinezweitedomain.de","bla.com"]);
```

Print the XML-Config to Terminal:
```
$bennoXML->dump();
```
