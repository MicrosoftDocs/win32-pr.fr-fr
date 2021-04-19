---
description: Contient des informations de titre sur la note du journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Titre, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545126"
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
<td><strong>Color</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType, simpleType</strong></a></td>
<td>Facultatif</td>
<td>Spécifie la couleur de l'arrière-plan.</td>
<td>Voir <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informations sur les éléments



|              |                                                         |
|--------------|---------------------------------------------------------|
| Type d'élément | ComplexType [**TitleType**](titletype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk              |
| Nom du schéma  | Lecteur de journal                                          |



 

 

 



