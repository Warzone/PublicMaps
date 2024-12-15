# Warzone Includes

This folder contains a collection of reusable XML files adopted for use across Warzone.

## Usage

Please see the [Includes section](https://pgm.dev/docs/modules/general/preprocessing#includes) covered in PGM Documentation.

To use an include for a map, an include statement must be added to its XML:

```xml
<map>
    ...
    <include id="include-name-goes-here"/>
    ...
</map>
```

Additionally, some includes may offer customizable settings as [constants](https://pgm.dev/docs/modules/general/main/#constants) that can be overridden by individual maps' XML.

For this example, we will be using `void-death` include to show how you can override a constant:

```xml
<map>
    <include id="void-death">
    ...
    <constants> <!-- the <constants> part is optional -->
        <constant id="void-plane">20</constant> <!-- the original value was -5, the new value is now 20 for this map -->
    </constants>
</map>
```

## Contributing

Like normal map files, includes must follow these requirements:

-   All includes must have valid XML syntax. The map protocol must be `1.4.2`.
-   Includes must be extensively tested as they have the potential to affect countless maps.