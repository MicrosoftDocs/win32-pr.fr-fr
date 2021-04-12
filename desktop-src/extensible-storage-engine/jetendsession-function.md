---
description: 'En savoir plus sur : fonction JetEndSession'
title: JetEndSession fonction)
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46bea6f5db745252a5e0ac6e8e03550dfead1b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319642"
---
# <a name="jetendsession-function"></a><span data-ttu-id="938ee-103">JetEndSession fonction)</span><span class="sxs-lookup"><span data-stu-id="938ee-103">JetEndSession Function</span></span>


<span data-ttu-id="938ee-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="938ee-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendsession-function"></a><span data-ttu-id="938ee-105">JetEndSession fonction)</span><span class="sxs-lookup"><span data-stu-id="938ee-105">JetEndSession Function</span></span>

<span data-ttu-id="938ee-106">La fonction **JetEndSession** met fin à la session et nettoie et libère toutes les ressources associées à la session spécifiée.</span><span class="sxs-lookup"><span data-stu-id="938ee-106">The **JetEndSession** function ends the session, and cleans up and deallocates any resources associated with the specified session.</span></span>

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="938ee-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="938ee-107">Parameters</span></span>

<span data-ttu-id="938ee-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="938ee-108">*sesid*</span></span>

<span data-ttu-id="938ee-109">Session à terminer.</span><span class="sxs-lookup"><span data-stu-id="938ee-109">The session to end.</span></span> <span data-ttu-id="938ee-110">Les ressources associées sont libérées à la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="938ee-110">Associated resources are released when the session ends.</span></span>

<span data-ttu-id="938ee-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="938ee-111">*grbit*</span></span>

<span data-ttu-id="938ee-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="938ee-112">Reserved.</span></span> <span data-ttu-id="938ee-113">Ce paramètre peut contenir l’indicateur JET_bitForceSessionClosed, mais cet indicateur est réservé et sa définition n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="938ee-113">This parameter can contain the JET_bitForceSessionClosed flag, but this flag is reserved and setting it has no effect.</span></span>

### <a name="return-value"></a><span data-ttu-id="938ee-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="938ee-114">Return Value</span></span>

<span data-ttu-id="938ee-115">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="938ee-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="938ee-116">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="938ee-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="938ee-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="938ee-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="938ee-118">Description</span><span class="sxs-lookup"><span data-stu-id="938ee-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="938ee-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="938ee-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="938ee-120">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="938ee-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938ee-121">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="938ee-121">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="938ee-122">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="938ee-122">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938ee-123">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="938ee-123">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="938ee-124">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a produit un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="938ee-124">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938ee-125">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="938ee-125">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="938ee-126">La session n’était pas une session JET valide.</span><span class="sxs-lookup"><span data-stu-id="938ee-126">The session was not a valid JET session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938ee-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="938ee-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="938ee-128">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="938ee-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938ee-129">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="938ee-129">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="938ee-130">L’opération a échoué car la mémoire n’a pas pu être allouée.</span><span class="sxs-lookup"><span data-stu-id="938ee-130">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938ee-131">JET_errSessionInUse</span><span class="sxs-lookup"><span data-stu-id="938ee-131">JET_errSessionInUse</span></span></p></td>
<td><p><span data-ttu-id="938ee-132">Cela signifie que la session était en cours d’utilisation sur un autre thread ou que la session n’a pas été définie ou réinitialisée correctement.</span><span class="sxs-lookup"><span data-stu-id="938ee-132">This means the session was in use on another thread, or the session was not set or reset properly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938ee-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="938ee-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="938ee-134">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="938ee-134">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="938ee-135">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="938ee-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938ee-136">JET_errOutOfBuffers</span><span class="sxs-lookup"><span data-stu-id="938ee-136">JET_errOutOfBuffers</span></span></p></td>
<td><p><span data-ttu-id="938ee-137">Erreur système qui indique qu’il n’y a plus de tampons.</span><span class="sxs-lookup"><span data-stu-id="938ee-137">System error that indicates that there are no more buffers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938ee-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="938ee-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="938ee-139">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="938ee-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938ee-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="938ee-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="938ee-141">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="938ee-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="938ee-142">En cas de réussite, le descripteur de session est fermé et non disponible, et toutes les ressources associées à cette session sont nettoyées.</span><span class="sxs-lookup"><span data-stu-id="938ee-142">On success, the session handle is closed, and unavailable, and all resources related to this session are cleaned up.</span></span>

<span data-ttu-id="938ee-143">En cas d’échec, plusieurs autres erreurs peuvent se produire dans le cadre de la fermeture de la table de tri, de la fermeture du curseur et de la restauration de la transaction.</span><span class="sxs-lookup"><span data-stu-id="938ee-143">On failure, there are several additional errors that could occur as part of sort table close, cursor close, and transaction rollback.</span></span> <span data-ttu-id="938ee-144">Ces erreurs sont relativement peu probables, et très peu probables si vos sessions ne sont pas entièrement utilisées lorsque **JetEndSession** est appelé.</span><span class="sxs-lookup"><span data-stu-id="938ee-144">These errors are fairly unlikely, and extremely unlikely if your sessions are completely not in use when **JetEndSession** is called.</span></span> <span data-ttu-id="938ee-145">Ces erreurs sont retournées si une partie de la session n’a pas pu être nettoyée correctement.</span><span class="sxs-lookup"><span data-stu-id="938ee-145">These errors will be returned if some part of the session was unable to be cleaned up properly.</span></span>

#### <a name="remarks"></a><span data-ttu-id="938ee-146">Notes</span><span class="sxs-lookup"><span data-stu-id="938ee-146">Remarks</span></span>

<span data-ttu-id="938ee-147">Cette API restaure toutes les transactions ouvertes (non validées au niveau 0).</span><span class="sxs-lookup"><span data-stu-id="938ee-147">This API will rollback any open transactions (not committed to level 0).</span></span> <span data-ttu-id="938ee-148">De même, tous les curseurs associés à cette session et les tables de tri qui ont été créées ou ouvertes sont nettoyés.</span><span class="sxs-lookup"><span data-stu-id="938ee-148">Also all cursors associated with this session, and any sort tables that have been created or opened will be cleaned up.</span></span>

#### <a name="requirements"></a><span data-ttu-id="938ee-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="938ee-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="938ee-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="938ee-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="938ee-151">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="938ee-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938ee-152"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="938ee-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="938ee-153">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="938ee-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938ee-154"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="938ee-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="938ee-155">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="938ee-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="938ee-156"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="938ee-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="938ee-157">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="938ee-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="938ee-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="938ee-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="938ee-159">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="938ee-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="938ee-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="938ee-160">See Also</span></span>

[<span data-ttu-id="938ee-161">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="938ee-161">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="938ee-162">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="938ee-162">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="938ee-163">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="938ee-163">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="938ee-164">JetRollback</span><span class="sxs-lookup"><span data-stu-id="938ee-164">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="938ee-165">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="938ee-165">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="938ee-166">JetStopService</span><span class="sxs-lookup"><span data-stu-id="938ee-166">JetStopService</span></span>](./jetstopservice-function.md)
