---
description: 'En savoir plus sur : structure JET_INDEXLIST'
title: Structure JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319774"
---
# <a name="jet_indexlist-structure"></a><span data-ttu-id="9e057-103">Structure JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="9e057-103">JET_INDEXLIST Structure</span></span>


<span data-ttu-id="9e057-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="9e057-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexlist-structure"></a><span data-ttu-id="9e057-105">Structure JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="9e057-105">JET_INDEXLIST Structure</span></span>

<span data-ttu-id="9e057-106">La structure **JET_INDEXLIST** contient les informations nécessaires pour traverser une table temporaire créée par les fonctions [JetGetIndexInfo](./jetgetindexinfo-function.md) ou [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="9e057-106">The **JET_INDEXLIST** structure contains the necessary information to traverse a temporary table that is created by the [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md) functions.</span></span> <span data-ttu-id="9e057-107">Chaque ligne de la table temporaire décrit une colonne d’un index.</span><span class="sxs-lookup"><span data-stu-id="9e057-107">Each row in the temporary table describes a column of an index.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a><span data-ttu-id="9e057-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9e057-108">Members</span></span>

<span data-ttu-id="9e057-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="9e057-109">**cbStruct**</span></span>

<span data-ttu-id="9e057-110">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="9e057-110">The size of the structure in bytes.</span></span> <span data-ttu-id="9e057-111">L’appel d’API met à jour ce champ, de sorte que l’appelant doit s’assurer que cette valeur correspond à sizeof (JET_INDEXLIST).</span><span class="sxs-lookup"><span data-stu-id="9e057-111">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_INDEXLIST ).</span></span>

<span data-ttu-id="9e057-112">**TableID**</span><span class="sxs-lookup"><span data-stu-id="9e057-112">**tableid**</span></span>

<span data-ttu-id="9e057-113">Identificateur de table de la table temporaire qui a été créée.</span><span class="sxs-lookup"><span data-stu-id="9e057-113">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="9e057-114">Il incombe à l’appelant de fermer la table.</span><span class="sxs-lookup"><span data-stu-id="9e057-114">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="9e057-115">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="9e057-115">**cRecord**</span></span>

<span data-ttu-id="9e057-116">Nombre d’enregistrements dans la table temporaire qui a été créée.</span><span class="sxs-lookup"><span data-stu-id="9e057-116">The number of records in the temporary table that was created.</span></span>

<span data-ttu-id="9e057-117">**columnidindexname**</span><span class="sxs-lookup"><span data-stu-id="9e057-117">**columnidindexname**</span></span>

<span data-ttu-id="9e057-118">Identificateur de colonne du nom de l’index.</span><span class="sxs-lookup"><span data-stu-id="9e057-118">The column identifier of the name of the index.</span></span>

