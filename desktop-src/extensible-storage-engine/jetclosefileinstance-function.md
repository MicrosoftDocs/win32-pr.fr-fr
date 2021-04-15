---
description: 'En savoir plus sur : fonction JetCloseFileInstance'
title: JetCloseFileInstance fonction)
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524969"
---
# <a name="jetclosefileinstance-function"></a><span data-ttu-id="f75a5-103">JetCloseFileInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="f75a5-103">JetCloseFileInstance Function</span></span>


<span data-ttu-id="f75a5-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f75a5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefileinstance-function"></a><span data-ttu-id="f75a5-105">JetCloseFileInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="f75a5-105">JetCloseFileInstance Function</span></span>

<span data-ttu-id="f75a5-106">La fonction **JetCloseFileInstance** ferme un fichier ouvert avec [JetOpenFileInstance](./jetopenfileinstance-function.md) une fois que les données de ce fichier ont été extraites à l’aide de [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="f75a5-106">The **JetCloseFileInstance** function closes a file that was opened with [JetOpenFileInstance](./jetopenfileinstance-function.md) after the data from that file has been extracted using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="f75a5-107">**Windows XP : JetCloseFileInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f75a5-107">**Windows XP:  JetCloseFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="f75a5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f75a5-108">Parameters</span></span>

<span data-ttu-id="f75a5-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="f75a5-109">*instance*</span></span>

<span data-ttu-id="f75a5-110">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="f75a5-110">The instance to use for this call.</span></span>

<span data-ttu-id="f75a5-111">Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f75a5-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="f75a5-112">L’utilisation de cette instance globale est implicitement dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="f75a5-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="f75a5-113">Pour Windows XP et les versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f75a5-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="f75a5-114">Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="f75a5-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="f75a5-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="f75a5-115">*hfFile*</span></span>

<span data-ttu-id="f75a5-116">Handle du fichier à lire.</span><span class="sxs-lookup"><span data-stu-id="f75a5-116">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="f75a5-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f75a5-117">Return Value</span></span>

<span data-ttu-id="f75a5-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="f75a5-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f75a5-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f75a5-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f75a5-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f75a5-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="f75a5-121">Description</span><span class="sxs-lookup"><span data-stu-id="f75a5-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f75a5-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f75a5-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f75a5-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f75a5-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f75a5-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f75a5-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f75a5-125">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="f75a5-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f75a5-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f75a5-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f75a5-127">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="f75a5-127">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="f75a5-128">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f75a5-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f75a5-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f75a5-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f75a5-130">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a produit un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="f75a5-130">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="f75a5-131">Cela peut se produire pour <strong>JetCloseFileInstance</strong> dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="f75a5-131">This can happen for <strong>JetCloseFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="f75a5-132">Le descripteur d’instance spécifié n’est pas valide (Windows XP et versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="f75a5-132">The specified instance handle is invalid (Windows XP and later releases)</span></span></p></li>
<li><p><span data-ttu-id="f75a5-133">Le descripteur de fichier spécifié n’est pas valide</span><span class="sxs-lookup"><span data-stu-id="f75a5-133">The specified file handle is invalid</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f75a5-134">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="f75a5-134">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="f75a5-135">L’opération a échoué, car aucune sauvegarde externe n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="f75a5-135">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f75a5-136">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f75a5-136">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f75a5-137">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="f75a5-137">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f75a5-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f75a5-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f75a5-139">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="f75a5-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f75a5-140">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="f75a5-140">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="f75a5-141">L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</span><span class="sxs-lookup"><span data-stu-id="f75a5-141">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f75a5-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f75a5-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f75a5-143">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f75a5-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f75a5-144">En cas de réussite, le descripteur de fichier est fermé.</span><span class="sxs-lookup"><span data-stu-id="f75a5-144">On success, the file handle is closed.</span></span> <span data-ttu-id="f75a5-145">Si un fichier de base de données a été fermé, le fichier correctif de base de données associé (le cas échéant) est détruit.</span><span class="sxs-lookup"><span data-stu-id="f75a5-145">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="f75a5-146">En cas d’échec, aucune modification ne se produit.</span><span class="sxs-lookup"><span data-stu-id="f75a5-146">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f75a5-147">Notes</span><span class="sxs-lookup"><span data-stu-id="f75a5-147">Remarks</span></span>

<span data-ttu-id="f75a5-148">Le moteur de base de données ne prend actuellement en charge qu’un seul fichier ouvert via [JetOpenFileInstance](./jetopenfileinstance-function.md) à la fois.</span><span class="sxs-lookup"><span data-stu-id="f75a5-148">The database engine currently only supports one open file through [JetOpenFileInstance](./jetopenfileinstance-function.md) at a time.</span></span> <span data-ttu-id="f75a5-149">Si un descripteur de fichier est ouvert à l’aide de [JetOpenFileInstance](./jetopenfileinstance-function.md) , il doit être fermé à l’aide de **JetCloseFileInstance** pour pouvoir ouvrir un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="f75a5-149">If a file handle is opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) then it must be closed using **JetCloseFileInstance** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f75a5-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f75a5-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f75a5-151"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f75a5-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f75a5-152">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f75a5-152">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f75a5-153"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f75a5-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f75a5-154">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f75a5-154">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f75a5-155"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f75a5-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f75a5-156">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f75a5-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f75a5-157"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f75a5-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f75a5-158">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f75a5-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f75a5-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f75a5-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f75a5-160">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f75a5-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f75a5-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f75a5-161">See Also</span></span>

[<span data-ttu-id="f75a5-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f75a5-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f75a5-163">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="f75a5-163">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="f75a5-164">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f75a5-164">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f75a5-165">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="f75a5-165">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="f75a5-166">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="f75a5-166">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="f75a5-167">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="f75a5-167">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
