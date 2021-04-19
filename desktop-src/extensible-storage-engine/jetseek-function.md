---
description: 'En savoir plus sur : fonction JetSeek'
title: JetSeek fonction)
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520165"
---
# <a name="jetseek-function"></a><span data-ttu-id="d0272-103">JetSeek fonction)</span><span class="sxs-lookup"><span data-stu-id="d0272-103">JetSeek Function</span></span>


<span data-ttu-id="d0272-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d0272-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetseek-function"></a><span data-ttu-id="d0272-105">JetSeek fonction)</span><span class="sxs-lookup"><span data-stu-id="d0272-105">JetSeek Function</span></span>

<span data-ttu-id="d0272-106">La fonction **JetSeek** positionne efficacement un curseur sur une entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et l’inégalité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d0272-106">The **JetSeek** function efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="d0272-107">Une clé de recherche doit avoir été construite précédemment à l’aide de [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="d0272-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d0272-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0272-108">Parameters</span></span>

<span data-ttu-id="d0272-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d0272-109">*sesid*</span></span>

<span data-ttu-id="d0272-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="d0272-110">The session to use for this call.</span></span>

<span data-ttu-id="d0272-111">*TableID*</span><span class="sxs-lookup"><span data-stu-id="d0272-111">*tableid*</span></span>

<span data-ttu-id="d0272-112">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="d0272-112">The cursor to use for this call.</span></span>

<span data-ttu-id="d0272-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d0272-113">*grbit*</span></span>

<span data-ttu-id="d0272-114">Groupe de bits qui contient les options à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="d0272-114">A group of bits that contain the options to be used for this call.</span></span> <span data-ttu-id="d0272-115">*Grbit* doit être différent de zéro et doit inclure une ou plusieurs des valeurs énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d0272-115">*Grbit* must be nonzero and must include one or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0272-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0272-116">Value</span></span></p></th>
<th><p><span data-ttu-id="d0272-117">Signification</span><span class="sxs-lookup"><span data-stu-id="d0272-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0272-118">JET_bitCheckUniqueness</span><span class="sxs-lookup"><span data-stu-id="d0272-118">JET_bitCheckUniqueness</span></span></p></td>
<td><p><span data-ttu-id="d0272-119">Un code d’erreur spécial, JET_wrnUniqueKey, est retourné s’il peut être déterminé de manière économique qu’il existe une seule entrée d’index correspondant à la clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-119">A special error code, JET_wrnUniqueKey, will be returned if it can be cheaply determined that there is exactly one index entry that matches the search key.</span></span></p>
<p><span data-ttu-id="d0272-120">Cette option est ignorée sauf si JET_bitSeekEQ est également spécifié.</span><span class="sxs-lookup"><span data-stu-id="d0272-120">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p>
<p><span data-ttu-id="d0272-121">Cette option est disponible uniquement sur Windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d0272-121">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-122">JET_bitSeekEQ</span><span class="sxs-lookup"><span data-stu-id="d0272-122">JET_bitSeekEQ</span></span></p></td>
<td><p><span data-ttu-id="d0272-123">Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui correspond exactement à la clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-123">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span> <span data-ttu-id="d0272-124">Le début de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le premier enregistrement de cet index.</span><span class="sxs-lookup"><span data-stu-id="d0272-124">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="d0272-125">Le début de l’index n’est pas le même que le bas de l’index, ce qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-125">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="d0272-126">Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique.</span><span class="sxs-lookup"><span data-stu-id="d0272-126">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-127">JET_bitSeekGE</span><span class="sxs-lookup"><span data-stu-id="d0272-127">JET_bitSeekGE</span></span></p></td>
<td><p><span data-ttu-id="d0272-128">Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui est supérieure ou égale à une entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-128">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="d0272-129">Le début de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le premier enregistrement de cet index.</span><span class="sxs-lookup"><span data-stu-id="d0272-129">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="d0272-130">Le début de l’index n’est pas le même que le bas de l’index, ce qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-130">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="d0272-131">Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches de la fin de l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-131">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-132">JET_bitSeekGT</span><span class="sxs-lookup"><span data-stu-id="d0272-132">JET_bitSeekGT</span></span></p></td>
<td><p><span data-ttu-id="d0272-133">Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui est supérieure à une entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-133">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="d0272-134">Le début de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le premier enregistrement de cet index.</span><span class="sxs-lookup"><span data-stu-id="d0272-134">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="d0272-135">Le début de l’index n’est pas le même que le bas de l’index, ce qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-135">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="d0272-136">Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches du début de l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-136">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-137">JET_bitSeekLE</span><span class="sxs-lookup"><span data-stu-id="d0272-137">JET_bitSeekLE</span></span></p></td>
<td><p><span data-ttu-id="d0272-138">Le curseur est positionné à l’entrée d’index la plus proche de la fin de l’index qui est inférieure ou égale à une entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-138">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="d0272-139">La fin de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le dernier enregistrement de cet index.</span><span class="sxs-lookup"><span data-stu-id="d0272-139">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="d0272-140">La fin de l’index n’est pas identique à la fin de l’index, qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-140">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="d0272-141">Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches du début de l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-141">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-142">JET_bitSeekLT</span><span class="sxs-lookup"><span data-stu-id="d0272-142">JET_bitSeekLT</span></span></p></td>
<td><p><span data-ttu-id="d0272-143">Le curseur est positionné à l’entrée d’index la plus proche de la fin de l’index qui est inférieure à une entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-143">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="d0272-144">La fin de l’index correspond à l’entrée d’index trouvée lors du déplacement vers le dernier enregistrement de cet index.</span><span class="sxs-lookup"><span data-stu-id="d0272-144">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="d0272-145">La fin de l’index n’est pas identique à la fin de l’index, qui peut varier en fonction de l’ordre de tri des colonnes clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-145">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="d0272-146">Il n’est pas judicieux d’utiliser cette option avec une clé de recherche qui a été construite à l’aide de <a href="gg269329(v=exchg.10).md">JetMakeKey</a> à l’aide d’une option générique destinée à rechercher les entrées d’index les plus proches de la fin de l’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-146">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-147">JET_bitSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d0272-147">JET_bitSetIndexRange</span></span></p></td>
<td><p><span data-ttu-id="d0272-148">Une plage d’index sera automatiquement configurée pour toutes les clés qui correspondent exactement à la clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-148">An index range will automatically be setup for all keys that exactly match the search key.</span></span> <span data-ttu-id="d0272-149">La plage d’index résultante est identique à celle qui aurait été créée par un appel à <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> avec les options JET_bitRangeInclusive et JET_bitRangeUpperLimit.</span><span class="sxs-lookup"><span data-stu-id="d0272-149">The resulting index range is identical to one that would have otherwise been created by a call to <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> with the JET_bitRangeInclusive and JET_bitRangeUpperLimit options.</span></span> <span data-ttu-id="d0272-150">Pour plus d’informations, consultez <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> .</span><span class="sxs-lookup"><span data-stu-id="d0272-150">See <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> for more information.</span></span></p>
<p><span data-ttu-id="d0272-151">Il s’agit d’une méthode pratique pour découvrir toutes les entrées d’index qui correspondent aux mêmes critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-151">This is a convenient method for discovering all the index entries that match the same search criteria.</span></span></p>
<p><span data-ttu-id="d0272-152">Cette option est ignorée sauf si JET_bitSeekEQ est également spécifié.</span><span class="sxs-lookup"><span data-stu-id="d0272-152">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d0272-153">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0272-153">Return Value</span></span>

