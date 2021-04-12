---
description: 'En savoir plus sur : fonction JetBeginTransaction'
title: Fonction JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318042"
---
# <a name="jetbegintransaction-function"></a><span data-ttu-id="e361b-103">Fonction JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="e361b-103">JetBeginTransaction Function</span></span>


<span data-ttu-id="e361b-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="e361b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction-function"></a><span data-ttu-id="e361b-105">Fonction JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="e361b-105">JetBeginTransaction Function</span></span>

<span data-ttu-id="e361b-106">La fonction **JetBeginTransaction** oblige une session à entrer dans une transaction et à créer un nouveau point d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="e361b-106">The **JetBeginTransaction** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="e361b-107">Cette fonction peut être appelée plusieurs fois sur une seule session pour provoquer la création de points d’enregistrement supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e361b-107">This function can be called more than once on a single session to cause the creation of additional save points.</span></span> <span data-ttu-id="e361b-108">Ces points d’enregistrement peuvent être utilisés pour conserver ou ignorer de manière sélective les modifications apportées à l’état de la base de données.</span><span class="sxs-lookup"><span data-stu-id="e361b-108">These save points can be used to selectively keep or discard changes to the state of the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="e361b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e361b-109">Parameters</span></span>

<span data-ttu-id="e361b-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e361b-110">*sesid*</span></span>

<span data-ttu-id="e361b-111">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="e361b-111">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="e361b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e361b-112">Return Value</span></span>

<span data-ttu-id="e361b-113">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="e361b-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e361b-114">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e361b-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e361b-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e361b-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="e361b-116">Description</span><span class="sxs-lookup"><span data-stu-id="e361b-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e361b-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e361b-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e361b-118">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e361b-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e361b-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e361b-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e361b-120">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e361b-120">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e361b-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e361b-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e361b-122">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="e361b-122">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="e361b-123">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e361b-123">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e361b-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e361b-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e361b-125">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="e361b-125">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e361b-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e361b-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e361b-127">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="e361b-127">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e361b-128">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e361b-128">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e361b-129">La même session ne peut pas être utilisée simultanément pour plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="e361b-129">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="e361b-130">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e361b-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e361b-131">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e361b-131">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e361b-132">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e361b-132">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e361b-133">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="e361b-133">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="e361b-134">Une nouvelle transaction ne peut pas être démarrée, car la session est déjà à la profondeur de point d’enregistrement maximale autorisée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="e361b-134">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e361b-135">En cas de réussite, la session fournie se trouve à l’intérieur d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="e361b-135">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="e361b-136">Si la session était précédemment à l’intérieur d’une transaction, un nouveau point d’enregistrement sera créé.</span><span class="sxs-lookup"><span data-stu-id="e361b-136">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="e361b-137">En cas d’échec, l’état transactionnel de la session reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="e361b-137">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="e361b-138">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="e361b-138">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e361b-139">Notes</span><span class="sxs-lookup"><span data-stu-id="e361b-139">Remarks</span></span>

<span data-ttu-id="e361b-140">Le moteur de base de données fournit un modèle d’isolation d’instantané pour ses transactions.</span><span class="sxs-lookup"><span data-stu-id="e361b-140">The database engine provides a snapshot isolation model for its transactions.</span></span> <span data-ttu-id="e361b-141">Cela signifie que, lorsqu’une session entre pour la première fois dans un état transactionnel, la session voit l’intégralité de la base de données figée à l’heure au début de la transaction.</span><span class="sxs-lookup"><span data-stu-id="e361b-141">This means that, when a session first enters into a transactional state, the session will see the entire database frozen in time at the start of the transaction.</span></span> <span data-ttu-id="e361b-142">Une session n’a pas besoin de lire le verrou de données, car elle peut toujours accéder à la version appropriée de ces données.</span><span class="sxs-lookup"><span data-stu-id="e361b-142">A session does not need to read lock any data because it can always access the appropriate version of that data.</span></span> <span data-ttu-id="e361b-143">Cela signifie qu’une session qui met à jour des données ne bloquera jamais une autre session pour la lecture de ces données.</span><span class="sxs-lookup"><span data-stu-id="e361b-143">This means that a session that is updating data will never block a different session from reading that data.</span></span>

