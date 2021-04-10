---
description: Définit les lignes de marge dessinées sur la page.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Élément Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210609"
---
# <a name="margin-element"></a>Élément Margin

Définit les lignes de marge dessinées sur la page.

## <a name="definition"></a>Définition

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Éléments parents

Aucun

## <a name="child-elements"></a>Éléments enfants

Aucun..

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Type</th>
<th>Obligatoire</th>
<th>Description</th>
<th>Valeurs possibles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Style</strong></td>
<td>SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></td>
<td>Obligatoire</td>
<td>Spécifie le type de ligne à dessiner.</td>
<td><ul>
<li>Aucun</li>
<li>Unie</li>
<li>Tiret</li>
<li>Points</li>
<li>Tiret-point</li>
<li>Tiret-point-point</li>
<li>Double</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Color</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</td>
<td>Facultatif</td>
<td>Couleur de l’élément.</td>
<td>Valeur RVB hexadécimale. Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} . Par exemple, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>Type</strong></td>
<td>SimpleType <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a></td>
<td>Facultatif</td>
<td>Indique la marge de gauche ou de droite.</td>
<td><ul>
<li>Gauche</li>
<li>Right</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Espacement</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Facultatif</td>
<td>Espacement entre les bords des pages et des marges.</td>
<td>Entier non négatif.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informations sur les éléments



|              |                                                           |
|--------------|-----------------------------------------------------------|
| Type d'élément | ComplexType [**MarginType**](margintype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                |
| Nom du schéma  | Lecteur de journal                                            |



 

 

 




