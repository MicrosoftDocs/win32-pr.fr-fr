---
description: 'En savoir plus sur les membres suivants : JET_INDEXLIST'
title: Membres JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035068"
---
# <a name="jet_indexlist-members"></a><span data-ttu-id="5db95-103">Membres JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="5db95-103">JET_INDEXLIST members</span></span>

<span data-ttu-id="5db95-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="5db95-104">Include protected members</span></span>  
<span data-ttu-id="5db95-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="5db95-105">Include inherited members</span></span>  

<span data-ttu-id="5db95-106">Informations sur une table temporaire contenant des informations sur tous les index d’une table donnée.</span><span class="sxs-lookup"><span data-stu-id="5db95-106">Information about a temporary table containing information about all indexes for a given table.</span></span>

<span data-ttu-id="5db95-107">Le type de [JET_INDEXLIST](./jet-indexlist-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="5db95-107">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="5db95-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="5db95-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5db95-109">Nom</span><span class="sxs-lookup"><span data-stu-id="5db95-109">Name</span></span></th>
<th><span data-ttu-id="5db95-110">Description</span><span class="sxs-lookup"><span data-stu-id="5db95-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="5db95-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span><span class="sxs-lookup"><span data-stu-id="5db95-112"><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5db95-113">Haut</span><span class="sxs-lookup"><span data-stu-id="5db95-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="5db95-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5db95-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5db95-115">Nom</span><span class="sxs-lookup"><span data-stu-id="5db95-115">Name</span></span></th>
<th><span data-ttu-id="5db95-116">Description</span><span class="sxs-lookup"><span data-stu-id="5db95-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="5db95-118"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="5db95-119">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de colonnes dans la clé d’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-119">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="5db95-120">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-120">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="5db95-122"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="5db95-123">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre d’entrées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-123">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="5db95-124">Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="5db95-124">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="5db95-125">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-125">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="5db95-127"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="5db95-128">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de clés uniques dans l’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-128">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="5db95-129">Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="5db95-129">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="5db95-130">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-130">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="5db95-132"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="5db95-133">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le type de colonne de la colonne en cours d’indexation.</span><span class="sxs-lookup"><span data-stu-id="5db95-133">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="5db95-134">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-134">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="5db95-136"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="5db95-137">Obtient le ColumnID de la colonne dans la table temporaire qui stocke la ColumnID de la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="5db95-137">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="5db95-138">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-138">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="5db95-140"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="5db95-141">Obtient le ColumnID de la colonne dans la table temporaire qui stocke les Grbit qui s’appliquent à la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="5db95-141">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="5db95-142">Consultez <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-142">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="5db95-143">La colonne est de type <a href="hh577895(v=exchg.10).md">texte</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-143">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="5db95-145"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="5db95-146">Obtient le ColumnID de la colonne dans la table temporaire qui stocke la page de codes de la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="5db95-146">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="5db95-147">La colonne est de type <a href="hh577895(v=exchg.10).md">short</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-147">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="5db95-149"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="5db95-150">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de pages dans l’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-150">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="5db95-151">Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="5db95-151">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="5db95-152">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-152">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="5db95-154"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="5db95-155">Obtient le ColumnID de la colonne dans la table temporaire qui stocke les Grbit qui s’appliquent à la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="5db95-155">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="5db95-156">Consultez <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-156">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="5db95-157">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-157">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="5db95-159"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="5db95-160">Obtient le ColumnID de la colonne dans la table temporaire qui stocke les grbits utilisés sur l’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-160">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="5db95-161">Consultez <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-161">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="5db95-162">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-162">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="5db95-164"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="5db95-165">Obtient le ColumnID de la colonne dans la table temporaire qui stocke l’index de de cette colonne dans la clé d’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-165">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="5db95-166">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-166">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="5db95-168"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="5db95-169">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nom de l’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-169">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="5db95-170">La colonne est de type <a href="hh577895(v=exchg.10).md">texte</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-170">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="5db95-172"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="5db95-173">Obtient le ColumnID de la colonne dans la table temporaire qui stocke l’ID de langue (LCID) de l’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-173">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="5db95-174">La colonne est de type <a href="hh577895(v=exchg.10).md">short</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-174">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="5db95-176"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="5db95-177">Obtient le ColumnID de la colonne dans la table temporaire qui stocke les indicateurs de normalisation Unicode pour l’index.</span><span class="sxs-lookup"><span data-stu-id="5db95-177">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="5db95-178">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="5db95-178">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="5db95-180"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="5db95-181">Obtient le nombre d’enregistrements dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="5db95-181">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="5db95-183"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="5db95-183"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="5db95-184">Obtient l’TableID de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="5db95-184">Gets tableid of the temporary table.</span></span> <span data-ttu-id="5db95-185">Elle doit être fermée lorsque la table n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5db95-185">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5db95-186">Haut</span><span class="sxs-lookup"><span data-stu-id="5db95-186">Top</span></span>

## <a name="methods"></a><span data-ttu-id="5db95-187">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5db95-187">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="5db95-188">Nom</span><span class="sxs-lookup"><span data-stu-id="5db95-188">Name</span></span></th>
<th><span data-ttu-id="5db95-189">Description</span><span class="sxs-lookup"><span data-stu-id="5db95-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="5db95-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="5db95-191"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="5db95-192">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="5db95-192">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="5db95-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="5db95-194"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="5db95-195">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="5db95-195">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="5db95-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="5db95-197"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="5db95-198">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="5db95-198">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="5db95-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="5db95-200"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="5db95-201">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="5db95-201">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="5db95-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="5db95-203"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="5db95-204">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="5db95-204">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="5db95-206"><a href="dn335165(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="5db95-206"><a href="dn335165(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="5db95-207">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="5db95-207">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>.</span></span> <span data-ttu-id="5db95-208">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="5db95-208">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5db95-209">Haut</span><span class="sxs-lookup"><span data-stu-id="5db95-209">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="5db95-210">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5db95-210">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5db95-211">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="5db95-211">Reference</span></span>

[<span data-ttu-id="5db95-212">Classe JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="5db95-212">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="5db95-213">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5db95-213">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
