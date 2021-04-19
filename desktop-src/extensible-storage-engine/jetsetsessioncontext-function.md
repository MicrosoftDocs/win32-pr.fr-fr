---
description: 'En savoir plus sur : fonction JetSetSessionContext'
title: JetSetSessionContext fonction)
TOCTitle: JetSetSessionContext Function
ms:assetid: e44efadf-a5c7-408a-ad68-56646b6ea650
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294124(v=EXCHG.10)
ms:contentKeyID: 32765738
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4aafafa17499b76282599586f7477ac1ef6f878d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514208"
---
# <a name="jetsetsessioncontext-function"></a><span data-ttu-id="98455-103">JetSetSessionContext fonction)</span><span class="sxs-lookup"><span data-stu-id="98455-103">JetSetSessionContext Function</span></span>


<span data-ttu-id="98455-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="98455-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetsessioncontext-function"></a><span data-ttu-id="98455-105">JetSetSessionContext fonction)</span><span class="sxs-lookup"><span data-stu-id="98455-105">JetSetSessionContext Function</span></span>

<span data-ttu-id="98455-106">La fonction **JetSetSessionContext** associe une session au thread actuel à l’aide du handle de contexte donné.</span><span class="sxs-lookup"><span data-stu-id="98455-106">The **JetSetSessionContext** function associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="98455-107">Cette association remplace la spécification de moteur par défaut selon laquelle une transaction pour une session donnée doit se produire entièrement sur le même thread.</span><span class="sxs-lookup"><span data-stu-id="98455-107">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span>

```cpp
    JET_ERR JET_API JetSetSessionContext(
      __in          JET_SESID sesid,
      __in          JET_API_PTR ulContext
    );
```

### <a name="parameters"></a><span data-ttu-id="98455-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98455-108">Parameters</span></span>

<span data-ttu-id="98455-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="98455-109">*sesid*</span></span>

<span data-ttu-id="98455-110">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="98455-110">The session to use for this call.</span></span>

<span data-ttu-id="98455-111">*ulContext*</span><span class="sxs-lookup"><span data-stu-id="98455-111">*ulContext*</span></span>

<span data-ttu-id="98455-112">Identificateur unique auquel cette session sera associée.</span><span class="sxs-lookup"><span data-stu-id="98455-112">A unique identifier to which this session will be associated.</span></span>

### <a name="return-value"></a><span data-ttu-id="98455-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98455-113">Return Value</span></span>

<span data-ttu-id="98455-114">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="98455-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="98455-115">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="98455-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98455-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="98455-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="98455-117">Description</span><span class="sxs-lookup"><span data-stu-id="98455-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98455-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="98455-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="98455-119">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="98455-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98455-120">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="98455-120">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="98455-121">Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="98455-121">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98455-122">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="98455-122">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="98455-123">Impossible d’effectuer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="98455-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="98455-124"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98455-124"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98455-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="98455-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="98455-126">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs valeurs de paramètre a produit un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="98455-126">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="98455-127">Cette erreur est retournée par <strong>JetSetSessionContext</strong> dans les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="98455-127">This error will be returned by <strong>JetSetSessionContext</strong> under the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="98455-128"><em>ulContext</em> a la valeur null</span><span class="sxs-lookup"><span data-stu-id="98455-128"><em>ulContext</em> is NULL</span></span></p></li>
<li><p><span data-ttu-id="98455-129"><em>ulContext</em> est-1</span><span class="sxs-lookup"><span data-stu-id="98455-129"><em>ulContext</em> is -1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98455-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="98455-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="98455-131">Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="98455-131">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98455-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="98455-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="98455-133">Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="98455-133">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98455-134">JET_errSessionContextAlreadySet</span><span class="sxs-lookup"><span data-stu-id="98455-134">JET_errSessionContextAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="98455-135">La session n’a pas pu être associée au thread actuel, car elle a déjà été associée à un thread.</span><span class="sxs-lookup"><span data-stu-id="98455-135">The session could not be associated with the current thread because it has already been associated with a thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98455-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="98455-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="98455-137">L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="98455-137">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="98455-138">Si cette fonction est établie, la session est associée au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="98455-138">If this function succeeds, the session will be associated with the current thread.</span></span> <span data-ttu-id="98455-139">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="98455-139">No change to the database state will occur.</span></span>

<span data-ttu-id="98455-140">Si cette fonction échoue, l’état de la session reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="98455-140">If this function fails, the session state will remain unchanged.</span></span> <span data-ttu-id="98455-141">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="98455-141">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="98455-142">Notes</span><span class="sxs-lookup"><span data-stu-id="98455-142">Remarks</span></span>

