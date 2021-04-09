---
description: 'En savoir plus sur : fonction JetDupSession'
title: JetDupSession fonction)
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aa320c329032f5867f5f762351277cc4567baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867553"
---
# <a name="jetdupsession-function"></a><span data-ttu-id="f8e5a-103">JetDupSession fonction)</span><span class="sxs-lookup"><span data-stu-id="f8e5a-103">JetDupSession Function</span></span>


<span data-ttu-id="f8e5a-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f8e5a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupsession-function"></a><span data-ttu-id="f8e5a-105">JetDupSession fonction)</span><span class="sxs-lookup"><span data-stu-id="f8e5a-105">JetDupSession Function</span></span>

<span data-ttu-id="f8e5a-106">La fonction **JetDupSession** démarre une session, puis initialise et retourne un handle de session ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="f8e5a-106">The **JetDupSession** function starts a session, and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="f8e5a-107">Les sessions contrôlent tous les accès à la base de données et sont utilisées pour contrôler l’étendue des transactions.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="f8e5a-108">La session peut être utilisée pour commencer, valider ou abandonner des transactions.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="f8e5a-109">La session est également utilisée pour attacher, créer ou ouvrir une base de données.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="f8e5a-110">La session est utilisée comme contexte pour toutes les opérations DDL et DML.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="f8e5a-111">Pour augmenter l’accès concurrentiel et l’accès parallèle à la base de données, plusieurs sessions peuvent être démarrées.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

<span data-ttu-id="f8e5a-112">**Remarque** Cette API agira de la même manière qu’un [JetBeginSession](./jetbeginsession-function.md) appelé sur l’instance de la session passée.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-112">**Note** This API will act in all ways as a [JetBeginSession](./jetbeginsession-function.md) called on the instance of the session passed in.</span></span> <span data-ttu-id="f8e5a-113">Cette fonction n’est pas recommandée, [JetBeginSession](./jetbeginsession-function.md) est préféré.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-113">This function is not recommended, [JetBeginSession](./jetbeginsession-function.md) is preferred.</span></span>

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a><span data-ttu-id="f8e5a-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8e5a-114">Parameters</span></span>

<span data-ttu-id="f8e5a-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f8e5a-115">*sesid*</span></span>

<span data-ttu-id="f8e5a-116">Session à utiliser comme source pour la duplication ou le début de la session.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-116">The session to use as the source for duplicating or beginning the session.</span></span>

<span data-ttu-id="f8e5a-117">*psesid*</span><span class="sxs-lookup"><span data-stu-id="f8e5a-117">*psesid*</span></span>

<span data-ttu-id="f8e5a-118">Pointeur vers la variable que le handle de session Initialise lors d’un retour réussi.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-118">A pointer to the variable that the session handle initializes on successful return.</span></span>

### <a name="return-value"></a><span data-ttu-id="f8e5a-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8e5a-119">Return Value</span></span>

<span data-ttu-id="f8e5a-120">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f8e5a-121">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f8e5a-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8e5a-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f8e5a-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="f8e5a-123">Description</span><span class="sxs-lookup"><span data-stu-id="f8e5a-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8e5a-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f8e5a-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-125">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e5a-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f8e5a-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-127">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e5a-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f8e5a-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-129">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="f8e5a-130">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e5a-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f8e5a-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-132">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e5a-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f8e5a-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-134">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e5a-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f8e5a-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-136">L’opération a échoué car la mémoire n’a pas pu être allouée.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-136">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e5a-137">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="f8e5a-137">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-138">Le nombre de sessions que le moteur autorise le client à démarrer est limité.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-138">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="f8e5a-139">Cette valeur peut être modifiée à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> avec la constante <em>JET_paramMaxSessions</em> .</span><span class="sxs-lookup"><span data-stu-id="f8e5a-139">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the <em>JET_paramMaxSessions</em> constant.</span></span> <span data-ttu-id="f8e5a-140">Le nombre de sessions par défaut est 16.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-140">The default number of sessions is 16.</span></span> <span data-ttu-id="f8e5a-141">Pour plus d’informations sur la <em>JET_paramMaxSessions</em>, consultez <a href="gg294139(v=exchg.10).md">paramètres système</a> .</span><span class="sxs-lookup"><span data-stu-id="f8e5a-141">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about <em>JET_paramMaxSessions</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e5a-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f8e5a-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-143">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e5a-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f8e5a-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f8e5a-145">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f8e5a-146">En cas de réussite, le descripteur de session est initialisé et peut être utilisé pour les opérations de base de données.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-146">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="f8e5a-147">En cas d’échec, aucune session n’est disponible ou une nouvelle session n’a pas pu être initialisée.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-147">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f8e5a-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8e5a-148">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8e5a-149"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f8e5a-149"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e5a-150">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-150">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e5a-151"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f8e5a-151"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e5a-152">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-152">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e5a-153"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f8e5a-153"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e5a-154">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-154">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8e5a-155"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f8e5a-155"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e5a-156">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-156">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8e5a-157"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f8e5a-157"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f8e5a-158">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f8e5a-158">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f8e5a-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8e5a-159">See Also</span></span>

[<span data-ttu-id="f8e5a-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f8e5a-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f8e5a-161">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="f8e5a-161">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="f8e5a-162">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="f8e5a-162">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="f8e5a-163">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f8e5a-163">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="f8e5a-164">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="f8e5a-164">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
