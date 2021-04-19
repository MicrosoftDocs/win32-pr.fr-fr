---
description: 'En savoir plus sur : fonction JetGetThreadStats'
title: JetGetThreadStats fonction)
TOCTitle: JetGetThreadStats Function
ms:assetid: 1b8df8cd-fc61-44fe-a15c-a166f7097c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269196(v=EXCHG.10)
ms:contentKeyID: 32765499
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetThreadStats
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85d45021910f818f297cd0bc9829580a18b7a296
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514779"
---
# <a name="jetgetthreadstats-function"></a><span data-ttu-id="eaaea-103">JetGetThreadStats fonction)</span><span class="sxs-lookup"><span data-stu-id="eaaea-103">JetGetThreadStats Function</span></span>


<span data-ttu-id="eaaea-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="eaaea-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetthreadstats-function"></a><span data-ttu-id="eaaea-105">JetGetThreadStats fonction)</span><span class="sxs-lookup"><span data-stu-id="eaaea-105">JetGetThreadStats Function</span></span>

<span data-ttu-id="eaaea-106">La fonction **JetGetThreadStats** récupère les informations de performance du moteur de base de données pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="eaaea-106">The **JetGetThreadStats** function retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="eaaea-107">Plusieurs appels peuvent être utilisés pour collecter des statistiques qui reflètent l’activité du moteur de base de données sur ce thread entre ces appels.</span><span class="sxs-lookup"><span data-stu-id="eaaea-107">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="eaaea-108">**Windows Vista :**  **JetGetThreadStats** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eaaea-108">**Windows Vista:**  **JetGetThreadStats** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetThreadStats(
      __out         void* pvResult,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a><span data-ttu-id="eaaea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eaaea-109">Parameters</span></span>

<span data-ttu-id="eaaea-110">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="eaaea-110">*pvResult*</span></span>

<span data-ttu-id="eaaea-111">Mémoire tampon de sortie qui reçoit les données de statistiques de thread.</span><span class="sxs-lookup"><span data-stu-id="eaaea-111">The output buffer which receives the thread statistics data.</span></span> <span data-ttu-id="eaaea-112">La mémoire tampon contient une structure [JET_THREADSTATS](./jet-threadstats-structure.md) après un appel réussi.</span><span class="sxs-lookup"><span data-stu-id="eaaea-112">The buffer contains a [JET_THREADSTATS](./jet-threadstats-structure.md) structure after a successful call.</span></span>

<span data-ttu-id="eaaea-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="eaaea-113">*cbMax*</span></span>

<span data-ttu-id="eaaea-114">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="eaaea-114">The maximum size in bytes of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="eaaea-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eaaea-115">Return Value</span></span>

<span data-ttu-id="eaaea-116">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="eaaea-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="eaaea-117">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eaaea-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eaaea-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="eaaea-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="eaaea-119">Description</span><span class="sxs-lookup"><span data-stu-id="eaaea-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eaaea-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="eaaea-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="eaaea-121">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="eaaea-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaaea-122">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="eaaea-122">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="eaaea-123">L’opération a échoué, car la mémoire tampon de sortie fournie était trop petite pour contenir les données demandées.</span><span class="sxs-lookup"><span data-stu-id="eaaea-123">The operation failed because the provided output buffer was too small to contain the requested data.</span></span> <span data-ttu-id="eaaea-124">La fonction <strong>JetGetThreadStats</strong> renvoie cette erreur lorsque la mémoire tampon de sortie est trop petite pour contenir la version la plus petite de la structure <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> prise en charge par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="eaaea-124">The <strong>JetGetThreadStats</strong> function will return this error when the output buffer is too small to contain the smallest version of the <a href="gg269227(v=exchg.10).md">JET_THREADSTATS</a> structure supported by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eaaea-125">En cas de réussite, la mémoire tampon de sortie contient une structure [JET_THREADSTATS](./jet-threadstats-structure.md) qui contient les statistiques du moteur de base de données pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="eaaea-125">On success, the output buffer will contain a [JET_THREADSTATS](./jet-threadstats-structure.md) structure that contains database engine statistics for the current thread.</span></span>

<span data-ttu-id="eaaea-126">En cas d’échec, l’état de la mémoire tampon de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="eaaea-126">On failure, the state of the output buffer is undefined.</span></span>

#### <a name="remarks"></a><span data-ttu-id="eaaea-127">Notes</span><span class="sxs-lookup"><span data-stu-id="eaaea-127">Remarks</span></span>

