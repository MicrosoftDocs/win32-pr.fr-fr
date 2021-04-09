---
description: 'En savoir plus sur : structure JET_ENUMCOLUMN'
title: Structure JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN Structure
ms:assetid: f8f512fd-5fcf-47ed-a5db-2fb3bd76c2d7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294138(v=EXCHG.10)
ms:contentKeyID: 32765752
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
ms.openlocfilehash: ca204fef4e67e6883584511b1ac424149a137b79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112107"
---
# <a name="jet_enumcolumn-structure"></a><span data-ttu-id="269f1-103">Structure JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="269f1-103">JET_ENUMCOLUMN Structure</span></span>


<span data-ttu-id="269f1-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="269f1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumn-structure"></a><span data-ttu-id="269f1-105">Structure JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="269f1-105">JET_ENUMCOLUMN Structure</span></span>

<span data-ttu-id="269f1-106">La structure **JET_ENUMCOLUMN** énumère les valeurs de colonne d’un enregistrement lorsque la fonction [JetEnumerateColumns](./jetenumeratecolumns-function.md) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="269f1-106">The **JET_ENUMCOLUMN** structure enumerates the column values of a record when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="269f1-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) retourne un tableau de structures **JET_ENUMCOLUMN** .</span><span class="sxs-lookup"><span data-stu-id="269f1-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMN** structures.</span></span> <span data-ttu-id="269f1-108">Le tableau est retourné dans la mémoire qui est allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible qui a été fourni à cette API.</span><span class="sxs-lookup"><span data-stu-id="269f1-108">The array is returned in memory that is allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that API.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      JET_ERR err;
      union {
        struct {
          unsigned long cEnumColumnValue;
          JET_ENUMCOLUMNVALUE rgEnumColumnValue;
        };
        struct {
          unsigned long cbData;
          void* pvData;
        };
      };
    } JET_ENUMCOLUMN;
