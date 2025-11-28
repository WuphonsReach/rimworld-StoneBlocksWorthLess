# Tests

## "Shelf" 

made from (20) stone blocks

| Material  | Bldg Value | $/block | Factor | Beauty |
| --------- | ---------- | ------- | ------ | ------ |
| Granite   | $13.30     | $0.10   | 0.05   | 100%   |
| Limestone | $13.30     | $0.10   | 0.40   | 100%   |
| Marble    | $28.40     | $0.90   | 0.40   | 135%   |
| Sandstone | $16.10     | $0.33   | 0.20   | 110%   |
| Slate     | $29.30     | $0.90   | 0.40   | 110%   |
| Vacstone  | $51.30     | $2.00   | 0.40   | 120%   |

Shelves seem to have a base market value, independent of what they are stuffed with.  That might be $11.30.  $11.30 + 20x0.9 = $29.30 which lines up exactly with slate.  The value is off a bit for the sandstone shelf because $11.30 + 20*.33 = $17.90 not $16.10.  But it's right on the nose for vacstone with $11.30 + 20x2 = $51.30.  The beauty stat seems to play a role as well.

The difference between Granite/Limestone on the "stuffProps/statFactors/MarketValue" indicates that this attribute has zero impact on the market value of the resulting building.

## "Toy Box"

made from (80) stone blocks

| Material  | Bldg Value | $/block | Factor | Beauty |
| --------- | ---------- | ------- | ------ | ------ |
| Granite   | $34.42     | $0.10   | 0.05   | 100%   |
| Limestone | $34.42     | $0.10   | 0.40   | 100%   |
| Marble    | $96.26     | $0.90   | 0.40   | 135%   |
| Sandstone | $48.50     | $0.33   | 0.20   | 110%   |
| Slate     | $98.42     | $0.90   | 0.40   | 110%   |
| Vacstone  | $186.42    | $2.00   | 0.40   | 120%   |

This comparison also indicates that "stuffProps/statFactors/MarketValue" has no impact on the market value of the resulting building.  The base value of the toy box is probably around $26.42 since that's the value for vacstone ($186.42 - 80 x $2) = $26.42.  Which is exactly what Granite and Limestone work out as.  But it doesn't work for Sandstone...

## "walls"

Note that the following values are only accurate to the nearest $0.10 due to only building 10x of each wall segment.

| Material  | Bldg Value | $/block | Factor | Beauty |
| --------- | ---------- | ------- | ------ | ------ |
| Granite   | $3.90      | $0.10   | 0.05   | 100%   |
| Limestone | $3.90      | $0.10   | 0.40   | 100%   |
| Marble    | $7.70      | $0.90   | 0.40   | 135%   |
| Sandstone | $4.60      | $0.33   | 0.20   | 110%   |
| Slate     | $7.90      | $0.90   | 0.40   | 110%   |
| Vacstone  | $13.40     | $2.00   | 0.40   | 120%   |

I wonder if beauty has a negative impact on building value.  Seems weird.  Or there's another variable somewhere.

Adjusting $/block and stuff market value factor:

| Material  | Bldg Value | $/block | Factor | Beauty |
| --------- | ---------- | ------- | ------ | ------ |
| Granite   | $4.90      | $0.30   | 0.05   | 100%   |
| Limestone | $4.90      | $0.30   | 0.10   | 100%   |
| Marble    | $7.70      | $0.90   | 0.40   | 135%   |
| Sandstone | $7.40      | $0.90   | 0.20   | 110%   |
| Slate     | $5.70      | $0.45   | 0.40   | 110%   |
| Vacstone  | $13.40     | $2.00   | 0.40   | 120%   |

This comparison also indicates that "stuffProps/statFactors/MarketValue" has no impact on the market value of the resulting wall segment.

The $/block seems to be the primary driver in the value of a wall segment.  A wall segment seems to have a base value around $3.30.  Adjusting the "statBases/MarketValue" on the "Wall" thingDef seems to break the calculation or I haven't figured out what the base value needs to be to preserve the value of gold walls.  