---
description: 'En savoir plus sur : fonction JetEnumerateColumns'
title: Fonction JetEnumerateColumns
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203891"
---
# <a name="jetenumeratecolumns-function"></a><span data-ttu-id="8c6a4-103">Fonction JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="8c6a4-103">JetEnumerateColumns Function</span></span>


<span data-ttu-id="8c6a4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="8c6a4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenumeratecolumns-function"></a><span data-ttu-id="8c6a4-105">Fonction JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="8c6a4-105">JetEnumerateColumns Function</span></span>

<span data-ttu-id="8c6a4-106">La fonction **JetEnumerateColumns** récupère efficacement un ensemble de colonnes et leurs valeurs à partir de l’enregistrement actuel d’un curseur ou de la mémoire tampon de copie de ce curseur.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-106">The **JetEnumerateColumns** function efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="8c6a4-107">Les colonnes et les valeurs récupérées peuvent être restreintes par une liste d’ID de colonne, de nombres *itagSequence* et d’autres caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-107">The columns and values retrieved can be restricted by a list of column IDs, *itagSequence* numbers, and other characteristics.</span></span> <span data-ttu-id="8c6a4-108">Cette API de récupération de colonne est unique dans la mesure où elle retourne des informations dans la mémoire allouée dynamiquement obtenue à l’aide d’un rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-108">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="8c6a4-109">Cette nouvelle flexibilité permet une récupération efficace des données de colonne avec des caractéristiques spécifiques (telles que la taille et la multiplicité) qui sont inconnues pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-109">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="8c6a4-110">Cela élimine le besoin d’utiliser les modes de découverte de [JetRetrieveColumn](./jetretrievecolumn-function.md) pour déterminer ces caractéristiques afin de configurer un dernier appel à [JetRetrieveColumn](./jetretrievecolumn-function.md) qui récupérera correctement les données souhaitées.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-110">This eliminates the need for the use of the discovery modes of [JetRetrieveColumn](./jetretrievecolumn-function.md) to determine those characteristics in order to setup a final call to [JetRetrieveColumn](./jetretrievecolumn-function.md) that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="8c6a4-111">**Windows XP : JetEnumerateColumns** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-111">**Windows XP:  JetEnumerateColumns** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8c6a4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c6a4-112">Parameters</span></span>

<span data-ttu-id="8c6a4-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-113">*sesid*</span></span>

<span data-ttu-id="8c6a4-114">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-114">The session to use for this call.</span></span>

<span data-ttu-id="8c6a4-115">*TableID*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-115">*tableid*</span></span>

<span data-ttu-id="8c6a4-116">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-116">The cursor to use for this call.</span></span>

<span data-ttu-id="8c6a4-117">*cEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-117">*cEnumColumnId*</span></span>

<span data-ttu-id="8c6a4-118">Tableau d’ID de colonne, chacun avec un tableau facultatif de nombres *itagSequence* à énumérer.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-118">An array of column IDs, each with an optional array of *itagSequence* numbers to enumerate.</span></span>

<span data-ttu-id="8c6a4-119">Si *cEnumColumnId* a la valeur 0 (zéro), *rgEnumColumnId* est ignoré et toutes les valeurs de colonne sont énumérées et retournées à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-119">If *cEnumColumnId* is 0 (zero) then *rgEnumColumnId* is ignored and all column values are enumerated and returned to the caller.</span></span> <span data-ttu-id="8c6a4-120">Si un élément du tableau d’ID de colonne fait référence à un ID de colonne 0 (zéro), l’énumération de cette colonne est ignorée et un emplacement correspondant dans la sortie est généré avec un état de colonne de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-120">If an element of the column ID array refers to a column ID of 0 (zero) then enumeration of that column is skipped and a corresponding slot in the output will be generated with a column status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="8c6a4-121">Si *ctagSequence* a la valeur 0 (zéro) pour un élément donné du tableau d’ID de colonne, *rgtagSequence* est ignoré et toutes les valeurs de colonne pour cet ID de colonne sont énumérées et retournées à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-121">If *ctagSequence* is 0 (zero) for a given element of the column ID array then *rgtagSequence* is ignored and all column values for that column ID are enumerated and returned to the caller.</span></span> <span data-ttu-id="8c6a4-122">Si un élément d’un tableau de nombres *itagSequence* fait référence à un nombre *itagSequence* égal à 0 (zéro), l’énumération de ce numéro de *itagSequence* est ignorée et un emplacement correspondant dans la sortie est généré avec un état de valeur de colonne JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-122">If an element of an *itagSequence* number array refers to a *itagSequence* number of 0 (zero) then the enumeration of that *itagSequence* number is skipped and a corresponding slot in the output will be generated with a column value status of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="8c6a4-123">*rgEnumColumnId*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-123">*rgEnumColumnId*</span></span>