<span data-ttu-id="9e057-119">Cette colonne est une [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-119">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-120">**columnidgrbitIndex**</span><span class="sxs-lookup"><span data-stu-id="9e057-120">**columnidgrbitIndex**</span></span>

<span data-ttu-id="9e057-121">Identificateur de colonne du *grbits* utilisé sur l’index.</span><span class="sxs-lookup"><span data-stu-id="9e057-121">The column identifier of the *grbits* used on the index.</span></span> <span data-ttu-id="9e057-122">Pour obtenir la liste des bits valides, consultez [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="9e057-122">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for a list of valid bits.</span></span>

<span data-ttu-id="9e057-123">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-123">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-124">**columnidcKey**</span><span class="sxs-lookup"><span data-stu-id="9e057-124">**columnidcKey**</span></span>

<span data-ttu-id="9e057-125">Identificateur de colonne du nombre de clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9e057-125">The column identifier of the number of keys in the index.</span></span>

<span data-ttu-id="9e057-126">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-126">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-127">**columnidcEntry**</span><span class="sxs-lookup"><span data-stu-id="9e057-127">**columnidcEntry**</span></span>

<span data-ttu-id="9e057-128">Identificateur de colonne du nombre d’entrées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9e057-128">The column identifier of the number of entries in the index.</span></span>

<span data-ttu-id="9e057-129">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-129">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-130">**columnidcPage**</span><span class="sxs-lookup"><span data-stu-id="9e057-130">**columnidcPage**</span></span>

<span data-ttu-id="9e057-131">Identificateur de colonne du nombre de pages utilisées par l’index. Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-131">The column identifier of the number of pages the index uses.This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-132">**columnidcColumn**</span><span class="sxs-lookup"><span data-stu-id="9e057-132">**columnidcColumn**</span></span>

<span data-ttu-id="9e057-133">Identificateur de colonne du nombre total de colonnes sur lesquelles l’index s’étend.</span><span class="sxs-lookup"><span data-stu-id="9e057-133">The column identifier of the total number of columns that the index spans.</span></span>

<span data-ttu-id="9e057-134">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-134">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-135">**columnidiColumn**</span><span class="sxs-lookup"><span data-stu-id="9e057-135">**columnidiColumn**</span></span>

<span data-ttu-id="9e057-136">Identificateur de colonne du nombre de colonnes dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9e057-136">The column identifier of the number of the columns in the index.</span></span> <span data-ttu-id="9e057-137">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9e057-137">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="9e057-138">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-138">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e057-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e057-139">Value</span></span></p></th>
<th><p><span data-ttu-id="9e057-140">Signification</span><span class="sxs-lookup"><span data-stu-id="9e057-140">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e057-141">cIndexInfoCols</span><span class="sxs-lookup"><span data-stu-id="9e057-141">cIndexInfoCols</span></span><br />
<span data-ttu-id="9e057-142">15</span><span class="sxs-lookup"><span data-stu-id="9e057-142">15</span></span></p></td>
<td><p><span data-ttu-id="9e057-143">Spécifie que 15 colonnes sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="9e057-143">Specifies that 15 columns are allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e057-144">cColumnInfoCols</span><span class="sxs-lookup"><span data-stu-id="9e057-144">cColumnInfoCols</span></span><br />
<span data-ttu-id="9e057-145">14</span><span class="sxs-lookup"><span data-stu-id="9e057-145">14</span></span></p></td>
<td><p><span data-ttu-id="9e057-146">Spécifie que 14 colonnes sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="9e057-146">Specifies that 14 columns are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e057-147">cObjectInfoCols</span><span class="sxs-lookup"><span data-stu-id="9e057-147">cObjectInfoCols</span></span><br />
<span data-ttu-id="9e057-148">9</span><span class="sxs-lookup"><span data-stu-id="9e057-148">9</span></span></p></td>
<td><p><span data-ttu-id="9e057-149">Spécifie que 9 colonnes sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="9e057-149">Specifies that 9 columns are allowed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e057-150">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="9e057-150">**columnidcolumnid**</span></span>

<span data-ttu-id="9e057-151">Identificateur de colonne de la colonne indexée. Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9e057-151">The column identifier of the column that is indexed.For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="9e057-152">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-152">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-153">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="9e057-153">**columnidcoltyp**</span></span>

<span data-ttu-id="9e057-154">Identificateur de colonne de la coltyp de la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="9e057-154">The column identifier of the coltyp of the column which is indexed.</span></span> <span data-ttu-id="9e057-155">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="9e057-155">For more information, see the Remarks section of this topic.</span></span> <span data-ttu-id="9e057-156">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-156">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-157">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="9e057-157">**columnidCountry**</span></span>

<span data-ttu-id="9e057-158">Identificateur de colonne de l’indicatif de pays de la colonne indexée.</span><span class="sxs-lookup"><span data-stu-id="9e057-158">The column identifier of the country code of the column that is indexed.</span></span> <span data-ttu-id="9e057-159">L’indicatif du pays est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="9e057-159">The country code is deprecated.</span></span>

<span data-ttu-id="9e057-160">Cette colonne est une [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-160">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-161">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="9e057-161">**columnidLangid**</span></span>

<span data-ttu-id="9e057-162">Identificateur de colonne de l’identificateur de langue (LCID) sous lequel l’index a été créé.</span><span class="sxs-lookup"><span data-stu-id="9e057-162">The column identifier of the language identifier (LCID) under which the index was created.</span></span> <span data-ttu-id="9e057-163">Pour plus d’informations, consultez [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-163">For more information, see [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<span data-ttu-id="9e057-164">Cette colonne est une [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-164">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-165">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="9e057-165">**columnidCp**</span></span>

<span data-ttu-id="9e057-166">Identificateur de colonne de la page de codes sous laquelle l’index a été créé.</span><span class="sxs-lookup"><span data-stu-id="9e057-166">The column identifier of the code page under which the index was created.</span></span> <span data-ttu-id="9e057-167">Pour plus d’informations, consultez [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-167">For more information, see [JET_COLUMNCREATE](./jet-columncreate-structure.md).</span></span>

<span data-ttu-id="9e057-168">Cette colonne est une [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-168">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-169">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="9e057-169">**columnidCollate**</span></span>

<span data-ttu-id="9e057-170">Identificateur de colonne de la séquence de classement sous laquelle l’index a été créé.</span><span class="sxs-lookup"><span data-stu-id="9e057-170">The column identifier of the collation sequence under which the index was created.</span></span> <span data-ttu-id="9e057-171">La séquence de classement est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9e057-171">The collation sequence is deprecated.</span></span>

<span data-ttu-id="9e057-172">Cette colonne est une [JET_coltypShort](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-172">This column is a [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-173">**columnidgrbitColumn**</span><span class="sxs-lookup"><span data-stu-id="9e057-173">**columnidgrbitColumn**</span></span>

<span data-ttu-id="9e057-174">Identificateur de colonne des *grbits* qui s’appliquent à l’ordre de la colonne dans l’index.</span><span class="sxs-lookup"><span data-stu-id="9e057-174">The column identifier of the *grbits* that apply to the order of the column in the index.</span></span>

<span data-ttu-id="9e057-175">Les données de cette colonne peuvent être classées en tant que JET_bitKeyAscending ou JET_bitKeyDescending.</span><span class="sxs-lookup"><span data-stu-id="9e057-175">The data for this column can be ordered as JET_bitKeyAscending or JET_bitKeyDescending.</span></span> <span data-ttu-id="9e057-176">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-176">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="9e057-177">Par exemple, un index défini en tant que « -Column1 \\ 0 + Column2 \\ 0 » aura JET_bitKeyDescending pour « Column1 » et JET_bitKeyAscending pour « Column2 ».</span><span class="sxs-lookup"><span data-stu-id="9e057-177">For example, an index defined as "-column1\\0+column2\\0" will have JET_bitKeyDescending for "column1", and JET_bitKeyAscending for "column2".</span></span>

<span data-ttu-id="9e057-178">Les options suivantes sont valides pour ce membre.</span><span class="sxs-lookup"><span data-stu-id="9e057-178">The following options are valid for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e057-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e057-179">Value</span></span></p></th>
<th><p><span data-ttu-id="9e057-180">Signification</span><span class="sxs-lookup"><span data-stu-id="9e057-180">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e057-181">JET_bitKeyAscending</span><span class="sxs-lookup"><span data-stu-id="9e057-181">JET_bitKeyAscending</span></span></p></td>
<td><p><span data-ttu-id="9e057-182">Segment d’index dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="9e057-182">An index segment in ascending order.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e057-183">JET_bitKeyDescending</span><span class="sxs-lookup"><span data-stu-id="9e057-183">JET_bitKeyDescending</span></span></p></td>
<td><p><span data-ttu-id="9e057-184">Segment d’index dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="9e057-184">An index segment in descending order.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e057-185">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="9e057-185">**columnidcolumnname**</span></span>

<span data-ttu-id="9e057-186">Identificateur de colonne du nom de la colonne.</span><span class="sxs-lookup"><span data-stu-id="9e057-186">The column identifier of the name of the column.</span></span>

<span data-ttu-id="9e057-187">Cette colonne est une [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-187">This column is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="9e057-188">**columnidLCMapFlags**</span><span class="sxs-lookup"><span data-stu-id="9e057-188">**columnidLCMapFlags**</span></span>

<span data-ttu-id="9e057-189">Identificateur de colonne des indicateurs utilisés pour créer l’index.</span><span class="sxs-lookup"><span data-stu-id="9e057-189">The column identifier of the flags that are used to create the index.</span></span> <span data-ttu-id="9e057-190">Pour plus d’informations, consultez la section **dwMapFlags** de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-190">For more information, see the **dwMapFlags** section of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).</span></span>

<span data-ttu-id="9e057-191">Cette colonne est une [JET_coltypLong](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="9e057-191">This column is a [JET_coltypLong](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="9e057-192">Notes</span><span class="sxs-lookup"><span data-stu-id="9e057-192">Remarks</span></span>

<span data-ttu-id="9e057-193">Chaque ligne de la table temporaire correspond à une colonne dans un index particulier.</span><span class="sxs-lookup"><span data-stu-id="9e057-193">Each row in the temporary table corresponds to a column in a particular index.</span></span>

<span data-ttu-id="9e057-194">Par exemple, l’index « + A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E \\ 0 » est supérieur à cinq colonnes et occupe cinq lignes dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="9e057-194">For example, the index "+A\\0+B\\0+C\\0+D\\0+E\\0" is more than five columns, and it will occupy five rows in the temporary table.</span></span> <span data-ttu-id="9e057-195">Chacune de ces cinq lignes aura une valeur de 5 dans la colonne identifiée par la colonne ColumnID.</span><span class="sxs-lookup"><span data-stu-id="9e057-195">Each of these five rows will have a value of 5 in the column that is identified by columnid column.</span></span> <span data-ttu-id="9e057-196">Toutefois, chaque ligne a une valeur différente pour la colonne ColumnId, comprise entre 0 et 4.</span><span class="sxs-lookup"><span data-stu-id="9e057-196">But each row will have a different value for columnid column, ranging from 0 to 4.</span></span>

<span data-ttu-id="9e057-197">Le nombre de clés dans un index particulier correspond au nombre de valeurs uniques qu’un appelant peut rechercher et obtenir une correspondance exacte.</span><span class="sxs-lookup"><span data-stu-id="9e057-197">The number of keys in a particular index corresponds to the number of unique values for which a caller can seek and get an exact match.</span></span> <span data-ttu-id="9e057-198">Le nombre d’entrées est le nombre de lignes correspondant à un index.</span><span class="sxs-lookup"><span data-stu-id="9e057-198">The number of entries is the number of rows that an index matches.</span></span> <span data-ttu-id="9e057-199">Si un index a une contrainte d’unicité, le nombre de clés est égal au nombre d’entrées.</span><span class="sxs-lookup"><span data-stu-id="9e057-199">If an index has a uniqueness constraint, then the number of keys is equal to the number of entries.</span></span> <span data-ttu-id="9e057-200">Par exemple, si une table contient les informations suivantes et qu’un index est créé sur la colonne nommée « Key », il existe trois clés (100, 200 et 500), mais il existe quatre entrées (« This », « is », « an » et « example »).</span><span class="sxs-lookup"><span data-stu-id="9e057-200">For example, if a table contains the following information and an index is created over the column named "key", then there are three keys (100, 200, and 500), but there are four entries ("this", "is", "an", and "example").</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e057-201">Clé</span><span class="sxs-lookup"><span data-stu-id="9e057-201">Key</span></span></p></th>
<th><p><span data-ttu-id="9e057-202">Entrée</span><span class="sxs-lookup"><span data-stu-id="9e057-202">Entry</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e057-203">100</span><span class="sxs-lookup"><span data-stu-id="9e057-203">100</span></span></p></td>
<td><p><span data-ttu-id="9e057-204">&quot;this&quot;</span><span class="sxs-lookup"><span data-stu-id="9e057-204">&quot;this&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e057-205">100</span><span class="sxs-lookup"><span data-stu-id="9e057-205">100</span></span></p></td>
<td><p><span data-ttu-id="9e057-206">&quot;is&quot;</span><span class="sxs-lookup"><span data-stu-id="9e057-206">&quot;is&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e057-207">200</span><span class="sxs-lookup"><span data-stu-id="9e057-207">200</span></span></p></td>
<td><p><span data-ttu-id="9e057-208">&quot;pièce&quot;</span><span class="sxs-lookup"><span data-stu-id="9e057-208">&quot;an&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e057-209">500</span><span class="sxs-lookup"><span data-stu-id="9e057-209">500</span></span></p></td>
<td><p><span data-ttu-id="9e057-210">&quot;example&quot;</span><span class="sxs-lookup"><span data-stu-id="9e057-210">&quot;example&quot;</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="9e057-211">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e057-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e057-212"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9e057-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9e057-213">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="9e057-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e057-214"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="9e057-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9e057-215">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9e057-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e057-216"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="9e057-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9e057-217">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="9e057-217">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9e057-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e057-218">See Also</span></span>

[<span data-ttu-id="9e057-219">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="9e057-219">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="9e057-220">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="9e057-220">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="9e057-221">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9e057-221">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="9e057-222">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9e057-222">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9e057-223">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9e057-223">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9e057-224">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="9e057-224">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="9e057-225">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9e057-225">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9e057-226">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9e057-226">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9e057-227">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="9e057-227">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="9e057-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9e057-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="9e057-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9e057-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)
