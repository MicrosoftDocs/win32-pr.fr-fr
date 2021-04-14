---
description: 'En savoir plus sur les membres suivants : JET_ENUMCOLUMN'
title: Membres JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a1281d7d81fc4e0db476c4ca0f9ac688a7a7b055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564569"
---
# <a name="jet_enumcolumn-members"></a><span data-ttu-id="55900-103">Membres JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="55900-103">JET_ENUMCOLUMN members</span></span>

<span data-ttu-id="55900-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="55900-104">Include protected members</span></span>  
<span data-ttu-id="55900-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="55900-105">Include inherited members</span></span>  

<span data-ttu-id="55900-106">Énumère les valeurs de colonne d’un enregistrement à l’aide de la fonction JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="55900-106">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="55900-107">JetEnumerateColumns retourne un tableau de structures JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="55900-107">JetEnumerateColumns returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="55900-108">Le tableau est retourné dans la mémoire qui a été allouée à l’aide du rappel fourni à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="55900-108">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

<span data-ttu-id="55900-109">Le type de [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="55900-109">The [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="55900-110">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="55900-110">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55900-111">Nom</span><span class="sxs-lookup"><span data-stu-id="55900-111">Name</span></span></th>
<th><span data-ttu-id="55900-112">Description</span><span class="sxs-lookup"><span data-stu-id="55900-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="55900-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="55900-114"><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55900-115">Haut</span><span class="sxs-lookup"><span data-stu-id="55900-115">Top</span></span>

## <a name="properties"></a><span data-ttu-id="55900-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="55900-116">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55900-117">Nom</span><span class="sxs-lookup"><span data-stu-id="55900-117">Name</span></span></th>
<th><span data-ttu-id="55900-118">Description</span><span class="sxs-lookup"><span data-stu-id="55900-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="55900-120"><a href="dn335137(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="55900-120"><a href="dn335137(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="55900-121">Obtient la taille de la valeur qui a été énumérée pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="55900-121">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="55900-122">Ce membre est utilisé uniquement si <a href="dn335086(v=exchg.10).md">Err</a> est égal à <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="55900-122">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="55900-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="55900-124"><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="55900-125">Obtient le nombre de valeurs de colonne énumérées pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="55900-125">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="55900-126">Ce membre est utilisé uniquement si <a href="dn335086(v=exchg.10).md">Err</a> n’est pas <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="55900-126">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="55900-128"><a href="dn335135(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="55900-128"><a href="dn335135(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="55900-129">Obtient l’ID ColumnID qui a été énuméré.</span><span class="sxs-lookup"><span data-stu-id="55900-129">Gets the columnid ID that was enumerated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="55900-131"><a href="dn335086(v=exchg.10).md">Raise</a></span><span class="sxs-lookup"><span data-stu-id="55900-131"><a href="dn335086(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="55900-132">Obtient le code d’état de la colonne qui résulte de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="55900-132">Gets the column status code that results from the enumeration.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="55900-134"><a href="dn335087(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="55900-134"><a href="dn335087(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="55900-135">Obtient la valeur qui a été énumérée pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="55900-135">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="55900-136">Ce membre est utilisé uniquement si <a href="dn335086(v=exchg.10).md">Err</a> est égal à <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="55900-136">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is equal to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span> <span data-ttu-id="55900-137">Cela pointe vers la mémoire allouée avec le rappel d’allocateur <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> passé à <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="55900-137">This points to memory allocated with the <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> allocator callback passed to <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>.</span></span> <span data-ttu-id="55900-138">N’oubliez pas de libérer la mémoire une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="55900-138">Remember to release the memory when finished.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="55900-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span><span class="sxs-lookup"><span data-stu-id="55900-140"><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></span></span></td>
<td><span data-ttu-id="55900-141">Obtient les valeurs de colonne énumérées pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="55900-141">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="55900-142">Ce membre est utilisé uniquement si <a href="dn335086(v=exchg.10).md">Err</a> n’est pas <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span><span class="sxs-lookup"><span data-stu-id="55900-142">This member is only used if <a href="dn335086(v=exchg.10).md">err</a> is not <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55900-143">Haut</span><span class="sxs-lookup"><span data-stu-id="55900-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="55900-144">Méthodes</span><span class="sxs-lookup"><span data-stu-id="55900-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="55900-145">Nom</span><span class="sxs-lookup"><span data-stu-id="55900-145">Name</span></span></th>
<th><span data-ttu-id="55900-146">Description</span><span class="sxs-lookup"><span data-stu-id="55900-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="55900-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="55900-148"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="55900-149">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="55900-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="55900-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="55900-151"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="55900-152">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="55900-152">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="55900-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="55900-154"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="55900-155">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="55900-155">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="55900-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="55900-157"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="55900-158">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="55900-158">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="55900-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="55900-160"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="55900-161">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="55900-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="55900-163"><a href="dn335132(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="55900-163"><a href="dn335132(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="55900-164">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="55900-164">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>.</span></span> <span data-ttu-id="55900-165">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="55900-165">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55900-166">Haut</span><span class="sxs-lookup"><span data-stu-id="55900-166">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="55900-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55900-167">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55900-168">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="55900-168">Reference</span></span>

[<span data-ttu-id="55900-169">Classe JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="55900-169">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="55900-170">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="55900-170">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
