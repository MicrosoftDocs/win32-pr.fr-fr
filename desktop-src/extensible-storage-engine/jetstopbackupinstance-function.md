---
description: 'En savoir plus sur : fonction JetStopBackupInstance'
title: JetStopBackupInstance fonction)
TOCTitle: JetStopBackupInstance Function
ms:assetid: 7d008eac-2a32-402b-91ef-965ed3c3b0de
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269309(v=EXCHG.10)
ms:contentKeyID: 32765599
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1813658ed1fb569795bdfa65ccada3ef8ee629c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112515"
---
# <a name="jetstopbackupinstance-function"></a><span data-ttu-id="dfb22-103">JetStopBackupInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="dfb22-103">JetStopBackupInstance Function</span></span>


<span data-ttu-id="dfb22-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="dfb22-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackupinstance-function"></a><span data-ttu-id="dfb22-105">JetStopBackupInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="dfb22-105">JetStopBackupInstance Function</span></span>

<span data-ttu-id="dfb22-106">La fonction **JetStopBackupInstance** empêche la continuation de l’activité liée à la sauvegarde de se poursuivre sur une instance en cours d’exécution spécifique, ce qui met fin à la sauvegarde en continu de manière prévisible.</span><span class="sxs-lookup"><span data-stu-id="dfb22-106">The **JetStopBackupInstance** function prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="dfb22-107">**Windows XP :**  **JetStopBackupInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dfb22-107">**Windows XP:**  **JetStopBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="dfb22-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfb22-108">Parameters</span></span>

<span data-ttu-id="dfb22-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="dfb22-109">*instance*</span></span>

<span data-ttu-id="dfb22-110">Identifie l’instance en cours d’exécution à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="dfb22-110">Identifies the running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="dfb22-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dfb22-111">Return Value</span></span>

<span data-ttu-id="dfb22-112">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="dfb22-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="dfb22-113">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dfb22-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dfb22-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dfb22-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="dfb22-115">Description</span><span class="sxs-lookup"><span data-stu-id="dfb22-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dfb22-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dfb22-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dfb22-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="dfb22-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfb22-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="dfb22-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="dfb22-119">Le paramètre d’instance spécifié a une valeur non valide (pas une instance en cours d’exécution).</span><span class="sxs-lookup"><span data-stu-id="dfb22-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="dfb22-120"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dfb22-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dfb22-121">Si cette fonction réussit, l’instance qui a été spécifiée échouera avec les nouvelles API de sauvegarde en continu.</span><span class="sxs-lookup"><span data-stu-id="dfb22-121">If this function succeeds, the instance that was specified will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="dfb22-122">Si cette fonction échoue, aucune étape de préparation de l’arrêt de la sauvegarde sur l’instance ne sera effectuée et aucune modification de l’état de l’instance ne se produira.</span><span class="sxs-lookup"><span data-stu-id="dfb22-122">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="dfb22-123">Notes</span><span class="sxs-lookup"><span data-stu-id="dfb22-123">Remarks</span></span>

<span data-ttu-id="dfb22-124">La sauvegarde est généralement déclenchée par un événement à l’extérieur du mécanisme de processus et à l’aide de cette API, l’application ESENT elle-même effectue d’autres appels vers les API de sauvegarde en continu.</span><span class="sxs-lookup"><span data-stu-id="dfb22-124">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="dfb22-125">La majorité des API de sauvegarde en continu échouent avec JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="dfb22-125">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="dfb22-126">Ainsi, toute progression de la sauvegarde en continu (telle que [JetReadFileInstance](./jetreadfileinstance-function.md)) renverra une erreur.</span><span class="sxs-lookup"><span data-stu-id="dfb22-126">As such, any streaming backup progress (such as [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="dfb22-127">Les opérations de sauvegarde qui font partie de l’arrêt de la sauvegarde (comme [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) sont toujours autorisées.</span><span class="sxs-lookup"><span data-stu-id="dfb22-127">Backup operations which are part of the backup termination (like [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dfb22-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfb22-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dfb22-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="dfb22-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dfb22-130">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dfb22-130">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfb22-131"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="dfb22-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dfb22-132">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dfb22-132">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfb22-133"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="dfb22-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dfb22-134">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="dfb22-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfb22-135"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="dfb22-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dfb22-136">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dfb22-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfb22-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="dfb22-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dfb22-138">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dfb22-138">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dfb22-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfb22-139">See Also</span></span>

[<span data-ttu-id="dfb22-140">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dfb22-140">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dfb22-141">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="dfb22-141">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="dfb22-142">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="dfb22-142">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="dfb22-143">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="dfb22-143">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="dfb22-144">JetStopService</span><span class="sxs-lookup"><span data-stu-id="dfb22-144">JetStopService</span></span>](./jetstopservice-function.md)
