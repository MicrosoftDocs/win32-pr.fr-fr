---
description: 'En savoir plus sur : fonction JetOpenFile'
title: Fonction JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516823"
---
# <a name="jetopenfile-function"></a><span data-ttu-id="b4456-103">Fonction JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="b4456-103">JetOpenFile Function</span></span>


<span data-ttu-id="b4456-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b4456-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfile-function"></a><span data-ttu-id="b4456-105">Fonction JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="b4456-105">JetOpenFile Function</span></span>

<span data-ttu-id="b4456-106">La fonction **JetOpenFile** ouvre une base de données attachée, un fichier de correctif de base de données ou un fichier journal de transactions d’une instance active afin d’effectuer une sauvegarde floue en continu.</span><span class="sxs-lookup"><span data-stu-id="b4456-106">The **JetOpenFile** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="b4456-107">Les données de ces fichiers peuvent ensuite être lues par le handle retourné à l’aide de [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4456-107">The data from these files can subsequently be read through the returned handle using [JetReadFile](./jetreadfile-function.md).</span></span> <span data-ttu-id="b4456-108">Le handle retourné doit être fermé à l’aide de [JetCloseFile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4456-108">The returned handle must be closed using [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="b4456-109">Une sauvegarde externe de l’instance doit avoir été précédemment lancée à l’aide de [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4456-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="b4456-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4456-110">Parameters</span></span>

<span data-ttu-id="b4456-111">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="b4456-111">*szFileName*</span></span>

<span data-ttu-id="b4456-112">Chemin relatif ou absolu d’une base de données attachée, d’un fichier de correctif de base de données ou d’un fichier journal de transactions géré par l’instance qui sera lue pour la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="b4456-112">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that will be read for backup.</span></span>

<span data-ttu-id="b4456-113">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="b4456-113">*phfFile*</span></span>

<span data-ttu-id="b4456-114">Mémoire tampon de sortie qui reçoit un handle vers le fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="b4456-114">The output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="b4456-115">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="b4456-115">*pulFileSizeLow*</span></span>

<span data-ttu-id="b4456-116">Mémoire tampon de sortie qui reçoit les 32 bits les moins significatifs de la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="b4456-116">The output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="b4456-117">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="b4456-117">*pulFileSizeHigh*</span></span>

<span data-ttu-id="b4456-118">Mémoire tampon de sortie qui reçoit les 32 bits les plus significatifs de la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="b4456-118">The output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="b4456-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4456-119">Return Value</span></span>

<span data-ttu-id="b4456-120">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="b4456-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b4456-121">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b4456-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4456-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4456-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="b4456-123">Description</span><span class="sxs-lookup"><span data-stu-id="b4456-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4456-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b4456-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b4456-125">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b4456-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-126">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="b4456-126">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="b4456-127">L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="b4456-127">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="b4456-128">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b4456-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b4456-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b4456-130">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b4456-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-131">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="b4456-131">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="b4456-132">L’opération a échoué car elle n’a pas pu ouvrir le fichier demandé en raison d’une violation de partage ou de privilèges insuffisants.</span><span class="sxs-lookup"><span data-stu-id="b4456-132">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-133">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="b4456-133">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="b4456-134">L’opération a échoué, car elle n’a pas pu ouvrir le fichier demandé, car il est introuvable dans le chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4456-134">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="b4456-135">Cette erreur est renvoyée uniquement par Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b4456-135">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b4456-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b4456-137">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="b4456-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="b4456-138">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b4456-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="b4456-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="b4456-140">L’opération de sauvegarde a échoué, car elle était appelée hors séquence.</span><span class="sxs-lookup"><span data-stu-id="b4456-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b4456-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b4456-142">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="b4456-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="b4456-143">Cela peut se produire pour <strong>JetOpenFile</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="b4456-143">This can happen for <strong>JetOpenFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="b4456-144">Le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="b4456-144">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="b4456-145">Le paramètre de nom de fichier spécifié est NULL ou une chaîne de longueur nulle (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="b4456-145">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-146">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="b4456-146">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="b4456-147">L’opération a échoué, car le chemin d’accès spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b4456-147">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-148">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="b4456-148">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="b4456-149">Le fichier demandé n’a pas pu être ouvert pour la sauvegarde, car il est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b4456-149">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="b4456-150">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b4456-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-151">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="b4456-151">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="b4456-152">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="b4456-152">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b4456-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b4456-154">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="b4456-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-155">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="b4456-155">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="b4456-156">L’opération a échoué, car la mémoire peut être allouée pour être terminée.</span><span class="sxs-lookup"><span data-stu-id="b4456-156">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="b4456-157"><strong>JetOpenFile</strong> retourne JET_errOutOfMemory si une tentative est faite pour ouvrir un autre fichier avant que le fichier précédent ouvert à l’aide de <strong>JetOpenFile</strong> ait été fermé par <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span><span class="sxs-lookup"><span data-stu-id="b4456-157"><strong>JetOpenFile</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFile</strong> has been closed by <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span></span> <span data-ttu-id="b4456-158">Un seul descripteur de fichier en attente est actuellement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4456-158">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-159">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="b4456-159">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="b4456-160">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="b4456-160">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b4456-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b4456-162">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="b4456-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span> <span data-ttu-id="b4456-163">JET_errRestoreInProgress il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="b4456-163">JET_errRestoreInProgress It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4456-164">En cas de réussite, un handle vers le fichier demandé est retourné.</span><span class="sxs-lookup"><span data-stu-id="b4456-164">On success, a handle to the requested file will be returned.</span></span> <span data-ttu-id="b4456-165">Si le descripteur concerne un fichier de base de données, ce fichier de base de données sera préparé pour la sauvegarde en continu, ce qui peut entraîner la création d’un fichier correctif de base de données au même emplacement que le fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="b4456-165">If the handle is for a database file, that database file will be prepared for streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="b4456-166">Le fichier de correctif de base de données a exactement le même chemin d’accès et le même nom de fichier que le fichier de base de données, mais il a un. Extension PAT.</span><span class="sxs-lookup"><span data-stu-id="b4456-166">The database patch file has the exact same path and filename as the database file, but has a .PAT extension.</span></span> <span data-ttu-id="b4456-167">La taille du fichier est également retournée.</span><span class="sxs-lookup"><span data-stu-id="b4456-167">The size of the file will also be returned.</span></span>

<span data-ttu-id="b4456-168">En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="b4456-168">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="b4456-169">Un fichier de correctif de base de données peut être créé temporairement sur le disque et tout fichier existant à l’emplacement du fichier correctif peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="b4456-169">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="b4456-170">L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance.</span><span class="sxs-lookup"><span data-stu-id="b4456-170">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="b4456-171">Sur Windows XP et versions ultérieures, la sauvegarde n’est pas annulée si une tentative de sauvegarde d’une base de données n’a pas été attachée à l’instance au moment de l’appel a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b4456-171">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="b4456-172">**Avertissement**  Pour des raisons de sécurité, il est important de noter que **JetOpenFile** ne vérifie pas que le chemin de fichier demandé est associé à l’ensemble des fichiers qui doivent être sauvegardés pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="b4456-172">**Warning**  For security reasons, it is important to note that **JetOpenFile** does not verify that the requested file path is associated with the set of files that should be backed up for the instance.</span></span> <span data-ttu-id="b4456-173">Par conséquent, il est possible d’utiliser cette fonction pour accéder à n’importe quel fichier pouvant être ouvert par le contexte de sécurité actuel du thread.</span><span class="sxs-lookup"><span data-stu-id="b4456-173">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="b4456-174">Il est impératif que l’application limite les chemins passés à cette fonction à un ensemble connu de chemins d’accès de fichier corrects, ou qu’une divulgation d’informations puisse être rendue possible.</span><span class="sxs-lookup"><span data-stu-id="b4456-174">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b4456-175">Notes</span><span class="sxs-lookup"><span data-stu-id="b4456-175">Remarks</span></span>

<span data-ttu-id="b4456-176">Les mémoires tampons de sortie du handle et de la taille du fichier doivent être présentes.</span><span class="sxs-lookup"><span data-stu-id="b4456-176">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="b4456-177">Si elles ne sont pas présentes, le moteur se bloque car les paramètres de mémoire tampon de sortie ne sont pas validés.</span><span class="sxs-lookup"><span data-stu-id="b4456-177">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="b4456-178">À ce stade, un seul fichier peut être ouvert à la sauvegarde à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="b4456-178">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="b4456-179">**JetOpenFile** ne déclare pas le privilège de sauvegarde avant l’ouverture du fichier demandé.</span><span class="sxs-lookup"><span data-stu-id="b4456-179">**JetOpenFile** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="b4456-180">La taille du fichier à lire comme indiqué par cette fonction peut ne pas correspondre à la taille du fichier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="b4456-180">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="b4456-181">Sur Windows XP et versions ultérieures, des informations supplémentaires peuvent être ajoutées à un fichier de base de données qui est utilisé par le moteur de base de données lors d’une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="b4456-181">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="b4456-182">Par conséquent, l’application doit uniquement s’appuyer sur la taille de fichier retournée par **JetOpenFile** ou sur le nombre réel d’octets de données retournés par [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4456-182">As such, the application should only rely on the file size returned by **JetOpenFile** or on the actual number of bytes of data returned by [JetReadFile](./jetreadfile-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="b4456-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4456-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4456-184"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b4456-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b4456-185">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="b4456-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-186"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b4456-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b4456-187">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b4456-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-188"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b4456-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b4456-189">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b4456-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-190"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="b4456-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b4456-191">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b4456-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4456-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b4456-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b4456-193">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b4456-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4456-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b4456-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b4456-195">Implémenté en tant que <strong>JetOpenFileW</strong> (Unicode) et <strong>JetOpenFileA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b4456-195">Implemented as <strong>JetOpenFileW</strong> (Unicode) and <strong>JetOpenFileA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b4456-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4456-196">See Also</span></span>

[<span data-ttu-id="b4456-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b4456-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b4456-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="b4456-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="b4456-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b4456-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b4456-200">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="b4456-200">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="b4456-201">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="b4456-201">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="b4456-202">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="b4456-202">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="b4456-203">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="b4456-203">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="b4456-204">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="b4456-204">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="b4456-205">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="b4456-205">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="b4456-206">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="b4456-206">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="b4456-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="b4456-207">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="b4456-208">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="b4456-208">JetTruncateLog</span></span>](./jettruncatelog-function.md)
