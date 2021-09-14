---
description: non pris en charge dans Windows 7 et versions ultérieures. Spécifie le contrôle à utiliser dans le générateur de requêtes.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3652a46d403bc258226de5a48f34ae16960ff517
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231563"
---
# <a name="querycontrol"></a>queryControl

non pris en charge dans Windows 7 et versions ultérieures. Spécifie le contrôle à utiliser dans le générateur de requêtes. Il ne doit y avoir qu’un seul élément [queryControl]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [queryControl]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax"></a>Syntaxe


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                   | Éléments enfants |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | None           |



 

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col  />
<col  />
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
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Default</td>
<td>Par défaut. Utilise le contrôle par défaut basé sur l' <typeInfo type=&quot;&quot;> attribut. Les types par défaut sont répertoriés ci-dessous. Tout autre type entraîne l’utilisation du &quot; contrôle de texte &quot; . 
<table>
<thead>
<tr class="header">
<th>ConditionType</th>
<th>Control</th>
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
<td>Nombre ou taille</td>
<td>NumericText</td>
</tr>
<tr class="even">
<td>Nombre ou taille (enum)</td>
<td>List</td>
</tr>
<tr class="odd">
<td>DateTime</td>
<td>Calendrier</td>
</tr>
<tr class="even">
<td>Booléen</td>
<td>Booléen</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Booléen</td>
<td>Utilise le contrôle booléen.</td>
</tr>
<tr class="odd">
<td>Calendrier</td>
<td>Utilise le contrôle de calendrier déroulant.</td>
</tr>
<tr class="even">
<td>CheckboxDropList</td>
<td>Utilise le contrôle de liste avec des cases à cocher.</td>
</tr>
<tr class="odd">
<td>Roulant</td>
<td>Utilise le contrôle de liste déroulante.</td>
</tr>
<tr class="even">
<td>MultiValueText</td>
<td>Utilise le contrôle d’édition de texte à valeurs multiples.</td>
</tr>
<tr class="odd">
<td>NumericText</td>
<td>Utilise le contrôle d’édition de texte numérique.</td>
</tr>
<tr class="even">
<td>Rating</td>
<td>Utilise le contrôle d’évaluation 5 étoiles.</td>
</tr>
<tr class="odd">
<td>Texte</td>
<td>Utilise le contrôle d’édition de texte.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
