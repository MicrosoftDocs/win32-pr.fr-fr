---
description: 'En savoir plus sur : fonction JetOpenFileInstance'
title: Fonction JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523067"
---
# <a name="jetopenfileinstance-function"></a><span data-ttu-id="bd45a-103">Fonction JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-103">JetOpenFileInstance Function</span></span>


<span data-ttu-id="bd45a-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="bd45a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfileinstance-function"></a><span data-ttu-id="bd45a-105">Fonction JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-105">JetOpenFileInstance Function</span></span>

<span data-ttu-id="bd45a-106">La fonction **JetOpenFileInstance** ouvre une base de données attachée, un fichier de correctif de base de données ou un fichier journal de transactions d’une instance active afin d’effectuer une sauvegarde floue en continu.</span><span class="sxs-lookup"><span data-stu-id="bd45a-106">The **JetOpenFileInstance** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="bd45a-107">Les données de ces fichiers peuvent ensuite être lues par le handle retourné à l’aide de [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd45a-107">The data from these files can subsequently be read through the returned handle using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span> <span data-ttu-id="bd45a-108">Le handle retourné doit être fermé à l’aide de [JetCloseFileInstance](./jetclosefileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd45a-108">The returned handle must be closed using [JetCloseFileInstance](./jetclosefileinstance-function.md).</span></span> <span data-ttu-id="bd45a-109">Une sauvegarde externe de l’instance doit avoir été précédemment lancée à l’aide de [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd45a-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span></span>

<span data-ttu-id="bd45a-110">**Windows XP :**  **JetOpenFileInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bd45a-110">**Windows XP:**  **JetOpenFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="bd45a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd45a-111">Parameters</span></span>

<span data-ttu-id="bd45a-112">*instancié*</span><span class="sxs-lookup"><span data-stu-id="bd45a-112">*instance*</span></span>

<span data-ttu-id="bd45a-113">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="bd45a-113">The instance to use for this call.</span></span>

<span data-ttu-id="bd45a-114">Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bd45a-114">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="bd45a-115">L’utilisation de cette instance globale est implicitement dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="bd45a-115">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="bd45a-116">Pour Windows XP et les versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="bd45a-116">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="bd45a-117">Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="bd45a-117">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="bd45a-118">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="bd45a-118">*szFileName*</span></span>

<span data-ttu-id="bd45a-119">Chemin relatif ou absolu d’une base de données attachée, d’un fichier de correctif de base de données ou d’un fichier journal de transactions géré par l’instance en lecture pour la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="bd45a-119">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that is read for backup.</span></span>

<span data-ttu-id="bd45a-120">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="bd45a-120">*phfFile*</span></span>

<span data-ttu-id="bd45a-121">Pointeur vers la mémoire tampon de sortie qui reçoit un handle vers le fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="bd45a-121">Pointer to the output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="bd45a-122">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="bd45a-122">*pulFileSizeLow*</span></span>

<span data-ttu-id="bd45a-123">Pointeur vers la mémoire tampon de sortie qui reçoit les 32 bits les moins significatifs de la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="bd45a-123">Pointer to the output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="bd45a-124">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="bd45a-124">*pulFileSizeHigh*</span></span>

<span data-ttu-id="bd45a-125">Pointeur vers la mémoire tampon de sortie qui reçoit les 32 bits les plus significatifs de la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="bd45a-125">Pointer to the output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="bd45a-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bd45a-126">Return Value</span></span>

<span data-ttu-id="bd45a-127">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="bd45a-127">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bd45a-128">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bd45a-128">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd45a-129">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bd45a-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="bd45a-130">Description</span><span class="sxs-lookup"><span data-stu-id="bd45a-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bd45a-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bd45a-132">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="bd45a-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-133">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="bd45a-133">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="bd45a-134">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="bd45a-134">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="bd45a-135">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bd45a-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bd45a-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bd45a-137">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="bd45a-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-138">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="bd45a-138">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="bd45a-139">L’opération a échoué car elle n’a pas pu ouvrir le fichier demandé en raison d’une violation de partage ou de privilèges insuffisants.</span><span class="sxs-lookup"><span data-stu-id="bd45a-139">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-140">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="bd45a-140">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="bd45a-141">L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="bd45a-141">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="bd45a-142">Cette erreur est renvoyée uniquement par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="bd45a-142">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-143">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="bd45a-143">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="bd45a-144">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="bd45a-144">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-145">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="bd45a-145">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="bd45a-146">L’opération a échoué, car le chemin d’accès spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="bd45a-146">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bd45a-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bd45a-148">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="bd45a-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="bd45a-149">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bd45a-149">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="bd45a-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="bd45a-151">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="bd45a-151">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="bd45a-152">Cela peut se produire pour <strong>JetOpenFileInstance</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="bd45a-152">This can happen for <strong>JetOpenFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="bd45a-153">Le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="bd45a-153">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="bd45a-154">Le paramètre de nom de fichier spécifié est NULL ou une chaîne de longueur nulle (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="bd45a-154">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-155">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="bd45a-155">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="bd45a-156">Le fichier demandé n’a pas pu être ouvert pour la sauvegarde, car il est introuvable.</span><span class="sxs-lookup"><span data-stu-id="bd45a-156">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="bd45a-157">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bd45a-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-158">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="bd45a-158">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="bd45a-159">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="bd45a-159">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bd45a-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bd45a-161">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="bd45a-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-162">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="bd45a-162">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="bd45a-163">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="bd45a-163">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="bd45a-164"><strong>JetOpenFileInstance</strong> retourne JET_errOutOfMemory si une tentative est faite pour ouvrir un autre fichier avant que le fichier précédent ouvert à l’aide de <strong>JetOpenFileInstance</strong> ait été fermé par <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="bd45a-164"><strong>JetOpenFileInstance</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFileInstance</strong> has been closed by <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span></span> <span data-ttu-id="bd45a-165">Un seul descripteur de fichier en attente est actuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bd45a-165">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bd45a-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bd45a-167">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="bd45a-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-168">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="bd45a-168">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="bd45a-169">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="bd45a-169">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bd45a-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bd45a-171">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="bd45a-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd45a-172">En cas de réussite, un handle vers le fichier demandé est retourné.</span><span class="sxs-lookup"><span data-stu-id="bd45a-172">On success, a handle to the requested file is returned.</span></span> <span data-ttu-id="bd45a-173">Si le descripteur concerne un fichier de base de données, ce fichier de base de données sera préparé pour une sauvegarde en continu, ce qui peut entraîner la création d’un fichier correctif de base de données au même emplacement que le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="bd45a-173">If the handle is for a database file, that database file will be prepared for a streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="bd45a-174">Le fichier de correctif de base de données a exactement le même chemin d’accès et le même nom de fichier que le fichier de base de données, mais avec un. Extension PAT.</span><span class="sxs-lookup"><span data-stu-id="bd45a-174">The database patch file has the exact same path and filename as the database file but with a .PAT extension.</span></span> <span data-ttu-id="bd45a-175">La taille du fichier est également retournée.</span><span class="sxs-lookup"><span data-stu-id="bd45a-175">The size of the file will also be returned.</span></span>

<span data-ttu-id="bd45a-176">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="bd45a-176">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="bd45a-177">Un fichier de correctif de base de données peut être créé temporairement sur le disque et tout fichier existant à l’emplacement du fichier correctif peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="bd45a-177">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="bd45a-178">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.</span><span class="sxs-lookup"><span data-stu-id="bd45a-178">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="bd45a-179">Sur Windows XP et versions ultérieures, la sauvegarde n’est pas annulée si une tentative de sauvegarde d’une base de données n’a pas été attachée à l’instance au moment de l’appel a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="bd45a-179">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="bd45a-180">**Avertissement**  Pour des raisons de sécurité, il est important de noter que **JetOpenFileInstance** ne vérifie pas que le chemin de fichier demandé est associé à l’ensemble des fichiers sauvegardés pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="bd45a-180">**Warning**  For security reasons, it is important to note that **JetOpenFileInstance** does not verify that the requested file path is associated with the set of files that are backed up for the instance.</span></span> <span data-ttu-id="bd45a-181">Par conséquent, il est possible d’utiliser cette fonction pour accéder à n’importe quel fichier pouvant être ouvert par le contexte de sécurité actuel du thread.</span><span class="sxs-lookup"><span data-stu-id="bd45a-181">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="bd45a-182">Il est impératif que l’application limite les chemins passés à cette fonction à un ensemble connu de chemins d’accès de fichier corrects, ou qu’une divulgation d’informations puisse être rendue possible.</span><span class="sxs-lookup"><span data-stu-id="bd45a-182">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bd45a-183">Notes</span><span class="sxs-lookup"><span data-stu-id="bd45a-183">Remarks</span></span>

<span data-ttu-id="bd45a-184">Les mémoires tampons de sortie du handle et de la taille du fichier doivent être présentes.</span><span class="sxs-lookup"><span data-stu-id="bd45a-184">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="bd45a-185">Si elles ne sont pas présentes, le moteur se bloque car les paramètres de mémoire tampon de sortie ne sont pas validés.</span><span class="sxs-lookup"><span data-stu-id="bd45a-185">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="bd45a-186">À ce stade, un seul fichier peut être ouvert à la sauvegarde à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="bd45a-186">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="bd45a-187">**JetOpenFileInstance** ne déclare pas le privilège de sauvegarde avant l’ouverture du fichier demandé.</span><span class="sxs-lookup"><span data-stu-id="bd45a-187">**JetOpenFileInstance** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="bd45a-188">La taille du fichier à lire comme indiqué par cette fonction peut ne pas correspondre à la taille du fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="bd45a-188">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="bd45a-189">Sur Windows XP et versions ultérieures, des informations supplémentaires peuvent être ajoutées à un fichier de base de données qui est utilisé par le moteur de base de données lors d’une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="bd45a-189">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="bd45a-190">Par conséquent, l’application doit uniquement s’appuyer sur la taille de fichier retournée par **JetOpenFileInstance** ou sur le nombre réel d’octets de données retournés par [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd45a-190">As such, the application should only rely on the file size returned by **JetOpenFileInstance** or on the actual number of bytes of data returned by [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="bd45a-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd45a-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="bd45a-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bd45a-193">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bd45a-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-194"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="bd45a-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bd45a-195">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bd45a-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-196"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="bd45a-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bd45a-197">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="bd45a-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-198"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="bd45a-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bd45a-199">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bd45a-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd45a-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bd45a-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bd45a-201">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bd45a-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd45a-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bd45a-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bd45a-203">Implémenté en tant que <strong>JetOpenFileInstanceW</strong> (Unicode) et <strong>JetOpenFileInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bd45a-203">Implemented as <strong>JetOpenFileInstanceW</strong> (Unicode) and <strong>JetOpenFileInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bd45a-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd45a-204">See Also</span></span>

[<span data-ttu-id="bd45a-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bd45a-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bd45a-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="bd45a-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="bd45a-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bd45a-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="bd45a-208">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="bd45a-208">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="bd45a-209">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-209">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="bd45a-210">JetCloseFileInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-210">JetCloseFileInstance</span></span>](./jetclosefileinstance-function.md)  
[<span data-ttu-id="bd45a-211">JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-211">JetGetAttachInfoInstance</span></span>](./jetgetattachinfoinstance-function.md)  
[<span data-ttu-id="bd45a-212">JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-212">JetGetLogInfoInstance</span></span>](./jetgetloginfoinstance-function.md)  
[<span data-ttu-id="bd45a-213">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-213">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="bd45a-214">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-214">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="bd45a-215">JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="bd45a-215">JetTruncateLogInstance</span></span>](./jettruncateloginstance-function.md)
