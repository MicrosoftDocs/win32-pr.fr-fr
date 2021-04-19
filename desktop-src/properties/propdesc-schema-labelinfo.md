---
description: Spécifie la façon dont les étiquettes de la propriété sont affichées.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527819"
---
# <a name="labelinfo"></a>labelInfo

Spécifie la façon dont les étiquettes de la propriété sont affichées. Il ne doit y avoir qu’un seul élément [labelInfo]() pour chaque élément [PropertyDescription](./propdesc-schema-propertydescription.md) .

S’il y a plusieurs éléments, le dernier est utilisé. Si aucun élément [labelInfo]() n’est fourni, l’étiquette de la propriété n’est pas affichée ; Toutefois, il s’agit généralement d’un défaut.

## <a name="syntax"></a>Syntaxe


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                   | Éléments enfants |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Aucun           |



 

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
<td>label</td>
<td>Public. Optionnel. Étiquette telle qu’elle s’affiche dans l’interface utilisateur (par exemple, l’étiquette de la colonne Détails ou le volet de visualisation). La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte. Utilisez la chaîne d’affichage indirecte, car elle peut être localisée. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription :: GetDisplayName</strong></a> retourne le nom complet résolu.</td>
</tr>
<tr class="even">
<td>sortDescription</td>
<td>Optionnel. Spécifie les chaînes proposées en tant qu’options de tri. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription :: GetSortDescription</strong></a> retourne cette description de tri. Les valeurs suivantes fournissent les chaînes d’interface utilisateur correspondantes.
<ul>
<li>Général : tri en cours de tri en cours &quot; &quot;  /  &quot;&quot;</li>
<li>AToZ : &quot; A sur &quot;  /  &quot; Z supérieur en haut&quot;</li>
<li>LowestHighest : &quot; du plus petit au &quot;  /  &quot; plus haut en haut&quot;</li>
<li>OldestNewest : &quot; du plus ancien au plus &quot;  /  &quot; récent en haut&quot;</li>
<li>SmallestLargest : &quot; le plus petit au &quot;  /  &quot; plus grand en haut&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>invitationText</td>
<td>Optionnel. Texte de la chaîne d’aide affiché en tant qu’instruction à l’utilisateur pour le contrôle ou l’info-bulle (par exemple, entrez le nom de l' &quot; auteur &quot; ). La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte. Utilisez la chaîne d’affichage indirecte, car elle peut être localisée. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription :: GetEditInvitation</strong></a> retourne le texte d’invitation résolu.</td>
</tr>
<tr class="even">
<td>hideLabel</td>
<td>Optionnel. La valeur par défaut est &quot;false&quot;. Indique si l’étiquette est masquée.</td>
</tr>
</tbody>
</table>



 

 

 
