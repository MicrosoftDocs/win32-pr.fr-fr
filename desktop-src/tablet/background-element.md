---
description: Contient l’arrière-plan d’un élément JournalDocument ou d’un élément JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Élément d’arrière-plan
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46388d56c04fc24ecd578788eecf9926ef01a301
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436584"
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
<td><strong>Couleur</strong></td>
<td><a href="colortype-simple-type.md"><strong>ColorType</strong></a> , simpleType</td>
<td>Facultatif</td>
<td>Spécifie la couleur de l'arrière-plan.</td>
<td>Voir <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informations sur les éléments



|                  | Valeur                                                             |
|------------------|-------------------------------------------------------------------|
| **Type d’élément** | ComplexType [**BackgroundType**](backgroundtype-complex-type.md) |
| **Espace de noms**    | urn : schemas-microsoft-com : TabletPC : RichInk                        |
| **Nom du schéma**  | Lecteur de journal                                                    |



 

 

 



