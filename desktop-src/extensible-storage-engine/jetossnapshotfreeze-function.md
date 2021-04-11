---
description: 'En savoir plus sur : fonction JetOSSnapshotFreeze'
title: Fonction JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204073"
---
# <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="f32ba-103">Fonction JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="f32ba-103">JetOSSnapshotFreeze Function</span></span>


<span data-ttu-id="f32ba-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f32ba-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="f32ba-105">Fonction JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="f32ba-105">JetOSSnapshotFreeze Function</span></span>

<span data-ttu-id="f32ba-106">La fonction **JetOSSnapshotFreeze** démarre un instantané.</span><span class="sxs-lookup"><span data-stu-id="f32ba-106">The **JetOSSnapshotFreeze** function starts a snapshot.</span></span> <span data-ttu-id="f32ba-107">Pendant que l’instantané est en cours, aucune activité d’écriture sur le disque par le moteur ne peut avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="f32ba-107">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="f32ba-108">**Windows XP :**  **JetOSSnapshotFreeze** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f32ba-108">**Windows XP:**  **JetOSSnapshotFreeze** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f32ba-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f32ba-109">Parameters</span></span>

<span data-ttu-id="f32ba-110">*snapId*</span><span class="sxs-lookup"><span data-stu-id="f32ba-110">*snapId*</span></span>

<span data-ttu-id="f32ba-111">Identificateur de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="f32ba-111">The identifier of the snapshot session.</span></span>

<span data-ttu-id="f32ba-112">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="f32ba-112">*pcInstanceInfo*</span></span>

<span data-ttu-id="f32ba-113">Nombre d’instances en cours d’exécution dans le moteur qui font partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="f32ba-113">The number of instances currently running in the engine that are part of the snapshot session.</span></span>

<span data-ttu-id="f32ba-114">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="f32ba-114">*paInstanceInfo*</span></span>

<span data-ttu-id="f32ba-115">Tableau de structures, une pour chaque instance en cours d’exécution qui fait partie de la session d’instantané, décrivant l’instance et les bases de données qui en font partie.</span><span class="sxs-lookup"><span data-stu-id="f32ba-115">An array of structures, one for each running instance that is part of the snapshot session, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="f32ba-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f32ba-116">*grbit*</span></span>

<span data-ttu-id="f32ba-117">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="f32ba-117">The options for this call.</span></span> <span data-ttu-id="f32ba-118">Ce paramètre est réservé pour une utilisation ultérieure et la seule valeur valide prise en charge est 0.</span><span class="sxs-lookup"><span data-stu-id="f32ba-118">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="f32ba-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f32ba-119">Return Value</span></span>

<span data-ttu-id="f32ba-120">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="f32ba-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f32ba-121">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f32ba-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f32ba-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f32ba-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="f32ba-123">Description</span><span class="sxs-lookup"><span data-stu-id="f32ba-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f32ba-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f32ba-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f32ba-125">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f32ba-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f32ba-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f32ba-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f32ba-127">Les pointeurs fournis pour les paramètres de sortie ont la valeur NULL, la session d’instantané n’est pas valide ou le paramètre <em>Grbit</em> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f32ba-127">The pointers provided for the output parameters are NULL, the snapshot session is invalid, or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f32ba-128">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="f32ba-128">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="f32ba-129">La session d’instantané n’est pas dans l’état approprié pour démarrer un blocage (par exemple, un blocage précédent a échoué sur cette session auparavant).</span><span class="sxs-lookup"><span data-stu-id="f32ba-129">The snapshot session is not in the appropriate state to start a freeze (for example, a previous freeze failed on this session before).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f32ba-130">JET_errOSSnapshotNotAllowed</span><span class="sxs-lookup"><span data-stu-id="f32ba-130">JET_errOSSnapshotNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="f32ba-131">Le moteur n’est pas dans un État dans lequel un instantané peut être exécuté.</span><span class="sxs-lookup"><span data-stu-id="f32ba-131">The engine is not in a state in which a snapshot can be performed.</span></span> <span data-ttu-id="f32ba-132">Une ou plusieurs sauvegardes de streaming sont déjà en cours, ou une ou plusieurs instances passent par des étapes de récupération ou se terminent.</span><span class="sxs-lookup"><span data-stu-id="f32ba-132">Either one or more streaming backups is already in progress, or one or more instances are going through recovery steps or terminating.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f32ba-133">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="f32ba-133">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="f32ba-134">L’identificateur de la session d’instantané n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f32ba-134">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f32ba-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f32ba-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f32ba-136">La fonction a échoué en raison d’une condition de mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="f32ba-136">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f32ba-137">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="f32ba-137">JET_errOutOfThreads</span></span></p></td>
<td><p><span data-ttu-id="f32ba-138">La fonction a échoué en raison de l’échec du démarrage d’un nouveau thread qui n’a pas pu démarrer.</span><span class="sxs-lookup"><span data-stu-id="f32ba-138">The function failed because a new thread doing the freeze failed to start.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f32ba-139">Si cette fonction est établie, aucune e/s d’écriture n’est émise pour les fichiers de base de données ou pour les fichiers journaux qui font partie des instances figées.</span><span class="sxs-lookup"><span data-stu-id="f32ba-139">If this function succeeds, there will not be any write IOs issued for the database files or for the log files that are part of instances that are frozen.</span></span> <span data-ttu-id="f32ba-140">En outre, les informations de l’instance sont correctement remplies et doivent être libérées ultérieurement en appelant [JetFreeBuffer](./jetfreebuffer-function.md) avec le pointeur vers le tableau d’informations d’instance qui a été retourné.</span><span class="sxs-lookup"><span data-stu-id="f32ba-140">Also, the instance information will be properly filled and it must be freed later on by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="f32ba-141">Si cette fonction échoue, le moteur continue de s’exécuter normalement avec les IOs se produisant comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="f32ba-141">If this function fails, the engine will keep running normally with the IOs occurring as usual.</span></span> <span data-ttu-id="f32ba-142">Il n’est pas nécessaire d’appeler [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) si le gel échoue.</span><span class="sxs-lookup"><span data-stu-id="f32ba-142">There is no need to call [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) if the freeze fails.</span></span> <span data-ttu-id="f32ba-143">En outre, les informations de l’instance ne sont pas remplies, il n’est donc pas nécessaire de libérer cette ressource.</span><span class="sxs-lookup"><span data-stu-id="f32ba-143">Also, the instance information will not be filled so there is no need to free this resource.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f32ba-144">Notes</span><span class="sxs-lookup"><span data-stu-id="f32ba-144">Remarks</span></span>

