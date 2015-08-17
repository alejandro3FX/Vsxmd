# Vsxmd

## AssemblyUnit

##### Namespace

Vsxmd.Units

##### Summary

Assembly unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `AssemblyUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The assembly XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `assembly`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

## BaseUnit

##### Namespace

Vsxmd.Units

##### Summary

The base unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `BaseUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The XML element. |
| elementName | System.String | The expected XML element name. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML `element` name not matches the expected `elementName`. |

### Element `property`

##### Summary

Gets the XML element.

### ElementContent `property`

##### Summary

Gets the Markdown content representing the element.

### GetAttribute `method`

##### Summary

Returns the `XAttribute` value of this `XElement` that has the specified `name`.

##### Returns

An `XAttribute` value that has the specified `name`; `null` if there is no attribute with the specified `name`.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | System.Xml.Linq.XName | The `XName` of the `XAttribute` to get. |

### GetChild `method`

##### Summary

Gets the first (in document order) child element with the specified `name`.

##### Returns

A `XName` that matches the specified `name`, or `null`.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | System.Xml.Linq.XName | The `XName` to match. |

### GetChildren `method`

##### Summary

Returns a collection of the child elements of this element or document, in document order. Only elements that have a matching `XName` are included in the collection.

##### Returns

An ``IEnumerable`1`` of `XElement` containing the children that have a matching `XName`, in document order.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | System.Xml.Linq.XName | The `XName` to match. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

## Converter

##### Namespace

Vsxmd

##### Summary

Convert from XML docuement to Markdown syntax.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `Converter` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| xmlPath | System.String | The XML document path. |

### ToMarkdown `method`

##### Summary

Convert to Markdown syntax.

##### Returns

The generated Markdown content.

##### Parameters

This method has no parameters.

## ExampleUnit

##### Namespace

Vsxmd.Units

##### Summary

Example unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `ExampleUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The example XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `example`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the example XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The example XML element. |

## ExceptionUnit

##### Namespace

Vsxmd.Units

##### Summary

Exception unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `ExceptionUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The exception XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `exception`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the exception XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement} | The exception XML element list. |

## Extensions

##### Namespace

Vsxmd.Units

##### Summary

Extensions helper.

### AsCode `method`

##### Summary

Wrap the `code` into Markdown backtick safely.

The backtick characters inside the `code` reverse as it is.

##### Returns

The Markdwon code span.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| code | System.String | The code span. |

##### Remarks

Reference: http://meta.stackexchange.com/questions/55437/how-can-the-backtick-character-be-included-in-code

### Escape `method`

##### Summary

Escape the content to keep it raw in Markdown syntax.

##### Returns

The escaped content.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| content | System.String | The content. |

### GetParamTypes `method`

##### Summary

Gets the method parameter type names from the member unit `name`.

##### Returns

The method parameter type name list.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | System.String | The member unit name. |

### Join `method`

##### Summary

Concatenates the `value`s with the `separator`.

##### Returns

The concatenated string.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| value | System.Collections.Generic.IEnumerable{System.String} | The string values. |
| separator | System.String | The separator. |

### NthLastOrDefault\`\`1 `method`

##### Summary

Gets the n-th last element from the `source`.

##### Returns

The target element, default(`TSource`) if not found.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| source | System.Collections.Generic.IEnumerable{\`\`0} | The source enumerable. |
| index | System.Int32 | The index for the n-th last. |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| TSource | The type of the elements of `source`. |

### TakeAllButLast\`\`1 `method`

##### Summary

Take all element except the last `count`.

##### Returns

The generated enumerable.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| source | System.Collections.Generic.IEnumerable{\`\`0} | The source enumerable. |
| count | System.Int32 | The number to except. |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| TSource | The type of the elements of `source`. |

### ToMarkdownText `method`

##### Summary

Convert the inline XML nodes to Markdown text. For example, it works for `summary` and `returns` elements.

##### Returns

The generated Markdwon content.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The XML element. |

##### Example

This method converts the following `summary` element

```
<summary>The <paramref name="element" /> value is <value>null</value>, it throws <c>ArgumentException</c>. For more, see <see cref="M:Vsxmd.Units.Extensions.ToMarkdownText(System.Xml.Linq.XElement)" />.</summary>
```

To the below Markdown content.

```
The `element` value is `null`, it throws `ArgumentException`. For more, see `ToMarkdownText`.
```

### ToNameSegments `method`

##### Summary

Split the member unit `name` to segments.

##### Returns

The name segments.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | System.String | The member unit name. |

##### Example

Split `M:Vsxmd.Converter.#ctor(System.String)` to `["Vsxmd", "Converter", "#ctor"]` string list.

## IUnit

##### Namespace

Vsxmd.Units

##### Summary

`IUnit` is wrapper to handle XML elements.

### ToMarkdown `method`

##### Summary

Represent the XML element content as Markdown syntax.

##### Returns

The generated Markdown content.

##### Parameters

This method has no parameters.

## MemberKind

##### Namespace

Vsxmd.Units.MemberUnit

### Constants `constants`

##### Summary

Constants

### Constructor `constants`

##### Summary

Constructor.

### Method `constants`

##### Summary

Method.

### NotSupported `constants`

##### Summary

Not supported member kind.

### Property `constants`

##### Summary

Property.

### Type `constants`

##### Summary

Type.

## MemberUnit

##### Namespace

Vsxmd.Units

##### Summary

