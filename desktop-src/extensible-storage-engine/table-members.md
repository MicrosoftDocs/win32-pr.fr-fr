---
description: 'En savoir plus sur : les membres de table'
title: Membres de table
TOCTitle: Table members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Table
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table_members(v=EXCHG.10)
ms:contentKeyID: 55104054
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b4e5bd09cf1c450197978e3126dc63fe96ec6425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566438"
---
# <a name="table-members"></a><span data-ttu-id="4fdd4-103">Membres de table</span><span class="sxs-lookup"><span data-stu-id="4fdd4-103">Table members</span></span>

<span data-ttu-id="4fdd4-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="4fdd4-104">Include protected members</span></span>  
<span data-ttu-id="4fdd4-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="4fdd4-105">Include inherited members</span></span>  

<span data-ttu-id="4fdd4-106">Classe qui encapsule un JET_TABLEID dans un objet jetable.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-106">A class that encapsulates a JET_TABLEID in a disposable object.</span></span> <span data-ttu-id="4fdd4-107">Une table existante est alors ouverte.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-107">This opens an existing table.</span></span> <span data-ttu-id="4fdd4-108">Pour créer une table, utilisez la méthode JetCreateTable.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-108">To create a table use the JetCreateTable method.</span></span>

<span data-ttu-id="4fdd4-109">Le type de [table](./table-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-109">The [Table](./table-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="4fdd4-110">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="4fdd4-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="4fdd4-111">Nom</span><span class="sxs-lookup"><span data-stu-id="4fdd4-111">Name</span></span></th>
<th><span data-ttu-id="4fdd4-112">Description</span><span class="sxs-lookup"><span data-stu-id="4fdd4-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="4fdd4-114"><a href="dn351234(v=exchg.10).md">Table</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-114"><a href="dn351234(v=exchg.10).md">Table</a></span></span></td>
<td><span data-ttu-id="4fdd4-115">Initialise une nouvelle instance de la classe table.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-115">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="4fdd4-116">La table est ouverte à partir de la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-116">The table is opened from the given database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4fdd4-117">Haut</span><span class="sxs-lookup"><span data-stu-id="4fdd4-117">Top</span></span>

## <a name="properties"></a><span data-ttu-id="4fdd4-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4fdd4-118">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="4fdd4-119">Nom</span><span class="sxs-lookup"><span data-stu-id="4fdd4-119">Name</span></span></th>
<th><span data-ttu-id="4fdd4-120">Description</span><span class="sxs-lookup"><span data-stu-id="4fdd4-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriété protégée" alt="Protected property" /></td>
<td><span data-ttu-id="4fdd4-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-122"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="4fdd4-123">Obtient une valeur indiquant si la ressource sous-jacente est actuellement allouée.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-123">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="4fdd4-124">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-124">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="4fdd4-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-126"><a href="dn351171(v=exchg.10).md">JetTableid</a></span></span></td>
<td><span data-ttu-id="4fdd4-127">Obtient le JET_TABLEID contenu dans cette table.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-127">Gets the JET_TABLEID that this table contains.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="4fdd4-129"><a href="dn351170(v=exchg.10).md">Nom</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-129"><a href="dn351170(v=exchg.10).md">Name</a></span></span></td>
<td><span data-ttu-id="4fdd4-130">Obtient le nom de cette table.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-130">Gets the name of this table.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4fdd4-131">Haut</span><span class="sxs-lookup"><span data-stu-id="4fdd4-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="4fdd4-132">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4fdd4-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="4fdd4-133">Nom</span><span class="sxs-lookup"><span data-stu-id="4fdd4-133">Name</span></span></th>
<th><span data-ttu-id="4fdd4-134">Description</span><span class="sxs-lookup"><span data-stu-id="4fdd4-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="4fdd4-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="4fdd4-137">Lève une exception si cet objet a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="4fdd4-138">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="4fdd4-140"><a href="dn351235(v=exchg.10).md">Fermer</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-140"><a href="dn351235(v=exchg.10).md">Close</a></span></span></td>
<td><span data-ttu-id="4fdd4-141">Fermez la table.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-141">Close the table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="4fdd4-143"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-143"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="4fdd4-144">Supprimez cet objet, en libérant la ressource esent sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-144">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="4fdd4-145">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-145">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="4fdd4-147"><a href="dn350543(v=exchg.10).md">Dispose (booléen)</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-147"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="4fdd4-148">Appelée par dispose et le finaliseur.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-148">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="4fdd4-149">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-149">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="4fdd4-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-151"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="4fdd4-152">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="4fdd4-154"><a href="dn350552(v=exchg.10).md">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-154"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="4fdd4-155">Finalise une instance de la classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-155">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="4fdd4-156">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-156">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="4fdd4-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-158"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="4fdd4-159">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="4fdd4-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-161"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="4fdd4-162">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="4fdd4-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-164"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="4fdd4-165">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="4fdd4-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-167"><a href="dn351168(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="4fdd4-168">Libérez le JET_TABLEID sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-168">Free the underlying JET_TABLEID.</span></span> <span data-ttu-id="4fdd4-169">(Substitue <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-169">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="4fdd4-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-171"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="4fdd4-172">Appelée par une sous-classe lorsqu’une ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-172">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="4fdd4-173">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-173">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="4fdd4-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-175"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="4fdd4-176">Appelée par une sous-classe lorsqu’une ressource est libérée.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-176">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="4fdd4-177">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-177">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="4fdd4-179"><a href="dn351237(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-179"><a href="dn351237(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="4fdd4-180">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente la <a href="dn351163(v=exchg.10).md">table</a>actuelle.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-180">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351163(v=exchg.10).md">Table</a>.</span></span> <span data-ttu-id="4fdd4-181">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="4fdd4-181">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4fdd4-182">Haut</span><span class="sxs-lookup"><span data-stu-id="4fdd4-182">Top</span></span>

## <a name="operators"></a><span data-ttu-id="4fdd4-183">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="4fdd4-183">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="4fdd4-184">Nom</span><span class="sxs-lookup"><span data-stu-id="4fdd4-184">Name</span></span></th>
<th><span data-ttu-id="4fdd4-185">Description</span><span class="sxs-lookup"><span data-stu-id="4fdd4-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="4fdd4-188"><a href="dn351239(v=exchg.10).md">Implicite (table à JET_TABLEID)</a></span><span class="sxs-lookup"><span data-stu-id="4fdd4-188"><a href="dn351239(v=exchg.10).md">Implicit(Table to JET_TABLEID)</a></span></span></td>
<td><span data-ttu-id="4fdd4-189">Opérateur de conversion implicite d’une table en JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-189">Implicit conversion operator from a Table to a JET_TABLEID.</span></span> <span data-ttu-id="4fdd4-190">Cela permet d’utiliser une table avec des API qui attendent une JET_TABLEID.</span><span class="sxs-lookup"><span data-stu-id="4fdd4-190">This allows a Table to be used with APIs which expect a JET_TABLEID.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4fdd4-191">Haut</span><span class="sxs-lookup"><span data-stu-id="4fdd4-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="4fdd4-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fdd4-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4fdd4-193">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4fdd4-193">Reference</span></span>

[<span data-ttu-id="4fdd4-194">Classe de table</span><span class="sxs-lookup"><span data-stu-id="4fdd4-194">Table class</span></span>](./table-class.md)

[<span data-ttu-id="4fdd4-195">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4fdd4-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
