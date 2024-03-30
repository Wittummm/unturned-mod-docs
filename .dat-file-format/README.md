---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 📁 Data File Format

Unturned supports two extensions, .dat and .asset, both are identical. ".dat" is usually version 1. ".asset" is usually version 2. Both types supports v1 and v2 but the convention should be followed.&#x20;

### Examples

{% code title="FirstBuilding.dat" %}
```
// Pure version 1
GUID 01de685f-0009-418a-ace8-637ad3063a7f
ID 50000

Type Large
Landmark_Quality Medium
LOD Area
LOD_Bias 0.8
```
{% endcode %}

{% code title="FirstBuilding.asset" fullWidth="false" %}
```
// Pure version 2
"Metadata"
{
    "GUID" "01de685f-0009-418a-ace8-637ad3063a7f"
    "Type" "SDG.Unturned.ObjectAsset, Assembly-CSharp, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null"
    "ID" "50000"
}
"Asset"
{
    "Type" "Large"
    "Landmark_Quality" "Medium"
    "LOD" "Area"
    "LOD_Bias" "0.8"
}
```
{% endcode %}

Metadata and Asset are not required features of version 2.&#x20;

***

(Proofread: NONE)\
[Official Documentation: Asset Definition](https://docs.smartlydressedgames.com/en/stable/assets/asset-definitions.html)\
[Official Documentation: .dat/Data File Format](https://docs.smartlydressedgames.com/en/stable/assets/data-file-format.html)