<span data-ttu-id="eaaea-128">Les informations fournies par deux appels consécutifs de cette API sont destinées à calculer le coût des autres opérations du moteur de base de données sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="eaaea-128">The information provided by two consecutive calls of this API are intended to be used to compute the expense of any other database engine operations on the current thread.</span></span> <span data-ttu-id="eaaea-129">En règle générale, cette opération s’effectue en acceptant une valeur avant et après la lecture des statistiques et en soustrayant le nombre d’opérations après le comptage avant d’obtenir le nombre net d’opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="eaaea-129">Generally, this is done by taking a before and after reading of the statistics and subtracting the after count from the before count to get the net count of operations performed.</span></span>

<span data-ttu-id="eaaea-130">Par exemple, une application peut appeler **JetGetThreadStats** une fois pour obtenir une lecture initiale des statistiques du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="eaaea-130">For example, an application could call **JetGetThreadStats** once to get an initial reading of the statistics for the current thread.</span></span> <span data-ttu-id="eaaea-131">Elle peut ensuite appeler la fonction [JetMove](./jetmove-function.md) avec le paramètre *cRow* défini sur JET_MoveNext pour passer à l’entrée d’index suivante sur un index.</span><span class="sxs-lookup"><span data-stu-id="eaaea-131">It could then call the [JetMove](./jetmove-function.md) function with the *cRow* parameter set to JET_MoveNext to move to the next index entry on an index.</span></span> <span data-ttu-id="eaaea-132">Il peut ensuite appeler **JetGetThreadStats** à nouveau pour recevoir une autre lecture des statistiques du thread.</span><span class="sxs-lookup"><span data-stu-id="eaaea-132">It could then call **JetGetThreadStats** again to get another reading of the thread's statistics.</span></span> <span data-ttu-id="eaaea-133">Il peut ensuite soustraire le compteur cPageReferenced de la deuxième lecture du premier.</span><span class="sxs-lookup"><span data-stu-id="eaaea-133">It could then subtract the cPageReferenced counter from the second reading from the first.</span></span> <span data-ttu-id="eaaea-134">Le résultat est le nombre de pages de base de données référencées par le moteur de base de données pour effectuer l’opération [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="eaaea-134">The result would be the number of database pages referenced by the database engine to perform the [JetMove](./jetmove-function.md) operation.</span></span>

<span data-ttu-id="eaaea-135">Les statistiques de chaque thread sont accumulées pendant la durée de vie de ce thread.</span><span class="sxs-lookup"><span data-stu-id="eaaea-135">The statistics for each thread are accumulated for the lifetime of that thread.</span></span> <span data-ttu-id="eaaea-136">Les statistiques sont réinitialisées si la DLL du moteur de base de données est déchargée du processus hôte.</span><span class="sxs-lookup"><span data-stu-id="eaaea-136">The statistics are reset if the database engine's DLL is unloaded from the host process.</span></span>

<span data-ttu-id="eaaea-137">La structure [JET_THREADSTATS](./jet-threadstats-structure.md) sera probablement développée à l’avenir pour contenir plus de statistiques.</span><span class="sxs-lookup"><span data-stu-id="eaaea-137">The [JET_THREADSTATS](./jet-threadstats-structure.md) structure will likely be expanded in the future to contain more statistics.</span></span> <span data-ttu-id="eaaea-138">De nouvelles statistiques seront ajoutées à la fin de la structure et peuvent être récupérées avec une taille de mémoire tampon de sortie accrue.</span><span class="sxs-lookup"><span data-stu-id="eaaea-138">New statistics will be added to the end of the structure and can be retrieved with an increased output buffer size.</span></span> <span data-ttu-id="eaaea-139">La présence de statistiques supplémentaires peut être déduite par une valeur cbStruct plus grande.</span><span class="sxs-lookup"><span data-stu-id="eaaea-139">The presence of additional statistics can be inferred by a larger cbStruct value.</span></span>

#### <a name="requirements"></a><span data-ttu-id="eaaea-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaaea-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eaaea-141"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="eaaea-141"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eaaea-142">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eaaea-142">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaaea-143"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="eaaea-143"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eaaea-144">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="eaaea-144">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaaea-145"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="eaaea-145"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eaaea-146">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="eaaea-146">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eaaea-147"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="eaaea-147"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="eaaea-148">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="eaaea-148">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eaaea-149"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="eaaea-149"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="eaaea-150">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="eaaea-150">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="eaaea-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaaea-151">See Also</span></span>

[<span data-ttu-id="eaaea-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="eaaea-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="eaaea-153">JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="eaaea-153">JET_THREADSTATS</span></span>](./jet-threadstats-structure.md)  
[<span data-ttu-id="eaaea-154">JetMove</span><span class="sxs-lookup"><span data-stu-id="eaaea-154">JetMove</span></span>](./jetmove-function.md)
