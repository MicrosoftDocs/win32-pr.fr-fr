---
description: En savoir plus sur les propriétés de JET_ENUMCOLUMN
title: Propriétés de la JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ee11c050d558fbefb15be4783a08b1808744718d043de038b297fdc5ebd9e3fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667919"
---
# <a name="jet_enumcolumn-properties"></a>Propriétés de la JET_ENUMCOLUMN

Inclure les membres protégés  
Inclure les membres hérités  

Le type de [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) expose les membres suivants.

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
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Obtient la taille de la valeur qui a été énumérée pour la colonne. Ce membre est utilisé uniquement si <a href="dn335086(v=exchg.10).md">Err</a> est égal à <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>Obtient le nombre de valeurs de colonne énumérées pour la colonne. Ce membre est utilisé uniquement si <a href="dn335086(v=exchg.10).md">Err</a> n’est pas <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">ColumnID</a></td>
<td>Obtient l’ID ColumnID qui a été énuméré.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">Raise</a></td>
<td>Obtient le code d’état de la colonne qui résulte de l’énumération.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Obtient la valeur qui a été énumérée pour la colonne. Ce membre est utilisé uniquement si <a href="dn335086(v=exchg.10).md">Err</a> est égal à <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>. Cela pointe vers la mémoire allouée avec le rappel d’allocateur <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> passé à <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>. N’oubliez pas de libérer la mémoire une fois que vous avez terminé.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>Obtient les valeurs de colonne énumérées pour la colonne. Ce membre est utilisé uniquement si <a href="dn335086(v=exchg.10).md">Err</a> n’est pas <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
