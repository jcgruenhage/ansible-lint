# ajv errors

```json
[
  {
    "instancePath": "/releases/1.0.0/release_date",
    "keyword": "pattern",
    "message": "must match pattern \"\\d\\d\\d\\d-\\d\\d-\\d\\d\"",
    "params": {
      "pattern": "\\d\\d\\d\\d-\\d\\d-\\d\\d"
    },
    "schemaPath": "#/$defs/release/properties/release_date/pattern"
  }
]
```

# check-jsonschema

stdout:

```json
{
  "status": "fail",
  "errors": [
    {
      "filename": "negative_test/changelogs/invalid-date/changelog.yml",
      "path": "$.releases.1.0.0.release_date",
      "message": "'01-01-2020' is not a 'date'",
      "has_sub_errors": false
    },
    {
      "filename": "negative_test/changelogs/invalid-date/changelog.yml",
      "path": "$.releases.1.0.0.release_date",
      "message": "'01-01-2020' does not match '\\\\d\\\\d\\\\d\\\\d-\\\\d\\\\d-\\\\d\\\\d'",
      "has_sub_errors": false
    }
  ],
  "parse_errors": []
}
```
