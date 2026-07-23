# Table normalization bug?

## Footnotes in a table

another change

| Country   | Availability                   |
| --------- | ------------------------------ |
| Albania   | Available<sup>\[^1]\[^2]</sup> |
| Algeria   | Available<sup>\[^1]\[^2]</sup> |
| Australia | Available<sup>\[^1]\[^2]</sup> |
| Austria   | Available<sup>\[^1]\[^2]</sup> |


| Country | Availability |
| --- | --- |
| Albania | Available[^1][^2] |
| Algeria | Available[^1][^2] |
| Australia | Available[^1][^2] |

[^1]: First footnote.
[^2]: Second footnote.
