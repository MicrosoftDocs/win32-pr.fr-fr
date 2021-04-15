---
description: 'En savoir plus sur les membres suivants : JET_INSTANCE_INFO'
title: Membres JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info_members(v=EXCHG.10)
ms:contentKeyID: 55103693
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 42d9bcd2c078766875fc8230eaf83dc07fdb4b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554197"
---
# <a name="jet_instance_info-members"></a><span data-ttu-id="fa4d3-103">Membres JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="fa4d3-103">JET_INSTANCE_INFO members</span></span>

<span data-ttu-id="fa4d3-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="fa4d3-104">Include protected members</span></span>  
<span data-ttu-id="fa4d3-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="fa4d3-105">Include inherited members</span></span>  

<span data-ttu-id="fa4d3-106">Reçoit des informations sur l’exécution d’instances de base de données lorsqu’elle est utilisée avec les fonctions JetGetInstanceInfo et JetOSSnapshotFreeze.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-106">Receives information about running database instances when used with the JetGetInstanceInfo and JetOSSnapshotFreeze functions.</span></span>

<span data-ttu-id="fa4d3-107">Le type de [JET_INSTANCE_INFO](./jet-instance-info-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-107">The [JET_INSTANCE_INFO](./jet-instance-info-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="fa4d3-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fa4d3-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="fa4d3-109">Nom</span><span class="sxs-lookup"><span data-stu-id="fa4d3-109">Name</span></span></th>
<th><span data-ttu-id="fa4d3-110">Description</span><span class="sxs-lookup"><span data-stu-id="fa4d3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="fa4d3-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-112"><a href="dn335189(v=exchg.10).md">cDatabases</a></span></span></td>
<td><span data-ttu-id="fa4d3-113">Obtient le nombre de bases de données attachées à l’instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-113">Gets the number of databases that are attached to the database instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="fa4d3-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-115"><a href="dn335190(v=exchg.10).md">hInstanceId</a></span></span></td>
<td><span data-ttu-id="fa4d3-116">Obtient le JET_INSTANCE de l’instance donnée.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-116">Gets the JET_INSTANCE of the given instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="fa4d3-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-118"><a href="dn335193(v=exchg.10).md">szDatabaseFileName</a></span></span></td>
<td><span data-ttu-id="fa4d3-119">Obtient une collection de chaînes, chacune contenant le nom de fichier d’une base de données attachée à l’instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-119">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="fa4d3-120">Le tableau contient des éléments cDatabases.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-120">The array has cDatabases elements.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="fa4d3-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-122"><a href="dn335194(v=exchg.10).md">szInstanceName</a></span></span></td>
<td><span data-ttu-id="fa4d3-123">Obtient le nom de l’instance de base de données.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-123">Gets the name of the database instance.</span></span> <span data-ttu-id="fa4d3-124">Cette valeur peut être null si l’instance n’a pas de nom.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-124">This value can be null if the instance does not have a name.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fa4d3-125">Haut</span><span class="sxs-lookup"><span data-stu-id="fa4d3-125">Top</span></span>

## <a name="methods"></a><span data-ttu-id="fa4d3-126">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fa4d3-126">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="fa4d3-127">Nom</span><span class="sxs-lookup"><span data-stu-id="fa4d3-127">Name</span></span></th>
<th><span data-ttu-id="fa4d3-128">Description</span><span class="sxs-lookup"><span data-stu-id="fa4d3-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="fa4d3-130"><a href="dn335184(v=exchg.10).md">Égal à (objet)</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-130"><a href="dn335184(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="fa4d3-131">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-131">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="fa4d3-132">(Substitue <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. Equals (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="fa4d3-132">(Overrides <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="fa4d3-134"><a href="dn335187(v=exchg.10).md">Égal à (JET_INSTANCE_INFO)</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-134"><a href="dn335187(v=exchg.10).md">Equals(JET_INSTANCE_INFO)</a></span></span></td>
<td><span data-ttu-id="fa4d3-135">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-135">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="fa4d3-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-137"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="fa4d3-138">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="fa4d3-138">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="fa4d3-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-140"><a href="dn335191(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="fa4d3-141">Retourne le code de hachage de cette instance.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-141">Returns the hash code for this instance.</span></span> <span data-ttu-id="fa4d3-142">(Substitue <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="fa4d3-142">(Overrides <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="fa4d3-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-144"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="fa4d3-145">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="fa4d3-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="fa4d3-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-147"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="fa4d3-148">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="fa4d3-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="fa4d3-150"><a href="dn335192(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="fa4d3-150"><a href="dn335192(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="fa4d3-151">Génère une représentation sous forme de chaîne de l’instance.</span><span class="sxs-lookup"><span data-stu-id="fa4d3-151">Generate a string representation of the instance.</span></span> <span data-ttu-id="fa4d3-152">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="fa4d3-152">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fa4d3-153">Haut</span><span class="sxs-lookup"><span data-stu-id="fa4d3-153">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="fa4d3-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa4d3-154">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fa4d3-155">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="fa4d3-155">Reference</span></span>

[<span data-ttu-id="fa4d3-156">Classe JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="fa4d3-156">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="fa4d3-157">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fa4d3-157">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
