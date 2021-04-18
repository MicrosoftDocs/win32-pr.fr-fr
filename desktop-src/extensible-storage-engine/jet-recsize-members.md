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
# <a name="jet_recsize-members"></a><span data-ttu-id="e2d30-103">Membres JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="e2d30-103">JET_RECSIZE members</span></span>

<span data-ttu-id="e2d30-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="e2d30-104">Include protected members</span></span>  
<span data-ttu-id="e2d30-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="e2d30-105">Include inherited members</span></span>  

<span data-ttu-id="e2d30-106">Utilisé par [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) pour retourner des informations sur les exigences d’utilisation d’un enregistrement dans l’espace de données utilisateur, le nombre de colonnes définies, le nombre de valeurs et l’espace de charge de structure d’enregistrement esent.</span><span class="sxs-lookup"><span data-stu-id="e2d30-106">Used by [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESENT record structure overhead space.</span></span>

<span data-ttu-id="e2d30-107">Le type de [JET_RECSIZE](./jet-recsize-structure2.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="e2d30-107">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="e2d30-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2d30-108">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e2d30-109">Nom</span><span class="sxs-lookup"><span data-stu-id="e2d30-109">Name</span></span></th>
<th><span data-ttu-id="e2d30-110">Description</span><span class="sxs-lookup"><span data-stu-id="e2d30-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-112"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-112"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="e2d30-113">Obtient le jeu de données utilisateur dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-113">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-115"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="e2d30-116">Obtient la taille compressée des données utilisateur dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-116">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="e2d30-117">C’est le même que <a href="hh557581(v=exchg.10).md">cbData</a> si aucune valeur long intrinsèque n’est compressée).</span><span class="sxs-lookup"><span data-stu-id="e2d30-117">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-119"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="e2d30-120">Obtient le jeu de données utilisateur dans l’enregistrement, mais stocké dans l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="e2d30-120">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-122"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="e2d30-123">Obtient la taille compressée des données utilisateur dans l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="e2d30-123">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="e2d30-124">C’est le même que <a href="hh557913(v=exchg.10).md">cbLongValueData</a> si aucune valeur long séparée n’est compressée.</span><span class="sxs-lookup"><span data-stu-id="e2d30-124">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-126"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="e2d30-127">Obtient la surcharge des données de valeur long.</span><span class="sxs-lookup"><span data-stu-id="e2d30-127">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-129"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="e2d30-130">Obtient la surcharge de la structure d’enregistrement ESENT pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-130">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="e2d30-131">Cela comprend la taille de la clé de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-131">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-133"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="e2d30-134">Obtient le nombre total de colonnes dans l’enregistrement qui sont compressées.</span><span class="sxs-lookup"><span data-stu-id="e2d30-134">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-136"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="e2d30-137">Obtient le nombre total de valeurs longues stockées dans l’arborescence de valeurs longues pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-137">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="e2d30-138">Cela n’inclut pas les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="e2d30-138">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-140"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="e2d30-141">Obtient l’accumulation du nombre total de valeurs au-delà de la première pour toutes les colonnes de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-141">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-143"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="e2d30-144">Obtient le nombre total de colonnes fixes et variables définies dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-144">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="e2d30-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-146"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="e2d30-147">Obtient le nombre total de colonnes avec balises définies dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e2d30-147">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2d30-148">Haut</span><span class="sxs-lookup"><span data-stu-id="e2d30-148">Top</span></span>

## <a name="methods"></a><span data-ttu-id="e2d30-149">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e2d30-149">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e2d30-150">Nom</span><span class="sxs-lookup"><span data-stu-id="e2d30-150">Name</span></span></th>
<th><span data-ttu-id="e2d30-151">Description</span><span class="sxs-lookup"><span data-stu-id="e2d30-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="e2d30-154"><a href="hh538879(v=exchg.10).md">Ajouter</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-154"><a href="hh538879(v=exchg.10).md">Add</a></span></span></td>
<td><span data-ttu-id="e2d30-155">Ajoutez les tailles dans deux structures de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="e2d30-155">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e2d30-157"><a href="hh558506(v=exchg.10).md">Égal à (objet)</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-157"><a href="hh558506(v=exchg.10).md">Equals(Object)</a></span></span></td>
<td><span data-ttu-id="e2d30-158">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="e2d30-158">Returns a value indicating whether this instance is equal to another instance.</span></span> <span data-ttu-id="e2d30-159">(Substitue <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.)</span><span class="sxs-lookup"><span data-stu-id="e2d30-159">(Overrides <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType.Equals(Object)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e2d30-161"><a href="hh577992(v=exchg.10).md">Égal à (JET_RECSIZE)</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-161"><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></span></span></td>
<td><span data-ttu-id="e2d30-162">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="e2d30-162">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e2d30-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-164"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="e2d30-165">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e2d30-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e2d30-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-167"><a href="hh557078(v=exchg.10).md">GetHashCode</a></span></span></td>
<td><span data-ttu-id="e2d30-168">Retourne le code de hachage de cette instance.</span><span class="sxs-lookup"><span data-stu-id="e2d30-168">Returns the hash code for this instance.</span></span> <span data-ttu-id="e2d30-169">(Substitue <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="e2d30-169">(Overrides <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType.GetHashCode()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e2d30-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-171"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="e2d30-172">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e2d30-172">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="e2d30-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-174"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="e2d30-175">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="e2d30-175">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="e2d30-178"><a href="hh579561(v=exchg.10).md">Soustraire</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-178"><a href="hh579561(v=exchg.10).md">Subtract</a></span></span></td>
<td><span data-ttu-id="e2d30-179">Calculez la différence de tailles entre deux structures de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="e2d30-179">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="e2d30-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-181"><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></span></span></td>
<td><span data-ttu-id="e2d30-182">(Héritée de <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span><span class="sxs-lookup"><span data-stu-id="e2d30-182">(Inherited from <a href="/dotnet/api/system.valuetype">ValueType</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2d30-183">Haut</span><span class="sxs-lookup"><span data-stu-id="e2d30-183">Top</span></span>

## <a name="operators"></a><span data-ttu-id="e2d30-184">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="e2d30-184">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e2d30-185">Nom</span><span class="sxs-lookup"><span data-stu-id="e2d30-185">Name</span></span></th>
<th><span data-ttu-id="e2d30-186">Description</span><span class="sxs-lookup"><span data-stu-id="e2d30-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="e2d30-189"><a href="hh578675(v=exchg.10).md">Complément</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-189"><a href="hh578675(v=exchg.10).md">Addition</a></span></span></td>
<td><span data-ttu-id="e2d30-190">Ajoutez les tailles dans deux structures de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="e2d30-190">Add the sizes in two JET_RECSIZE structures.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="e2d30-193"><a href="hh596362(v=exchg.10).md">Égalité</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-193"><a href="hh596362(v=exchg.10).md">Equality</a></span></span></td>
<td><span data-ttu-id="e2d30-194">Détermine si deux instances spécifiées de JET_RECSIZE sont égales.</span><span class="sxs-lookup"><span data-stu-id="e2d30-194">Determines whether two specified instances of JET_RECSIZE are equal.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="e2d30-197"><a href="hh578809(v=exchg.10).md">Inégalité</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-197"><a href="hh578809(v=exchg.10).md">Inequality</a></span></span></td>
<td><span data-ttu-id="e2d30-198">Détermine si deux instances spécifiées de JET_RECSIZE ne sont pas égales.</span><span class="sxs-lookup"><span data-stu-id="e2d30-198">Determines whether two specified instances of JET_RECSIZE are not equal.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="e2d30-201"><a href="hh596696(v=exchg.10).md">Soustraction</a></span><span class="sxs-lookup"><span data-stu-id="e2d30-201"><a href="hh596696(v=exchg.10).md">Subtraction</a></span></span></td>
<td><span data-ttu-id="e2d30-202">Calculez la différence de tailles entre deux structures de JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="e2d30-202">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2d30-203">Haut</span><span class="sxs-lookup"><span data-stu-id="e2d30-203">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e2d30-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2d30-204">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2d30-205">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="e2d30-205">Reference</span></span>

[<span data-ttu-id="e2d30-206">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="e2d30-206">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="e2d30-207">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="e2d30-207">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
