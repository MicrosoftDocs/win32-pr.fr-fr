---
description: 'En savoir plus sur les éléments suivants : StringColumnValue'
title: Membres StringColumnValue
TOCTitle: StringColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.StringColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55104040
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: aad09e22b1ee43d9f0cfb537a9067a63b7d3b739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865606"
---
# <a name="stringcolumnvalue-members"></a>Membres StringColumnValue

Inclure les membres protégés  
Inclure les membres hérités  

Valeur de colonne de chaîne Unicode.

Le type [StringColumnValue](./stringcolumnvalue-class.md) expose les membres suivants.

## <a name="constructors"></a>Constructeurs

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn351187(v=exchg.10).md">StringColumnValue</a></td>
<td></td>
</tr>
</tbody>
</table>


Haut

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
<td><a href="dn351195(v=exchg.10).md">Durée</a></td>
<td>Obtient la longueur d’octet d’une valeur de colonne, qui est égale à zéro si la colonne est NULL ; sinon, elle correspond à la longueur en octets de la valeur de chaîne. La longueur en octets est déterminée en supposant que deux octets par caractère. (Substitue <a href="dn334213(v=exchg.10).md">ColumnValue. Length</a>.)</td>
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
<td><a href="dn351137(v=exchg.10).md">Taille</a></td>
<td>Obtient la taille de la valeur dans la colonne. La valeur 0 est retournée pour les colonnes de taille variable (par exemple, Binary et String). (Substitue <a href="dn334172(v=exchg.10).md">ColumnValue. Size</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351204(v=exchg.10).md">Valeur</a></td>
<td>Obtient ou définit la valeur de la colonne. Utilisez <a href="dn334138(v=exchg.10).md">SetColumns (JET_SESID, JET_TABLEID, [])</a> pour mettre à jour un enregistrement avec la valeur de colonne.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351202(v=exchg.10).md">ValueAsObject</a></td>
<td>Obtient le dernier jeu ou la dernière valeur Récupérée de la colonne. La valeur est retournée en tant qu’objet générique. (Substitue <a href="dn334214(v=exchg.10).md">ColumnValue. ValueAsObject</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="methods"></a>Méthodes

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn351134(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Données récupérées à partir d’ESENT, décoder les données et définir la valeur dans l’objet ColumnValue. (Substitue <a href="dn334208(v=exchg.10).md">ColumnValue. GetValueFromBytes ([], Int32, Int32, Int32)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn351194(v=exchg.10).md">ToString</a></td>
<td>Obtient une représentation sous forme de chaîne de cet objet. (Substitue <a href="dn334163(v=exchg.10).md">ColumnValue. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[StringColumnValue, classe](./stringcolumnvalue-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
