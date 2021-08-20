---
description: Contient les informations qui décrivent le composant vertical des lignes du papier à lettres utilisé par la note du journal. Utilisé, par exemple, lorsque la note contient des lignes de grille.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Élément vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f9f074d144a9910b16823d5c9a6e2793e59472bd0f2b60fcd72da1d6a0e4d92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675565"
---
# <a name="vertical-element"></a>Élément vertical

Contient les informations qui décrivent le composant vertical des lignes du papier à lettres utilisé par la note du journal. Utilisé, par exemple, lorsque la note contient des lignes de grille.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun.

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
<td><strong>Couleur</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</td>
<td>Facultatif</td>
<td>Couleur de l’élément.</td>
<td>Valeur RVB hexadécimale. Correspond à l’expression régulière suivante : # [0-9A-zA-Z] {6} . Par exemple, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Facultatif</td>
<td>Espacement avant l’élément.</td>
<td>Entier non négatif.</td>
</tr>
<tr class="even">
<td><strong>SpacingBetween</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Facultatif</td>
<td>Espacement entre cet élément et les éléments environnants.</td>
<td>Entier non négatif.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                         |
|--------------|---------------------------------------------------------------|
| Type d'élément | ComplexType [**VerticalType**](verticaltype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                    |
| Nom du schéma  | Lecteur de journal                                                |



 

 

 




