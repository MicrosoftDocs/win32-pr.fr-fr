---
description: 'En savoir plus sur les éléments suivants : EsentResource'
title: Membres EsentResource
TOCTitle: EsentResource members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource_members(v=EXCHG.10)
ms:contentKeyID: 55107302
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af0f0a4baa76cc702c6f4048e42e9ec78463e5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552853"
---
# <a name="esentresource-members"></a>Membres EsentResource

Inclure les membres protégés  
Inclure les membres hérités  

Il s’agit de la classe de base pour tous les objets de ressource esent. Les sous-classes de cette classe peuvent allouer et libérer des ressources non managées.

Le type [EsentResource](./esentresource-class.md) expose les membres suivants.

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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn350551(v=exchg.10).md">EsentResource</a></td>
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
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriété protégée" alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">HasResource</a></td>
<td>Obtient une valeur indiquant si la ressource sous-jacente est actuellement allouée.</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>Lève une exception si cet objet a été supprimé.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose ()</a></td>
<td>Supprimez cet objet, en libérant la ressource esent sous-jacente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (booléen)</a></td>
<td>Appelée par dispose et le finaliseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finaliser</a></td>
<td>Finalise une instance de la classe EsentResource. (Substitue <a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Object. Finalize ()</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn350545(v=exchg.10).md">ReleaseResource</a></td>
<td>Implémenté par la sous-classe pour libérer une ressource.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></td>
<td>Appelée par une sous-classe lorsqu’une ressource est allouée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></td>
<td>Appelée par une sous-classe lorsqu’une ressource est libérée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.tostring#System_Object_ToString">ToString</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[EsentResource, classe](./esentresource-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
