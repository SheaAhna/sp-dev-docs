---
title: ActivationDependencies element (FeatureDefinition complexType)
manager: soliver
ms.date: 9/16/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 79b463d1-7b48-a56d-f9b5-0b0a3f91375b
---

# ActivationDependencies element (FeatureDefinition complexType)

(AppHostWebFeatures)

> [!NOTE]
> The string `app` appears as part of or all of some element, attribute, and file names because SharePoint Add-ins were originally called "apps for SharePoint." To ensure backward compatibility, the schemas have not been changed.

## Element information

|   |   |
|---|---|
| **Element type**  | FeatureActivationDependencyDefinitions |
| **Namespace**  | `http://schemas.microsoft.com/sharepoint/` |
| **Schema file**  | apphostwebfeatures.xsd |

## Definition

```XML
    <xs:element name="ActivationDependencies" type="FeatureActivationDependencyDefinitions" minOccurs="0" maxOccurs="1"></xs:element>
```

## Elements and attributes

If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.

### Parent elements

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Element</p></th>
<th align="left"><p>Type</p></th>
<th align="left"><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="feature-element-apphostwebfeatures.md">Feature</a></p></td>
<td align="left"><p><a href="featuredefinition-complextype-apphostwebfeatures.md">FeatureDefinition</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

<br/>

### Child elements

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Element</p></th>
<th align="left"><p>Type</p></th>
<th align="left"><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="activationdependency-element-featureactivationdependencydefinitions-complextypea.md">ActivationDependency</a></p></td>
<td align="left"><p><a href="featureactivationdependencydefinition-complextype-apphostwebfeatures.md">FeatureActivationDependencyDefinition</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

### Attributes

None.

<br/>

<br/>
