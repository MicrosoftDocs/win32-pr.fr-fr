---
description: 'En savoir plus sur : fonction JetReadFileInstance'
title: Fonction JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524958"
---
# <a name="jetreadfileinstance-function"></a><span data-ttu-id="4e4f4-103">Fonction JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="4e4f4-103">JetReadFileInstance Function</span></span>


<span data-ttu-id="4e4f4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="4e4f4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfileinstance-function"></a><span data-ttu-id="4e4f4-105">Fonction JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="4e4f4-105">JetReadFileInstance Function</span></span>

<span data-ttu-id="4e4f4-106">La fonction **JetReadFileInstance** récupère le contenu d’un fichier ouvert avec la fonction [JetOpenFileInstance](./jetopenfileinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4e4f4-106">The **JetReadFileInstance** function retrieves the contents of a file opened with the [JetOpenFileInstance](./jetopenfileinstance-function.md) function.</span></span>

<span data-ttu-id="4e4f4-107">**Windows XP**:   **JetReadFileInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-107">**Windows XP**:   **JetReadFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a><span data-ttu-id="4e4f4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e4f4-108">Parameters</span></span>

<span data-ttu-id="4e4f4-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="4e4f4-109">*instance*</span></span>

<span data-ttu-id="4e4f4-110">Instance à utiliser pour un appel d’API particulier.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-110">The instance to use for a particular API call.</span></span>

<span data-ttu-id="4e4f4-111">Notez que pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-111">Note that for Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="4e4f4-112">L’utilisation de cette instance globale est implicitement dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="4e4f4-113">Pour Windows XP et les versions ultérieures, vous pouvez appeler la variante API qui n’accepte pas ce paramètre uniquement quand le moteur est en mode hérité (mode de compatibilité Windows 2000) dans les cas où une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-113">For Windows XP and later releases, you can call the API variant that does not accept this parameter only when the engine is in legacy mode (Windows 2000 compatibility mode) in cases where only one instance is supported.</span></span> <span data-ttu-id="4e4f4-114">Dans le cas contraire, l’opération échoue et retourne l’erreur JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-114">Otherwise, the operation will fail and return the JET_errRunningInMultiInstanceMode error.</span></span>

<span data-ttu-id="4e4f4-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="4e4f4-115">*hfFile*</span></span>

<span data-ttu-id="4e4f4-116">Handle du fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-116">The handle of the file to be read.</span></span>

<span data-ttu-id="4e4f4-117">*va*</span><span class="sxs-lookup"><span data-stu-id="4e4f4-117">*pv*</span></span>

<span data-ttu-id="4e4f4-118">Mémoire tampon de sortie qui recevra les données du fichier.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-118">The output buffer that will receive the file data.</span></span>

<span data-ttu-id="4e4f4-119">*libéré*</span><span class="sxs-lookup"><span data-stu-id="4e4f4-119">*cb*</span></span>

<span data-ttu-id="4e4f4-120">Taille maximale, en octets, de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-120">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="4e4f4-121">*PCB*</span><span class="sxs-lookup"><span data-stu-id="4e4f4-121">*pcb*</span></span>

<span data-ttu-id="4e4f4-122">Quantité réelle de données de fichier récupérées.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-122">The actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="4e4f4-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4e4f4-123">Return Value</span></span>

<span data-ttu-id="4e4f4-124">Cette fonction facilite le retour de tout [JET_ERR](./jet-err.md) types de données définis dans l’API ESE (Extensible Storage Engine).</span><span class="sxs-lookup"><span data-stu-id="4e4f4-124">This function facilitates the return of any [JET_ERR](./jet-err.md) data types that are defined in the Extensible Storage Engine (ESE) API.</span></span> <span data-ttu-id="4e4f4-125">Pour plus d’informations sur les erreurs JET, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4e4f4-125">For more information about JET errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e4f4-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4e4f4-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="4e4f4-127">Signification</span><span class="sxs-lookup"><span data-stu-id="4e4f4-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4e4f4-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-129">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e4f4-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="4e4f4-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-131">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="4e4f4-131">The operation failed because the current external backup has been aborted by a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span> <span data-ttu-id="4e4f4-132">Cette erreur est retournée uniquement par Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-132">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4e4f4-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-134">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="4e4f4-134">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e4f4-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4e4f4-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-136">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable nécessitant que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-136">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error requiring that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="4e4f4-137">Cette erreur est retournée uniquement par Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-137">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-138">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4e4f4-138">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-139">L’un des paramètres spécifiés contient une valeur inattendue ou une valeur qui n’a pas de sens lorsqu’elle est associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-139">One of the specified parameters contained either an unexpected value or a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4e4f4-140">Cela peut se produire pour la fonction <strong>JetReadFileInstance</strong> lorsque l’un des éléments suivants se produit :</span><span class="sxs-lookup"><span data-stu-id="4e4f4-140">This can happen for the <strong>JetReadFileInstance</strong> function when any of the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="4e4f4-141">Le handle d’instance spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-141">The specified instance handle is invalid.</span></span> <span data-ttu-id="4e4f4-142">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-142">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="4e4f4-143">La taille de la mémoire tampon de sortie n’est pas un multiple de la taille de page de la base de données (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="4e4f4-143">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="4e4f4-144">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-144">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="4e4f4-145">La taille de la mémoire tampon de sortie est inférieure à trois pages de base de données (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), et il s’agit du premier appel à la fonction <strong>JetReadFileInstance</strong> pour le handle spécifié.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-145">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), and this is the first call to the <strong>JetReadFileInstance</strong> function for the specified handle.</span></span> <span data-ttu-id="4e4f4-146">Windows XP et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-146">Windows XP and later Windows versions.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e4f4-147">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="4e4f4-147">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-148">L’opération a échoué car une altération des données irrécupérable a été détectée lors de la lecture d’un fichier journal de transactions.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-148">The operation failed because unrecoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="4e4f4-149">Cette erreur est retournée uniquement par Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-149">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="4e4f4-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-151">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e4f4-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4e4f4-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-153">Impossible de terminer l’opération, car l’instance associée à cette session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-153">It is not possible to complete the operation because the instance associated with this session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-154">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="4e4f4-154">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-155">L’opération a échoué car une altération des données irrécupérable a été détectée lors de la lecture d’une page de base de données à partir d’un fichier de base de données ou d’un fichier correctif</span><span class="sxs-lookup"><span data-stu-id="4e4f4-155">The operation failed because unrecoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e4f4-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4e4f4-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-157">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à cette session.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-158">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="4e4f4-158">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-159">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000) dans le cas où une seule instance est prise en charge, alors que plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-159">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) in a case where only one instance is supported but multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e4f4-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4e4f4-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-161">Il n’est pas possible de terminer l’opération, car l’instance associée à cette session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-161">It is not possible to complete the operation because the instance associated with this session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4e4f4-162">En cas de réussite, le segment de données suivant du fichier est lu dans la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-162">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="4e4f4-163">Le nombre réel d’octets récupérés est également retourné.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-163">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="4e4f4-164">Le décalage de fichier à partir duquel la lecture suivante aura lieu sera avancé par ce montant.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-164">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="4e4f4-165">En cas d’échec, l’état de la mémoire tampon de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-165">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="4e4f4-166">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde pour l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-166">The failure will result in the cancellation of the entire backup process for the current instance.</span></span> <span data-ttu-id="4e4f4-167">Dans Windows XP et les versions ultérieures de Windows, la sauvegarde n’est pas annulée si une erreur s’est produite lors de la lecture d’un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-167">In Windows XP and later Windows versions, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="4e4f4-168">Toutefois, la sauvegarde de ce fichier de base de données restera annulée et le descripteur correspondant sera automatiquement fermé.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-168">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4e4f4-169">Notes</span><span class="sxs-lookup"><span data-stu-id="4e4f4-169">Remarks</span></span>