```

### <a name="members"></a><span data-ttu-id="269f1-109">Membres</span><span class="sxs-lookup"><span data-stu-id="269f1-109">Members</span></span>

<span data-ttu-id="269f1-110">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="269f1-110">**columnid**</span></span>

<span data-ttu-id="269f1-111">ID de colonne qui a été énuméré.</span><span class="sxs-lookup"><span data-stu-id="269f1-111">The column ID that was enumerated.</span></span>

<span data-ttu-id="269f1-112">**Raise**</span><span class="sxs-lookup"><span data-stu-id="269f1-112">**err**</span></span>

<span data-ttu-id="269f1-113">Code d’état de la colonne qui résulte de l’énumération de la colonne.</span><span class="sxs-lookup"><span data-stu-id="269f1-113">The column status code that results from the enumeration of the column.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="269f1-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="269f1-114">Error Codes</span></span></p></th>
<th><p><span data-ttu-id="269f1-115">Signification</span><span class="sxs-lookup"><span data-stu-id="269f1-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="269f1-116">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="269f1-116">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="269f1-117">L’ID de colonne est en dehors des limites autorisées d’un ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="269f1-117">The column ID is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="269f1-118">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="269f1-118">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="269f1-119">La colonne décrite par l’ID de colonne n’existe pas dans la table.</span><span class="sxs-lookup"><span data-stu-id="269f1-119">The column described by the column ID does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="269f1-120">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="269f1-120">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="269f1-121">Toutes les valeurs de cette colonne sont NULL.</span><span class="sxs-lookup"><span data-stu-id="269f1-121">All values for this column are NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="269f1-122">JET_wrnColumnPresent</span><span class="sxs-lookup"><span data-stu-id="269f1-122">JET_wrnColumnPresent</span></span></p></td>
<td><p><span data-ttu-id="269f1-123">JET_bitEnumeratePresenceOnly a été spécifié et au moins une valeur de colonne non NULL aurait été retournée pour cette colonne.</span><span class="sxs-lookup"><span data-stu-id="269f1-123">JET_bitEnumeratePresenceOnly was specified and at least one non-NULL column value would have been returned for this column.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="269f1-124">JET_wrnColumnSingleValue</span><span class="sxs-lookup"><span data-stu-id="269f1-124">JET_wrnColumnSingleValue</span></span></p></td>
<td><p><span data-ttu-id="269f1-125">JET_bitEnumerateCompressOutput a été spécifié et une seule valeur de colonne non NULL a été retournée pour cette colonne.</span><span class="sxs-lookup"><span data-stu-id="269f1-125">JET_bitEnumerateCompressOutput was specified and exactly one non-NULL column value has been returned for this column.</span></span> <span data-ttu-id="269f1-126">Par conséquent, la forme compressée de <strong>JET_ENUMCOLUMN</strong> a été retournée.</span><span class="sxs-lookup"><span data-stu-id="269f1-126">As a result, the compressed form of <strong>JET_ENUMCOLUMN</strong> has been returned.</span></span> <span data-ttu-id="269f1-127">Pour plus d’informations, consultez <strong>JET_ENUMCOLUMN</strong> .</span><span class="sxs-lookup"><span data-stu-id="269f1-127">See <strong>JET_ENUMCOLUMN</strong> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="269f1-128">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="269f1-128">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="269f1-129">L’ID de colonne dans le struct <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> qui correspond à ce <strong>JET_ENUMCOLUMN</strong> struct était égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="269f1-129">The column ID in the <a href="gg269251(v=exchg.10).md">JET_ENUMCOLUMNID</a> struct corresponding to this <strong>JET_ENUMCOLUMN</strong> struct was zero.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="269f1-130">**cEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="269f1-130">**cEnumColumnValue**</span></span>

<span data-ttu-id="269f1-131">Tableau de valeurs de colonne qui a été énuméré pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="269f1-131">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="269f1-132">La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="269f1-132">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="269f1-133">Cette mémoire tampon de sortie est utilisée lorsque le code d’état de la colonne n’est pas égal à JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="269f1-133">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="269f1-134">Pour plus d’informations, consultez [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="269f1-134">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="269f1-135">Cette erreur est retournée si « Err \! = JET_wrnColumnSingleValue ».</span><span class="sxs-lookup"><span data-stu-id="269f1-135">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="269f1-136">**rgEnumColumnValue**</span><span class="sxs-lookup"><span data-stu-id="269f1-136">**rgEnumColumnValue**</span></span>

<span data-ttu-id="269f1-137">Tableau de valeurs de colonne qui a été énuméré pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="269f1-137">The array of column values that was enumerated for the column.</span></span> <span data-ttu-id="269f1-138">La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="269f1-138">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="269f1-139">Cette mémoire tampon de sortie est utilisée lorsque le code d’état de la colonne n’est pas égal à JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="269f1-139">This output buffer is used when the column status code is not equal to JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="269f1-140">Pour plus d’informations, consultez [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="269f1-140">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="269f1-141">Cette erreur est retournée si « Err \! = JET_wrnColumnSingleValue ».</span><span class="sxs-lookup"><span data-stu-id="269f1-141">This is returned if "err \!= JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="269f1-142">**cbData**</span><span class="sxs-lookup"><span data-stu-id="269f1-142">**cbData**</span></span>

<span data-ttu-id="269f1-143">Valeur de colonne qui a été énumérée pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="269f1-143">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="269f1-144">La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="269f1-144">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="269f1-145">Cette mémoire tampon de sortie est utilisée uniquement lorsque le code d’état de la colonne est JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="269f1-145">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="269f1-146">Pour plus d’informations, consultez [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="269f1-146">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="269f1-147">Cette erreur est retournée si « Err = = JET_wrnColumnSingleValue ».</span><span class="sxs-lookup"><span data-stu-id="269f1-147">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

<span data-ttu-id="269f1-148">**pvData**</span><span class="sxs-lookup"><span data-stu-id="269f1-148">**pvData**</span></span>

<span data-ttu-id="269f1-149">Valeur de colonne qui a été énumérée pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="269f1-149">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="269f1-150">La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="269f1-150">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="269f1-151">Cette mémoire tampon de sortie est utilisée uniquement lorsque le code d’état de la colonne est JET_wrnColumnSingleValue.</span><span class="sxs-lookup"><span data-stu-id="269f1-151">This output buffer is only used when the column status code is JET_wrnColumnSingleValue.</span></span> <span data-ttu-id="269f1-152">Pour plus d’informations, consultez [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="269f1-152">For more information, see [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="269f1-153">Cette erreur est retournée si « Err = = JET_wrnColumnSingleValue ».</span><span class="sxs-lookup"><span data-stu-id="269f1-153">This is returned if "err == JET_wrnColumnSingleValue".</span></span>

### <a name="requirements"></a><span data-ttu-id="269f1-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="269f1-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="269f1-155"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="269f1-155"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="269f1-156">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="269f1-156">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="269f1-157"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="269f1-157"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="269f1-158">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="269f1-158">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="269f1-159"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="269f1-159"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="269f1-160">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="269f1-160">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="269f1-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="269f1-161">See Also</span></span>

[<span data-ttu-id="269f1-162">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="269f1-162">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="269f1-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="269f1-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="269f1-164">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="269f1-164">JET_ENUMCOLUMNID</span></span>](./jet-enumcolumnid-structure.md)  
[<span data-ttu-id="269f1-165">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="269f1-165">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="269f1-166">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="269f1-166">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="269f1-167">realloc</span><span class="sxs-lookup"><span data-stu-id="269f1-167">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
