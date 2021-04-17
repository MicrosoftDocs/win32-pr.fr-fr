---
description: 'En savoir plus sur les membres suivants : JET_RECORDLIST'
title: Membres JET_RECORDLIST
TOCTitle: JET_RECORDLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RECORDLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recordlist_members(v=EXCHG.10)
ms:contentKeyID: 55103811
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d2e43304dfd554be09d410c3885ca63fd199124b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569542"
---
# <a name="jet_recordlist-members"></a><span data-ttu-id="1ae10-103">Membres JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="1ae10-103">JET_RECORDLIST members</span></span>

<span data-ttu-id="1ae10-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="1ae10-104">Include protected members</span></span>  
<span data-ttu-id="1ae10-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="1ae10-105">Include inherited members</span></span>  

<span data-ttu-id="1ae10-106">Informations sur une table temporaire contenant des informations sur tous les index d’une table donnée.</span><span class="sxs-lookup"><span data-stu-id="1ae10-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="1ae10-107">Le type de [JET_RECORDLIST](./jet-recordlist-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="1ae10-107">The [JET_RECORDLIST](./jet-recordlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="1ae10-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="1ae10-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1ae10-109">Nom</span><span class="sxs-lookup"><span data-stu-id="1ae10-109">Name</span></span></th>
<th><span data-ttu-id="1ae10-110">Description</span><span class="sxs-lookup"><span data-stu-id="1ae10-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="1ae10-112"><a href="dn335241(v=exchg.10).md">JET_RECORDLIST</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-112"><a href="dn335241(v=exchg.10).md">JET_RECORDLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ae10-113">Haut</span><span class="sxs-lookup"><span data-stu-id="1ae10-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="1ae10-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1ae10-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1ae10-115">Nom</span><span class="sxs-lookup"><span data-stu-id="1ae10-115">Name</span></span></th>
<th><span data-ttu-id="1ae10-116">Description</span><span class="sxs-lookup"><span data-stu-id="1ae10-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="1ae10-118"><a href="dn335244(v=exchg.10).md">columnidBookmark</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-118"><a href="dn335244(v=exchg.10).md">columnidBookmark</a></span></span></td>
<td><span data-ttu-id="1ae10-119">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le signet de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1ae10-119">Gets the columnid of the column in the temporary table which stores the bookmark of the record.</span></span> <span data-ttu-id="1ae10-120">La colonne est de type JET_coltyp. Financière.</span><span class="sxs-lookup"><span data-stu-id="1ae10-120">The column is of type JET_coltyp.Text.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="1ae10-122"><a href="dn335252(v=exchg.10).md">cRecords</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-122"><a href="dn335252(v=exchg.10).md">cRecords</a></span></span></td>
<td><span data-ttu-id="1ae10-123">Obtient le nombre d’enregistrements dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1ae10-123">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="1ae10-125"><a href="dn335255(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-125"><a href="dn335255(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="1ae10-126">Obtient l’TableID de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="1ae10-126">Gets tableid of the temporary table.</span></span> <span data-ttu-id="1ae10-127">Elle doit être fermée lorsque la table n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1ae10-127">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ae10-128">Haut</span><span class="sxs-lookup"><span data-stu-id="1ae10-128">Top</span></span>

## <a name="methods"></a><span data-ttu-id="1ae10-129">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1ae10-129">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1ae10-130">Nom</span><span class="sxs-lookup"><span data-stu-id="1ae10-130">Name</span></span></th>
<th><span data-ttu-id="1ae10-131">Description</span><span class="sxs-lookup"><span data-stu-id="1ae10-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="1ae10-133"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-133"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="1ae10-134">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="1ae10-134">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="1ae10-136"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-136"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="1ae10-137">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="1ae10-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="1ae10-139"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-139"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="1ae10-140">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="1ae10-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="1ae10-142"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-142"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="1ae10-143">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="1ae10-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="1ae10-145"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-145"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="1ae10-146">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="1ae10-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="1ae10-148"><a href="dn335242(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="1ae10-148"><a href="dn335242(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="1ae10-149">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="1ae10-149">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="1ae10-150">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="1ae10-150">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ae10-151">Haut</span><span class="sxs-lookup"><span data-stu-id="1ae10-151">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="1ae10-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ae10-152">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ae10-153">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="1ae10-153">Reference</span></span>

[<span data-ttu-id="1ae10-154">Classe JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="1ae10-154">JET_RECORDLIST class</span></span>](./jet-recordlist-class.md)

[<span data-ttu-id="1ae10-155">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1ae10-155">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
