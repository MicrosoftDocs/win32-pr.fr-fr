---
description: 'En savoir plus sur les membres suivants : JET_ENUMCOLUMNID'
title: Membres JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_members(v=EXCHG.10)
ms:contentKeyID: 55103504
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f852541d8e16a1a9edfd87afe59a0a8a4c4c4af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033852"
---
# <a name="jet_enumcolumnid-members"></a><span data-ttu-id="ae8c6-103">Membres JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="ae8c6-103">JET_ENUMCOLUMNID members</span></span>

<span data-ttu-id="ae8c6-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="ae8c6-104">Include protected members</span></span>  
<span data-ttu-id="ae8c6-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="ae8c6-105">Include inherited members</span></span>  

<span data-ttu-id="ae8c6-106">Énumère un ensemble spécifique de colonnes et, éventuellement, un ensemble spécifique de plusieurs valeurs pour ces colonnes lorsque la fonction JetEnumerateColumns est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-106">Enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the JetEnumerateColumns function is used.</span></span> <span data-ttu-id="ae8c6-107">JetEnumerateColumns accepte éventuellement un tableau de structures de JET_ENUMCOLUMNID.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-107">JetEnumerateColumns optionally takes an array of JET_ENUMCOLUMNID structures.</span></span>

<span data-ttu-id="ae8c6-108">Le type de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-108">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="ae8c6-109">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="ae8c6-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ae8c6-110">Nom</span><span class="sxs-lookup"><span data-stu-id="ae8c6-110">Name</span></span></th>
<th><span data-ttu-id="ae8c6-111">Description</span><span class="sxs-lookup"><span data-stu-id="ae8c6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ae8c6-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-113"><a href="dn335140(v=exchg.10).md">JET_ENUMCOLUMNID</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae8c6-114">Haut</span><span class="sxs-lookup"><span data-stu-id="ae8c6-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="ae8c6-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ae8c6-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ae8c6-116">Nom</span><span class="sxs-lookup"><span data-stu-id="ae8c6-116">Name</span></span></th>
<th><span data-ttu-id="ae8c6-117">Description</span><span class="sxs-lookup"><span data-stu-id="ae8c6-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ae8c6-119"><a href="dn335141(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-119"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="ae8c6-120">Obtient ou définit l’ID ColumnID à énumérer.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-120">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ae8c6-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-122"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="ae8c6-123">Obtient ou définit le nombre de valeurs de colonne (par index de base un) à énumérer pour l’ID de colonne spécifié.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-123">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="ae8c6-124">Si ctagSequence a la valeur 0 (zéro), rgtagSequence est ignoré et toutes les valeurs de colonne pour l’ID de colonne spécifié seront énumérées.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-124">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ae8c6-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-126"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="ae8c6-127">Obtient ou définit le tableau d’index de base un dans le tableau de valeurs de colonne pour une colonne donnée.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-127">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="ae8c6-128">Un élément unique est un itagSequence qui est défini dans JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-128">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="ae8c6-129">Un itagSequence de 0 (zéro) signifie &quot; Skip &quot; .</span><span class="sxs-lookup"><span data-stu-id="ae8c6-129">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="ae8c6-130">Un itagSequence de 1 signifie que retourne la première valeur de colonne de la colonne, 2 le second, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-130">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae8c6-131">Haut</span><span class="sxs-lookup"><span data-stu-id="ae8c6-131">Top</span></span>

## <a name="methods"></a><span data-ttu-id="ae8c6-132">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ae8c6-132">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ae8c6-133">Nom</span><span class="sxs-lookup"><span data-stu-id="ae8c6-133">Name</span></span></th>
<th><span data-ttu-id="ae8c6-134">Description</span><span class="sxs-lookup"><span data-stu-id="ae8c6-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ae8c6-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-136"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="ae8c6-137">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="ae8c6-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-139"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="ae8c6-140">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ae8c6-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="ae8c6-143">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ae8c6-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="ae8c6-146">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="ae8c6-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="ae8c6-149">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ae8c6-151"><a href="dn335091(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="ae8c6-151"><a href="dn335091(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="ae8c6-152">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-152">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335139(v=exchg.10).md">JET_ENUMCOLUMNID</a>.</span></span> <span data-ttu-id="ae8c6-153">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-153">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae8c6-154">Haut</span><span class="sxs-lookup"><span data-stu-id="ae8c6-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ae8c6-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae8c6-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ae8c6-156">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ae8c6-156">Reference</span></span>

[<span data-ttu-id="ae8c6-157">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="ae8c6-157">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="ae8c6-158">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ae8c6-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
