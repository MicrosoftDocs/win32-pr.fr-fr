---
description: Contient le contenu d’une page de journal.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Élément de contenu [lecteur de journal]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432151"
---
# <a name="content-element-journal-reader"></a>Lecteur du journal des éléments de contenu \[\]

Contient le contenu d’une page de journal.

## <a name="definition"></a>Définition

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Éléments parents

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Éléments enfants

[**, Nœud**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Dessin**](drawing-element.md)

[**Text**](text-element.md)

[**Image**](image-element.md)

[**Indicateur**](flag-element.md)

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
<th>PossibleValues</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Type</strong></td>
<td><a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a></td>
<td>Obligatoire</td>
<td>Si le type est &quot; inerte &quot; , le contenu ne peut pas être modifié.<br/></td>
<td><ul>
<li>Normal</li>
<li>Inertes</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informations sur les éléments



|  Élément     | Valeur                                                     |
|--------------|-------------------------------------------------------------|
| Type d'élément | ComplexType [**ContentType**](contenttype-complex-type.md) |
| Espace de noms    | urn : schemas-microsoft-com : TabletPC : RichInk                  |
| Nom du schéma  | Lecteur de journal                                              |



 

 

 




