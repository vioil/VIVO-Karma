# positions.txt

## Add Column

## Add Node/Literal

## PyTransforms
#### _position_uri_
From column: _position_type_
``` python
return "http://vivo.columbia.edu/individual/position-"+getValue("UID")+"_"+getValue("org_ID")+"_"+getValue("position_type").replace(" ","_")

```

#### _person_uri_
From column: _UID_
``` python
return "http://vivo.columbia.edu/individual/nperson-"+getValue("UID")
```

#### _org_ID_uri_
From column: _org_ID_
``` python
return "http://vivo.columbia.edu/individual/n"+getValue("org_ID")
```


## Selections

## Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _UID_ | `vlocal:UID` | `vivo:FacultyMember1`|
| _job_title_ | `vivo:hrJobTitle` | `vivo:FacultyMember1`|
| _org_ID_ | `vlocal:DepartmentID` | `vivo:AcademicDepartment1`|
| _org_ID_uri_ | `uri` | `vivo:AcademicDepartment1`|
| _org_name_ | `rdfs:label` | `vivo:AcademicDepartment1`|
| _person_uri_ | `uri` | `vivo:FacultyMember1`|
| _position_type_ | `rdfs:label` | `vivo:FacultyPosition1`|
| _position_uri_ | `uri` | `vivo:FacultyPosition1`|


## Links
| From | Property | To |
|  --- | -------- | ---|
| `vivo:FacultyPosition1` | `vivo:relates` | `vivo:AcademicDepartment1`|
| `vivo:FacultyPosition1` | `vivo:relates` | `vivo:FacultyMember1`|
