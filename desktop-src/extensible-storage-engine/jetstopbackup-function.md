---
description: 'En savoir plus sur : fonction JetStopBackup'
title: JetStopBackup fonction)
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106531382"
---
# <a name="jetstopbackup-function"></a><span data-ttu-id="65c38-103">JetStopBackup fonction)</span><span class="sxs-lookup"><span data-stu-id="65c38-103">JetStopBackup Function</span></span>


<span data-ttu-id="65c38-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="65c38-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackup-function"></a><span data-ttu-id="65c38-105">JetStopBackup fonction)</span><span class="sxs-lookup"><span data-stu-id="65c38-105">JetStopBackup Function</span></span>

<span data-ttu-id="65c38-106">La fonction **JetStopBackup** empêche toute activité liée à la sauvegarde en continu de continuer sur une instance en cours d’exécution spécifique, ce qui met fin à la sauvegarde en continu de manière prévisible.</span><span class="sxs-lookup"><span data-stu-id="65c38-106">The **JetStopBackup** function prevents any streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="65c38-107">**Windows XP :**  Cette fonction est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="65c38-107">**Windows XP:**  This function is introduced in Windows XP.</span></span>

<span data-ttu-id="65c38-108">[JetStopService](./jetstopservice-function.md) est l’appel hérité lorsqu’une seule instance est autorisée.</span><span class="sxs-lookup"><span data-stu-id="65c38-108">[JetStopService](./jetstopservice-function.md) is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="65c38-109">Dans ce cas, la seule instance active est celle qui est préparée pour l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="65c38-109">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="65c38-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65c38-110">Parameters</span></span>

<span data-ttu-id="65c38-111">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="65c38-111">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="65c38-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65c38-112">Return Value</span></span>

<span data-ttu-id="65c38-113">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="65c38-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="65c38-114">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="65c38-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65c38-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="65c38-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="65c38-116">Description</span><span class="sxs-lookup"><span data-stu-id="65c38-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65c38-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="65c38-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="65c38-118">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="65c38-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65c38-119">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="65c38-119">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="65c38-120">Il n’est pas évident de déterminer l’instance à préparer pour l’arrêt lors de l’utilisation de <a href="gg269240(v=exchg.10).md">JetStopService</a> avec plusieurs modes d’instance.</span><span class="sxs-lookup"><span data-stu-id="65c38-120">It is not clear which instance to prepare for termination when using <a href="gg269240(v=exchg.10).md">JetStopService</a> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="65c38-121"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="65c38-121"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="65c38-122">Si cette fonction réussit, l’instance commence à faire échouer les nouvelles API de sauvegarde en continu.</span><span class="sxs-lookup"><span data-stu-id="65c38-122">If this function succeeds, the instance will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="65c38-123">Si cette fonction échoue, aucune étape de préparation de l’arrêt de la sauvegarde sur l’instance ne sera effectuée et aucune modification de l’état de l’instance ne se produira.</span><span class="sxs-lookup"><span data-stu-id="65c38-123">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="65c38-124">Notes</span><span class="sxs-lookup"><span data-stu-id="65c38-124">Remarks</span></span>

<span data-ttu-id="65c38-125">La sauvegarde est généralement déclenchée par un événement à l’extérieur du mécanisme de processus et à l’aide de cette API, l’application ESENT elle-même effectue d’autres appels vers les API de sauvegarde en continu.</span><span class="sxs-lookup"><span data-stu-id="65c38-125">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="65c38-126">La majorité des API de sauvegarde en continu échouent avec JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="65c38-126">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="65c38-127">Par conséquent, toute progression de la sauvegarde en continu (telle que [JetReadFileInstance](./jetreadfileinstance-function.md)) renverra une erreur.</span><span class="sxs-lookup"><span data-stu-id="65c38-127">As such, any streaming backup progress (like [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="65c38-128">Les opérations de sauvegarde qui font partie de l’arrêt de la sauvegarde (par exemple, [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) sont toujours autorisées.</span><span class="sxs-lookup"><span data-stu-id="65c38-128">Backup operations which are part of the backup termination (such as [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="65c38-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65c38-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65c38-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="65c38-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="65c38-131">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="65c38-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65c38-132"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="65c38-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="65c38-133">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="65c38-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65c38-134"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="65c38-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="65c38-135">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="65c38-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65c38-136"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="65c38-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="65c38-137">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="65c38-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="65c38-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="65c38-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="65c38-139">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="65c38-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="65c38-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65c38-140">See Also</span></span>

[<span data-ttu-id="65c38-141">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="65c38-141">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="65c38-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="65c38-142">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="65c38-143">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="65c38-143">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="65c38-144">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="65c38-144">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="65c38-145">JetStopService</span><span class="sxs-lookup"><span data-stu-id="65c38-145">JetStopService</span></span>](./jetstopservice-function.md)
