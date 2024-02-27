# Custom Coding Keys

Add the ``Codable()`` Macro to your Type to easily customize your CodingKeys with one line of code!

## Overview

Make CodingKey customization easy!

```swift
// Your Code:
@Codable
struct YourType: Codable {
    @CodingKey("your-Custom_naming")
    let firstProperty: String
    @SnakeCase
    let secondProperty: String
    @KebabCase
    let thirdProperty: String
    @CamelCase
    let fourth_property: String
}
```

Generates 

```swift
enum CodingKeys: String, CodingKey {
case firstProperty = "your-Custom_naming"
case secondProperty = "second_property"
case thirdProperty = "third-property"
case fourth_property = "fourthproperty"
}
```


## Topics

### Prerequisites 

- ``Codable()``

### Custom Keys

- ``CodingKey(_:)``
- ``CodingKeyPrefix(_:)``
- ``CodingKeySuffix(_:)``

### NamingConventions

- ``CamelCase()``
- ``FlatCase()``
- ``PascalCase()``
- ``UpperCase()``
- ``SnakeCase()``
- ``CamelSnakeCase()``
- ``PascalSnakeCase()``
- ``ScreamingSnakeCase()``
- ``KebabCase()``
- ``CamelKebabCase()``
- ``PascalKebabCase()``
- ``ScreamingKebabCase()``