---
description: Contient l’arrière-plan d’un élément JournalDocument ou d’un élément JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Élément d’arrière-plan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530662"
---
# <a name="background-element"></a>Élément d’arrière-plan

Contient l’arrière-plan d’un élément [**JournalDocument**](journaldocument-element.md) ou d’un élément [**JournalPage**](journalpage-element.md) .

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Éléments parents

[**Stationery**](stationery-element.md)

## <a name="child-elements"></a>Éléments enfants

[**Image**](image-element.md)

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
<td>Spécifie le style de l’arrière-plan.</td>
<td><ul>
<li>Aucun</li>
<li>Unie</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Color</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</td>
<td>Facultatif</td>
<td>Spécifie la couleur de l'arrière-plan.</td>
<td>Voir <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informations sur les éléments



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| Type d'élément | ComplexType [**BackgroundType**](backgroundtype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                        |
| Nom du schéma  | Lecteur de journal                                                    |



 

 

 