<span data-ttu-id="f32ba-145">Pendant la période de blocage, aucune e/s d’écriture n’est émise pour les bases de données attachées ou les journaux de transactions, même s’il peut y avoir des e/s d’écriture émises dans les bases de données temporaires ou les fichiers de streaming.</span><span class="sxs-lookup"><span data-stu-id="f32ba-145">During the freeze period, there will not be any write IOs issued to the attached databases or the transaction logs, although there might be write IOs issued to the temporary databases or streaming files.</span></span>

<span data-ttu-id="f32ba-146">L’État dans lequel se trouvent les bases de données et les fichiers journaux pendant le gel (l’État dans lequel les fichiers se trouvent dans une image d’instantané de volume) est tel qu’une récupération normale sera possible si ces fichiers sont restaurés ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f32ba-146">The state in which the databases and the log files will be during the freeze (the state in which the files would be in a Volume Snapshot image) will be such that a normal recovery will be possible if those files are restored later.</span></span>

<span data-ttu-id="f32ba-147">Étant donné qu’il n’y a pas d’opérations d’écriture pendant la période de blocage, les appels d’API normaux dans le moteur peuvent être bloqués pour cet intervalle.</span><span class="sxs-lookup"><span data-stu-id="f32ba-147">Because there are no write operations during the freeze period, normal API calls into the engine might be stalled for that interval.</span></span> <span data-ttu-id="f32ba-148">L’application cliente doit être en mesure de gérer les appels d’API qui peuvent prendre plus de temps que d’habitude si un blocage se produit.</span><span class="sxs-lookup"><span data-stu-id="f32ba-148">The client application must be able to handle API calls that might take longer then normal if a freeze occurs.</span></span>

<span data-ttu-id="f32ba-149">En raison des effets possibles décrits ci-dessus, il existe un délai d’expiration interne après lequel la session d’instantané arrêtera la phase de blocage, même si les API qui effectuent le dégel ou l’abandon n’étaient pas appelées.</span><span class="sxs-lookup"><span data-stu-id="f32ba-149">Due to the possible effects described above, there is an internal timeout after which the snapshot session will stop the freeze phase even if the APIs doing the thaw or abort were not called.</span></span> <span data-ttu-id="f32ba-150">La valeur du délai d’attente peut être modifiée à l’aide du paramètre système [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="f32ba-150">The value of the timeout can be changed using the [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) system parameter.</span></span> <span data-ttu-id="f32ba-151">Notez que l’intervalle de blocage classique est compris entre 10 secondes et le délai d’expiration par défaut est d’environ 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="f32ba-151">Note that the typical freeze interval is in the range of 10 seconds with the default timeout somewhere around 60 seconds.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f32ba-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f32ba-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f32ba-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f32ba-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f32ba-154">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f32ba-154">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f32ba-155"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f32ba-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f32ba-156">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f32ba-156">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f32ba-157"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f32ba-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f32ba-158">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f32ba-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f32ba-159"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f32ba-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f32ba-160">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f32ba-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f32ba-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f32ba-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f32ba-162">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f32ba-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f32ba-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f32ba-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f32ba-164">Implémenté en tant que <strong>JetOSSnapshotFreezeW</strong> (Unicode) et <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f32ba-164">Implemented as <strong>JetOSSnapshotFreezeW</strong> (Unicode) and <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f32ba-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f32ba-165">See Also</span></span>

[<span data-ttu-id="f32ba-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f32ba-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f32ba-167">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="f32ba-167">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="f32ba-168">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="f32ba-168">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="f32ba-169">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="f32ba-169">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="f32ba-170">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="f32ba-170">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="f32ba-171">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="f32ba-171">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="f32ba-172">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="f32ba-172">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
