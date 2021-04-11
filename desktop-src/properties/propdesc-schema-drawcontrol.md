---
description: Spécifie le contrôle à utiliser lors de l’affichage de la propriété.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034284"
---
# <a name="drawcontrol"></a>drawControl

Spécifie le contrôle à utiliser lors de l’affichage de la propriété. Il ne doit y avoir qu’un seul élément [drawControl]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [drawControl]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

Cette forme du contrôle n’autorise pas la modification de propriété.

## <a name="syntax"></a>Syntaxe


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
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
<td>Public. Optionnel. La valeur par défaut est &quot; default &quot; . Les valeurs valides sont les suivantes. 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Default</td>
<td>Par défaut. Utilise le contrôle par défaut basé sur l' <typeInfo type=&quot;&quot;> attribut. Le type par défaut est &quot; String &quot; (valeur multiple) et le contrôle par défaut est &quot; MultiValueText &quot; . Tout autre type entraîne l’utilisation du &quot; &quot; contrôle StaticText.</td>
</tr>
<tr class="even">
<td>MultiLineText</td>
<td>Utilise le contrôle de texte sur plusieurs lignes.</td>
</tr>
<tr class="odd">
<td>MultiValueText</td>
<td>Utilise le contrôle de texte à valeurs multiples.</td>
</tr>
<tr class="even">
<td>PercentBar</td>
<td>Utilise le contrôle de barre de pourcentage.</td>
</tr>
<tr class="odd">
<td>Barre de progression</td>
<td>Utilise le contrôle de barre de progression.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Utilise le contrôle d’évaluation 5 étoiles.</td>
</tr>
<tr class="odd">
<td>StaticText</td>
<td>Utilise <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription :: FormatForDisplay</strong></a> pour afficher la valeur de la propriété.</td>
</tr>
<tr class="even">
<td>IconList</td>
<td><strong>Windows 7 et versions ultérieures.</strong> Énumération d’icônes.</td>
</tr>
<tr class="odd">
<td>BooleanCheckMark</td>
<td><strong>Windows 7 et versions ultérieures.</strong></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