Member unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `MemberUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The member XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `member`. |

### Comparer `property`

##### Summary

Gets the member unit comparer.

### IsSupported `property`

##### Summary

Gets if this member type is supported.

### TypeName `property`

##### Summary

Gets the type name.

##### Example

`Vsxmd.Program`, `Vsxmd.Units.TypeUnit`.

### ComplementType `method`

##### Summary

Complement a type unit if the member unit `group` does not have one. One member unit group has the same `TypeName`.

##### Returns

The complemented member unit group.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| group | System.Collections.Generic.IEnumerable{Vsxmd.Units.MemberUnit} | The member unit group. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

## MemberUnitComparer

##### Namespace

Vsxmd.Units.MemberUnit

### Compare `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

## ParamUnit

##### Namespace

Vsxmd.Units

##### Summary

Param unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `ParamUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The param XML element. |
| paramType | System.String | The paramter type corresponding to the param XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `param`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the param XML element to Markdown safely.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement} | The param XML element list. |
| paramTypes | System.Collections.Generic.IEnumerable{System.String} | The paramater type names. |
| isParameterKind | System.Boolean | Indicates if the member kind have parameters, which is constructor or methods. |

##### Remarks

When the parameter (a.k.a `elements`) list is empty:

If parent element kind is constructor or method, it returns a hint about "no parameters".

If parent element kind is not the value mentioned above, it returns an empty string.

## PermissionUnit

##### Namespace

Vsxmd.Units

##### Summary

Permission unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `PermissionUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The permission XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `permission`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the permission XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement} | The permission XML element list. |

## Program

##### Namespace

Vsxmd

##### Summary

Program entry.

##### Permissions

| Name | Description |
| ---- | ----------- |
| System.Security.PermissionSet | Vsxmd provides no program APIs. |

##### Remarks

Usage syntax: `Vsxmd.exe <input-XML-path> [output-Markdown-path]`

The `input-XML-path` argument is required. It references to the VS generated XML documentation file.

The `output-Markdown-path` argument is optional. It indicates the file path for the Markdown output file. When not specific, it will be a `.md` file with same file name as the XML documentation file, path at the XML documentation folder.

### Main `method`

##### Summary

Program main function entry.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| args | System.String[] | Program arguments. |

##### See Also

- `Vsxmd.Program`

## RemarksUnit

##### Namespace

Vsxmd.Units

##### Summary

Remarks unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `RemarksUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The remarks XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `remarks`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the remarks XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The remarks XML element. |

## ReturnsUnit

##### Namespace

Vsxmd.Units

##### Summary

Returns unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `ReturnsUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The returns XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `returns`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the returns XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The returns XML element. |

## SeealsoUnit

##### Namespace

Vsxmd.Units

##### Summary

Seealso unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `SeealsoUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The seealso XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `seealso`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the seealso XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement} | The seealso XML element list. |

## SummaryUnit

##### Namespace

Vsxmd.Units

##### Summary

Summary unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `SummaryUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The summary XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `summary`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the summary XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The summary XML element. |

## Test

##### Namespace

Vsxmd.Program

### TestBacktickInSummary `method`

##### Summary

Test backtick characters in summary comment.

See \`should not inside code block\`.

See `` `backtick inside code block` ``

See \``code block inside backtick`\`

##### Returns

Nothing.

##### Parameters

This method has no parameters.

### TestGenericException `method`

##### Summary

Test generic exception type.

##### Returns

Nothing.

##### Parameters

This method has no parameters.

##### Exceptions

| Name | Description |
| ---- | ----------- |
| Vsxmd.Program.Test.TestGenericParameter\`\`2(System.Linq.Expressions.Expression{System.Func{\`\`0,\`\`1,System.String}}) | Just for test. |

### TestGenericParameter\`\`2 `method`

##### Summary

Test generic parameter type.

##### Returns

Nothing.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| expression | System.Linq.Expressions.Expression{System.Func{\`\`0,\`\`1,System.String}} | The linq expression. |

##### Generic Types

| Name | Description |
| ---- | ----------- |
| T1 | Generic type 1. |
| T2 | Generic type 2. |

### TestGenericPermission `method`

##### Summary

Test generic exception type.

##### Returns

Nothing.

##### Parameters

This method has no parameters.

##### Permissions

| Name | Description |
| ---- | ----------- |
| Vsxmd.Program.Test.TestGenericParameter\`\`2(System.Linq.Expressions.Expression{System.Func{\`\`0,\`\`1,System.String}}) | Just for test. |

### TestGenericRefence `method`

##### Summary

Test generic reference type.

See ```TestGenericParameter``2```.

##### Returns

Nothing.

##### Parameters

This method has no parameters.

## TypeparamUnit

##### Namespace

Vsxmd.Units

##### Summary

Typeparam unit.

### #ctor `constructor`

##### Summary

Initializes a new instance of the `TypeparamUnit` class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| element | System.Xml.Linq.XElement | The typeparam XML element. |

##### Exceptions

| Name | Description |
| ---- | ----------- |
| System.ArgumentException | Throw if XML element name is not `typeparam`. |

### ToMarkdown `method`

##### Summary

*Inherit from parent.*

##### Parameters

This method has no parameters.

### ToMarkdown `method`

##### Summary

Convert the param XML element to Markdown safely. If elemnt is `null`, return empty string.

##### Returns

The generated Markdown.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| elements | System.Collections.Generic.IEnumerable{System.Xml.Linq.XElement} | The param XML element list. |