---
description: 'En savoir plus sur : structure JET_SETCOLUMN'
title: Structure JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750517"
---
# <a name="jet_setcolumn-structure"></a><span data-ttu-id="87cc4-103">Structure JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="87cc4-103">JET_SETCOLUMN Structure</span></span>


<span data-ttu-id="87cc4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="87cc4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setcolumn-structure"></a><span data-ttu-id="87cc4-105">Structure JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="87cc4-105">JET_SETCOLUMN Structure</span></span>

<span data-ttu-id="87cc4-106">La structure **JET_SETCOLUMN** contient des paramètres d’entrée et de sortie pour [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="87cc4-106">The **JET_SETCOLUMN** structure contains input and output parameters for [JetSetColumns](./jetsetcolumns-function.md).</span></span> <span data-ttu-id="87cc4-107">Les champs de la structure décrivent la valeur de colonne à définir, comment la définir et où récupérer les données du jeu de colonnes.</span><span class="sxs-lookup"><span data-stu-id="87cc4-107">Fields in the structure describe what column value to set, how to set it, and where to get the column set data.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a><span data-ttu-id="87cc4-108">Membres</span><span class="sxs-lookup"><span data-stu-id="87cc4-108">Members</span></span>

<span data-ttu-id="87cc4-109">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="87cc4-109">**columnid**</span></span>

<span data-ttu-id="87cc4-110">Identificateur de colonne pour une colonne à définir.</span><span class="sxs-lookup"><span data-stu-id="87cc4-110">The column identifier for a column to set.</span></span>

<span data-ttu-id="87cc4-111">**pvData**</span><span class="sxs-lookup"><span data-stu-id="87cc4-111">**pvData**</span></span>

<span data-ttu-id="87cc4-112">Pointeur vers les données à définir dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="87cc4-112">A pointer to data to set into a column.</span></span>

<span data-ttu-id="87cc4-113">**cbData**</span><span class="sxs-lookup"><span data-stu-id="87cc4-113">**cbData**</span></span>

<span data-ttu-id="87cc4-114">Taille de l’allocation, en octets, à partir de **pvData** en octets.</span><span class="sxs-lookup"><span data-stu-id="87cc4-114">The size of allocation, in bytes, starting at **pvData** in bytes.</span></span>

<span data-ttu-id="87cc4-115">**grbit**</span><span class="sxs-lookup"><span data-stu-id="87cc4-115">**grbit**</span></span>

<span data-ttu-id="87cc4-116">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="87cc4-116">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87cc4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="87cc4-117">Value</span></span></p></th>
<th><p><span data-ttu-id="87cc4-118">Signification</span><span class="sxs-lookup"><span data-stu-id="87cc4-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87cc4-119">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="87cc4-119">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="87cc4-120">Ajoute des données à une colonne de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="87cc4-120">Appends data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="87cc4-121">Le même comportement peut être obtenu en déterminant la taille de la valeur longue existante et en spécifiant <strong>ibLongValue</strong> dans <strong>psetinfo</strong>.</span><span class="sxs-lookup"><span data-stu-id="87cc4-121">The same behavior can be achieved by determining the size of the existing long value and specifying <strong>ibLongValue</strong> in <strong>psetinfo</strong>.</span></span> <span data-ttu-id="87cc4-122">Toutefois, il est plus simple d’utiliser ce <em>Grbit</em>, car la connaissance de la taille de la valeur de colonne existante n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="87cc4-122">However, it's simpler to use this <em>grbit</em>, since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87cc4-123">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="87cc4-123">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="87cc4-124">Remplace la valeur de type long existante par les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="87cc4-124">Replaces the existing long value with the new data.</span></span> <span data-ttu-id="87cc4-125">Lorsque cette option est utilisée, c’est comme si la valeur long existante ait été définie à 0 (zéro) avant de définir les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="87cc4-125">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87cc4-126">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="87cc4-126">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="87cc4-127">Interprète la mémoire tampon d’entrée comme un nombre entier d’octets à définir comme longueur de la valeur longue décrite par le ColumnID donné et, si elle est fournie, le numéro de séquence dans psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="87cc4-127">Interprets the input buffer as an integer number of bytes to set as the length of the long value described by the given columnid and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="87cc4-128">Si la taille donnée est supérieure à la valeur de colonne existante, la colonne est étendue avec 0.</span><span class="sxs-lookup"><span data-stu-id="87cc4-128">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="87cc4-129">Si la taille est inférieure à la valeur de colonne existante, la valeur sera tronquée.</span><span class="sxs-lookup"><span data-stu-id="87cc4-129">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87cc4-130">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="87cc4-130">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="87cc4-131">Affecte une longueur nulle à une valeur.</span><span class="sxs-lookup"><span data-stu-id="87cc4-131">Sets a value to zero length.</span></span> <span data-ttu-id="87cc4-132">Normalement, une valeur de colonne est définie sur NULL en passant un cbMax de 0.</span><span class="sxs-lookup"><span data-stu-id="87cc4-132">Normally, a column value is set to NULL by passing a cbMax of 0.</span></span> <span data-ttu-id="87cc4-133">Toutefois, pour certains types, comme <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, une valeur de colonne peut être de longueur 0 et non null, et cette option est utilisée pour différencier les valeurs NULL et 0.</span><span class="sxs-lookup"><span data-stu-id="87cc4-133">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 length instead of NULL, and this option is used to differentiate between NULL and 0 length.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87cc4-134">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="87cc4-134">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="87cc4-135">Force une valeur long, les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>à être stockées séparément du reste des données d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="87cc4-135">Forces a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="87cc4-136">Cela se produit normalement lorsque la taille de la valeur long l’empêche d’être stockée avec les données d’enregistrement restantes.</span><span class="sxs-lookup"><span data-stu-id="87cc4-136">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="87cc4-137">Toutefois, cette option peut être utilisée pour forcer le stockage séparé de la valeur de type long.</span><span class="sxs-lookup"><span data-stu-id="87cc4-137">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="87cc4-138">Notez que les valeurs longues d’une taille de 4 octets ou plus petite ne peuvent pas être forcées à être séparées.</span><span class="sxs-lookup"><span data-stu-id="87cc4-138">Note that long values four bytes in size or smaller cannot be forced to be separate.</span></span> <span data-ttu-id="87cc4-139">Dans ce cas, l’option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="87cc4-139">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87cc4-140">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="87cc4-140">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="87cc4-141">Applique des valeurs distinctes dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="87cc4-141">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="87cc4-142">Cette option compare les données de la colonne source, sans aucune transformation, à d’autres valeurs de colonne existantes et une erreur est retournée si un doublon est trouvé.</span><span class="sxs-lookup"><span data-stu-id="87cc4-142">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="87cc4-143">Si cette option est spécifiée, JET_bitSetAppendLv, JET_bitSetOverwriteLV et JET_bitSetSizeLV ne peuvent pas être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="87cc4-143">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87cc4-144">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="87cc4-144">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="87cc4-145">Applique des valeurs distinctes dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="87cc4-145">Enforces distinct values in a multi-valued column.</span></span> <span data-ttu-id="87cc4-146">Cette option compare la transformation clé normalisée des données de colonne à d’autres valeurs de colonne existantes transformées de façon similaire, et une erreur est retournée si un doublon est trouvé.</span><span class="sxs-lookup"><span data-stu-id="87cc4-146">This option compares the key normalized transformation of column data to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="87cc4-147">Si cette option est spécifiée, JET_bitSetAppendLv, JET_bitSetOverwriteLV et JET_bitSetSizeLV ne peuvent pas être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="87cc4-147">If this option is given, then JET_bitSetAppendLv, JET_bitSetOverwriteLV, and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87cc4-148">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="87cc4-148">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="87cc4-149">Fait en sorte que la colonne retourne la valeur de colonne par défaut lors des opérations de récupération de colonne suivantes.</span><span class="sxs-lookup"><span data-stu-id="87cc4-149">Causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="87cc4-150">Toutes les valeurs de colonnes existantes sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="87cc4-150">All existing column values are removed.</span></span> <span data-ttu-id="87cc4-151">Cette option s’applique uniquement aux colonnes avec balises, éparses ou à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="87cc4-151">This option is only applicable for tagged, sparse, or multi-valued columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87cc4-152">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="87cc4-152">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="87cc4-153">Conserve la valeur long, les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou JET_coltypeLongBinary, stockées avec les données d’enregistrement restantes, si possible.</span><span class="sxs-lookup"><span data-stu-id="87cc4-153">Keeps the long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or JET_coltypeLongBinary, stored with the remaining record data if possible.</span></span> <span data-ttu-id="87cc4-154">Normalement, les colonnes de type long sont stockées séparément quand leur longueur dépasse 1024 octets ou si la longueur de l’enregistrement dépasse la limite de taille associée à la taille de la page.</span><span class="sxs-lookup"><span data-stu-id="87cc4-154">Normally, long columns are stored separately when their length exceeds 1024 bytes or would otherwise cause the record length to exceed its page size related size limitation.</span></span> <span data-ttu-id="87cc4-155">Toutefois, si cette option est définie, l’opération de définition de colonne échoue avec l’erreur JET_errColumnTooBig au lieu de stocker cette valeur de colonne séparément des données d’enregistrement restantes.</span><span class="sxs-lookup"><span data-stu-id="87cc4-155">However, if this option is set, the set column operation will fail with error JET_errColumnTooBig rather than store this column value separate from the remaining record data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87cc4-156">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="87cc4-156">**ibLongValue**</span></span>

<span data-ttu-id="87cc4-157">Offset au premier octet à récupérer d’une colonne de type [JET_coltypLongBinary](./jet-coltyp.md)ou [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="87cc4-157">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="87cc4-158">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="87cc4-158">**itagSequence**</span></span>

<span data-ttu-id="87cc4-159">Décrit le numéro de séquence de la valeur dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="87cc4-159">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="87cc4-160">Un **itagSequence** de 0 indique que la valeur de colonne définie doit être ajoutée en tant que nouvelle instance d’une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="87cc4-160">An **itagSequence** of 0 indicates that the column value set should be added as a new instance of a multi-valued column.</span></span>

<span data-ttu-id="87cc4-161">**Raise**</span><span class="sxs-lookup"><span data-stu-id="87cc4-161">**err**</span></span>

<span data-ttu-id="87cc4-162">Codes d’erreur et avertissements retournés par l’opération de définition de colonne.</span><span class="sxs-lookup"><span data-stu-id="87cc4-162">Error codes and warnings returned from the set column operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="87cc4-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87cc4-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87cc4-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="87cc4-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="87cc4-165">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="87cc4-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87cc4-166"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="87cc4-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="87cc4-167">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="87cc4-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87cc4-168"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="87cc4-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="87cc4-169">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="87cc4-169">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="87cc4-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87cc4-170">See Also</span></span>

[<span data-ttu-id="87cc4-171">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="87cc4-171">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="87cc4-172">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="87cc4-172">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="87cc4-173">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="87cc4-173">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="87cc4-174">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="87cc4-174">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="87cc4-175">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="87cc4-175">JetSetColumns</span></span>](./jetsetcolumns-function.md)
