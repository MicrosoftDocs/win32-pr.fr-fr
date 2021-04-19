---
description: 'En savoir plus sur : fonction JetSetColumn'
title: Fonction JetSetColumn
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c1fd267bea6bbb995a13ce65f97f1f531572a52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538648"
---
# <a name="jetsetcolumn-function"></a><span data-ttu-id="124fe-103">Fonction JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="124fe-103">JetSetColumn Function</span></span>


<span data-ttu-id="124fe-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="124fe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumn-function"></a><span data-ttu-id="124fe-105">Fonction JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="124fe-105">JetSetColumn Function</span></span>

<span data-ttu-id="124fe-106">La fonction **JetSetColumn** modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou à mettre à jour l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="124fe-106">The **JetSetColumn** function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="124fe-107">Elle peut remplacer une valeur existante, ajouter une nouvelle valeur à une séquence de valeurs dans une colonne à valeurs multiples, supprimer une valeur d’une séquence de valeurs dans une colonne à valeurs multiples, ou mettre à jour tout ou partie d’une valeur longue, une colonne de type [JET_coltypLongText](./jet-coltyp.md) ou [JET_coltypLongBinary](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="124fe-107">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value, a column of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md).</span></span>

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a><span data-ttu-id="124fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="124fe-108">Parameters</span></span>

<span data-ttu-id="124fe-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="124fe-109">*sesid*</span></span>

<span data-ttu-id="124fe-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="124fe-110">The session to use for this call.</span></span>

<span data-ttu-id="124fe-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="124fe-111">*tableid*</span></span>

<span data-ttu-id="124fe-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="124fe-112">The cursor to use for this call.</span></span>

<span data-ttu-id="124fe-113">*ColumnID*</span><span class="sxs-lookup"><span data-stu-id="124fe-113">*columnid*</span></span>

<span data-ttu-id="124fe-114">[JET_COLUMNID](./jet-columnid.md) de la colonne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="124fe-114">The [JET_COLUMNID](./jet-columnid.md) of the column to be retrieved.</span></span> <span data-ttu-id="124fe-115">Vous pouvez également donner une valeur *ColumnID* égale à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="124fe-115">Alternatively, a *columnid* value of 0 (zero) can be given.</span></span> <span data-ttu-id="124fe-116">Lorsque la valeur *ColumnID* 0 (zéro) est donnée, toutes les colonnes avec balises, les colonnes éparses et les colonnes à valeurs multiples, sont traitées comme une seule colonne.</span><span class="sxs-lookup"><span data-stu-id="124fe-116">When *columnid* 0 (zero) is given, all tagged columns, sparse and multi-valued columns, are treated as a single column.</span></span> <span data-ttu-id="124fe-117">Cela facilite la récupération de toutes les colonnes éparses présentes dans un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="124fe-117">This facilitates retrieving all sparse columns that are present in a record.</span></span>

<span data-ttu-id="124fe-118">*pvData*</span><span class="sxs-lookup"><span data-stu-id="124fe-118">*pvData*</span></span>

<span data-ttu-id="124fe-119">Mémoire tampon d’entrée contenant les données à utiliser pour la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="124fe-119">Input buffer containing data to use for column value.</span></span>

<span data-ttu-id="124fe-120">*cbData*</span><span class="sxs-lookup"><span data-stu-id="124fe-120">*cbData*</span></span>

<span data-ttu-id="124fe-121">Taille en octets de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="124fe-121">Size in bytes of the input buffer.</span></span>

<span data-ttu-id="124fe-122">*grbit*</span><span class="sxs-lookup"><span data-stu-id="124fe-122">*grbit*</span></span>

