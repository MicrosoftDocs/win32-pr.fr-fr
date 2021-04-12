---
description: 'En savoir plus sur les propriétés suivantes : BytesColumnValue'
title: Propriétés BytesColumnValue
TOCTitle: BytesColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100964
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: bafae34a3fa6dac29cc504ebe9a34c0abd7b870a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321009"
---
# <a name="bytescolumnvalue-properties"></a>Propriétés BytesColumnValue

Inclure les membres protégés  
Inclure les membres hérités  

Le type [BytesColumnValue](./bytescolumnvalue-class.md) expose les membres suivants.

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
<td><a href="dn334166(v=exchg.10).md">ColumnID</a></td>
<td>Obtient ou définit le ColumnID à définir ou à récupérer. (Héritée de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Error</a></td>
<td>Obtient l’avertissement généré par la récupération ou la définition de cette colonne. (Héritée de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Obtient ou définit la séquence de ITAG de colonne. (Héritée de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334126(v=exchg.10).md">Durée</a></td>
<td>Obtient la longueur d’octet d’une valeur de colonne, qui est égale à zéro si la colonne est NULL ; sinon, correspond à la longueur réelle du tableau d’octets. (Substitue <a href="dn334213(v=exchg.10).md">ColumnValue. Length</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Obtient ou définit les options de récupération de colonne. (Héritée de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Obtient ou définit les options de mise à jour de colonne. (Héritée de <a href="dn334206(v=exchg.10).md">ColumnValue</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriété protégée" alt="Protected property" /></td>
<td><a href="dn334176(v=exchg.10).md">Taille</a></td>
<td>Obtient la taille de la valeur dans la colonne. La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String). (Substitue <a href="dn334172(v=exchg.10).md">ColumnValue. Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334129(v=exchg.10).md">Valeur</a></td>
<td>Obtient ou définit la valeur de la colonne. Utilisez <a href="dn334138(v=exchg.10).md">SetColumns (JET_SESID, JET_TABLEID, [])</a> pour mettre à jour un enregistrement avec la valeur de colonne.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334177(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtient le dernier jeu ou la dernière valeur Récupérée de la colonne. La valeur est retournée en tant qu’objet générique. (Substitue <a href="dn334214(v=exchg.10).md">ColumnValue. ValueAsObject</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[BytesColumnValue, classe](./bytescolumnvalue-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
