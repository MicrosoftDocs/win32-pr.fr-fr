---
description: 'En savoir plus sur les membres suivants : JET_THREADSTATS'
title: Membres JET_THREADSTATS (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: JET_THREADSTATS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats_members(v=EXCHG.10)
ms:contentKeyID: 39514028
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 13713d00431337f5e2190e2f547729e96a7cfb634fe1a95dddba570a9236f1f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890279"
---
# <a name="jet_threadstats-members"></a>Membres JET_THREADSTATS

Inclure les membres protégés  
Inclure les membres hérités  

Contient des statistiques cumulatives sur le travail effectué par le moteur de base de données sur le thread actuel. Ces informations sont retournées via JetGetThreadStats.

Le type de [JET_THREADSTATS](./jet-threadstats-structure2.md) expose les membres suivants.

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
<td><a href="hh578305(v=exchg.10).md">cbLogRecord</a></td>
<td>Obtient la taille totale, en octets, des enregistrements du journal des transactions qui ont été générés par le moteur de base de données sur le thread actuel.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578110(v=exchg.10).md">cLogRecord</a></td>
<td>Obtient le nombre total d’enregistrements du journal des transactions qui ont été générés par le moteur de base de données sur le thread actuel.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh578651(v=exchg.10).md">cPageDirtied</a></td>
<td>Obtient le nombre total de pages de base de données, sans modifications non écrites, qui ont été modifiées par le moteur de base de données sur le thread actuel.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh557376(v=exchg.10).md">cPagePreread</a></td>
<td>Obtient le nombre total de pages de base de données prérécupérées à partir du disque par le moteur de base de données sur le thread actuel.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh163392(v=exchg.10).md">cPageRead</a></td>
<td>Obtient le nombre total de pages de base de données récupérées à partir du disque par le moteur de base de données sur le thread actuel.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh596234(v=exchg.10).md">cPageRedirtied</a></td>
<td>Obtient le nombre total de pages de base de données, avec des modifications non écrites, qui ont été modifiées par le moteur de base de données sur le thread actuel.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="hh557174(v=exchg.10).md">cPageReferenced</a></td>
<td>Obtient le nombre total de pages de base de données visitées par le moteur de base de données sur le thread actuel.</td>
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
<td><a href="hh565584(v=exchg.10).md">Ajouter</a></td>
<td>Ajoutez les statistiques dans deux structures JET_THREADSTATS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh538903(v=exchg.10).md">Créer</a></td>
<td>Crée un nouveau <a href="hh578565(v=exchg.10).md">JET_THREADSTATS</a> structure avec la valeur spécifiée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh557146(v=exchg.10).md">Égal à (objet)</a></td>
<td>Retourne une valeur indiquant si cette instance est égale à une autre instance. (Substitue <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh596601(v=exchg.10).md">Égal à (JET_THREADSTATS)</a></td>
<td>Retourne une valeur indiquant si cette instance est égale à une autre instance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh579156(v=exchg.10).md">GetHashCode</a></td>
<td>Retourne le code de hachage de cette instance. (Substitue <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh579433(v=exchg.10).md">Soustraire</a></td>
<td>Calcule la différence de statistiques entre deux structures de JET_THREADSTATS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="hh558249(v=exchg.10).md">ToString</a></td>
<td>Obtient une représentation sous forme de chaîne de cet objet. (Substitue <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType. ToString ()</a>.)</td>
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
<td><a href="hh163281(v=exchg.10).md">Addition</a></td>
<td>Ajoutez les statistiques dans deux structures JET_THREADSTATS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh558521(v=exchg.10).md">Égalité</a></td>
<td>Détermine si deux instances spécifiées de JET_THREADSTATS sont égales.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh577527(v=exchg.10).md">Inégalité</a></td>
<td>Détermine si deux instances spécifiées de JET_THREADSTATS ne sont pas égales.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="hh557686(v=exchg.10).md">Soustraction</a></td>
<td>Calcule la différence de statistiques entre deux structures de JET_THREADSTATS.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Structure JET_THREADSTATS](./jet-threadstats-structure2.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