<span data-ttu-id="124fe-123">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="124fe-123">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="124fe-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="124fe-124">Value</span></span></p></th>
<th><p><span data-ttu-id="124fe-125">Signification</span><span class="sxs-lookup"><span data-stu-id="124fe-125">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="124fe-126">JET_bitSetAppendLV</span><span class="sxs-lookup"><span data-stu-id="124fe-126">JET_bitSetAppendLV</span></span></p></td>
<td><p><span data-ttu-id="124fe-127">Cette option est utilisée pour ajouter des données à une colonne de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span><span class="sxs-lookup"><span data-stu-id="124fe-127">This option is used to append data to a column of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>.</span></span> <span data-ttu-id="124fe-128">Le même comportement peut être obtenu en déterminant la taille de la valeur longue existante et en spécifiant <em>ibLongValue</em> dans <em>psetinfo</em>.</span><span class="sxs-lookup"><span data-stu-id="124fe-128">The same behavior can be achieved by determining the size of the existing long value and specifying <em>ibLongValue</em> in <em>psetinfo</em>.</span></span> <span data-ttu-id="124fe-129">Toutefois, il est plus simple d’utiliser ce <em>Grbit</em> car le fait de connaître la taille de la valeur de colonne existante n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="124fe-129">However, it's simpler to use this <em>grbit</em> since knowing the size of the existing column value is not necessary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-130">JET_bitSetOverwriteLV</span><span class="sxs-lookup"><span data-stu-id="124fe-130">JET_bitSetOverwriteLV</span></span></p></td>
<td><p><span data-ttu-id="124fe-131">Cette option est utilisée pour remplacer la valeur de type long existante par les données qui viennent d’être fournies.</span><span class="sxs-lookup"><span data-stu-id="124fe-131">This option is used replace the existing long value with the newly provided data.</span></span> <span data-ttu-id="124fe-132">Lorsque cette option est utilisée, c’est comme si la valeur long existante ait été définie à 0 (zéro) avant de définir les nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="124fe-132">When this option is used, it is as though the existing long value has been set to 0 (zero) length prior to setting the new data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-133">JET_bitSetRevertToDefaultValue</span><span class="sxs-lookup"><span data-stu-id="124fe-133">JET_bitSetRevertToDefaultValue</span></span></p></td>
<td><p><span data-ttu-id="124fe-134">Cette option s’applique uniquement aux colonnes avec balises, éparses ou à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="124fe-134">This option is only applicable for tagged, sparse or multi-valued columns.</span></span> <span data-ttu-id="124fe-135">Elle fait en sorte que la colonne retourne la valeur de colonne par défaut lors des opérations de récupération de colonne suivantes.</span><span class="sxs-lookup"><span data-stu-id="124fe-135">It causes the column to return the default column value on subsequent retrieve column operations.</span></span> <span data-ttu-id="124fe-136">Toutes les valeurs de colonnes existantes sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="124fe-136">All existing column values are removed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-137">JET_bitSetSeparateLV</span><span class="sxs-lookup"><span data-stu-id="124fe-137">JET_bitSetSeparateLV</span></span></p></td>
<td><p><span data-ttu-id="124fe-138">Cette option permet de forcer le stockage d’une valeur longue, de colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, séparément du reste des données d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="124fe-138">This option is used to force a long value, columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>, to be stored separately from the remainder of record data.</span></span> <span data-ttu-id="124fe-139">Cela se produit normalement lorsque la taille de la valeur long l’empêche d’être stockée avec les données d’enregistrement restantes.</span><span class="sxs-lookup"><span data-stu-id="124fe-139">This occurs normally when the size of the long value prevents it from being stored with remaining record data.</span></span> <span data-ttu-id="124fe-140">Toutefois, cette option peut être utilisée pour forcer le stockage séparé de la valeur de type long.</span><span class="sxs-lookup"><span data-stu-id="124fe-140">However, this option can be used to force the long value to be stored separately.</span></span> <span data-ttu-id="124fe-141">Notez que les valeurs longues de 4 octets de taille inférieure ne peuvent pas être forcées à être séparées.</span><span class="sxs-lookup"><span data-stu-id="124fe-141">Note that long values four bytes in size of smaller cannot be forced to be separate.</span></span> <span data-ttu-id="124fe-142">Dans ce cas, l’option est ignorée.</span><span class="sxs-lookup"><span data-stu-id="124fe-142">In such cases, the option is ignored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-143">JET_bitSetSizeLV</span><span class="sxs-lookup"><span data-stu-id="124fe-143">JET_bitSetSizeLV</span></span></p></td>
<td><p><span data-ttu-id="124fe-144">Cette option est utilisée pour interpréter la mémoire tampon d’entrée comme un nombre entier d’octets à définir comme longueur de la valeur longue décrite par le <em>ColumnID</em> donné et, le cas échéant, le numéro de séquence dans psetinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="124fe-144">This option is used to interpret the input buffer as a integer number of bytes to set as the length of the long value described by the given <em>columnid</em> and if provided, the sequence number in psetinfo-&gt;itagSequence.</span></span> <span data-ttu-id="124fe-145">Si la taille donnée est supérieure à la valeur de colonne existante, la colonne est étendue avec 0.</span><span class="sxs-lookup"><span data-stu-id="124fe-145">If the size given is larger than the existing column value, the column will be extended with 0s.</span></span> <span data-ttu-id="124fe-146">Si la taille est inférieure à la valeur de colonne existante, la valeur sera tronquée.</span><span class="sxs-lookup"><span data-stu-id="124fe-146">If the size is smaller than the existing column value then the value will be truncated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-147">JET_bitSetUniqueMultiValues</span><span class="sxs-lookup"><span data-stu-id="124fe-147">JET_bitSetUniqueMultiValues</span></span></p></td>
<td><p><span data-ttu-id="124fe-148">Cette option permet d’imposer que toutes les valeurs d’une colonne à valeurs multiples soient distinctes.</span><span class="sxs-lookup"><span data-stu-id="124fe-148">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="124fe-149">Cette option compare les données de la colonne source, sans aucune transformation, à d’autres valeurs de colonne existantes et une erreur est retournée si un doublon est trouvé.</span><span class="sxs-lookup"><span data-stu-id="124fe-149">This option compares the source column data, without any transformations, to other existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="124fe-150">Si cette option est spécifiée, JET_bitSetAppendLV, JET_bitSetOverwriteLV et JET_bitSetSizeLV ne peuvent pas être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="124fe-150">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-151">JET_bitSetUniqueNormalizedMultiValues</span><span class="sxs-lookup"><span data-stu-id="124fe-151">JET_bitSetUniqueNormalizedMultiValues</span></span></p></td>
<td><p><span data-ttu-id="124fe-152">Cette option permet d’imposer que toutes les valeurs d’une colonne à valeurs multiples soient distinctes.</span><span class="sxs-lookup"><span data-stu-id="124fe-152">This option is used to enforce that all values in a multi-valued column are distinct.</span></span> <span data-ttu-id="124fe-153">Cette option compare la transformation clé normalisée des données de colonne à d’autres valeurs de colonne existantes transformées de façon similaire, et une erreur est retournée si un doublon est trouvé.</span><span class="sxs-lookup"><span data-stu-id="124fe-153">This option compares the key normalized transformation of column data, to other similarly transformed existing column values and an error is returned if a duplicate is found.</span></span> <span data-ttu-id="124fe-154">Si cette option est spécifiée, JET_bitSetAppendLV, JET_bitSetOverwriteLV et JET_bitSetSizeLV ne peuvent pas être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="124fe-154">If this option is given, then JET_bitSetAppendLV, JET_bitSetOverwriteLV and JET_bitSetSizeLV cannot also be given.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-155">JET_bitSetZeroLength</span><span class="sxs-lookup"><span data-stu-id="124fe-155">JET_bitSetZeroLength</span></span></p></td>
<td><p><span data-ttu-id="124fe-156">Cette option est utilisée pour définir une valeur de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="124fe-156">This option is used to set a value to zero length.</span></span> <span data-ttu-id="124fe-157">Normalement, une valeur de colonne est définie sur <strong>null</strong> en passant un cbMax de 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="124fe-157">Normally, a column value is set to <strong>NULL</strong> by passing a cbMax of 0 (zero).</span></span> <span data-ttu-id="124fe-158">Toutefois, pour certains types, comme <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, une valeur de colonne peut avoir une longueur de 0 (zéro) au lieu de <strong>null</strong>, et cette option est utilisée pour différencier les <strong>valeurs NULL</strong> et 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="124fe-158">However, for some types, like <a href="gg269213(v=exchg.10).md">JET_coltypText</a>, a column value can be 0 (zero) length instead of <strong>NULL</strong>, and this option is used to differentiate between <strong>NULL</strong> and 0 (zero) length.</span></span></p>
<p><span data-ttu-id="124fe-159"><strong>Remarque</strong>  En général, si la colonne est une colonne de longueur fixe, ce bit est ignoré et la colonne est définie sur <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="124fe-159"><strong>Note</strong>  In general, if the column is a fixed-length column, this bit is ignored and the column is set to <strong>NULL</strong>.</span></span> <span data-ttu-id="124fe-160">Toutefois, si la colonne est une colonne avec balises de longueur fixe, la longueur de la colonne est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="124fe-160">However, if the column is a fixed-length tagged column, the column length is set to 0.</span></span> <span data-ttu-id="124fe-161">Lorsque la colonne avec balises de longueur fixe a la valeur 0, les tentatives de récupération de la colonne avec <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ou <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> échouent, mais la longueur réelle qui est retournée dans le paramètre <em>cbActual</em> est 0.</span><span class="sxs-lookup"><span data-stu-id="124fe-161">When the fixed-length tagged column is set to 0 length, attempts to retrieve the column with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> will succeed, but the actual length that is returned in the <em>cbActual</em> parameter is 0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-162">JET_bitSetIntrinsicLV</span><span class="sxs-lookup"><span data-stu-id="124fe-162">JET_bitSetIntrinsicLV</span></span></p></td>
<td><p><span data-ttu-id="124fe-163">Cette option permet de stocker la valeur longue entière dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="124fe-163">This option is used to store the entire long value in the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-164">JET_bitSetCompressed</span><span class="sxs-lookup"><span data-stu-id="124fe-164">JET_bitSetCompressed</span></span></p></td>
<td><p><span data-ttu-id="124fe-165">Cette option est utilisée pour tenter de compresser les données lors du stockage des données.</span><span class="sxs-lookup"><span data-stu-id="124fe-165">This option is used to attempt data compression when storing the data.</span></span></p>
<p><span data-ttu-id="124fe-166"><strong>Windows 7 :</strong>  JET_bitSetCompressed est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="124fe-166"><strong>Windows 7:</strong>  JET_bitSetCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-167">JET_bitSetUncompressed</span><span class="sxs-lookup"><span data-stu-id="124fe-167">JET_bitSetUncompressed</span></span></p></td>
<td><p><span data-ttu-id="124fe-168">Cette option est utilisée pour ne pas tenter de compresser lors du stockage des données.</span><span class="sxs-lookup"><span data-stu-id="124fe-168">This option is used not attempt compression when storing the data.</span></span></p>
<p><span data-ttu-id="124fe-169"><strong>Windows 7 :</strong>  JET_bitSetUnCompressed est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="124fe-169"><strong>Windows 7:</strong>  JET_bitSetUnCompressed is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="124fe-170">*psetinfo*</span><span class="sxs-lookup"><span data-stu-id="124fe-170">*psetinfo*</span></span>

