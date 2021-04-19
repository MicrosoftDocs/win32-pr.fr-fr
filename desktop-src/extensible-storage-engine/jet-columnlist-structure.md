---
description: 'En savoir plus sur : structure JET_COLUMNLIST'
title: Structure JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 9bce36c818dd35408d95c770540ff4865bdf639b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531673"
---
# <a name="jet_columnlist-structure"></a><span data-ttu-id="19fd2-103">Structure JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="19fd2-103">JET_COLUMNLIST Structure</span></span>


<span data-ttu-id="19fd2-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="19fd2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnlist-structure"></a><span data-ttu-id="19fd2-105">Structure JET_COLUMNLIST</span><span class="sxs-lookup"><span data-stu-id="19fd2-105">JET_COLUMNLIST Structure</span></span>

<span data-ttu-id="19fd2-106">La structure **JET_COLUMNLIST** contient les informations nécessaires pour parcourir la table temporaire créée par les fonctions [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) .</span><span class="sxs-lookup"><span data-stu-id="19fd2-106">The **JET_COLUMNLIST** structure contains the information necessary to traverse the temporary table that is created by the [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions.</span></span> <span data-ttu-id="19fd2-107">Chaque ligne de la table temporaire décrit une colonne de la table spécifiée dans l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="19fd2-107">Each row in the temporary table describes a column in the table given in the API call.</span></span> <span data-ttu-id="19fd2-108">Cette structure est utilisée uniquement avec [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="19fd2-108">This structure is used with only with [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a><span data-ttu-id="19fd2-109">Membres</span><span class="sxs-lookup"><span data-stu-id="19fd2-109">Members</span></span>

<span data-ttu-id="19fd2-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="19fd2-110">**cbStruct**</span></span>

<span data-ttu-id="19fd2-111">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="19fd2-111">The size of the structure in bytes.</span></span> <span data-ttu-id="19fd2-112">L’appel d’API met à jour ce champ, de sorte que l’appelant doit s’assurer que cette valeur correspond à sizeof (JET_COLUMNLIST).</span><span class="sxs-lookup"><span data-stu-id="19fd2-112">The API call will update this field, so the caller should ensure that this value matches sizeof( JET_COLUMNLIST ).</span></span>

<span data-ttu-id="19fd2-113">**TableID**</span><span class="sxs-lookup"><span data-stu-id="19fd2-113">**tableid**</span></span>

<span data-ttu-id="19fd2-114">Identificateur de table de la table temporaire qui a été créée.</span><span class="sxs-lookup"><span data-stu-id="19fd2-114">The table identifier of the temporary table that was created.</span></span> <span data-ttu-id="19fd2-115">Il incombe à l’appelant de fermer la table.</span><span class="sxs-lookup"><span data-stu-id="19fd2-115">It is the responsibility of the caller to close the table.</span></span>

<span data-ttu-id="19fd2-116">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="19fd2-116">**cRecord**</span></span>

<span data-ttu-id="19fd2-117">Nombre d’enregistrements dans la table temporaire qui a été créée par l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="19fd2-117">The number of records in the temporary table that was created by the API call.</span></span>

<span data-ttu-id="19fd2-118">**columnidPresentationOrder**</span><span class="sxs-lookup"><span data-stu-id="19fd2-118">**columnidPresentationOrder**</span></span>

<span data-ttu-id="19fd2-119">Identificateur de colonne de l’ordre de présentation.</span><span class="sxs-lookup"><span data-stu-id="19fd2-119">The column identifier of the presentation order.</span></span>

<span data-ttu-id="19fd2-120">L’ordre de présentation est utilisé pour trier les lignes de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="19fd2-120">The presentation order is used to sort the rows of the temporary table.</span></span> <span data-ttu-id="19fd2-121">L’ordre de présentation est un [JET_coltypLong](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-121">The presentation order is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="19fd2-122">Si le niveau d’information spécifié n’était pas un niveau compact, il est également marqué comme JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="19fd2-122">If the information level that was specified was not a compact level, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="19fd2-123">**columnidcolumnname**</span><span class="sxs-lookup"><span data-stu-id="19fd2-123">**columnidcolumnname**</span></span>

<span data-ttu-id="19fd2-124">Identificateur de colonne du nom de la colonne.</span><span class="sxs-lookup"><span data-stu-id="19fd2-124">The column identifier of the name of the column.</span></span>

<span data-ttu-id="19fd2-125">Si le niveau d’information spécifié n’était pas compact, il est également marqué comme JET_bitColumnTTKey.</span><span class="sxs-lookup"><span data-stu-id="19fd2-125">If the information level specified was not compact, then it is also marked as JET_bitColumnTTKey.</span></span>

<span data-ttu-id="19fd2-126">**columnidcolumnid**</span><span class="sxs-lookup"><span data-stu-id="19fd2-126">**columnidcolumnid**</span></span>

<span data-ttu-id="19fd2-127">Identificateur de colonne de l’identificateur de colonne.</span><span class="sxs-lookup"><span data-stu-id="19fd2-127">The column identifier of the column identifier.</span></span>

<span data-ttu-id="19fd2-128">L’identificateur de colonne est un [JET_coltypLong](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-128">The column identifier is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-129">**columnidcoltyp**</span><span class="sxs-lookup"><span data-stu-id="19fd2-129">**columnidcoltyp**</span></span>

<span data-ttu-id="19fd2-130">Identificateur de colonne du type de colonne.</span><span class="sxs-lookup"><span data-stu-id="19fd2-130">The column identifier of the column type.</span></span>

<span data-ttu-id="19fd2-131">Le type de colonne est un [JET_coltypLong](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-131">The column type is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-132">**columnidCountry**</span><span class="sxs-lookup"><span data-stu-id="19fd2-132">**columnidCountry**</span></span>

<span data-ttu-id="19fd2-133">Identificateur de colonne de l’indicatif du pays.</span><span class="sxs-lookup"><span data-stu-id="19fd2-133">The column identifier of the country code.</span></span>

<span data-ttu-id="19fd2-134">L’indicatif du pays est un [JET_coltypShort](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-134">The country code is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-135">**columnidLangid**</span><span class="sxs-lookup"><span data-stu-id="19fd2-135">**columnidLangid**</span></span>

<span data-ttu-id="19fd2-136">Identificateur de colonne de l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="19fd2-136">The column identifier of the language identifier.</span></span>

<span data-ttu-id="19fd2-137">L’identificateur de langue est un [JET_coltypShort](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-137">The language identifier is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-138">**columnidCp**</span><span class="sxs-lookup"><span data-stu-id="19fd2-138">**columnidCp**</span></span>

<span data-ttu-id="19fd2-139">Identificateur de colonne de la page de codes.</span><span class="sxs-lookup"><span data-stu-id="19fd2-139">The column identifier of the code page.</span></span>

<span data-ttu-id="19fd2-140">La page de codes est un [JET_coltypShort](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-140">The code page is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-141">**columnidCollate**</span><span class="sxs-lookup"><span data-stu-id="19fd2-141">**columnidCollate**</span></span>

<span data-ttu-id="19fd2-142">Identificateur de colonne de la séquence de classement.</span><span class="sxs-lookup"><span data-stu-id="19fd2-142">The column identifier of the collation sequence.</span></span>

<span data-ttu-id="19fd2-143">La séquence de classement est un [JET_coltypShort](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-143">The collation sequence is a fixed [JET_coltypShort](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-144">**columnidcbMax**</span><span class="sxs-lookup"><span data-stu-id="19fd2-144">**columnidcbMax**</span></span>

<span data-ttu-id="19fd2-145">Identificateur de colonne du champ **cbMax** .</span><span class="sxs-lookup"><span data-stu-id="19fd2-145">The column identifier of the **cbMax** field.</span></span>

<span data-ttu-id="19fd2-146">Le **cbMax** est un [JET_coltypLong](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-146">The **cbMax** is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-147">**columnidgrbit**</span><span class="sxs-lookup"><span data-stu-id="19fd2-147">**columnidgrbit**</span></span>

<span data-ttu-id="19fd2-148">Identificateur de colonne du *grbits* de la colonne.</span><span class="sxs-lookup"><span data-stu-id="19fd2-148">The column identifier of the *grbits* of the column.</span></span> <span data-ttu-id="19fd2-149">Le champ *Grbit* est un [JET_coltypLong](./jet-coltyp.md)fixe.</span><span class="sxs-lookup"><span data-stu-id="19fd2-149">The *grbit* field is a fixed [JET_coltypLong](./jet-coltyp.md).</span></span> <span data-ttu-id="19fd2-150">Pour plus d’informations sur ces bits, consultez [JET_COLUMNDEF](./jet-columndef-structure.md).</span><span class="sxs-lookup"><span data-stu-id="19fd2-150">For more information about these bits, see [JET_COLUMNDEF](./jet-columndef-structure.md).</span></span>

<span data-ttu-id="19fd2-151">Les valeurs possibles pour **columnidgrbit** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="19fd2-151">The following are possible values for **columnidgrbit**:</span></span>

<span data-ttu-id="19fd2-152">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="19fd2-152">JET_bitColumnTagged</span></span>

<span data-ttu-id="19fd2-153">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="19fd2-153">JET_bitColumnFixed</span></span>

<span data-ttu-id="19fd2-154">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="19fd2-154">JET_bitColumnUpdatable</span></span>

<span data-ttu-id="19fd2-155">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="19fd2-155">JET_bitColumnNotNULL</span></span>

<span data-ttu-id="19fd2-156">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="19fd2-156">JET_bitColumnAutoincrement</span></span>

<span data-ttu-id="19fd2-157">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="19fd2-157">JET_bitColumnVersion</span></span>

<span data-ttu-id="19fd2-158">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="19fd2-158">JET_bitColumnMultiValued</span></span>

<span data-ttu-id="19fd2-159">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="19fd2-159">JET_bitColumnEscrowUpdate</span></span>

<span data-ttu-id="19fd2-160">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="19fd2-160">JET_bitColumnFinalize</span></span>

<span data-ttu-id="19fd2-161">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="19fd2-161">JET_bitColumnDeleteOnZero</span></span>

<span data-ttu-id="19fd2-162">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="19fd2-162">JET_bitColumnUserDefinedDefault</span></span>

<span data-ttu-id="19fd2-163">**columnidDefault**</span><span class="sxs-lookup"><span data-stu-id="19fd2-163">**columnidDefault**</span></span>

<span data-ttu-id="19fd2-164">Identificateur de colonne de la valeur par défaut de la colonne.</span><span class="sxs-lookup"><span data-stu-id="19fd2-164">The column identifier of the default value of the column.</span></span>

<span data-ttu-id="19fd2-165">La valeur par défaut est un [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="19fd2-165">The default value is a [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-166">**columnidBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="19fd2-166">**columnidBaseTableName**</span></span>

<span data-ttu-id="19fd2-167">Identificateur de colonne du nom de la table à partir de laquelle la table a été dérivée.</span><span class="sxs-lookup"><span data-stu-id="19fd2-167">The column identifier of the name of the table from which the table was derived.</span></span>

<span data-ttu-id="19fd2-168">Le nom de la table est un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="19fd2-168">The table name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-169">**columnidBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="19fd2-169">**columnidBaseColumnName**</span></span>

<span data-ttu-id="19fd2-170">Identificateur de colonne du nom de la colonne à partir de laquelle la colonne a été dérivée.</span><span class="sxs-lookup"><span data-stu-id="19fd2-170">The column identifier of the name of the column from which the column was derived.</span></span>

<span data-ttu-id="19fd2-171">Le nom de la colonne est un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="19fd2-171">The column name is a [JET_coltypText](./jet-coltyp.md).</span></span>

<span data-ttu-id="19fd2-172">**columnidDefinitionName**</span><span class="sxs-lookup"><span data-stu-id="19fd2-172">**columnidDefinitionName**</span></span>

<span data-ttu-id="19fd2-173">Identificateur de colonne du nom de la définition de colonne.</span><span class="sxs-lookup"><span data-stu-id="19fd2-173">The column identifier of the name of the column definition.</span></span>

<span data-ttu-id="19fd2-174">Le nom de la définition de colonne est un [JET_coltypText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="19fd2-174">The column definition name is a [JET_coltypText](./jet-coltyp.md).</span></span>

### <a name="remarks"></a><span data-ttu-id="19fd2-175">Notes</span><span class="sxs-lookup"><span data-stu-id="19fd2-175">Remarks</span></span>

<span data-ttu-id="19fd2-176">Par défaut, l’ordre des lignes dans la table temporaire est trié par le nom de la colonne.</span><span class="sxs-lookup"><span data-stu-id="19fd2-176">By default, the order of the rows in the temporary table is sorted by the name of the column.</span></span> <span data-ttu-id="19fd2-177">Elle peut également être triée par identificateur de colonne.</span><span class="sxs-lookup"><span data-stu-id="19fd2-177">It can also be sorted by column identifier.</span></span> <span data-ttu-id="19fd2-178">Pour plus d’informations sur le tri par identificateur de colonne, consultez [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="19fd2-178">For more information about how to sort by column identifier, see [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).</span></span>

<span data-ttu-id="19fd2-179">L’appel à [JetGetColumnInfo](./jetgetcolumninfo-function.md) ou [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) peut spécifier une forme compacte de résultats.</span><span class="sxs-lookup"><span data-stu-id="19fd2-179">The call to [JetGetColumnInfo](./jetgetcolumninfo-function.md) or [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) might specify a compact form of results.</span></span> <span data-ttu-id="19fd2-180">Si des colonnes ont été héritées d’une table de modèle, les résultats Compact ne les stockent pas.</span><span class="sxs-lookup"><span data-stu-id="19fd2-180">If any columns have been inherited from a template table, the compact results will not store them.</span></span>

### <a name="requirements"></a><span data-ttu-id="19fd2-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19fd2-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19fd2-182"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="19fd2-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="19fd2-183">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="19fd2-183">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19fd2-184"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="19fd2-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="19fd2-185">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="19fd2-185">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19fd2-186"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="19fd2-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="19fd2-187">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="19fd2-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="19fd2-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19fd2-188">See Also</span></span>

[<span data-ttu-id="19fd2-189">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="19fd2-189">JET_COLTYP</span></span>](./jet-coltyp.md)

[<span data-ttu-id="19fd2-190">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="19fd2-190">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)

[<span data-ttu-id="19fd2-191">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="19fd2-191">JET_COLUMNID</span></span>](./jet-columnid.md)

[<span data-ttu-id="19fd2-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="19fd2-192">JET_ERR</span></span>](./jet-err.md)

[<span data-ttu-id="19fd2-193">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="19fd2-193">JET_GRBIT</span></span>](./jet-grbit.md)

[<span data-ttu-id="19fd2-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="19fd2-194">JET_SESID</span></span>](./jet-sesid.md)

[<span data-ttu-id="19fd2-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="19fd2-195">JET_TABLEID</span></span>](./jet-tableid.md)

[<span data-ttu-id="19fd2-196">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="19fd2-196">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)

[<span data-ttu-id="19fd2-197">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="19fd2-197">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)
