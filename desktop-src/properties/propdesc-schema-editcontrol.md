---
description: Spécifie le contrôle à utiliser lors de la modification de la propriété.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdb47a3866c156ff10dba8eed4584f814793b863e8f615ae5e1a10b8d687ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118055989"
---
# <a name="editcontrol"></a>editControl

Spécifie le contrôle à utiliser lors de la modification de la propriété. Il ne doit y avoir qu’un seul élément [editControl]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [editControl]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

Si <typeInfo isInnate="true"> , cet élément est ignoré, car une propriété innée ne peut pas être modifiée.

## <a name="syntax"></a>Syntaxe


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                   | Éléments enfants |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Aucun           |



 

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>contrôle</td>
<td>Public. Facultatif. La valeur par défaut est &quot; default &quot; . Les valeurs valides sont les suivantes. 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Par défaut</td>
<td>Par défaut. Utilise le contrôle par défaut basé sur l' <typeInfo type=&quot;&quot;> attribut. Les types par défaut sont répertoriés ci-dessous. Tout autre type entraîne l’utilisation du &quot; contrôle de texte &quot; . 
<table>
<thead>
<tr class="header">
<th>Type</th>
<th>Contrôler</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Texte</td>
</tr>
<tr class="even">
<td>Chaîne (valeurs multiples)</td>
<td>MultiValueText</td>
</tr>
<tr class="odd">
<td>DateTime</td>
<td>Calendrier</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Calendrier</td>
<td>Utilise le contrôle calendrier.</td>
</tr>
<tr class="odd">
<td>CheckboxDropList</td>
<td>Utilise le contrôle de liste avec des cases à cocher.</td>
</tr>
<tr class="even">
<td>Roulant</td>
<td>Utilise le contrôle de liste déroulante.</td>
</tr>
<tr class="odd">
<td>MultiLineText</td>
<td>Utilise le contrôle d’édition de texte sur plusieurs lignes.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Utilise le contrôle d’édition de texte à valeurs multiples.</td>
</tr>
<tr class="odd">
<td>Rating</td>
<td>Utilise le contrôle d’évaluation 5 étoiles.</td>
</tr>
<tr class="even">
<td>Texte</td>
<td>Utilise le contrôle d’édition de texte.</td>
</tr>
<tr class="odd">
<td>IconList</td>
<td><strong>Windows 7 et versions ultérieures.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