<span data-ttu-id="124fe-171">Pointeur vers des paramètres d’entrée facultatifs qui peuvent être définis pour cette fonction à l’aide de la structure [JET_SETINFO](./jet-setinfo-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="124fe-171">Pointer to optional input parameters that can be set for this function using the [JET_SETINFO](./jet-setinfo-structure.md) structure.</span></span>

<span data-ttu-id="124fe-172">Si *psetinfo* est donné comme **null** , la fonction se comporte comme si un *ItagSequence* de 1 et un *ibLongValue* de 0 (zéro) ont été donnés.</span><span class="sxs-lookup"><span data-stu-id="124fe-172">If *psetinfo* is given as **NULL** then the function behaves as though an *itagSequence* of 1 and an *ibLongValue* of 0 (zero) were given.</span></span> <span data-ttu-id="124fe-173">Cela amène le jeu de colonnes à définir la première valeur d’une colonne à valeurs multiples et à définir des données de type long en commençant à l’offset 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="124fe-173">This causes column set to set the first value of a multi-valued column, and to set long data beginning at offset 0 (zero).</span></span>

<span data-ttu-id="124fe-174">Les options suivantes peuvent être définies pour ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="124fe-174">The following options can be set for this parameter:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="124fe-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="124fe-175">Value</span></span></p></th>
<th><p><span data-ttu-id="124fe-176">Signification</span><span class="sxs-lookup"><span data-stu-id="124fe-176">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="124fe-177">ibLongValue</span><span class="sxs-lookup"><span data-stu-id="124fe-177">ibLongValue</span></span></p></td>
<td><p><span data-ttu-id="124fe-178">Décalage binaire dans une valeur de colonne longue où les données de jeu doivent commencer.</span><span class="sxs-lookup"><span data-stu-id="124fe-178">Binary offset into a long column value where set data should begin.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-179">itagSequence</span><span class="sxs-lookup"><span data-stu-id="124fe-179">itagSequence</span></span></p></td>
<td><p><span data-ttu-id="124fe-180">Numéro de séquence de la valeur de colonne à valeurs multiples souhaitée à définir.</span><span class="sxs-lookup"><span data-stu-id="124fe-180">Sequence number of the desired multi-valued column value to set.</span></span> <span data-ttu-id="124fe-181">Si <em>itagSequence</em> est défini sur 0 (zéro), la valeur fournie doit être ajoutée à la fin de la séquence de valeurs à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="124fe-181">If <em>itagSequence</em> is set to 0 (zero), then the value provided should be appended to then end of the sequence of multi-valued values.</span></span> <span data-ttu-id="124fe-182">Si le numéro de séquence fourni est supérieur à la dernière valeur à valeurs multiples existante, la valeur donnée est ajoutée à la fin de la séquence de valeurs.</span><span class="sxs-lookup"><span data-stu-id="124fe-182">If the sequence number provided is greater than the last existing multi-valued value, then again the given value is appended to the end of the sequence of values.</span></span> <span data-ttu-id="124fe-183">Si le numéro de séquence correspond à une valeur existante, cette valeur est remplacée par la valeur donnée.</span><span class="sxs-lookup"><span data-stu-id="124fe-183">If the sequence number corresponds to an existing value then that value is replaced with the given value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="124fe-184">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="124fe-184">Return Value</span></span>

<span data-ttu-id="124fe-185">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="124fe-185">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="124fe-186">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="124fe-186">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="124fe-187">Code de retour</span><span class="sxs-lookup"><span data-stu-id="124fe-187">Return code</span></span></p></th>
<th><p><span data-ttu-id="124fe-188">Description</span><span class="sxs-lookup"><span data-stu-id="124fe-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="124fe-189">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="124fe-189">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="124fe-190">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="124fe-190">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-191">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="124fe-191">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="124fe-192">L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="124fe-192">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-193">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="124fe-193">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="124fe-194">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="124fe-194">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-195">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="124fe-195">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="124fe-196">La colonne décrite par le <em>ColumnID</em> donné n’existe pas dans la table.</span><span class="sxs-lookup"><span data-stu-id="124fe-196">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-197">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="124fe-197">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="124fe-198">Une tentative non conforme a été effectuée pour mettre à jour une valeur long pendant une opération de mise à jour d’origine de la suppression d’une copie Insert.</span><span class="sxs-lookup"><span data-stu-id="124fe-198">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-199">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="124fe-199">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="124fe-200">Les données de la valeur de colonne donnée dans la mémoire tampon d’entrée dépassent la limite de taille naturelle pour une colonne de longueur fixe ou configurée pour le texte de longueur fixe ou les colonnes binaires.</span><span class="sxs-lookup"><span data-stu-id="124fe-200">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="124fe-201">Cette erreur est également retournée lors du passage de plus de 1024 octets de données pour une longue colonne et de la définition de l’indicateur de JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="124fe-201">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-202">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="124fe-202">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="124fe-203">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="124fe-203">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="124fe-204"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="124fe-204"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-205">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="124fe-205">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="124fe-206">La taille de données de la valeur de colonne donnée ne correspond pas à ce qui est naturel pour le type de données de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="124fe-206">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-207">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="124fe-207">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="124fe-208">Une tentative non conforme a été effectuée pour mettre à jour une colonne à incrémentation automatique pendant une opération d’insertion ou de mise à jour, ou pour mettre à jour une colonne de version pendant une opération de remplacement.</span><span class="sxs-lookup"><span data-stu-id="124fe-208">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-209">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="124fe-209">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="124fe-210">Les options fournies sont inconnues ou une combinaison non conforme de paramètres de bits connus.</span><span class="sxs-lookup"><span data-stu-id="124fe-210">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-211">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="124fe-211">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="124fe-212">Le psetinfo- &gt; cbStruct donné n’est pas une taille valide pour la structure <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="124fe-212">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-213">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="124fe-213">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="124fe-214">L’opération de définition de colonne a tenté de créer une valeur dupliquée et spécifiée soit JET_bitSetUniqueMultiValues, soit JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="124fe-214">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-215">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="124fe-215">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="124fe-216">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="124fe-216">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-217">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="124fe-217">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="124fe-218">Une tentative non conforme a été effectuée pour mettre à jour une valeur de colonne longue lorsque la session appelante n’était pas dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="124fe-218">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-219">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="124fe-219">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="124fe-220">Une tentative non conforme a été effectuée pour définir une colonne non<strong>null</strong> à <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="124fe-220">An illegal attempt was made to set a non-<strong>NULL</strong> column to <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-221">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="124fe-221">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="124fe-222">Identique à JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="124fe-222">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-223">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="124fe-223">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="124fe-224">La valeur de la colonne n’a pas pu être définie sur la valeur dans la mémoire tampon d’entrée, car elle aurait provoqué un dépassement de la limite de taille liée à la taille de la page de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="124fe-224">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="124fe-225">Les colonnes de type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> peuvent être stockées séparément des données de l’enregistrement restant.</span><span class="sxs-lookup"><span data-stu-id="124fe-225">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="124fe-226">Toutefois, les autres colonnes doivent être stockées avec l’enregistrement et peuvent entraîner le dépassement de la limite de taille des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="124fe-226">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="124fe-227">Même les colonnes longues nécessitent 5 octets d’espace dans l’enregistrement en tant que liaison, ce qui peut entraîner des JET_errRecordTooBig retournées.</span><span class="sxs-lookup"><span data-stu-id="124fe-227">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-228">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="124fe-228">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="124fe-229">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="124fe-229">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-230">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="124fe-230">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="124fe-231">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="124fe-231">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="124fe-232"><strong>Windows XP :</strong>  Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="124fe-232"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-233">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="124fe-233">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="124fe-234">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="124fe-234">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-235">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="124fe-235">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="124fe-236">Le curseur ne se trouve pas actuellement dans le processus d’insertion d’un nouvel enregistrement ou de mise à jour d’un enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="124fe-236">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-237">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="124fe-237">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="124fe-238">Cette erreur se produit lorsque la taille de la Banque des versions configurée est insuffisante pour contenir toutes les mises à jour en suspens.</span><span class="sxs-lookup"><span data-stu-id="124fe-238">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-239">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="124fe-239">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="124fe-240">La valeur de colonne dans la mémoire tampon d’entrée a dépassé la longueur maximale configurée pour une colonne de longueur variable et a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="124fe-240">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="124fe-241">En cas de réussite, la partie souhaitée d’une valeur de colonne pour la colonne donnée est définie avec les données copiées à partir de la mémoire tampon d’entrée.</span><span class="sxs-lookup"><span data-stu-id="124fe-241">On success, the desired portion of a column value for the given column is set with data copied from the input buffer.</span></span> <span data-ttu-id="124fe-242">Le jeu de données a peut-être été tronqué s’il dépasse la longueur maximale spécifiée pour une colonne de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="124fe-242">The data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="124fe-243">En cas d’échec, l’emplacement du curseur reste inchangé et aucune donnée de valeur de colonne n’est mise à jour dans le tampon de copie.</span><span class="sxs-lookup"><span data-stu-id="124fe-243">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="124fe-244">Notes</span><span class="sxs-lookup"><span data-stu-id="124fe-244">Remarks</span></span>

<span data-ttu-id="124fe-245">En définissant des valeurs longues, les valeurs des colonnes [JET_coltypLongBinary](./jet-coltyp.md) de type [JET_coltypLongText](./jet-coltyp.md) ou [JET_coltypLongBinary](./jet-coltyp.md)doivent être effectuées uniquement lorsque la session appelante est dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="124fe-245">Setting long values, values for columns [JET_coltypLongBinary](./jet-coltyp.md) of type [JET_coltypLongText](./jet-coltyp.md) or [JET_coltypLongBinary](./jet-coltyp.md), should be done only when the calling session is in a transaction.</span></span> <span data-ttu-id="124fe-246">Si la session appelante n’est pas dans une transaction, les modifications apportées aux valeurs longues qui sont stockées séparément peuvent être validées entièrement même lorsque l’opération de mise à jour est annulée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="124fe-246">If the calling session is not in a transaction, modifications to long values which are stored separately may be committed fully even when the update operation is later cancelled.</span></span> <span data-ttu-id="124fe-247">Si la session appelante est dans une transaction, les effets de la mise à jour peuvent être entièrement annulés en annulant la mise à jour et en restaurant la transaction de session.</span><span class="sxs-lookup"><span data-stu-id="124fe-247">If the calling session is in a transaction, then the effects of the update can be fully rolled back by canceling the update and rolling back the session transaction.</span></span>

<span data-ttu-id="124fe-248">Les mises à jour d’index ne sont pas effectuées suite à des opérations **JetSetColumn** .</span><span class="sxs-lookup"><span data-stu-id="124fe-248">Index updates are not performed as a result of **JetSetColumn** operations.</span></span> <span data-ttu-id="124fe-249">Au lieu de cela, les index sont mis à jour uniquement une fois que toutes les modifications de colonne sont terminées et [JetUpdate](./jetupdate-function.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="124fe-249">Instead, indexes are updated only after all column modifications are complete and [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="124fe-250">Cela permet la mise à jour la plus efficace des index lorsque des index impliquent la modification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="124fe-250">This permits the most efficient updating of indexes when indexes involve more than one column being modified.</span></span>

<span data-ttu-id="124fe-251">La taille d’un enregistrement est limitée en fonction de la taille de la page de base de données.</span><span class="sxs-lookup"><span data-stu-id="124fe-251">A record is limited in size based on the database page size.</span></span> <span data-ttu-id="124fe-252">Toute valeur de type long de l’enregistrement supérieur à cinq octets est stockée séparément de l’enregistrement si les données de l’enregistrement dépassent la limite résultant d’une opération **JetSetColumn** .</span><span class="sxs-lookup"><span data-stu-id="124fe-252">Any long values in the record larger than five bytes will be stored separate from the record should the data in the record exceed its limit as a result of a **JetSetColumn** operation.</span></span> <span data-ttu-id="124fe-253">Le JET_errRecordTooBig d’erreur est renvoyé uniquement une fois que toutes les données de colonne d’enregistrement séparable ont été stockées séparément de l’enregistrement et que l’enregistrement dépasse la limite de taille d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="124fe-253">The error JET_errRecordTooBig will only be returned after all separable record column data has been stored separately from the record and the record still exceeds the record size limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="124fe-254">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="124fe-254">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="124fe-255"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="124fe-255"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="124fe-256">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="124fe-256">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-257"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="124fe-257"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="124fe-258">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="124fe-258">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-259"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="124fe-259"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="124fe-260">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="124fe-260">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="124fe-261"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="124fe-261"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="124fe-262">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="124fe-262">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="124fe-263"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="124fe-263"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="124fe-264">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="124fe-264">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="124fe-265">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="124fe-265">See Also</span></span>

[<span data-ttu-id="124fe-266">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="124fe-266">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="124fe-267">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="124fe-267">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="124fe-268">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="124fe-268">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="124fe-269">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="124fe-269">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="124fe-270">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="124fe-270">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="124fe-271">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="124fe-271">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="124fe-272">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="124fe-272">JetSetColumns</span></span>](./jetsetcolumns-function.md)
