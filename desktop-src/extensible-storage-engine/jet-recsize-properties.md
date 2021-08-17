---
description: En savoir plus sur les propriétés de JET_RECSIZE
title: Propriétés de JET_RECSIZE (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 522acb283022150cf6baeb8e82be3ebbe3cabbbe7c7cd50289f8d2312fbccb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118763790"
---
# <a name="jet_recsize-properties"></a>Propriétés de la JET_RECSIZE

Inclure les membres protégés  
Inclure les membres hérités  

Le type de [JET_RECSIZE](./jet-recsize-structure2.md) expose les membres suivants.

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
<td><a href="hh557581(v=exchg.10).md">cbData</a></td>
<td>Obtient le jeu de données utilisateur dans l’enregistrement.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></td>
<td>Obtient la taille compressée des données utilisateur dans l’enregistrement. C’est le même que <a href="hh557581(v=exchg.10).md">cbData</a> si aucune valeur long intrinsèque n’est compressée).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh557913(v=exchg.10).md">cbLongValueData</a></td>
<td>Obtient le jeu de données utilisateur dans l’enregistrement, mais stocké dans l’arborescence de valeurs longues.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></td>
<td>Obtient la taille compressée des données utilisateur dans l’arborescence de valeurs longues. C’est le même que <a href="hh557913(v=exchg.10).md">cbLongValueData</a> si aucune valeur long séparée n’est compressée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></td>
<td>Obtient la surcharge des données de valeur long.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh565836(v=exchg.10).md">cbOverhead</a></td>
<td>Obtient la surcharge de la structure d’enregistrement ESENT pour cet enregistrement. Cela comprend la taille de la clé de l’enregistrement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></td>
<td>Obtient le nombre total de colonnes dans l’enregistrement qui sont compressées.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh596288(v=exchg.10).md">cLongValues</a></td>
<td>Obtient le nombre total de valeurs longues stockées dans l’arborescence de valeurs longues pour cet enregistrement. Cela n’inclut pas les valeurs longues intrinsèques.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh577486(v=exchg.10).md">cMultiValues</a></td>
<td>Obtient l’accumulation du nombre total de valeurs au-delà de la première pour toutes les colonnes de l’enregistrement.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></td>
<td>Obtient le nombre total de colonnes fixes et variables définies dans cet enregistrement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></td>
<td>Obtient le nombre total de colonnes avec balises définies dans cet enregistrement.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_RECSIZE](./jet-recsize-structure2.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
