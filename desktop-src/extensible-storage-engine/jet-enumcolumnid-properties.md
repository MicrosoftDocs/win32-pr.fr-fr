---
description: En savoir plus sur les propriétés de JET_ENUMCOLUMNID
title: Propriétés de la JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191588"
---
# <a name="jet_enumcolumnid-properties"></a>Propriétés de la JET_ENUMCOLUMNID

Inclure les membres protégés  
Inclure les membres hérités  

Le type de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expose les membres suivants.

## <a name="properties"></a>Propriétés

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335141(v=exchg.10).md">ColumnID</a></td>
<td>Obtient ou définit l’ID ColumnID à énumérer.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagSequence</a></td>
<td>Obtient ou définit le nombre de valeurs de colonne (par index de base un) à énumérer pour l’ID de colonne spécifié. Si ctagSequence a la valeur 0 (zéro), rgtagSequence est ignoré et toutes les valeurs de colonne pour l’ID de colonne spécifié seront énumérées.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>Obtient ou définit le tableau d’index de base un dans le tableau de valeurs de colonne pour une colonne donnée. Un élément unique est un itagSequence qui est défini dans JET_RETRIEVECOLUMN. Un itagSequence de 0 (zéro) signifie &quot; Skip &quot; . Un itagSequence de 1 signifie que retourne la première valeur de colonne de la colonne, 2 le second, et ainsi de suite.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
