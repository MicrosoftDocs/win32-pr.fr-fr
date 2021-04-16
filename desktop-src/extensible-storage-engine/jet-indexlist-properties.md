---
description: En savoir plus sur les propriétés de JET_INDEXLIST
title: Propriétés de la JET_INDEXLIST
TOCTitle: JET_INDEXLIST properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_properties(v=EXCHG.10)
ms:contentKeyID: 55103599
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7a1f500f5d51c0487ea490d2051bfc5e4639afbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551784"
---
# <a name="jet_indexlist-properties"></a><span data-ttu-id="67d25-103">Propriétés de la JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="67d25-103">JET_INDEXLIST properties</span></span>

<span data-ttu-id="67d25-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="67d25-104">Include protected members</span></span>  
<span data-ttu-id="67d25-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="67d25-105">Include inherited members</span></span>  

<span data-ttu-id="67d25-106">Le type de [JET_INDEXLIST](./jet-indexlist-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="67d25-106">The [JET_INDEXLIST](./jet-indexlist-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="67d25-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67d25-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="67d25-108">Nom</span><span class="sxs-lookup"><span data-stu-id="67d25-108">Name</span></span></th>
<th><span data-ttu-id="67d25-109">Description</span><span class="sxs-lookup"><span data-stu-id="67d25-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span><span class="sxs-lookup"><span data-stu-id="67d25-111"><a href="dn335125(v=exchg.10).md">columnidcColumn</a></span></span></td>
<td><span data-ttu-id="67d25-112">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de colonnes dans la clé d’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-112">Gets the columnid of the column in the temporary table which stores the number of columns in the index key.</span></span> <span data-ttu-id="67d25-113">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-113">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span><span class="sxs-lookup"><span data-stu-id="67d25-115"><a href="dn335126(v=exchg.10).md">columnidcEntry</a></span></span></td>
<td><span data-ttu-id="67d25-116">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre d’entrées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-116">Gets the columnid of the column in the temporary table which stores the number of entries in the index.</span></span> <span data-ttu-id="67d25-117">Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="67d25-117">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="67d25-118">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-118">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span><span class="sxs-lookup"><span data-stu-id="67d25-120"><a href="dn335127(v=exchg.10).md">columnidcKey</a></span></span></td>
<td><span data-ttu-id="67d25-121">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de clés uniques dans l’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-121">Gets the columnid of the column in the temporary table which stores the number of unique keys in the index.</span></span> <span data-ttu-id="67d25-122">Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="67d25-122">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="67d25-123">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-123">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span><span class="sxs-lookup"><span data-stu-id="67d25-125"><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></span></span></td>
<td><span data-ttu-id="67d25-126">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le type de colonne de la colonne en cours d’indexation.</span><span class="sxs-lookup"><span data-stu-id="67d25-126">Gets the columnid of the column in the temporary table which stores the column type of the column being indexed.</span></span> <span data-ttu-id="67d25-127">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-127">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="67d25-129"><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></span></span></td>
<td><span data-ttu-id="67d25-130">Obtient le ColumnID de la colonne dans la table temporaire qui stocke la ColumnID de la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="67d25-130">Gets the columnid of the column in the temporary table which stores the columnid of the column being indexed.</span></span> <span data-ttu-id="67d25-131">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-131">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span><span class="sxs-lookup"><span data-stu-id="67d25-133"><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></span></span></td>
<td><span data-ttu-id="67d25-134">Obtient le ColumnID de la colonne dans la table temporaire qui stocke les Grbit qui s’appliquent à la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="67d25-134">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="67d25-135">Consultez <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-135">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="67d25-136">La colonne est de type <a href="hh577895(v=exchg.10).md">texte</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-136">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span><span class="sxs-lookup"><span data-stu-id="67d25-138"><a href="dn335168(v=exchg.10).md">columnidCp</a></span></span></td>
<td><span data-ttu-id="67d25-139">Obtient le ColumnID de la colonne dans la table temporaire qui stocke la page de codes de la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="67d25-139">Gets the columnid of the column in the temporary table which stores the code page of the indexed column.</span></span> <span data-ttu-id="67d25-140">La colonne est de type <a href="hh577895(v=exchg.10).md">short</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-140">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span><span class="sxs-lookup"><span data-stu-id="67d25-142"><a href="dn335136(v=exchg.10).md">columnidcPage</a></span></span></td>
<td><span data-ttu-id="67d25-143">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nombre de pages dans l’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-143">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="67d25-144">Cette valeur n’est pas actuelle et est uniquement mise à jour par &quot; API. JetComputeStats &quot; .</span><span class="sxs-lookup"><span data-stu-id="67d25-144">This value is not current and is only is updated by &quot;Api.JetComputeStats&quot;.</span></span> <span data-ttu-id="67d25-145">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-145">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span><span class="sxs-lookup"><span data-stu-id="67d25-147"><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></span></span></td>
<td><span data-ttu-id="67d25-148">Obtient le ColumnID de la colonne dans la table temporaire qui stocke les Grbit qui s’appliquent à la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="67d25-148">Gets the columnid of the column in the temporary table which stores the grbit that apply to the indexed column.</span></span> <span data-ttu-id="67d25-149">Consultez <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-149">See <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>.</span></span> <span data-ttu-id="67d25-150">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-150">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span><span class="sxs-lookup"><span data-stu-id="67d25-152"><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></span></span></td>
<td><span data-ttu-id="67d25-153">Obtient le ColumnID de la colonne dans la table temporaire qui stocke les grbits utilisés sur l’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-153">Gets the columnid of the column in the temporary table which stores the grbits used on the index.</span></span> <span data-ttu-id="67d25-154">Consultez <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-154">See <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>.</span></span> <span data-ttu-id="67d25-155">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-155">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span><span class="sxs-lookup"><span data-stu-id="67d25-157"><a href="dn335170(v=exchg.10).md">columnidiColumn</a></span></span></td>
<td><span data-ttu-id="67d25-158">Obtient le ColumnID de la colonne dans la table temporaire qui stocke l’index de de cette colonne dans la clé d’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-158">Gets the columnid of the column in the temporary table which stores the index of of this column in the index key.</span></span> <span data-ttu-id="67d25-159">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-159">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span><span class="sxs-lookup"><span data-stu-id="67d25-161"><a href="dn335138(v=exchg.10).md">columnidindexname</a></span></span></td>
<td><span data-ttu-id="67d25-162">Obtient le ColumnID de la colonne dans la table temporaire qui stocke le nom de l’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-162">Gets the columnid of the column in the temporary table which stores the name of the index.</span></span> <span data-ttu-id="67d25-163">La colonne est de type <a href="hh577895(v=exchg.10).md">texte</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-163">The column is of type <a href="hh577895(v=exchg.10).md">Text</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span><span class="sxs-lookup"><span data-stu-id="67d25-165"><a href="dn335171(v=exchg.10).md">columnidLangid</a></span></span></td>
<td><span data-ttu-id="67d25-166">Obtient le ColumnID de la colonne dans la table temporaire qui stocke l’ID de langue (LCID) de l’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-166">Gets the columnid of the column in the temporary table which stores the language id (LCID) of the index.</span></span> <span data-ttu-id="67d25-167">La colonne est de type <a href="hh577895(v=exchg.10).md">short</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-167">The column is of type <a href="hh577895(v=exchg.10).md">Short</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span><span class="sxs-lookup"><span data-stu-id="67d25-169"><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></span></span></td>
<td><span data-ttu-id="67d25-170">Obtient le ColumnID de la colonne dans la table temporaire qui stocke les indicateurs de normalisation Unicode pour l’index.</span><span class="sxs-lookup"><span data-stu-id="67d25-170">Gets the columnid of the column in the temporary table which stores the unicode normalization flags for the index.</span></span> <span data-ttu-id="67d25-171">La colonne est de type <a href="hh577895(v=exchg.10).md">long</a>.</span><span class="sxs-lookup"><span data-stu-id="67d25-171">The column is of type <a href="hh577895(v=exchg.10).md">Long</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span><span class="sxs-lookup"><span data-stu-id="67d25-173"><a href="dn335173(v=exchg.10).md">cRecord</a></span></span></td>
<td><span data-ttu-id="67d25-174">Obtient le nombre d’enregistrements dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="67d25-174">Gets the number of records in the temporary table.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="67d25-176"><a href="dn335174(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="67d25-176"><a href="dn335174(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="67d25-177">Obtient l’TableID de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="67d25-177">Gets tableid of the temporary table.</span></span> <span data-ttu-id="67d25-178">Elle doit être fermée lorsque la table n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="67d25-178">This should be closed when the table is no longer needed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="67d25-179">Haut</span><span class="sxs-lookup"><span data-stu-id="67d25-179">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="67d25-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67d25-180">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="67d25-181">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="67d25-181">Reference</span></span>

[<span data-ttu-id="67d25-182">Classe JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="67d25-182">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="67d25-183">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="67d25-183">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
