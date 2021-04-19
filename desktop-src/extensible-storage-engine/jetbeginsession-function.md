---
description: 'En savoir plus sur : fonction JetBeginSession'
title: Fonction JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541993"
---
# <a name="jetbeginsession-function"></a><span data-ttu-id="ae03d-103">Fonction JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="ae03d-103">JetBeginSession Function</span></span>


<span data-ttu-id="ae03d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ae03d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginsession-function"></a><span data-ttu-id="ae03d-105">Fonction JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="ae03d-105">JetBeginSession Function</span></span>

<span data-ttu-id="ae03d-106">La fonction **JetBeginSession** démarre une session et initialise et retourne un handle de session ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="ae03d-106">The **JetBeginSession** function starts a session and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="ae03d-107">Les sessions contrôlent tous les accès à la base de données et sont utilisées pour contrôler l’étendue des transactions.</span><span class="sxs-lookup"><span data-stu-id="ae03d-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="ae03d-108">La session peut être utilisée pour commencer, valider ou abandonner des transactions.</span><span class="sxs-lookup"><span data-stu-id="ae03d-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="ae03d-109">La session est également utilisée pour attacher, créer ou ouvrir une base de données.</span><span class="sxs-lookup"><span data-stu-id="ae03d-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="ae03d-110">La session est utilisée comme contexte pour toutes les opérations DDL et DML.</span><span class="sxs-lookup"><span data-stu-id="ae03d-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="ae03d-111">Pour augmenter l’accès concurrentiel et l’accès parallèle à la base de données, plusieurs sessions peuvent être démarrées.</span><span class="sxs-lookup"><span data-stu-id="ae03d-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a><span data-ttu-id="ae03d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae03d-112">Parameters</span></span>

<span data-ttu-id="ae03d-113">*instancié*</span><span class="sxs-lookup"><span data-stu-id="ae03d-113">*instance*</span></span>

<span data-ttu-id="ae03d-114">Instance de base de données à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="ae03d-114">The database instance to use for this call.</span></span>

<span data-ttu-id="ae03d-115">*psesid*</span><span class="sxs-lookup"><span data-stu-id="ae03d-115">*psesid*</span></span>

<span data-ttu-id="ae03d-116">Pointeur vers la variable que le handle de session Initialise lors d’un retour réussi.</span><span class="sxs-lookup"><span data-stu-id="ae03d-116">Pointer to the variable that the session handle initializes on successful return.</span></span>

<span data-ttu-id="ae03d-117">*szUserName*</span><span class="sxs-lookup"><span data-stu-id="ae03d-117">*szUserName*</span></span>

<span data-ttu-id="ae03d-118">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="ae03d-118">This parameter is reserved.</span></span>

<span data-ttu-id="ae03d-119">*szPassword*</span><span class="sxs-lookup"><span data-stu-id="ae03d-119">*szPassword*</span></span>

<span data-ttu-id="ae03d-120">Ce paramètre est réservé.</span><span class="sxs-lookup"><span data-stu-id="ae03d-120">This parameter is reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="ae03d-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae03d-121">Return Value</span></span>

<span data-ttu-id="ae03d-122">Cette fonction permet le retour de tout [JET_ERR](./jet-err.md)s qui sont définis dans cette API.</span><span class="sxs-lookup"><span data-stu-id="ae03d-122">This function allows for the return of any [JET_ERR](./jet-err.md)s that are defined in this API.</span></span> <span data-ttu-id="ae03d-123">Pour plus d’informations sur les erreurs jet, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ae03d-123">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae03d-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ae03d-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="ae03d-125">Description</span><span class="sxs-lookup"><span data-stu-id="ae03d-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae03d-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ae03d-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ae03d-127">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ae03d-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae03d-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="ae03d-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="ae03d-129">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="ae03d-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae03d-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="ae03d-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="ae03d-131">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="ae03d-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="ae03d-132">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ae03d-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae03d-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="ae03d-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="ae03d-134">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="ae03d-134">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae03d-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="ae03d-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="ae03d-136">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="ae03d-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae03d-137">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="ae03d-137">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="ae03d-138">L’opération a échoué car la mémoire n’a pas pu être allouée.</span><span class="sxs-lookup"><span data-stu-id="ae03d-138">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae03d-139">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="ae03d-139">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="ae03d-140">Le nombre de sessions que le moteur autorise le client à démarrer est limité.</span><span class="sxs-lookup"><span data-stu-id="ae03d-140">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="ae03d-141">Cette valeur peut être modifiée à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec la constante JET_paramMaxSessions.</span><span class="sxs-lookup"><span data-stu-id="ae03d-141">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the JET_paramMaxSessions constant.</span></span> <span data-ttu-id="ae03d-142">Le nombre de sessions par défaut est 16.</span><span class="sxs-lookup"><span data-stu-id="ae03d-142">The default number of sessions is 16.</span></span> <span data-ttu-id="ae03d-143">Pour plus d’informations sur la JET_paramMaxSessions, consultez <a href="gg294139(v=exchg.10).md">paramètres système</a> .</span><span class="sxs-lookup"><span data-stu-id="ae03d-143">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about JET_paramMaxSessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae03d-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="ae03d-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="ae03d-145">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="ae03d-145">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae03d-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="ae03d-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="ae03d-147">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ae03d-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ae03d-148">En cas de réussite, le descripteur de session est initialisé et peut être utilisé pour les opérations de base de données.</span><span class="sxs-lookup"><span data-stu-id="ae03d-148">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="ae03d-149">En cas d’échec, aucune session n’est disponible ou une nouvelle session n’a pas pu être initialisée.</span><span class="sxs-lookup"><span data-stu-id="ae03d-149">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ae03d-150">Notes</span><span class="sxs-lookup"><span data-stu-id="ae03d-150">Remarks</span></span>