<span data-ttu-id="e361b-144">Une autre implication de l’utilisation de l’isolement d’instantané est le modèle de verrouillage utilisé pour les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="e361b-144">Another implication of the use of snapshot isolation is the locking model used for updates.</span></span> <span data-ttu-id="e361b-145">Le moteur de base de données récompense un verrou d’écriture sur un élément de données donné dans la première session qui le demande.</span><span class="sxs-lookup"><span data-stu-id="e361b-145">The database engine will award a write lock on a given piece of data to the first session that requests it.</span></span> <span data-ttu-id="e361b-146">Ce verrou d’écriture est libéré lorsque la transaction est validée ou abandonnée complètement, de sorte que la session n’est plus dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="e361b-146">This write lock is released when the transaction is either committed or aborted completely such that the session is no longer in a transaction.</span></span> <span data-ttu-id="e361b-147">Lorsqu’une session maintient un verrou en écriture, toute autre session qui demande le même verrou d’écriture n’est pas bloquée tant que le verrou d’écriture n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="e361b-147">While a session holds a write lock, any other session that requests the same write lock will not block until the write lock is available.</span></span> <span data-ttu-id="e361b-148">Au lieu de cela, cette deuxième session échouera immédiatement avec JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="e361b-148">Rather, that second session will immediately fail with JET_errWriteConflict.</span></span> <span data-ttu-id="e361b-149">Pour résoudre ce conflit, la deuxième session doit abandonner (ou valider) entièrement sa transaction, attendre une courte période de temps pour que la première session valide ou abandonne sa transaction, puis recommencer.</span><span class="sxs-lookup"><span data-stu-id="e361b-149">To resolve this conflict, the second session must abort (or commit) its transaction completely, wait some small period of time for the first session to commit or abort its transaction, and then start all over again.</span></span>