<span data-ttu-id="8c6a4-124">Consultez *cEnumColumnId*.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-124">See *cEnumColumnId*.</span></span>

<span data-ttu-id="8c6a4-125">*pcEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-125">*pcEnumColumn*</span></span>

<span data-ttu-id="8c6a4-126">Retourne le tableau énuméré des colonnes et leurs valeurs en mémoire allouées via le rappel compatible *itagSequence* fourni.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-126">Returns the enumerated array of columns and their values in memory allocated through the provided *itagSequence* compatible callback.</span></span>

<span data-ttu-id="8c6a4-127">Si un tableau d’ID de colonne est demandé en entrée, l’ordre et la taille du tableau de sortie reflètent l’ordre et la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-127">If an array of column IDs is requested on input then the order and size of the output array will reflect the order and size of the input array.</span></span> <span data-ttu-id="8c6a4-128">De même, si un tableau de nombres *itagSequence* est demandé pour un ID de colonne particulier en entrée, l’ordre et la taille du tableau de sortie des valeurs de colonne pour cette colonne reflètent l’ordre et la taille du tableau d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-128">Similarly, if an array of *itagSequence* numbers is requested for a particular column ID on input then the order and size of the output array of column values for that column will reflect the order and size of the input array.</span></span>

<span data-ttu-id="8c6a4-129">Les paramètres de sortie ont la valeur 0 (zéro) et la **valeur null** pour toutes les erreurs, à l’exception de JET_errBadColumnId et JET_errColumnNotFound.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-129">The output parameters are set to 0 (zero) and **NULL** on any error except for JET_errBadColumnId and JET_errColumnNotFound.</span></span> <span data-ttu-id="8c6a4-130">Lorsque ces erreurs sont retournées, les données de sortie sont valides et complètes pour tous les ID de colonne sauf les affectés.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-130">When these errors are returned, the output data is valid and complete for all but the affected column IDs.</span></span> <span data-ttu-id="8c6a4-131">Le code d’état de chacun des ID de colonne affectés est défini sur l’une de ces erreurs, de sorte que l’appelant peut déterminer les ID de colonne qui sont incorrects et éventuellement prendre des mesures correctives.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-131">The status code for each of the affected column IDs is set to one of these errors so that the caller may determine which column IDs were bad and potentially take corrective action.</span></span>

<span data-ttu-id="8c6a4-132">*prgEnumColumn*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-132">*prgEnumColumn*</span></span>

<span data-ttu-id="8c6a4-133">Consultez *pcEnumColumn*.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-133">See *pcEnumColumn*.</span></span>

<span data-ttu-id="8c6a4-134">*pfnRealloc*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-134">*pfnRealloc*</span></span>

<span data-ttu-id="8c6a4-135">Identifie un rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) et un pointeur de contexte facultatif utilisé pour allouer de la mémoire pour le tableau de sortie des colonnes et leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-135">Identifies a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback and an optional context pointer used to allocate memory for the output array of columns and their values.</span></span>

<span data-ttu-id="8c6a4-136">*pvReallocContext*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-136">*pvReallocContext*</span></span>

<span data-ttu-id="8c6a4-137">Consultez *pfnRealloc*.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-137">See *pfnRealloc*.</span></span>

<span data-ttu-id="8c6a4-138">*cbDataMost*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-138">*cbDataMost*</span></span>

<span data-ttu-id="8c6a4-139">Définit une limite sur la quantité de données à retourner à partir d’une colonne de texte long ou d’une colonne binaire longue.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-139">Sets a cap on the amount of data to return from a long text or long binary column.</span></span>