<span data-ttu-id="4e4f4-170">Tout appel à la fonction **JetReadFileInstance** effectué à l’aide d’un handle qui a déjà retourné toutes les données du fichier sous-jacent (par exemple, si un appel précédent a retourné moins d’octets que la taille de la mémoire tampon de sortie) est toujours concluant, mais retourne zéro octet de données.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-170">Any call to the **JetReadFileInstance** function made by using a handle that has already returned all the data in the underlying file (such as if a previous call returned fewer bytes than the size of the output buffer) will always succeed but will return zero bytes of data.</span></span>

<span data-ttu-id="4e4f4-171">Vous devez utiliser une mémoire tampon de sortie importante pour optimiser les performances de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-171">You should use a large output buffer to maximize backup performance.</span></span> <span data-ttu-id="4e4f4-172">Vous devrez peut-être faire des essais pour trouver le compromis optimal entre la consommation des ressources et le débit pour une situation particulière.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-172">You might need to experiment to find the optimal tradeoff between resource consumption and throughput for a particular situation.</span></span> <span data-ttu-id="4e4f4-173">Dans tous les cas, la mémoire tampon de sortie ne doit pas être inférieure à 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-173">In any case, the output buffer should be no smaller than 64 KB.</span></span> <span data-ttu-id="4e4f4-174">Le pointeur que vous transmettez à **JetReadFileInstance** doit être aligné sur une limite de page mémoire (soit 4 Ko soit 8 Ko).</span><span class="sxs-lookup"><span data-stu-id="4e4f4-174">The pointer that you pass to **JetReadFileInstance** must be aligned with a memory page boundary (either 4 KB or 8 KB).</span></span> <span data-ttu-id="4e4f4-175">Pour ce faire, vous pouvez appeler la fonction **VirtualAlloc** .</span><span class="sxs-lookup"><span data-stu-id="4e4f4-175">You can do this by calling the **VirtualAlloc** function.</span></span>

