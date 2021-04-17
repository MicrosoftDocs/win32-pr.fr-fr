---
description: 'En savoir plus sur les membres suivants : JET_ENUMCOLUMNVALUE'
title: Membres JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55103510
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2950caf527af07312f4f27c9464ee4088830fe1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566505"
---
# <a name="jet_enumcolumnvalue-members"></a><span data-ttu-id="e3cf0-103">Membres JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="e3cf0-103">JET_ENUMCOLUMNVALUE members</span></span>

<span data-ttu-id="e3cf0-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="e3cf0-104">Include protected members</span></span>  
<span data-ttu-id="e3cf0-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="e3cf0-105">Include inherited members</span></span>  

<span data-ttu-id="e3cf0-106">Énumère les valeurs de colonne d’un enregistrement à l’aide de la fonction JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="e3cf0-107">[JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, \[ \] , int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) retourne un tableau de structures de JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-107">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="e3cf0-108">Le tableau est retourné dans la mémoire qui a été allouée à l’aide du rappel fourni à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="e3cf0-109">Le type de [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-109">The [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="e3cf0-110">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="e3cf0-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e3cf0-111">Nom</span><span class="sxs-lookup"><span data-stu-id="e3cf0-111">Name</span></span></th>
<th><span data-ttu-id="e3cf0-112">Description</span><span class="sxs-lookup"><span data-stu-id="e3cf0-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e3cf0-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-114"><a href="dn335095(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3cf0-115">Haut</span><span class="sxs-lookup"><span data-stu-id="e3cf0-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="e3cf0-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e3cf0-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e3cf0-117">Nom</span><span class="sxs-lookup"><span data-stu-id="e3cf0-117">Name</span></span></th>
<th><span data-ttu-id="e3cf0-118">Description</span><span class="sxs-lookup"><span data-stu-id="e3cf0-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e3cf0-120"><a href="dn335097(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-120"><a href="dn335097(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="e3cf0-121">Obtient la taille de la valeur de colonne pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-121">Gets the size of the column value for the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e3cf0-123"><a href="dn335144(v=exchg.10).md">Raise</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-123"><a href="dn335144(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="e3cf0-124">Obtient le code d’état de colonne résultant de l’énumération de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-124">Gets the column status code resulting from the enumeration of the column value.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e3cf0-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-126"><a href="dn335102(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="e3cf0-127">Obtient la valeur de colonne (par index de base un) qui a été énumérée.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-127">Gets the column value (by one-based index) that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e3cf0-129"><a href="dn335149(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-129"><a href="dn335149(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="e3cf0-130">Obtient la valeur qui a été énumérée pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-130">Gets the value that was enumerated for the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3cf0-131">Haut</span><span class="sxs-lookup"><span data-stu-id="e3cf0-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="e3cf0-132">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e3cf0-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e3cf0-133">Nom</span><span class="sxs-lookup"><span data-stu-id="e3cf0-133">Name</span></span></th>
<th><span data-ttu-id="e3cf0-134">Description</span><span class="sxs-lookup"><span data-stu-id="e3cf0-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e3cf0-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="e3cf0-137">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e3cf0-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e3cf0-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="e3cf0-140">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e3cf0-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e3cf0-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="e3cf0-143">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e3cf0-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e3cf0-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="e3cf0-146">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e3cf0-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e3cf0-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="e3cf0-149">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e3cf0-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e3cf0-151"><a href="dn335096(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="e3cf0-151"><a href="dn335096(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="e3cf0-152">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="e3cf0-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335142(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="e3cf0-153">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="e3cf0-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e3cf0-154">Haut</span><span class="sxs-lookup"><span data-stu-id="e3cf0-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e3cf0-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3cf0-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e3cf0-156">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e3cf0-156">Reference</span></span>

[<span data-ttu-id="e3cf0-157">Classe JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="e3cf0-157">JET_ENUMCOLUMNVALUE class</span></span>](./jet-enumcolumnvalue-class.md)

[<span data-ttu-id="e3cf0-158">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e3cf0-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
