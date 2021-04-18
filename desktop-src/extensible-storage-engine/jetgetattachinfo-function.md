---
description: 'En savoir plus sur : fonction JetGetAttachInfo'
title: Fonction JetGetAttachInfo
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa1e51931c11e0fce0b18c0c102c4d54c0b47976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519517"
---
# <a name="jetgetattachinfo-function"></a><span data-ttu-id="2be2c-103">Fonction JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="2be2c-103">JetGetAttachInfo Function</span></span>


<span data-ttu-id="2be2c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2be2c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfo-function"></a><span data-ttu-id="2be2c-105">Fonction JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="2be2c-105">JetGetAttachInfo Function</span></span>

<span data-ttu-id="2be2c-106">La fonction **JetGetAttachInfo** est utilisée lors d’une sauvegarde lancée par [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) pour interroger une instance pour obtenir les noms des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2be2c-106">The **JetGetAttachInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="2be2c-107">Seules les bases de données actuellement attachées à l’instance à l’aide de [JetAttachDatabase](./jetattachdatabase-function.md) seront prises en compte.</span><span class="sxs-lookup"><span data-stu-id="2be2c-107">Only databases currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="2be2c-108">Ces fichiers peuvent être ouverts par la suite à l’aide de [JetOpenFile](./jetopenfile-function.md) et lus à l’aide de [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="2be2c-108">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="2be2c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2be2c-109">Parameters</span></span>

<span data-ttu-id="2be2c-110">*szz*</span><span class="sxs-lookup"><span data-stu-id="2be2c-110">*szz*</span></span>

<span data-ttu-id="2be2c-111">Mémoire tampon de sortie qui reçoit la liste des chaînes terminées par le caractère null qui décrivent l’ensemble des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2be2c-111">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="2be2c-112">La liste de chaînes retournée dans cette mémoire tampon est dans le même format qu’une chaîne multiple utilisée par le registre.</span><span class="sxs-lookup"><span data-stu-id="2be2c-112">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="2be2c-113">Chaque chaîne se terminant par un caractère NULL est retournée dans la séquence suivie d’une marque de fin null finale.</span><span class="sxs-lookup"><span data-stu-id="2be2c-113">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="2be2c-114">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="2be2c-114">*cbMax*</span></span>

<span data-ttu-id="2be2c-115">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="2be2c-115">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="2be2c-116">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="2be2c-116">*pcbActual*</span></span>

<span data-ttu-id="2be2c-117">Pointeur vers la mémoire tampon de sortie qui a reçu la quantité réelle de données de chaîne.</span><span class="sxs-lookup"><span data-stu-id="2be2c-117">Pointer to the output buffer that received the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="2be2c-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2be2c-118">Return Value</span></span>

<span data-ttu-id="2be2c-119">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="2be2c-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2be2c-120">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2be2c-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2be2c-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2be2c-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="2be2c-122">Description</span><span class="sxs-lookup"><span data-stu-id="2be2c-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2be2c-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2be2c-124">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2be2c-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be2c-125">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="2be2c-125">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="2be2c-126">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="2be2c-126">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="2be2c-127">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2be2c-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2be2c-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2be2c-129">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2be2c-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be2c-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2be2c-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2be2c-131">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="2be2c-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="2be2c-132">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2be2c-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-133">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="2be2c-133">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="2be2c-134">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="2be2c-134">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="2be2c-135"><strong>JetGetAttachInfo</strong> renvoie cette erreur si la sauvegarde actuelle n’est pas une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="2be2c-135"><strong>JetGetAttachInfo</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be2c-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2be2c-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2be2c-137">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="2be2c-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="2be2c-138">Cela peut se produire pour <strong>JetGetAttachInfo</strong> lorsque le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="2be2c-138">This can happen for <strong>JetGetAttachInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-139">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="2be2c-139">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="2be2c-140">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="2be2c-140">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be2c-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2be2c-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2be2c-142">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="2be2c-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2be2c-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2be2c-144">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="2be2c-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be2c-145">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="2be2c-145">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="2be2c-146">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="2be2c-146">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-147">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2be2c-147">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2be2c-148">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2be2c-148">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2be2c-149">En cas de réussite, les informations demandées sur l’ensemble des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde seront placées dans les tampons de sortie, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2be2c-149">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="2be2c-150">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="2be2c-150">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="2be2c-151">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.</span><span class="sxs-lookup"><span data-stu-id="2be2c-151">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2be2c-152">Notes</span><span class="sxs-lookup"><span data-stu-id="2be2c-152">Remarks</span></span>

<span data-ttu-id="2be2c-153">Il est important de noter que cette API ne retourne pas d’erreur ou d’avertissement si la mémoire tampon de sortie est trop petite pour accepter la liste complète des fichiers qui doivent faire partie du jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2be2c-153">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="2be2c-154">L’application doit toujours fournir une mémoire tampon pour recevoir la taille réelle de cette liste et utiliser ces informations pour déterminer si la liste a été tronquée.</span><span class="sxs-lookup"><span data-stu-id="2be2c-154">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2be2c-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2be2c-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-156"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2be2c-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2be2c-157">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2be2c-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be2c-158"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2be2c-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2be2c-159">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2be2c-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-160"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2be2c-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2be2c-161">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2be2c-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be2c-162"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="2be2c-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2be2c-163">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2be2c-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2be2c-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2be2c-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2be2c-165">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2be2c-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2be2c-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2be2c-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2be2c-167">Implémenté en tant que <strong>JetGetAttachInfoW</strong> (Unicode) et <strong>JetGetAttachInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2be2c-167">Implemented as <strong>JetGetAttachInfoW</strong> (Unicode) and <strong>JetGetAttachInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2be2c-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2be2c-168">See Also</span></span>

[<span data-ttu-id="2be2c-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2be2c-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2be2c-170">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2be2c-170">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2be2c-171">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="2be2c-171">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="2be2c-172">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="2be2c-172">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="2be2c-173">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="2be2c-173">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="2be2c-174">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="2be2c-174">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="2be2c-175">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="2be2c-175">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="2be2c-176">JetStopService</span><span class="sxs-lookup"><span data-stu-id="2be2c-176">JetStopService</span></span>](./jetstopservice-function.md)
