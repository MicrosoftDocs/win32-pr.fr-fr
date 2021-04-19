---
description: 'En savoir plus sur : structure JET_ENUMCOLUMNVALUE'
title: Structure JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518840"
---
# <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="f20cd-103">Structure JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="f20cd-103">JET_ENUMCOLUMNVALUE Structure</span></span>


<span data-ttu-id="f20cd-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f20cd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="f20cd-105">Structure JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="f20cd-105">JET_ENUMCOLUMNVALUE Structure</span></span>

<span data-ttu-id="f20cd-106">La structure **JET_ENUMCOLUMNVALUE** énumère les valeurs de colonne d’un enregistrement à l’aide de la fonction [JetEnumerateColumns](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f20cd-106">The **JET_ENUMCOLUMNVALUE** structure enumerates the column values of a record using the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function.</span></span> <span data-ttu-id="f20cd-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) retourne un tableau de structures **JET_ENUMCOLUMNVALUE** .</span><span class="sxs-lookup"><span data-stu-id="f20cd-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNVALUE** structures.</span></span> <span data-ttu-id="f20cd-108">Le tableau est retourné dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible qui a été fourni à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f20cd-108">The array is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that function.</span></span>

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a><span data-ttu-id="f20cd-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f20cd-109">Members</span></span>

<span data-ttu-id="f20cd-110">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="f20cd-110">**itagSequence**</span></span>

<span data-ttu-id="f20cd-111">Valeur de colonne (par index de base un) qui a été énumérée.</span><span class="sxs-lookup"><span data-stu-id="f20cd-111">The column value (by one-based index) that was enumerated.</span></span>

<span data-ttu-id="f20cd-112">**Raise**</span><span class="sxs-lookup"><span data-stu-id="f20cd-112">**err**</span></span>

<span data-ttu-id="f20cd-113">Code d’état de colonne résultant de l’énumération de la valeur de colonne.</span><span class="sxs-lookup"><span data-stu-id="f20cd-113">The column status code resulting from the enumeration of the column value.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f20cd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f20cd-114">Value</span></span></p></th>
<th><p><span data-ttu-id="f20cd-115">Signification</span><span class="sxs-lookup"><span data-stu-id="f20cd-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f20cd-116">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="f20cd-116">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="f20cd-117">La valeur de la colonne demandée est NULL.</span><span class="sxs-lookup"><span data-stu-id="f20cd-117">The requested column value is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f20cd-118">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="f20cd-118">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="f20cd-119">Le <em>itagSequence</em> spécifié dans l’élément du tableau <em>rgtagSequence</em> dans le struct <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> qui correspond à ce <strong>JET_ENUMCOLUMNVALUE</strong> struct était égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f20cd-119">The <em>itagSequence</em> that is specified in the element of the <em>rgtagSequence</em> array in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct corresponding to this <strong>JET_ENUMCOLUMNVALUE</strong> struct was zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f20cd-120">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="f20cd-120">JET_wrnColumnTruncated</span></span></p></td>
<td><p><span data-ttu-id="f20cd-121">La valeur de colonne demandée a été tronquée à la taille spécifiée avant d’être retournée.</span><span class="sxs-lookup"><span data-stu-id="f20cd-121">The requested column value was truncated to the specified size before being returned.</span></span></p>
<p><span data-ttu-id="f20cd-122">Cette troncation se produit uniquement pour les colonnes de texte long et les colonnes binaires longues contenant de grandes quantités de données.</span><span class="sxs-lookup"><span data-stu-id="f20cd-122">This truncation occurs only for long text and long binary columns that contain large amounts of data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f20cd-123">**cbData**</span><span class="sxs-lookup"><span data-stu-id="f20cd-123">**cbData**</span></span>

<span data-ttu-id="f20cd-124">Valeur de colonne qui a été énumérée pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="f20cd-124">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="f20cd-125">La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="f20cd-125">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="f20cd-126">**pvData**</span><span class="sxs-lookup"><span data-stu-id="f20cd-126">**pvData**</span></span>

<span data-ttu-id="f20cd-127">Valeur de colonne qui a été énumérée pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="f20cd-127">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="f20cd-128">La mémoire tampon de sortie est retournée dans la mémoire qui a été allouée à l’aide du rappel de [réallocation](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible fourni à [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="f20cd-128">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="f20cd-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f20cd-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f20cd-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f20cd-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f20cd-131">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f20cd-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f20cd-132"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f20cd-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f20cd-133">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f20cd-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f20cd-134"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f20cd-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f20cd-135">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f20cd-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f20cd-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f20cd-136">See Also</span></span>

[<span data-ttu-id="f20cd-137">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="f20cd-137">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="f20cd-138">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="f20cd-138">JET_ENUMCOLUMNVALUE</span></span>]()  
[<span data-ttu-id="f20cd-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f20cd-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f20cd-140">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="f20cd-140">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="f20cd-141">realloc</span><span class="sxs-lookup"><span data-stu-id="f20cd-141">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
