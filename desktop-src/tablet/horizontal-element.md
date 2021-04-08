---
description: Contient des informations de mise en forme pour les lignes horizontales utilisées pour le papier à lettres dans une note du journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Élément horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751893"
---
# <a name="horizontal-element"></a>Élément horizontal

Contient des informations de mise en forme pour les lignes horizontales utilisées pour le papier à lettres dans une note du journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Éléments enfants

Aucun

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



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| Type d'élément | [**ComplexType HorizontalType**](horizontaltype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                        |
| Nom du schéma  | Lecteur de journal                                                    |



 

 

 