<span data-ttu-id="98455-143">Une session est généralement liée à un thread spécifique pour la durée d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="98455-143">A session is usually bound to a specific thread for the duration of a transaction.</span></span> <span data-ttu-id="98455-144">Ce comportement est conçu pour aider les applications à détecter et empêcher le partage conceptuel d’une seule session entre plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="98455-144">This behavior is designed to help applications detect and prevent the conceptually ill-advised sharing of a single session amongst multiple threads.</span></span> <span data-ttu-id="98455-145">Parfois, cette vérification simple ne fonctionne pas avec l’architecture de l’application.</span><span class="sxs-lookup"><span data-stu-id="98455-145">Sometimes, this simple check does not work with the application's architecture.</span></span> <span data-ttu-id="98455-146">Par exemple, si l’application héberge des objets côté serveur à l’aide d’un pool de threads et que les transactions s’étendent sur plusieurs appels serveur à un objet donné, cette protection peut entraîner l’échec de certains de ces appels avec JET_errSessionSharingViolation même si le modèle d’utilisation est correct.</span><span class="sxs-lookup"><span data-stu-id="98455-146">For example, if the application is hosting server-side objects using a thread pool and transactions span multiple server calls to a given object then this protection may cause some of those calls to fail with JET_errSessionSharingViolation even though the usage pattern is correct.</span></span> <span data-ttu-id="98455-147">Cette situation est courante pour les serveurs d’objets COM.</span><span class="sxs-lookup"><span data-stu-id="98455-147">This situation is common for COM object servers.</span></span>

<span data-ttu-id="98455-148">**JetSetSessionContext** et [JetResetSessionContext](./jetresetsessioncontext-function.md) résolvent ce problème en rendant ce partage de session un peu plus flexible.</span><span class="sxs-lookup"><span data-stu-id="98455-148">**JetSetSessionContext** and [JetResetSessionContext](./jetresetsessioncontext-function.md) solve this problem by making this session sharing check a little more flexible.</span></span> <span data-ttu-id="98455-149">Lorsque l’application commence à effectuer une série d’appels d’API ESE à l’aide d’une session particulière, elle définit tout d’abord le contexte de session sur une valeur donnée.</span><span class="sxs-lookup"><span data-stu-id="98455-149">When the application starts to make a series of ESE API calls using a particular session, it first sets the session context to a given value.</span></span> <span data-ttu-id="98455-150">Cette action associe la session au thread appelant.</span><span class="sxs-lookup"><span data-stu-id="98455-150">This action associates the session to the calling thread.</span></span> <span data-ttu-id="98455-151">Dans l’exemple donné, ce contexte peut être l’adresse de l’objet qui contient le handle de session JET.</span><span class="sxs-lookup"><span data-stu-id="98455-151">In the given example, this context could be the address of the object that contains the JET session handle.</span></span> <span data-ttu-id="98455-152">Une fois les appels de l’API ESE effectués, l’application réinitialise le contexte de session.</span><span class="sxs-lookup"><span data-stu-id="98455-152">Once the ESE API calls have been made, the application resets the session context.</span></span> <span data-ttu-id="98455-153">Cette action dissocie la session du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="98455-153">This action disassociates the session from the calling thread.</span></span> <span data-ttu-id="98455-154">L’objet et sa session peuvent ensuite être utilisés par un autre thread, même si la session a une transaction active.</span><span class="sxs-lookup"><span data-stu-id="98455-154">The object and its session can then be used by another thread even if the session has an active transaction.</span></span>

<span data-ttu-id="98455-155">Il est important de noter que **JetSetSessionContext** doit être appelé avant l’ouverture d’une transaction sur cette session ou que l’Association ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="98455-155">It is important to note that **JetSetSessionContext** must be called prior to opening a transaction on that session or the association will not work.</span></span>

<span data-ttu-id="98455-156">**JetSetSessionContext** est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="98455-156">**JetSetSessionContext** is thread safe.</span></span> <span data-ttu-id="98455-157">Plusieurs threads peuvent tenter de définir un contexte de thread sur la même session en même temps et un seul sera gagnant.</span><span class="sxs-lookup"><span data-stu-id="98455-157">Multiple threads can try to set a thread context on the same session at the same time and only one will win.</span></span> <span data-ttu-id="98455-158">Ce fait peut être utilisé par l’application comme un moyen d’allouer une session à partir d’un pool sans stocker l’état externe sur son allocation.</span><span class="sxs-lookup"><span data-stu-id="98455-158">This fact can be used by the application as a means to allocate a session from a pool without storing external state about its allocation.</span></span>

#### <a name="requirements"></a><span data-ttu-id="98455-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98455-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98455-160"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="98455-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="98455-161">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="98455-161">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98455-162"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="98455-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="98455-163">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="98455-163">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98455-164"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="98455-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="98455-165">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="98455-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98455-166"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="98455-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="98455-167">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="98455-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98455-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="98455-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="98455-169">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="98455-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="98455-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98455-170">See Also</span></span>

[<span data-ttu-id="98455-171">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="98455-171">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="98455-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="98455-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="98455-173">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="98455-173">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="98455-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="98455-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="98455-175">JetStopService</span><span class="sxs-lookup"><span data-stu-id="98455-175">JetStopService</span></span>](./jetstopservice-function.md)