<span data-ttu-id="e361b-150">Pour la prise en charge de l’isolation d’instantané, le moteur de base de données stocke toutes les versions de toutes les données modifiées dans la mémoire depuis le premier démarrage de la transaction active la plus ancienne dans une session.</span><span class="sxs-lookup"><span data-stu-id="e361b-150">In support of snapshot isolation, the database engine stores all versions of all modified data in memory since the time when the oldest active transaction on any session was first started.</span></span> <span data-ttu-id="e361b-151">Cela a des implications importantes pour votre application.</span><span class="sxs-lookup"><span data-stu-id="e361b-151">This has important implications for your application.</span></span> <span data-ttu-id="e361b-152">Tout comportement qui provoque la génération d’un grand nombre de versions en mémoire peut provoquer l’épuisement de la taille maximale de la Banque de versions (voir [JET_paramMaxVerPages](./resource-parameters.md) dans [paramètres système](./extensible-storage-engine-system-parameters.md) pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="e361b-152">Any behavior that causes a large number of versions to build up in memory may cause the instance to exhaust its maximum version store size (see [JET_paramMaxVerPages](./resource-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md) for more information).</span></span> <span data-ttu-id="e361b-153">Ce comportement comprend, sans s’y limiter, les mises à jour très volumineuses dans une transaction unique et les transactions à long terme.</span><span class="sxs-lookup"><span data-stu-id="e361b-153">Such behavior includes, but is not limited to very large updates in a single transaction and very long running transactions.</span></span> <span data-ttu-id="e361b-154">Par conséquent, il est très important de configurer correctement la taille de la Banque des versions pour le chargement transactionnel attendu de l’application.</span><span class="sxs-lookup"><span data-stu-id="e361b-154">As a result, it is very important to properly configure the version store size for the expected transactional load of the application.</span></span> <span data-ttu-id="e361b-155">Il est également important de veiller à limiter le nombre de mises à jour effectuées dans une transaction unique.</span><span class="sxs-lookup"><span data-stu-id="e361b-155">It is also important to take great care to limit the number of updates performed in a single transaction.</span></span> <span data-ttu-id="e361b-156">En outre, il est important de rendre les transactions aussi courtes que possible dans des scénarios de charge élevée.</span><span class="sxs-lookup"><span data-stu-id="e361b-156">Furthermore, it is important to make transactions as short in duration as possible under high load scenarios.</span></span>

<span data-ttu-id="e361b-157">Il est fortement recommandé que l’application soit toujours dans le contexte d’une transaction lors de l’appel d’API ESE qui récupèrent ou mettent à jour des données.</span><span class="sxs-lookup"><span data-stu-id="e361b-157">It is highly recommended that the application always be in the context of a transaction when calling ESE APIs that retrieve or update data.</span></span> <span data-ttu-id="e361b-158">Si ce n’est pas le cas, le moteur de base de données encapsule automatiquement chaque appel d’API ESE de ce type dans une transaction au nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="e361b-158">If this is not done, the database engine will automatically wrap each ESE API call of this type in a transaction on behalf of the application.</span></span> <span data-ttu-id="e361b-159">Le coût de ces transactions très courtes peut s’ajouter rapidement dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="e361b-159">The cost of these very short transactions can add up quickly in some cases.</span></span>

<span data-ttu-id="e361b-160">Le comportement par défaut du moteur est de limiter l’utilisation d’une session au même thread à partir du moment où le premier appel à **JetBeginTransaction** est effectué jusqu’au moment où l’appel correspondant à [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) est effectué.</span><span class="sxs-lookup"><span data-stu-id="e361b-160">The default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to **JetBeginTransaction** is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="e361b-161">Ce comportement peut être modifié pour supprimer cette restriction en définissant un contexte de session personnalisé à l’aide de [JetSetSessionContext](./jetsetsessioncontext-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="e361b-161">This behavior can be changed to remove this restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

<span data-ttu-id="e361b-162">Le moteur de base de données prend également en charge les modifications de schéma transactionnel.</span><span class="sxs-lookup"><span data-stu-id="e361b-162">The database engine also supports transactional schema modifications.</span></span> <span data-ttu-id="e361b-163">Par exemple, il est possible de commencer une nouvelle transaction, de créer une table, d’ajouter quelques colonnes, de créer un ou deux index, puis d’abandonner la transaction.</span><span class="sxs-lookup"><span data-stu-id="e361b-163">For example, it is possible to begin a new transaction, create a table, add a few columns, create an index or two, and then abort the transaction.</span></span> <span data-ttu-id="e361b-164">Les éléments de schéma qui viennent d’être ajoutés seront supprimés de la base de données.</span><span class="sxs-lookup"><span data-stu-id="e361b-164">The schema elements that were just added will be removed from the database.</span></span> <span data-ttu-id="e361b-165">Il est également possible de mélanger des modifications de schéma et des mises à jour de base de données ordinaires dans la même transaction.</span><span class="sxs-lookup"><span data-stu-id="e361b-165">It is also possible to mix schema modifications and ordinary database updates in the same transaction.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e361b-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e361b-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e361b-167"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="e361b-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e361b-168">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="e361b-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e361b-169"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="e361b-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e361b-170">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e361b-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e361b-171"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="e361b-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e361b-172">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="e361b-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e361b-173"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="e361b-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e361b-174">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e361b-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e361b-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e361b-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e361b-176">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e361b-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e361b-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e361b-177">See Also</span></span>

[<span data-ttu-id="e361b-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e361b-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e361b-179">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e361b-179">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e361b-180">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e361b-180">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e361b-181">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="e361b-181">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="e361b-182">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="e361b-182">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="e361b-183">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="e361b-183">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="e361b-184">JetRollback</span><span class="sxs-lookup"><span data-stu-id="e361b-184">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="e361b-185">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="e361b-185">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="e361b-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e361b-186">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="e361b-187">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="e361b-187">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