<span data-ttu-id="8c6a4-140">Ce paramètre peut être utilisé pour empêcher l’énumération d’une valeur de colonne extrêmement volumineuse.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-140">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span> <span data-ttu-id="8c6a4-141">En règle générale, une telle énumération peut échouer l’appel d’API avec JET_errOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-141">Ordinarily, such an enumeration might fail the API call with JET_errOutOfMemory.</span></span> <span data-ttu-id="8c6a4-142">Si une valeur de colonne importante est tronquée de telle manière, l’état de la valeur de colonne sera JET_wrnColumnTruncated.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-142">If a large column value is truncated in such a manner then the column value's status will be JET_wrnColumnTruncated.</span></span>

<span data-ttu-id="8c6a4-143">*grbit*</span><span class="sxs-lookup"><span data-stu-id="8c6a4-143">*grbit*</span></span>

<span data-ttu-id="8c6a4-144">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-144">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c6a4-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c6a4-145">Value</span></span></p></th>
<th><p><span data-ttu-id="8c6a4-146">Signification</span><span class="sxs-lookup"><span data-stu-id="8c6a4-146">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-147">JET_bitEnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="8c6a4-147">JET_bitEnumerateCompressOutput</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-148">Lors de l’énumération des valeurs de colonne, toutes les colonnes pour lesquelles nous récupérons toutes les valeurs et qui ont une seule valeur de colonne non NULL peuvent être retournées dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-148">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="8c6a4-149">L’état de ces colonnes est défini sur JET_wrnColumnSingleValue et la taille de la valeur de colonne et la mémoire contenant la valeur de colonne sont retournées directement dans la structure <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="8c6a4-149">The status for such columns will be set to JET_wrnColumnSingleValue and the size of the column value and the memory containing the column value will be returned directly in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="8c6a4-150">Il n’est pas garanti que toutes les colonnes admissibles soient compressées de cette manière.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-150">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="8c6a4-151">Pour plus d’informations, consultez <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="8c6a4-151">See <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-152">JET_bitEnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="8c6a4-152">JET_bitEnumerateCopy</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-153">Cette option indique que les valeurs de colonne modifiées de l’enregistrement doivent être énumérées au lieu des valeurs de colonne d’origine.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-153">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="8c6a4-154">Si une valeur de colonne n’a pas été modifiée, la valeur de colonne d’origine est énumérée.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-154">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="8c6a4-155">De cette façon, une valeur de colonne qui n’a pas encore été insérée ou mise à jour peut être énumérée lors de l’insertion ou de la mise à jour d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-155">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span></p>
<p><span data-ttu-id="8c6a4-156">Cette option est identique à JET_bitRetrieveCopy lorsqu’elle est utilisée avec <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> ou <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-156">This option is identical to JET_bitRetrieveCopy when used with <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> or <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-157">JET_bitEnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="8c6a4-157">JET_bitEnumerateIgnoreDefault</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-158">Si une colonne donnée n’est pas présente dans l’enregistrement, aucune valeur de colonne n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-158">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="8c6a4-159">En règle générale, la valeur par défaut de la colonne, le cas échéant, est retournée dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-159">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="8c6a4-160">Il est garanti que si la colonne est définie sur une valeur différente de la valeur par défaut, cette valeur différente sera retournée (autrement dit, si une colonne avec une valeur par défaut est explicitement définie sur <strong>null</strong> , une valeur <strong>null</strong> est retournée en tant que valeur pour cette colonne).</span><span class="sxs-lookup"><span data-stu-id="8c6a4-160">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to <strong>NULL</strong> then a <strong>NULL</strong> will be returned as the value for that column).</span></span> <span data-ttu-id="8c6a4-161">Notez que, même si cette option est demandée, il est toujours possible de voir une valeur de colonne qui se trouve être égale à la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-161">Note that, even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="8c6a4-162">Aucun effort n’est apporté pour supprimer des valeurs de colonne qui correspondent à leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-162">No effort is made to remove column values that match their default values.</span></span></p>
<p><span data-ttu-id="8c6a4-163">Il est important de noter que cette option affecte la sortie de <strong>JetEnumerateColumns</strong> lorsqu’elle est utilisée avec JET_bitEnumeratePresenceOnly ou JET_bitEnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-163">It is important to note that this option affects the output of <strong>JetEnumerateColumns</strong> when used with JET_bitEnumeratePresenceOnly or JET_bitEnumerateTaggedOnly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-164">JET_bitEnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="8c6a4-164">JET_bitEnumerateIgnoreUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-165">Si une colonne donnée n’est pas présente dans l’enregistrement et qu’elle a une valeur par défaut définie par l’utilisateur, aucune valeur de colonne n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-165">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="8c6a4-166">Cette option empêchera le rappel qui calcule la valeur par défaut définie par l’utilisateur pour la colonne à être appelée lors de l’énumération des valeurs de cette colonne.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-166">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></p>
<p><span data-ttu-id="8c6a4-167"><strong>Windows Server 2003 et versions antérieures :  </strong> Pour Windows Server 2003 et versions antérieures, l’opération échoue avec JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-167"><strong>Windows Server 2003 and earlier:  </strong>For Windows Server 2003 and earlier releases, the operation will fail with JET_errCallbackFailed.</span></span></p>
<p><span data-ttu-id="8c6a4-168"><strong>Windows Server 2003 SP1 :  </strong> Cette valeur possible est disponible uniquement pour les systèmes d’exploitation Windows Server 2003 SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-168"><strong>Windows Server 2003 SP1:  </strong>This possible value is only available for Windows Server 2003 SP1 and later operating systems.</span></span> <span data-ttu-id="8c6a4-169">Si cette valeur possible est spécifiée et que la table contient une colonne qui a une valeur par défaut définie par l’utilisateur, l’opération échoue avec JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-169">If this possible value is specified and the table contains a column that has a user defined default value, then the operation will fail with JET_errCallbackFailed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-170">JET_bitEnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="8c6a4-170">JET_bitEnumeratePresenceOnly</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-171">Si une valeur non NULL existe pour la colonne ou la valeur de colonne demandée, les données associées ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-171">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="8c6a4-172">Au lieu de cela, l’état associé à la colonne ou à la valeur de cette colonne sera défini sur JET_wrnColumnPresent.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-172">Instead, the associated status for that column or column value will be set to JET_wrnColumnPresent.</span></span> <span data-ttu-id="8c6a4-173">Si la colonne ou la valeur de colonne est <strong>null</strong> , JET_wrnColumnNull est retourné comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-173">If the column or column value is <strong>NULL</strong> then JET_wrnColumnNull will be returned as usual.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-174">JET_bitEnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="8c6a4-174">JET_bitEnumerateTaggedOnly</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-175">Lors de l’énumération de toutes les valeurs de colonne dans l’enregistrement (par exemple, lorsque <em>cEnumColumnId</em> est égal à zéro), seules les valeurs de colonne avec balises sont retournées.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-175">When enumerating all column values in the record (for example,that is when <em>cEnumColumnId</em> is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="8c6a4-176">Cette option n’est pas autorisée lors de l’énumération d’un tableau spécifique d’ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-176">This option is not allowed when enumerating a specific array of column IDs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-177">JET_bitEnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="8c6a4-177">JET_bitEnumerateInRecordOnly</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-178"><strong>Windows 7 :  </strong> JET_bitEnumerateInRecordOnly est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-178"><strong>Windows 7:  </strong>JET_bitEnumerateInRecordOnly is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8c6a4-179">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8c6a4-179">Return Value</span></span>

<span data-ttu-id="8c6a4-180">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-180">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8c6a4-181">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8c6a4-181">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c6a4-182">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8c6a4-182">Return code</span></span></p></th>
<th><p><span data-ttu-id="8c6a4-183">Description</span><span class="sxs-lookup"><span data-stu-id="8c6a4-183">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-184">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8c6a4-184">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-185">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-185">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-186">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="8c6a4-186">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-187">L’ID de colonne indiqué est en dehors des limites autorisées d’un ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-187">The column ID given is outside the legal limits of a column ID.</span></span> <span data-ttu-id="8c6a4-188">Cette erreur est retournée par <strong>JetEnumerateColumns</strong> si des ID de colonne spécifiques ont été demandés, si l’un de ces ID de colonne n’était pas valide et si le premier ID de colonne non valide a échoué avec cette erreur pour son code d’état de colonne.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-188">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column ids were requested, one of those column ids was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-189">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8c6a4-189">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-190">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-190">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-191">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="8c6a4-191">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-192">La colonne décrite par l’ID de colonne indiqué n’existe pas dans la table.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-192">The column described by the given column ID does not exist in the table.</span></span> <span data-ttu-id="8c6a4-193">Cette erreur est retournée par <strong>JetEnumerateColumns</strong> si des ID de colonne spécifiques ont été demandés, si l’un de ces ID de colonne n’était pas valide et si le premier ID de colonne non valide a échoué avec cette erreur pour son code d’état de colonne.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-193">This error will be returned by <strong>JetEnumerateColumns</strong> if specific column IDs were requested, one of those column IDs was invalid, and the first invalid column ID failed with this error for its column status code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-194">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8c6a4-194">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-195">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-195">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="8c6a4-196"><strong>Windows XP :  </strong> Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-196"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-197">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="8c6a4-197">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-198">L’une des options demandées n’est pas valide ou n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-198">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="8c6a4-199">Cette erreur est retournée par <strong>JetEnumerateColumns</strong> quand :</span><span class="sxs-lookup"><span data-stu-id="8c6a4-199">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="8c6a4-200">JET_bitEnumerateLocal est spécifié.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-200">JET_bitEnumerateLocal is specified.</span></span></p></li>
<li><p><span data-ttu-id="8c6a4-201">Un <em>Grbit</em> illégal est spécifié.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-201">An illegal <em>grbit</em> is specified.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-202">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8c6a4-202">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-203">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-203">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="8c6a4-204">Cette erreur est retournée par <strong>JetEnumerateColumns</strong> quand :</span><span class="sxs-lookup"><span data-stu-id="8c6a4-204">This error will be returned by <strong>JetEnumerateColumns</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="8c6a4-205"><em>pcEnumColumn</em> a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-205"><em>pcEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="8c6a4-206"><em>prgEnumColumn</em> a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-206"><em>prgEnumColumn</em> is <strong>NULL</strong>.</span></span></p></li>
<li><p><span data-ttu-id="8c6a4-207"><em>pfnRealloc</em> a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-207"><em>pfnRealloc</em> is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-208">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="8c6a4-208">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-209">Le curseur n’est pas positionné sur un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-209">The cursor is not positioned on a record.</span></span> <span data-ttu-id="8c6a4-210">Cela peut se produire pour de nombreuses raisons différentes.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-210">This can happen for many different reasons.</span></span> <span data-ttu-id="8c6a4-211">Par exemple, cela se produit si le curseur est actuellement positionné après le dernier enregistrement de l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-211">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-212">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8c6a4-212">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-213">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-213">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-214">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="8c6a4-214">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-215">Le curseur est positionné sur un enregistrement qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-215">The cursor is positioned on a record that has been deleted.</span></span> <span data-ttu-id="8c6a4-216">Cela peut se produire pour de nombreuses raisons différentes.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-216">This can happen for many different reasons.</span></span> <span data-ttu-id="8c6a4-217">La raison la plus courante est que la session n’est pas dans une transaction, que le curseur a été placé sur un enregistrement, que cet enregistrement a été supprimé, puis que le curseur a tenté de référencer cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-217">The most common reason is that the session is not in a transaction, the cursor was positioned on a record, that record was deleted, and then the cursor attempted to reference that record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-218">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8c6a4-218">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-219">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-219">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-220">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="8c6a4-220">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-221">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-221">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="8c6a4-222"><strong>Windows XP :  </strong> Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-222"><strong>Windows XP:  </strong>This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-223">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8c6a4-223">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8c6a4-224">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-224">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8c6a4-225">En cas de réussite, les données demandées sont retournées dans les tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-225">On success, the requested data will be returned in the output buffers.</span></span> <span data-ttu-id="8c6a4-226">Il incombe à l’appelant de libérer la mémoire allouée par ce rappel et renvoyée dans les mémoires tampons de sortie.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-226">It is the caller's responsibility to free any memory allocated by this callback and returned in the output buffers.</span></span> <span data-ttu-id="8c6a4-227">Cette mémoire doit être libérée par le rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fourni.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-227">That memory should be freed through the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="8c6a4-228">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-228">No change to the database state will occur.</span></span>

<span data-ttu-id="8c6a4-229">En cas d’échec, aucune des données demandées n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-229">On failure, none of the requested data will be returned.</span></span> <span data-ttu-id="8c6a4-230">Toute mémoire qui a été allouée pendant l’appel sera libérée automatiquement à l’aide du rappel compatible [réalloué](/cpp/c-runtime-library/reference/realloc?view=vs-2019) fourni.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-230">Any memory that was allocated during the call will be freed automatically using the provided [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback.</span></span> <span data-ttu-id="8c6a4-231">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-231">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8c6a4-232">Notes</span><span class="sxs-lookup"><span data-stu-id="8c6a4-232">Remarks</span></span>

<span data-ttu-id="8c6a4-233">Si vous énumérez toutes les valeurs de colonne dans l’enregistrement et que vous n’avez pas spécifié JET_bitEnumerateIgnoreDefaults, vous ne pouvez pas supposer que vous ne verrez jamais une colonne ou une valeur de colonne avec le code d’État JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-233">If you are enumerating all column values in the record and you did not specify JET_bitEnumerateIgnoreDefaults then you cannot assume that you will never see a column or column value with a status code of JET_wrnColumnNull.</span></span> <span data-ttu-id="8c6a4-234">Vous pouvez voir ce code d’État si une colonne a une valeur par défaut et a été explicitement définie sur **null** ou si la colonne est une colonne non éparse (par exemple, une colonne fixe ou variable).</span><span class="sxs-lookup"><span data-stu-id="8c6a4-234">You can see this status code if a column has a default value and was explicitly set to **NULL** or if the column is a non-sparse column (for example, a fixed or variable column).</span></span>

<span data-ttu-id="8c6a4-235">Le paramètre *cbDataMost* ne s’applique pas à toutes les valeurs de colonne.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-235">The *cbDataMost* parameter does not apply to all column values.</span></span> <span data-ttu-id="8c6a4-236">Ce paramètre tronque uniquement le texte long et les valeurs de colonne binaires longues qui sont tellement volumineuses qu’elles ont été stockées séparément de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-236">This parameter will only truncate long text and long binary column values that are so large that they have been stored separately from the record.</span></span>

<span data-ttu-id="8c6a4-237">Si **JetEnumerateColumns** retourne des données dans ses paramètres de sortie, l’appelant est chargé de libérer la mémoire dans le tableau, ainsi que toute mémoire référencée par des pointeurs incorporés dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-237">If **JetEnumerateColumns** returns data in its output parameters then the caller is responsible for freeing the memory in the array as well as any memory referred to by pointers embedded in that array.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8c6a4-238">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c6a4-238">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-239"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8c6a4-239"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6a4-240">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-240">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-241"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="8c6a4-241"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6a4-242">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-242">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-243"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="8c6a4-243"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6a4-244">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-244">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c6a4-245"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="8c6a4-245"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6a4-246">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-246">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c6a4-247"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8c6a4-247"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8c6a4-248">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8c6a4-248">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8c6a4-249">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c6a4-249">See Also</span></span>

[<span data-ttu-id="8c6a4-250">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8c6a4-250">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8c6a4-251">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8c6a4-251">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8c6a4-252">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8c6a4-252">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8c6a4-253">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8c6a4-253">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8c6a4-254">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="8c6a4-254">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="8c6a4-255">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8c6a4-255">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="8c6a4-256">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="8c6a4-256">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="8c6a4-257">JET_PFNREALLOC</span><span class="sxs-lookup"><span data-stu-id="8c6a4-257">JET_PFNREALLOC</span></span>](./jet-pfnrealloc-callback-function.md)  
[<span data-ttu-id="8c6a4-258">realloc</span><span class="sxs-lookup"><span data-stu-id="8c6a4-258">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[<span data-ttu-id="8c6a4-259">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="8c6a4-259">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="8c6a4-260">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="8c6a4-260">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)
