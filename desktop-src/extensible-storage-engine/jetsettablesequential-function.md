---
description: 'En savoir plus sur : fonction JetSetTableSequential'
title: JetSetTableSequential fonction)
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536965"
---
# <a name="jetsettablesequential-function"></a><span data-ttu-id="a77f8-103">JetSetTableSequential fonction)</span><span class="sxs-lookup"><span data-stu-id="a77f8-103">JetSetTableSequential Function</span></span>


<span data-ttu-id="a77f8-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a77f8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsettablesequential-function"></a><span data-ttu-id="a77f8-105">JetSetTableSequential fonction)</span><span class="sxs-lookup"><span data-stu-id="a77f8-105">JetSetTableSequential Function</span></span>

<span data-ttu-id="a77f8-106">La fonction **JetSetTableSequential** avertit le moteur de base de données que l’application analyse l’intégralité de l’index actuel qui contient un curseur donné.</span><span class="sxs-lookup"><span data-stu-id="a77f8-106">The **JetSetTableSequential** function notifies the database engine that the application is scanning the entire current index that contains a given cursor.</span></span> <span data-ttu-id="a77f8-107">Par conséquent, les méthodes utilisées pour accéder aux données d’index seront paramétrées pour rendre ce scénario aussi rapide que possible.</span><span class="sxs-lookup"><span data-stu-id="a77f8-107">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span>

<span data-ttu-id="a77f8-108">**Windows XP :**  **JetSetTableSequential** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a77f8-108">**Windows XP:**  **JetSetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a77f8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a77f8-109">Parameters</span></span>

<span data-ttu-id="a77f8-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a77f8-110">*sesid*</span></span>

<span data-ttu-id="a77f8-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="a77f8-111">The session to use for this call.</span></span>

<span data-ttu-id="a77f8-112">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a77f8-112">*tableid*</span></span>

<span data-ttu-id="a77f8-113">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="a77f8-113">The cursor to use for this call.</span></span>

<span data-ttu-id="a77f8-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a77f8-114">*grbit*</span></span>

<span data-ttu-id="a77f8-115">Groupe de bits qui spécifient zéro, une ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="a77f8-115">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a77f8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a77f8-116">Value</span></span></p></th>
<th><p><span data-ttu-id="a77f8-117">Signification</span><span class="sxs-lookup"><span data-stu-id="a77f8-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a77f8-118">JET_bitPrereadForward</span><span class="sxs-lookup"><span data-stu-id="a77f8-118">JET_bitPrereadForward</span></span></p></td>
<td><p><span data-ttu-id="a77f8-119">Cette option est utilisée pour indexer vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="a77f8-119">This option is used to index in the forward direction.</span></span></p>
<p><span data-ttu-id="a77f8-120"><strong>Windows 7 :</strong>  <strong>JET_bitPrereadForward</strong> est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a77f8-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a77f8-121">JET_bitPrereadBackward</span><span class="sxs-lookup"><span data-stu-id="a77f8-121">JET_bitPrereadBackward</span></span></p></td>
<td><p><span data-ttu-id="a77f8-122">Cette option est utilisée pour indexer dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="a77f8-122">This option is used to index in the backward direction.</span></span></p>
<p><span data-ttu-id="a77f8-123"><strong>Windows 7 :</strong>  <strong>JET_bitPrereadBackward</strong> est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a77f8-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a77f8-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a77f8-124">Return Value</span></span>

<span data-ttu-id="a77f8-125">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="a77f8-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a77f8-126">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a77f8-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a77f8-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a77f8-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="a77f8-128">Description</span><span class="sxs-lookup"><span data-stu-id="a77f8-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a77f8-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a77f8-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a77f8-130">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été suspendue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a77f8-130">The operation cannot complete because all activity on the instance that is associated with the session has been quiesced as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a77f8-131">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a77f8-131">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a77f8-132">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="a77f8-132">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a77f8-133"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a77f8-133"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a77f8-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a77f8-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a77f8-135">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="a77f8-135">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a77f8-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a77f8-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a77f8-137">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="a77f8-137">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a77f8-138">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a77f8-138">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a77f8-139">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a77f8-139">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a77f8-140">Si cette fonction fonctionne, l’index actuel du curseur est optimisé pour une analyse séquentielle de la totalité de l’index.</span><span class="sxs-lookup"><span data-stu-id="a77f8-140">If this function succeeds, the current index of the cursor is optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="a77f8-141">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a77f8-141">No change to the database state will occur.</span></span>

<span data-ttu-id="a77f8-142">Si cette fonction échoue, aucune modification de la configuration du curseur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a77f8-142">If this function fails, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="a77f8-143">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a77f8-143">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a77f8-144">Notes</span><span class="sxs-lookup"><span data-stu-id="a77f8-144">Remarks</span></span>

<span data-ttu-id="a77f8-145">Si l’application doit analyser efficacement un sous-ensemble connu d’un index, une optimisation similaire est également effectuée chaque fois qu’une plage d’index est établie à l’aide de [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="a77f8-145">If the application needs to efficiently scan a known subset of an index, a similar optimization is also performed whenever an index range is established by using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span> <span data-ttu-id="a77f8-146">Cette optimisation est disponible uniquement sur Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a77f8-146">This optimization is only available on Windows XP and later releases.</span></span>

<span data-ttu-id="a77f8-147">Si l’application doit analyser efficacement un sous-ensemble inconnu d’un index, aucune action ne doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="a77f8-147">If the application needs to efficiently scan an unknown subset of an index, no action should be taken.</span></span> <span data-ttu-id="a77f8-148">Le moteur peut détecter automatiquement le comportement de l’analyse et récupérer les données à l’avance.</span><span class="sxs-lookup"><span data-stu-id="a77f8-148">The engine can automatically detect scanning behavior and will fetch data ahead of time.</span></span> <span data-ttu-id="a77f8-149">Toutefois, ce comportement n’est pas aussi agressif.</span><span class="sxs-lookup"><span data-stu-id="a77f8-149">This behavior is not as aggressive, however.</span></span>

<span data-ttu-id="a77f8-150">Cette optimisation rendra l’analyse efficace de l’index principal et fera en sorte que l’analyse des données d’entrée d’index dans un index secondaire soit efficace.</span><span class="sxs-lookup"><span data-stu-id="a77f8-150">This optimization will make scanning the primary index efficient and will make scanning just the index entry data in a secondary index efficient.</span></span> <span data-ttu-id="a77f8-151">Il n’effectue pas l’analyse d’un index secondaire pendant la récupération des données d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a77f8-151">It will not make scanning a secondary index while retrieving record data efficient.</span></span> <span data-ttu-id="a77f8-152">Cela est dû au fait que le moteur n’effectue pas de lecture anticipée sur les données de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a77f8-152">This is because the engine does not perform a read-ahead on the record data.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a77f8-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a77f8-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a77f8-154"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a77f8-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a77f8-155">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a77f8-155">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a77f8-156"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a77f8-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a77f8-157">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a77f8-157">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a77f8-158"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a77f8-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a77f8-159">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a77f8-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a77f8-160"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="a77f8-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a77f8-161">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a77f8-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a77f8-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a77f8-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a77f8-163">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a77f8-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a77f8-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a77f8-164">See Also</span></span>

[<span data-ttu-id="a77f8-165">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a77f8-165">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a77f8-166">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a77f8-166">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a77f8-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a77f8-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a77f8-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a77f8-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a77f8-169">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="a77f8-169">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="a77f8-170">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a77f8-170">JetStopService</span></span>](./jetstopservice-function.md)