<span data-ttu-id="d0272-154">Cette fonction permet le retour de tout [JET_ERRs](./jet-err.md) défini dans cette API.</span><span class="sxs-lookup"><span data-stu-id="d0272-154">This function allows for the return of any [JET_ERRs](./jet-err.md) that are defined in this API.</span></span> <span data-ttu-id="d0272-155">Pour plus d’informations sur les erreurs jet, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d0272-155">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0272-156">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d0272-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="d0272-157">Description</span><span class="sxs-lookup"><span data-stu-id="d0272-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0272-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d0272-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d0272-159">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d0272-159">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="d0272-160">Pour <strong>JetSeek</strong>, cela signifie qu’une entrée d’index correspondant exactement aux critères de recherche a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="d0272-160">For <strong>JetSeek</strong>, this means that an index entry was found that exactly matched the search criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-161">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d0272-161">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d0272-162">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d0272-162">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-163">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d0272-163">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d0272-164">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="d0272-164">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d0272-165">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d0272-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-166">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="d0272-166">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="d0272-167">Il n’existe pas de clé de recherche pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="d0272-167">There is no current search key for the cursor.</span></span> <span data-ttu-id="d0272-168"><strong>JetSeek</strong> requiert que le curseur ait une clé de recherche valide, car il l’utilise pour les critères de recherche utilisés pour rechercher des entrées d’index.</span><span class="sxs-lookup"><span data-stu-id="d0272-168"><strong>JetSeek</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-169">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d0272-169">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d0272-170">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="d0272-170">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-171">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="d0272-171">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="d0272-172">Aucune entrée d’index correspondant aux critères de recherche n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="d0272-172">No index entry was found that matched the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d0272-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d0272-174">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="d0272-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-175">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="d0272-175">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="d0272-176">Une entrée d’index correspondant aux critères de recherche a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="d0272-176">An index entry was found that matched the search criteria.</span></span> <span data-ttu-id="d0272-177">Toutefois, cette entrée d’index n’était pas une correspondance exacte.</span><span class="sxs-lookup"><span data-stu-id="d0272-177">However, that index entry was not an exact match.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-178">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d0272-178">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d0272-179">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="d0272-179">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d0272-180">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d0272-180">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-181">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d0272-181">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d0272-182">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="d0272-182">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-183">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="d0272-183">JET_wrnUniqueKey</span></span></p></td>
<td><p><span data-ttu-id="d0272-184">Une seule entrée d’index a été trouvée et correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-184">Exactly one index entry was found that exactly matched the search criteria.</span></span> <span data-ttu-id="d0272-185">Cette erreur est renvoyée uniquement si JET_bitSeekCheckUniqueness a été spécifiée et qu’elle était économique pour déterminer que l’entrée d’index correspondante était la seule entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-185">This error will only be returned if JET_bitSeekCheckUniqueness was specified and it was cheap to determine that the matching index entry was the only index entry that exactly matches the search criteria.</span></span></p>
<p><span data-ttu-id="d0272-186">Cette erreur est renvoyée uniquement par Windows Server 2003 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d0272-186">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d0272-187">En cas de réussite, le curseur est positionné au niveau d’une entrée d’index qui correspond aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d0272-187">On success, the cursor will be positioned at an index entry that matches the search criteria.</span></span> <span data-ttu-id="d0272-188">Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée.</span><span class="sxs-lookup"><span data-stu-id="d0272-188">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="d0272-189">Si une plage d’index est en vigueur, cette plage d’index sera annulée.</span><span class="sxs-lookup"><span data-stu-id="d0272-189">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="d0272-190">Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="d0272-190">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="d0272-191">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="d0272-191">No change to the database state will occur.</span></span> <span data-ttu-id="d0272-192">Lorsque plusieurs entrées d’index ont la même valeur, l’entrée la plus proche du début de l’index est toujours sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d0272-192">When multiple index entries have the same value, the entry closest to the start of the index is always selected.</span></span>