<span data-ttu-id="ae03d-151">Une attention particulière doit être utilisée lors de l’utilisation de sessions sur différents threads.</span><span class="sxs-lookup"><span data-stu-id="ae03d-151">Careful attention must be used when using sessions across different threads.</span></span> <span data-ttu-id="ae03d-152">Une session suit le thread sur lequel elle a été utilisée pendant [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md)ou [JetRollback](./jetrollback-function.md), et génère une erreur si elle est utilisée sur plusieurs threads avec une transaction ouverte.</span><span class="sxs-lookup"><span data-stu-id="ae03d-152">A session tracks which thread it was used on during [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md), or [JetRollback](./jetrollback-function.md), and it will throw an error if used on multiple threads with an open transaction.</span></span> <span data-ttu-id="ae03d-153">Le [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) peut modifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="ae03d-153">The [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) can change this behavior.</span></span> <span data-ttu-id="ae03d-154">Étant donné que la session est toujours un contexte sérialisé, plusieurs opérations de base de données ne peuvent pas être exécutées simultanément sur une seule session, en série uniquement.</span><span class="sxs-lookup"><span data-stu-id="ae03d-154">Since the session is still a serialized context, and multiple database operations cannot be performed on a single session concurrently, only serially.</span></span> <span data-ttu-id="ae03d-155">Toutefois, vous pouvez utiliser plusieurs sessions pour obtenir un accès simultané à la base de données.</span><span class="sxs-lookup"><span data-stu-id="ae03d-155">However, you can use multiple sessions to achieve concurrent database access.</span></span> <span data-ttu-id="ae03d-156">Les sessions peuvent être utilisées à l’intérieur d’une transaction entre les threads en définissant et en réinitialisant les contextes de session.</span><span class="sxs-lookup"><span data-stu-id="ae03d-156">Sessions can be used inside a transaction across threads by setting and resetting the session contexts.</span></span>

<span data-ttu-id="ae03d-157">Le descripteur de session doit être fermé avec [JetEndSession](./jetendsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="ae03d-157">The session handle should be closed with [JetEndSession](./jetendsession-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="ae03d-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae03d-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae03d-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ae03d-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ae03d-160">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="ae03d-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae03d-161"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="ae03d-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ae03d-162">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ae03d-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae03d-163"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="ae03d-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ae03d-164">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="ae03d-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae03d-165"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="ae03d-165"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ae03d-166">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ae03d-166">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae03d-167"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ae03d-167"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ae03d-168">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ae03d-168">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae03d-169"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="ae03d-169"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="ae03d-170">Implémenté en tant que <strong>JetBeginSessionW</strong> (Unicode) et <strong>JetBeginSessionA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ae03d-170">Implemented as <strong>JetBeginSessionW</strong> (Unicode) and <strong>JetBeginSessionA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ae03d-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae03d-171">See Also</span></span>

[<span data-ttu-id="ae03d-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ae03d-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ae03d-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ae03d-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="ae03d-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="ae03d-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="ae03d-175">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="ae03d-175">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="ae03d-176">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="ae03d-176">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="ae03d-177">JetDupSession</span><span class="sxs-lookup"><span data-stu-id="ae03d-177">JetDupSession</span></span>](./jetdupsession-function.md)  
[<span data-ttu-id="ae03d-178">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="ae03d-178">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="ae03d-179">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="ae03d-179">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="ae03d-180">JetRollback</span><span class="sxs-lookup"><span data-stu-id="ae03d-180">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="ae03d-181">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="ae03d-181">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="ae03d-182">JetStopService</span><span class="sxs-lookup"><span data-stu-id="ae03d-182">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="ae03d-183">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="ae03d-183">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
