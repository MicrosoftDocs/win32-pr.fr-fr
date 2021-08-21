---
description: En savoir plus sur les propriétés de JET_INDEXLIST
title: Propriétés de la JET_INDEXLIST
TOCTitle: JET_INDEXLIST properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_properties(v=EXCHG.10)
ms:contentKeyID: 55103599
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f7ea80bedb3cfd9fd3088e7d7793725db63666dbf9e76e84472af34d60734c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118074944"
---
# <a name="jet_indexlist-properties"></a>Propriétés de la JET_INDEXLIST

Inclure les membres protégés  
Inclure les membres hérités  

Le type de [JET_INDEXLIST](./jet-indexlist-class.md) expose les membres suivants.

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
<td><a href="dn335125(v=exchg.10).md">columnidcColumn</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de colonnes dans la clé d’index. La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335126(v=exchg.10).md">columnidcEntry</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre d’entrées dans l’index. Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; . La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335127(v=exchg.10).md">columnidcKey</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de clés uniques dans l’index. Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; . La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke le type de colonne de la colonne en cours d’indexation. La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke la ColumnID de la colonne indexée. La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke les Grbit qui s’appliquent à la colonne indexée. Consultez <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>. La colonne est de type <a href="hh577895(v=exchg.10).md">texte</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335168(v=exchg.10).md">columnidCp</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke la page de codes de la colonne indexée. La colonne est de type <a href="hh577895(v=exchg.10).md">short</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335136(v=exchg.10).md">columnidcPage</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de pages dans l’index. Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; . La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke les Grbit qui s’appliquent à la colonne indexée. Consultez <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>. La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke les grbits utilisés sur l’index. Consultez <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>. La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335170(v=exchg.10).md">columnidiColumn</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke l’index de de cette colonne dans la clé d’index. La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335138(v=exchg.10).md">columnidindexname</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nom de l’index. La colonne est de type <a href="hh577895(v=exchg.10).md">texte</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335171(v=exchg.10).md">columnidLangid</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke l’ID de langue (LCID) de l’index. La colonne est de type <a href="hh577895(v=exchg.10).md">short</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></td>
<td>Obtient le ColumnID de la colonne dans la table temporaire qui stocke les indicateurs de normalisation Unicode pour l’index. La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335173(v=exchg.10).md">cRecord</a></td>
<td>Obtient le nombre d’enregistrements dans la table temporaire.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335174(v=exchg.10).md">TableID</a></td>
<td>Obtient l’TableID de la table temporaire. Elle doit être fermée lorsque la table n’est plus nécessaire.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_INDEXLIST](./jet-indexlist-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