<span data-ttu-id="d0272-193">En cas d’échec, la position du curseur reste inchangée, à moins que JET_errRecordNotFound ne soit retourné.</span><span class="sxs-lookup"><span data-stu-id="d0272-193">On failure, the position of the cursor will remain unchanged unless JET_errRecordNotFound was returned.</span></span> <span data-ttu-id="d0272-194">Dans ce cas, le curseur est positionné à l’emplacement où l’entrée d’index qui correspondait aux critères de recherche spécifiés par la clé de recherche dans ce curseur et l’inégalité spécifiée aurait été.</span><span class="sxs-lookup"><span data-stu-id="d0272-194">In that case, the cursor will be positioned where the index entry that matched the search criteria specified by the search key in that cursor and the specified inequality would have been.</span></span> <span data-ttu-id="d0272-195">Le curseur peut être déplacé par rapport à cette position, mais il n’est pas toujours sur une entrée d’index valide.</span><span class="sxs-lookup"><span data-stu-id="d0272-195">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="d0272-196">Si un enregistrement a été préparé pour la mise à jour, cette mise à jour sera annulée.</span><span class="sxs-lookup"><span data-stu-id="d0272-196">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="d0272-197">Si une plage d’index est en vigueur, cette plage d’index sera annulée.</span><span class="sxs-lookup"><span data-stu-id="d0272-197">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="d0272-198">Si une clé de recherche a été construite pour le curseur, cette clé de recherche sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="d0272-198">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="d0272-199">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="d0272-199">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d0272-200">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0272-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0272-201"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d0272-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d0272-202">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="d0272-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-203"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d0272-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d0272-204">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d0272-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-205"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="d0272-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d0272-206">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d0272-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0272-207"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="d0272-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d0272-208">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d0272-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0272-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d0272-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d0272-210">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d0272-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d0272-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0272-211">See Also</span></span>

[<span data-ttu-id="d0272-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d0272-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d0272-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d0272-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d0272-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d0272-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d0272-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d0272-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d0272-216">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="d0272-216">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="d0272-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d0272-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="d0272-218">JetStopService</span><span class="sxs-lookup"><span data-stu-id="d0272-218">JetStopService</span></span>](./jetstopservice-function.md)
