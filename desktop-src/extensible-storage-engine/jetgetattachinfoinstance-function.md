---
description: 'En savoir plus sur : fonction JetGetAttachInfoInstance'
title: JetGetAttachInfoInstance fonction)
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28abf76632f147b6e909c1b8fb036062d5d3af74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865626"
---
# <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="8e98c-103">JetGetAttachInfoInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="8e98c-103">JetGetAttachInfoInstance Function</span></span>


<span data-ttu-id="8e98c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="8e98c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="8e98c-105">JetGetAttachInfoInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="8e98c-105">JetGetAttachInfoInstance Function</span></span>

<span data-ttu-id="8e98c-106">La fonction **JetGetAttachInfoInstance** est utilisée lors d’une sauvegarde lancée par [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) pour interroger une instance pour obtenir les noms des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="8e98c-106">The **JetGetAttachInfoInstance** function is used during a backup initiated by [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="8e98c-107">Seules les bases de données qui sont actuellement attachées à l’instance à l’aide de [JetAttachDatabase](./jetattachdatabase-function.md) sont prises en compte.</span><span class="sxs-lookup"><span data-stu-id="8e98c-107">Only databases that are currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="8e98c-108">Ces fichiers peuvent être ouverts par la suite à l’aide de [JetOpenFileInstance](./jetopenfileinstance-function.md) et lus à l’aide de [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="8e98c-108">These files may subsequently be opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) and read using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="8e98c-109">**Windows XP : JetGetAttachInfoInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8e98c-109">**Windows XP:  JetGetAttachInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="8e98c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e98c-110">Parameters</span></span>

<span data-ttu-id="8e98c-111">*instancié*</span><span class="sxs-lookup"><span data-stu-id="8e98c-111">*instance*</span></span>

<span data-ttu-id="8e98c-112">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="8e98c-112">The instance to use for this call.</span></span>

<span data-ttu-id="8e98c-113">Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8e98c-113">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="8e98c-114">L’utilisation de cette instance globale est implicitement dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="8e98c-114">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="8e98c-115">Pour Windows XP et les versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8e98c-115">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="8e98c-116">Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="8e98c-116">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="8e98c-117">*szz*</span><span class="sxs-lookup"><span data-stu-id="8e98c-117">*szz*</span></span>

<span data-ttu-id="8e98c-118">Mémoire tampon de sortie qui reçoit la liste des chaînes terminées par le caractère null qui décrivent l’ensemble des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="8e98c-118">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="8e98c-119">La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre.</span><span class="sxs-lookup"><span data-stu-id="8e98c-119">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="8e98c-120">Chaque chaîne se terminant par un caractère NULL est retournée dans la séquence suivie d’une marque de fin null finale.</span><span class="sxs-lookup"><span data-stu-id="8e98c-120">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="8e98c-121">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="8e98c-121">*cbMax*</span></span>

<span data-ttu-id="8e98c-122">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8e98c-122">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="8e98c-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="8e98c-123">*pcbActual*</span></span>

<span data-ttu-id="8e98c-124">Pointeur vers la mémoire tampon de sortie qui reçoit la quantité réelle de données de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8e98c-124">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="8e98c-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8e98c-125">Return Value</span></span>

<span data-ttu-id="8e98c-126">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="8e98c-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8e98c-127">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8e98c-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e98c-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8e98c-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="8e98c-129">Description</span><span class="sxs-lookup"><span data-stu-id="8e98c-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8e98c-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8e98c-131">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8e98c-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e98c-132">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="8e98c-132">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="8e98c-133">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="8e98c-133">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="8e98c-134">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8e98c-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-135">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8e98c-135">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8e98c-136">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="8e98c-136">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e98c-137">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8e98c-137">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8e98c-138">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="8e98c-138">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8e98c-139">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8e98c-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-140">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="8e98c-140">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="8e98c-141">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="8e98c-141">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="8e98c-142"><strong>JetGetAttachInfoInstance</strong> renvoie cette erreur si la sauvegarde actuelle n’est pas une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="8e98c-142"><strong>JetGetAttachInfoInstance</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e98c-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8e98c-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8e98c-144">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="8e98c-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="8e98c-145">Cela peut se produire pour <strong>JetGetAttachInfoInstance</strong> lorsque le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="8e98c-145">This can happen for <strong>JetGetAttachInfoInstance</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-146">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="8e98c-146">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="8e98c-147">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="8e98c-147">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e98c-148">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8e98c-148">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8e98c-149">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="8e98c-149">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-150">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8e98c-150">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8e98c-151">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="8e98c-151">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e98c-152">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="8e98c-152">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="8e98c-153">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="8e98c-153">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8e98c-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8e98c-155">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8e98c-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8e98c-156">En cas de réussite, les informations demandées sur l’ensemble des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde seront placées dans les tampons de sortie, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="8e98c-156">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="8e98c-157">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8e98c-157">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="8e98c-158">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.</span><span class="sxs-lookup"><span data-stu-id="8e98c-158">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8e98c-159">Notes</span><span class="sxs-lookup"><span data-stu-id="8e98c-159">Remarks</span></span>

<span data-ttu-id="8e98c-160">Il est important de noter que cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="8e98c-160">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="8e98c-161">L’application doit toujours fournir une mémoire tampon pour recevoir la taille réelle de cette liste et utiliser ces informations pour déterminer si la liste a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="8e98c-161">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8e98c-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e98c-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-163"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="8e98c-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8e98c-164">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8e98c-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e98c-165"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="8e98c-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8e98c-166">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8e98c-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-167"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="8e98c-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8e98c-168">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="8e98c-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e98c-169"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="8e98c-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8e98c-170">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8e98c-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e98c-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8e98c-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8e98c-172">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8e98c-172">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e98c-173"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8e98c-173"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8e98c-174">Implémenté en tant que <strong>JetGetAttachInfoInstanceW</strong> (Unicode) et <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8e98c-174">Implemented as <strong>JetGetAttachInfoInstanceW</strong> (Unicode) and <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8e98c-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e98c-175">See Also</span></span>

[<span data-ttu-id="8e98c-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8e98c-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8e98c-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="8e98c-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="8e98c-178">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="8e98c-178">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="8e98c-179">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="8e98c-179">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="8e98c-180">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="8e98c-180">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="8e98c-181">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="8e98c-181">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="8e98c-182">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="8e98c-182">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="8e98c-183">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="8e98c-183">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