<span data-ttu-id="4e4f4-176">Plusieurs appels simultanés à **JetReadFileInstance** effectués à l’aide du même descripteur de fichier ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-176">Multiple concurrent calls to **JetReadFileInstance** made by using the same file handle are not supported.</span></span> <span data-ttu-id="4e4f4-177">Cela signifie qu’il n’est pas possible de mettre en file d’attente plusieurs mémoires tampons pour la lecture simultanée dans le même fichier afin d’obtenir un débit séquentiel élevé.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-177">This means that it is not possible to queue several buffers for concurrent reading against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="4e4f4-178">Vous devez utiliser un seul tampon de grande taille à la place.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-178">You should use a single large buffer instead.</span></span>

<span data-ttu-id="4e4f4-179">Si vous avez configuré une instance particulière de telle sorte que la modification de pages de base de données soit activée (voir le paramètre [JET_paramCircularLog](./transaction-log-parameters.md) dans les [paramètres système](./extensible-storage-engine-system-parameters.md)), les données supprimées sont supprimées de la base de données en tant qu’effet secondaire d’un appel à **JetReadFileInstance** sur le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-179">If you have configured a particular instance such that database page scrubbing is enabled (see the [JET_paramCircularLog](./transaction-log-parameters.md) parameter in [System Parameters](./extensible-storage-engine-system-parameters.md)), deleted data will be removed from the database as a side-effect of a call to **JetReadFileInstance** against the database file.</span></span>

<span data-ttu-id="4e4f4-180">Il est très important de comprendre comment la sauvegarde et l’altération des données interagissent.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-180">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="4e4f4-181">Si le moteur de base de données détecte une altération des données au cours d’une sauvegarde, il échouera à la sauvegarde de la base de données concernée ou de la totalité de l’instance.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-181">If the database engine detects data corruption during a backup, it will fail the backup of either the affected database or the entire instance.</span></span> <span data-ttu-id="4e4f4-182">Il s’agit d’une décision de conception consciente destinée à vous protéger contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-182">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="4e4f4-183">Si le moteur de base de données a permis à une sauvegarde de se dérouler alors que des données sont endommagées, il est possible qu’une sauvegarde plus ancienne et non endommagée soit ignorée.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-183">If the database engine allowed a backup to succeed where data corruption was present, it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="4e4f4-184">Cela serait désastreux, car il serait possible de corriger les données endommagées sur l’instance en direct en restaurant cette sauvegarde et en relisant tous les fichiers du journal des transactions sur cette base de données.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-184">This would be unfortunate because then it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="4e4f4-185">Ce scénario de perte de données nulle suppose que l’enregistrement circulaire n’est pas activé (voir [JET_paramCircularLog](./transaction-log-parameters.md) dans les [paramètres système](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="4e4f4-185">This zero-data-loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="4e4f4-186">Il est également important de comprendre que les cas d’endommagement des données sont généralement détectés pour la première fois lors de la sauvegarde en continu.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-186">It is also important to understand that cases of data corruption are usually first detected during streaming backup.</span></span> <span data-ttu-id="4e4f4-187">Cela est dû au fait que la sauvegarde en continu est le seul processus qui analyse régulièrement chaque page d’un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-187">This is because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="4e4f4-188">Il est également probable que la sauvegarde en continu sera le premier processus de détection des signes précoces de défaillance matérielle comme indiqué par des erreurs de corruption de données intermittentes, en raison de la quantité de données récupérées par la sauvegarde et de la vitesse à laquelle ces données sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-188">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors, because of both the amount of data retrieved by backup and the speed at which that data is retrieved.</span></span>

<span data-ttu-id="4e4f4-189">La corruption des données est détectée par le moteur de base de données via l’utilisation de sommes de contrôle de bloc.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-189">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="4e4f4-190">Ces sommes de contrôle sont définies juste avant l’écriture d’une page de base de données et sont vérifiées lors de la lecture d’une page de base de données.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-190">These checksums are set just before a database page write and are verified on a database page read.</span></span> <span data-ttu-id="4e4f4-191">Ce schéma permet au moteur de base de données de déterminer que les données ont été endommagées à un moment donné, mais ne permet pas au moteur de base de données de déterminer la source de l’altération.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-191">This scheme enables the database engine to determine that data has been corrupted at some point, but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="4e4f4-192">Historiquement, les instances de ces données endommagées proviennent de sources autres que le moteur de base de données lui-même.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-192">Historically, instances of such data corruption have originated from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4e4f4-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e4f4-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-194">Client</span><span class="sxs-lookup"><span data-stu-id="4e4f4-194">Client</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-195">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e4f4-196">Serveur</span><span class="sxs-lookup"><span data-stu-id="4e4f4-196">Server</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-197">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-198">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e4f4-198">Header</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-199">Est déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-199">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e4f4-200">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e4f4-200">Library</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-201">Utilise ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-201">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e4f4-202">DLL</span><span class="sxs-lookup"><span data-stu-id="4e4f4-202">DLL</span></span></p></td>
<td><p><span data-ttu-id="4e4f4-203">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4e4f4-203">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4e4f4-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e4f4-204">See Also</span></span>

[<span data-ttu-id="4e4f4-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4e4f4-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4e4f4-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="4e4f4-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="4e4f4-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4e4f4-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="4e4f4-208">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="4e4f4-208">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="4e4f4-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="4e4f4-209">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="4e4f4-210">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="4e4f4-210">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
