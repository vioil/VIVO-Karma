# positions - positions.tsv

## Add Column

## Add Node/Literal

## PyTransforms
#### _position_uri_
From column: _position_type_
``` python
return "http://vivo.northwestern/position/n"+getValue("UID")+"_"+getValue("org_ID")+"_"+getValue("position_type").replace(" ","_")
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _UID_ | `uri` | `vivo:FacultyMember1`|
| _job_title_ | `vivo:hrJobTitle` | `vivo:FacultyMember1`|
| _org_ID_ | `uri` | `foaf:Organization1`|
| _org_name_ | `rdfs:label` | `foaf:Organization1`|
| _position_type_ | `rdfs:label` | `vivo:Position1`|
| _position_uri_ | `uri` | `vivo:Position1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `vivo:Position1` | `vivo:relates` | `vivo:FacultyMember1`|
| `vivo:Position1` | `vivo:relates` | `foaf:Organization1`|
