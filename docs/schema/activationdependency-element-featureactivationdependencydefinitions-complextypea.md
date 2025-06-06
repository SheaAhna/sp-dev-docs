---
title: ActivationDependency element (FeatureActivationDependencyDefinitions complexType)
description: Discusses the definition, elements and attributes for ActivationDependency element (FeatureActivationDependencyDefinitions complexType).
manager: soliver
ms.date: 06/14/2022
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f022cb63-3d73-bc27-dc13-e1d172b6082d
---

# ActivationDependency element (FeatureActivationDependencyDefinitions complexType)

(AppHostWebFeatures)

> [!NOTE]
> The string `app` appears as part of or all of some element, attribute, and file names because SharePoint Add-ins were originally called "apps for SharePoint." To ensure backward compatibility, the schemas have not been changed.

## Element information

|Information|Location|
|---|---|
| **Element type**  | FeatureActivationDependencyDefinition |
| **Namespace**  | `http://schemas.microsoft.com/sharepoint/` |
| **Schema file**  | apphostwebfeatures.xsd |

## Definition

```XML
    <xs:element name="ActivationDependency" type="FeatureActivationDependencyDefinition" minOccurs="0" maxOccurs="unbounded"></xs:element>
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
<td align="left"><p><a href="activationdependencies-element-featuredefinition-complextypeapphostwebfeatures.md">ActivationDependencies</a></p></td>
<td align="left"><p><a href="featureactivationdependencydefinitions-complextype-apphostwebfeatures.md">FeatureActivationDependencyDefinitions</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Child elements

None.



### Attributes

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="10%" />
<col width="30%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Attribute</p></th>
<th align="left"><p>Type</p></th>
<th align="left"><p>Required</p></th>
<th align="left"><p>Description</p></th>
<th align="left"><p>Possible values</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>FeatureDescription</p></td>
<td align="left"><p>xs:string</p></td>
<td align="left"><p>optional</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Values of the xs:string type.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FeatureId</p></td>
<td align="left"><p>UniqueIdentifier</p></td>
<td align="left"><p>required</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Values of the UniqueIdentifier type.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FeatureTitle</p></td>
<td align="left"><p>xs:string</p></td>
<td align="left"><p>optional</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Values of the xs:string type.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MinimumVersion</p></td>
<td align="left"><p><a href="featureversion-simpletype-apphostwebfeatures.md">FeatureVersion</a></p></td>
<td align="left"><p>optional</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Values of the FeatureVersion type.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SolutionId</p></td>
<td align="left"><p>UniqueIdentifier</p></td>
<td align="left"><p>optional</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Values of the UniqueIdentifier type.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SolutionName</p></td>
<td align="left"><p>xs:string</p></td>
<td align="left"><p>optional</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Values of the xs:string type.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SolutionTitle</p></td>
<td align="left"><p>xs:string</p></td>
<td align="left"><p>optional</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Values of the xs:string type.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SolutionUrl</p></td>
<td align="left"><p>xs:string</p></td>
<td align="left"><p>optional</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Values of the xs:string type.</p></td>
</tr>
</tbody>
</table>
