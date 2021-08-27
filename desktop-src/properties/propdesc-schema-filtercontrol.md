---
description: Spécifie le contrôle à utiliser dans le menu filtre d’en-tête.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: filterControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac7424cf281c08f1d8de87686e95a38be3f4f3a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627545"
---
# <a name="filtercontrol"></a>filterControl

Spécifie le contrôle à utiliser dans le menu filtre d’en-tête. Il ne doit y avoir qu’un seul élément [filterControl]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [filterControl]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.

## <a name="syntax"></a>Syntax


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                   | Éléments enfants |
|--------------------------------------------------|----------------|
| [displayInfo](./propdesc-schema-displayinfo.md) | Aucune           |



 

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
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valeur par défaut</td>
<td>Par défaut. Utilise le contrôle par défaut basé sur l' <typeInfo type=&quot;&quot;> attribut. Le type par défaut est &quot; DateTime &quot; et le contrôle par défaut est &quot; Calendar &quot; . Tout autre type ne produit aucun contrôle de filtre spécial.</td>
</tr>
<tr class="even">
<td>Calendrier</td>
<td>Utilise le contrôle calendrier.</td>
</tr>
<tr class="odd">
<td>Rating</td>
<td>Utilise le contrôle d’évaluation 5 étoiles.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
