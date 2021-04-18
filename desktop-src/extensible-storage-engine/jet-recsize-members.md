---
description: 'En savoir plus sur les membres suivants : JET_RECSIZE'
title: Membres JET_RECSIZE (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 224d22b5dea0447297163fb6b5e1a70fe62a6396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565254"
---
# <a name="jet_recsize-members"></a>Membres JET_RECSIZE

Inclure les membres protégés  
Inclure les membres hérités  

Utilisé par [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) pour retourner des informations sur les exigences d’utilisation d’un enregistrement dans l’espace de données utilisateur, le nombre de colonnes définies, le nombre de valeurs et l’espace de charge de structure d’enregistrement esent.

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh538879(v=exchg.10).md">Ajouter</a></td>
<td>Ajoutez les tailles dans deux structures de JET_RECSIZE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh558506(v=exchg.10).md">Égal à (objet)</a></td>
<td>Retourne une valeur indiquant si cette instance est égale à une autre instance. (Substitue <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh577992(v=exchg.10).md">Égal à (JET_RECSIZE)</a></td>
<td>Retourne une valeur indiquant si cette instance est égale à une autre instance.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh557078(v=exchg.10).md">GetHashCode</a></td>
<td>Retourne le code de hachage de cette instance. (Substitue <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh579561(v=exchg.10).md">Soustraire</a></td>
<td>Calculez la différence de tailles entre deux structures de JET_RECSIZE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></td>
<td>(Héritée de <a href="/dotnet/api/system.valuetype">ValueType</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="operators"></a>Opérateurs

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
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh578675(v=exchg.10).md">Complément</a></td>
<td>Ajoutez les tailles dans deux structures de JET_RECSIZE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh596362(v=exchg.10).md">Égalité</a></td>
<td>Détermine si deux instances spécifiées de JET_RECSIZE sont égales.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh578809(v=exchg.10).md">Inégalité</a></td>
<td>Détermine si deux instances spécifiées de JET_RECSIZE ne sont pas égales.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh596696(v=exchg.10).md">Soustraction</a></td>
<td>Calculez la différence de tailles entre deux structures de JET_RECSIZE.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_RECSIZE](./jet-recsize-structure2.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
