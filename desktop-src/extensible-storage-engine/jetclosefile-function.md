---
description: 'En savoir plus sur : fonction JetCloseFile'
title: JetCloseFile fonction)
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393380"
---
# <a name="jetclosefile-function"></a><span data-ttu-id="a0a0c-103">JetCloseFile fonction)</span><span class="sxs-lookup"><span data-stu-id="a0a0c-103">JetCloseFile Function</span></span>


<span data-ttu-id="a0a0c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a0a0c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefile-function"></a><span data-ttu-id="a0a0c-105">JetCloseFile fonction)</span><span class="sxs-lookup"><span data-stu-id="a0a0c-105">JetCloseFile Function</span></span>

<span data-ttu-id="a0a0c-106">La fonction **JetCloseFile** ferme un fichier ouvert avec [JetOpenFile](./jetopenfile-function.md) une fois que les données de ce fichier ont été extraites à l’aide de [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="a0a0c-106">The **JetCloseFile** function closes a file that was opened with [JetOpenFile](./jetopenfile-function.md) after the data from that file has been extracted using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="a0a0c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0a0c-107">Parameters</span></span>

<span data-ttu-id="a0a0c-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="a0a0c-108">*hfFile*</span></span>

<span data-ttu-id="a0a0c-109">Handle du fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-109">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="a0a0c-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a0a0c-110">Return Value</span></span>

<span data-ttu-id="a0a0c-111">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a0a0c-112">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a0a0c-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0a0c-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a0a0c-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="a0a0c-114">Description</span><span class="sxs-lookup"><span data-stu-id="a0a0c-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0a0c-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a0a0c-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-116">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0a0c-117">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a0a0c-117">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-118">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-118">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0a0c-119">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a0a0c-119">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-120">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-120">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a0a0c-121">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-121">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0a0c-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a0a0c-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-123">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-123">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a0a0c-124">Cela peut se produire pour <strong>JetCloseFile</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="a0a0c-124">This can happen for <strong>JetCloseFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a0a0c-125">Le handle d’instance spécifié n’est pas valide (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="a0a0c-125">The specified instance handle is invalid (Windows XP and later releases),</span></span></p></li>
<li><p><span data-ttu-id="a0a0c-126">Le descripteur de fichier spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-126">The specified file handle is invalid.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0a0c-127">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="a0a0c-127">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-128">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-128">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0a0c-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a0a0c-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-130">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-130">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0a0c-131">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a0a0c-131">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-132">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-132">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0a0c-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a0a0c-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-134">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-134">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0a0c-135">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a0a0c-135">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a0a0c-136">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-136">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0a0c-137">En cas de réussite, le descripteur de fichier est fermé.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-137">On success, the file handle is closed.</span></span> <span data-ttu-id="a0a0c-138">Si un fichier de base de données a été fermé, le fichier correctif de base de données associé (le cas échéant) est détruit.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-138">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="a0a0c-139">En cas d’échec, aucune modification ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-139">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a0a0c-140">Notes</span><span class="sxs-lookup"><span data-stu-id="a0a0c-140">Remarks</span></span>

<span data-ttu-id="a0a0c-141">Le moteur de base de données ne prend actuellement en charge qu’un seul fichier ouvert via [JetOpenFile](./jetopenfile-function.md) à la fois.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-141">The database engine currently only supports one open file through [JetOpenFile](./jetopenfile-function.md) at a time.</span></span> <span data-ttu-id="a0a0c-142">Si un descripteur de fichier est ouvert à l’aide de [JetOpenFile](./jetopenfile-function.md) , il doit être fermé à l’aide de **JetCloseFile** pour pouvoir ouvrir un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-142">If a file handle is opened using [JetOpenFile](./jetopenfile-function.md) then it must be closed using **JetCloseFile** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a0a0c-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0a0c-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0a0c-144"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a0a0c-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a0a0c-145">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0a0c-146"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a0a0c-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a0a0c-147">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0a0c-148"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a0a0c-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a0a0c-149">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0a0c-150"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="a0a0c-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a0a0c-151">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0a0c-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a0a0c-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a0a0c-153">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a0a0c-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a0a0c-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0a0c-154">See Also</span></span>

[<span data-ttu-id="a0a0c-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a0a0c-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a0a0c-156">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a0a0c-156">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a0a0c-157">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="a0a0c-157">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="a0a0c-158">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="a0a0c-158">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="a0a0c-159">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="a0a0c-159">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="a0a0c-160">JetStopService</span><span class="sxs-lookup"><span data-stu-id="a0a0c-160">JetStopService</span></span>](./jetstopservice-function.md)
