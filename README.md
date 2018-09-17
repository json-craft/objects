Person.json

```javascript
{
    "name": "string",
    "age": "int8",
    "address": "Address",
    "contactDetails": "ContactDetail[]",
    "friends": "int64[]",
}
```

Address.json

```javascript
{
    "street": {
        "@type": "string",
        "@validation": "required|unique|min:3|max:40",
        "@description": "Street without house number"
    },
    "number": "int16"
    "zip": "number",
    "country": "Country"
}
```

Country.json

```javascript
{
    "@type": "enum",
    "@values": ["DE", "EN" ]
}
```

ContactDetail.json

```javascript
{
    "type": "ContactDetailType"
}
```

Phone.json

```javascript
{
    "@extends": "ContactDetail",
    "number": "string"
}
```

Mail.json

```javascript
{
    "@extends": "ContactDetail",
    "mail": {
        "@type": "string",
        "@validation": "required|mail"
    }
}
```
