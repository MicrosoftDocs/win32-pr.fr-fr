---
description: 'En savoir plus sur les propriétés suivantes : ColumnValue'
title: Propriétés ColumnValue
TOCTitle: ColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.ColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100998
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 5a9819d052bc2142cdbae6caedbda6678dc54cb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416032"
---
# <a name="columnvalue-properties"></a>Propriétés ColumnValue

Inclure les membres protégés  
Inclure les membres hérités  

Le type [ColumnValue](./columnvalue-class.md) expose les membres suivants.

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
<td>Obtient ou définit le ColumnID à définir ou à récupérer.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Error</a></td>
<td>Obtient l’avertissement généré par la récupération ou la définition de cette colonne.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Obtient ou définit la séquence de ITAG de colonne.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334213(v=exchg.10).md">Durée</a></td>
<td>Obtient la longueur d’octet d’une valeur de colonne, qui est égale à zéro si la colonne est null, sinon elle correspond à la taille des colonnes de taille fixe et représente la longueur réelle en octets pour les colonnes de taille variable (c’est-à-dire binaire et chaîne). Pour les chaînes, la longueur est déterminée en supposant deux octets par caractère.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Obtient ou définit les options de récupération de colonne.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Obtient ou définit les options de mise à jour de colonne.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriété protégée" alt="Protected property" /></td>
<td><a href="dn334172(v=exchg.10).md">Taille</a></td>
<td>Obtient la taille de la valeur dans la colonne. La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn334214(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtient le dernier jeu ou la dernière valeur Récupérée de la colonne. La valeur est retournée en tant qu’objet générique.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[ColumnValue, classe](./columnvalue-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
