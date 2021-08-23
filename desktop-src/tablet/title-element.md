---
description: Contient des informations de titre sur la note du journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Titre, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52648e3f5783e706c91cf42a041e3a2e01952427ea4f66381405789827aa2eee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589319"
---
# <a name="title-element"></a>Titre, élément

Contient des informations de titre sur la note du journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**Stationery**](stationery-element.md)

## <a name="child-elements"></a>Éléments enfants

[**Partie titlearea**](titlearea-element.md)

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
<td><strong>xs:string</strong></td>
<td>Obligatoire</td>
<td>Spécifie le type de bordure entourant le titre de la note.</td>
<td><ul>
<li>Aucun</li>
<li>SolidSquare</li>
<li>OutlineSquare</li>
<li>SolidRoundRect</li>
<li>OutlineRoundRect</li>
<li>SolidRoundRectDottedBaseline</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DateStyle</strong></td>
<td><strong>xs:string</strong></td>
<td>Obligatoire</td>
<td>Définit si le titre contient une date ou non.</td>
<td><ul>
<li>Aucun</li>
<li>Court</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Couleur</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType, simpleType</strong></a></td>
<td>Facultatif</td>
<td>Spécifie la couleur de l'arrière-plan.</td>
<td>Voir <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informations sur les éléments



| Élément      | Valeur                                                   |
|--------------|---------------------------------------------------------|
| Type d'élément | ComplexType [**TitleType**](titletype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk              |
| Nom du schéma  | Lecteur de journal                                          |



 

 

 



