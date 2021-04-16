---
description: En savoir plus sur les propriétés de JET_RETINFO
title: Propriétés de la JET_RETINFO
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554125"
---
# <a name="jet_retinfo-properties"></a>Propriétés de la JET_RETINFO

Inclure les membres protégés  
Inclure les membres hérités  

Le type de [JET_RETINFO](./jet-retinfo-class.md) expose les membres suivants.

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
<td><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></td>
<td>Obtient le ColumnID de la colonne balisée, à valeurs multiples ou partiellement allouées Récupérée lorsque toutes les colonnes avec balises sont récupérées en passant 0 comme ColumnID à JetRetrieveColumn.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335220(v=exchg.10).md">ibLongValue</a></td>
<td>Obtient ou définit le décalage vers le premier octet à récupérer à partir d’une colonne de type <a href="hh577895(v=exchg.10).md">LONGBINARY</a>, ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351035(v=exchg.10).md">itagSequence</a></td>
<td>Obtient ou définit le numéro de séquence de la valeur dans une colonne à valeurs multiples. Le tableau de valeurs est de base un. La première valeur est séquence 1, et non 0. Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé en tant que itagSequence.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_RETINFO](./jet-retinfo-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
