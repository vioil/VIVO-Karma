# person - person.tsv

## Add Column

## Add Node/Literal

## PyTransforms
#### _email_uri_
From column: _Email_
``` python
return "email"+getValue("UID")
```

#### _vcard_uri_
From column: _UID_
``` python
return "vcard"+getValue("UID")
```

#### _date_hiredURI_
From column: _date_hired_
``` python
return "http://vivo.columbia.edu/individual/" + getValue("date_hired")
```

#### _date_terminatedURI_
From column: _date_terminated_
``` python
return "http://vivo.columbia.edu/individual/" + getValue("date_terminated")
```

#### _name_URI_
From column: _MidName_
``` python
return "name"+getValue("UID")
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _Email_ | `vcard:email` | `vcard:Email1`|
| _FirstName_ | `vcard:givenName` | `vcard:Name1`|
| _FullName_ | `rdfs:label` | `vivo:FacultyMember1`|
| _LastName_ | `vcard:familyName` | `vcard:Name1`|
| _MidName_ | `vivo:middleName` | `vcard:Name1`|
| _NETID_ | `vlocal:netID` | `vivo:FacultyMember1`|
| _Title_ | `vivo:hrJobTitle` | `vivo:FacultyMember1`|
| _UID_ | `uri` | `vivo:FacultyMember1`|
| _date_hired_ | `vivo:dateTime` | `vivo:DateTimeValue1`|
| _date_hiredURI_ | `uri` | `vivo:DateTimeValue1`|
| _date_terminated_ | `vivo:dateTime` | `vivo:DateTimeValue2`|
| _date_terminatedURI_ | `uri` | `vivo:DateTimeValue2`|
| _email_uri_ | `uri` | `vcard:Email1`|
| _name_URI_ | `uri` | `vcard:Name1`|
| _vcard_uri_ | `uri` | `vcard:Individual1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `vcard:Individual1` | `vcard:hasEmail` | `vcard:Email1`|
| `vcard:Individual1` | `vcard:hasName` | `vcard:Name1`|
| `vivo:DateTimeValue1` | `vivo:dateTimePrecision` | `xsd:http://vivoweb.org/ontology/core#yearPrecision`|
| `vivo:DateTimeValue2` | `vivo:dateTimePrecision` | `xsd:http://vivoweb.org/ontology/core#yearPrecision`|
| `vivo:FacultyMember1` | `vivo:start` | `vivo:DateTimeValue1`|
| `vivo:FacultyMember1` | `vivo:end` | `vivo:DateTimeValue2`|
| `vivo:FacultyMember1` | `obo:ARG_2000028` | `vcard:Individual1`|
