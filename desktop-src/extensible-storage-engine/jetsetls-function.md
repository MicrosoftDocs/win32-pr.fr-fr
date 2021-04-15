---
description: 'En savoir plus sur : fonction JetSetLS'
title: Fonction JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525557"
---
# <a name="jetsetls-function"></a><span data-ttu-id="a4782-103">Fonction JetSetLS</span><span class="sxs-lookup"><span data-stu-id="a4782-103">JetSetLS Function</span></span>


<span data-ttu-id="a4782-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="a4782-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetls-function"></a><span data-ttu-id="a4782-105">Fonction JetSetLS</span><span class="sxs-lookup"><span data-stu-id="a4782-105">JetSetLS Function</span></span>

<span data-ttu-id="a4782-106">La fonction **JetSetLS** permet à l’application d’associer un handle de contexte appelé stockage local avec un curseur ou la table associée à ce curseur.</span><span class="sxs-lookup"><span data-stu-id="a4782-106">The **JetSetLS** function enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="a4782-107">Ce descripteur de contexte peut être utilisé par l’application pour stocker les données auxiliaires associées à un curseur ou une table.</span><span class="sxs-lookup"><span data-stu-id="a4782-107">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="a4782-108">L’application est notifiée ultérieurement à l’aide d’un rappel d’exécution lorsque le handle de contexte doit être libéré.</span><span class="sxs-lookup"><span data-stu-id="a4782-108">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="a4782-109">Cela permet d’associer l’État alloué dynamiquement à un curseur ou une table.</span><span class="sxs-lookup"><span data-stu-id="a4782-109">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="a4782-110">**Windows XP :**  **JetSetLS** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a4782-110">**Windows XP:**  **JetSetLS** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a4782-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4782-111">Parameters</span></span>

<span data-ttu-id="a4782-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a4782-112">*sesid*</span></span>

<span data-ttu-id="a4782-113">Session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="a4782-113">The session to use for this call.</span></span>

<span data-ttu-id="a4782-114">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a4782-114">*tableid*</span></span>

<span data-ttu-id="a4782-115">Curseur à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="a4782-115">The cursor to use for this call.</span></span>

<span data-ttu-id="a4782-116">*ls*</span><span class="sxs-lookup"><span data-stu-id="a4782-116">*ls*</span></span>

<span data-ttu-id="a4782-117">Handle de contexte à associer au curseur ou à la table.</span><span class="sxs-lookup"><span data-stu-id="a4782-117">The context handle to be associated with the cursor or table.</span></span>

<span data-ttu-id="a4782-118">Lorsque JET_bitLSReset est spécifié, la valeur réelle de ce paramètre est ignorée et JET_LSNil est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a4782-118">When JET_bitLSReset is specified then the actual value of this parameter is ignored and JET_LSNil is used.</span></span>

<span data-ttu-id="a4782-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a4782-119">*grbit*</span></span>

<span data-ttu-id="a4782-120">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="a4782-120">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4782-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4782-121">Value</span></span></p></th>
<th><p><span data-ttu-id="a4782-122">Signification</span><span class="sxs-lookup"><span data-stu-id="a4782-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4782-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="a4782-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="a4782-124">Cette option indique que le handle de contexte doit être associé au curseur donné.</span><span class="sxs-lookup"><span data-stu-id="a4782-124">This option indicates that the context handle should be associated with the given cursor.</span></span></p>
<p><span data-ttu-id="a4782-125">Si ni JET_bitLSCursor ni JET_bitLSTable n’est spécifié, JET_bitLSCursor est présumé.</span><span class="sxs-lookup"><span data-stu-id="a4782-125">If neither JET_bitLSCursor nor JET_bitLSTable is specified then JET_bitLSCursor is presumed.</span></span></p>
<p><span data-ttu-id="a4782-126">L’utilisation de cette option avec JET_bitLSTable n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="a4782-126">It is illegal to use this option with JET_bitLSTable.</span></span> <span data-ttu-id="a4782-127">L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</span><span class="sxs-lookup"><span data-stu-id="a4782-127">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4782-128">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="a4782-128">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="a4782-129">Cette option indique que le handle de contexte spécifié doit être ignoré et que le handle de contexte pour l’objet choisi doit être réinitialisé à JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="a4782-129">This option indicates that the specified context handle should be ignored and that the context handle for the chosen object should be reset to JET_LSNil.</span></span></p>
<p><span data-ttu-id="a4782-130">Il est important de noter que cette action n’entraîne pas de rappel pour nettoyer la valeur précédente du handle de contexte pour l’objet choisi.</span><span class="sxs-lookup"><span data-stu-id="a4782-130">It is important to note that this action will not result in a callback to cleanup the previous value of the context handle for the chosen object.</span></span> <span data-ttu-id="a4782-131">Le nettoyage approprié du descripteur de contexte précédent peut être effectué à l’aide de <a href="gg269234(v=exchg.10).md">JetGetLS</a> avec JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="a4782-131">Proper cleanup of the previous context handle can be achieved using <a href="gg269234(v=exchg.10).md">JetGetLS</a> with JET_bitLSReset.</span></span> <span data-ttu-id="a4782-132">Pour plus d’informations, consultez <a href="gg269234(v=exchg.10).md">JetGetLS</a> .</span><span class="sxs-lookup"><span data-stu-id="a4782-132">See <a href="gg269234(v=exchg.10).md">JetGetLS</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4782-133">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="a4782-133">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="a4782-134">Cette option indique que le descripteur de contexte doit être associé à la table associée au curseur donné.</span><span class="sxs-lookup"><span data-stu-id="a4782-134">This option indicates that the context handle should be associated with the table associated with the given cursor.</span></span></p>
<p><span data-ttu-id="a4782-135">L’utilisation de cette option avec JET_bitLSCursor n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="a4782-135">It is illegal to use this option with JET_bitLSCursor.</span></span> <span data-ttu-id="a4782-136">L’opération échouera avec JET_errInvalidgrbit si cette tentative est effectuée.</span><span class="sxs-lookup"><span data-stu-id="a4782-136">The operation will fail with JET_errInvalidgrbit if this is attempted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a4782-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a4782-137">Return Value</span></span>

<span data-ttu-id="a4782-138">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="a4782-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a4782-139">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a4782-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4782-140">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a4782-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="a4782-141">Description</span><span class="sxs-lookup"><span data-stu-id="a4782-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4782-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a4782-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a4782-143">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="a4782-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4782-144">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a4782-144">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a4782-145">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a4782-145">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4782-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="a4782-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="a4782-147">L’une des options demandées n’est pas valide, a été utilisée de manière incorrecte ou n’a pas été implémentée.</span><span class="sxs-lookup"><span data-stu-id="a4782-147">One of the options requested was invalid, used incorrectly, or not implemented.</span></span> <span data-ttu-id="a4782-148">Cela peut se produire pour <strong>JetSetLS</strong> quand JET_bitLSCursor et JET_bitLSTable sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a4782-148">This can happen for <strong>JetSetLS</strong> when JET_bitLSCursor and JET_bitLSTable are both specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4782-149">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a4782-149">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a4782-150">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="a4782-150">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a4782-151">Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a4782-151">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4782-152">JET_errLSAlreadySet</span><span class="sxs-lookup"><span data-stu-id="a4782-152">JET_errLSAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="a4782-153">Le handle de contexte indiqué n’a pas pu être associé à l’objet demandé, car un handle de contexte lui est déjà associé.</span><span class="sxs-lookup"><span data-stu-id="a4782-153">The given context handle could not be associated with the requested object because it already had a context handle associated with it.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4782-154">JET_errLSCallbackNotSpecified</span><span class="sxs-lookup"><span data-stu-id="a4782-154">JET_errLSCallbackNotSpecified</span></span></p></td>
<td><p><span data-ttu-id="a4782-155">Le handle de contexte indiqué n’a pas pu être associé à l’objet demandé, car le rappel d’exécution n’a pas été configuré pour l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="a4782-155">The given context handle could not be associated with the requested object because the runtime callback has not been configured for the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4782-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a4782-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a4782-157">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="a4782-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4782-158">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a4782-158">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a4782-159">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="a4782-159">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4782-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a4782-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a4782-161">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a4782-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a4782-162">En cas de réussite, le handle de contexte donné a été associé avec succès à l’objet demandé.</span><span class="sxs-lookup"><span data-stu-id="a4782-162">On success, the given context handle was successfully associated with the requested object.</span></span> <span data-ttu-id="a4782-163">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a4782-163">No change to the database state will occur.</span></span>

<span data-ttu-id="a4782-164">En cas d’échec, aucune modification de l’état de l’objet demandé n’est survenue.</span><span class="sxs-lookup"><span data-stu-id="a4782-164">On failure, no change to the state of the requested object has occurred.</span></span> <span data-ttu-id="a4782-165">Aucune modification de l’état de la base de données ne se produit.</span><span class="sxs-lookup"><span data-stu-id="a4782-165">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a4782-166">Notes</span><span class="sxs-lookup"><span data-stu-id="a4782-166">Remarks</span></span>

<span data-ttu-id="a4782-167">Le stockage local d’un curseur ou d’une table doit être affiché en tant que cache volatile.</span><span class="sxs-lookup"><span data-stu-id="a4782-167">The Local Storage for a cursor or table should be viewed as a volatile cache.</span></span> <span data-ttu-id="a4782-168">L’application doit d’abord essayer de récupérer le handle de contexte à l’aide de [JetGetLS](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="a4782-168">The application should first try to retrieve the context handle using [JetGetLS](./jetgetls-function.md).</span></span> <span data-ttu-id="a4782-169">Si la valeur n’est pas définie (JET_LSNil), l’application doit créer un nouveau contexte et la charger dans le cache à l’aide de **JetSetLS**.</span><span class="sxs-lookup"><span data-stu-id="a4782-169">If the value is not set (that is it is JET_LSNil) then the application should create a new context and load it into the cache using **JetSetLS**.</span></span> <span data-ttu-id="a4782-170">L’application peut purger le cache à l’aide d’un appel à [JetGetLS](./jetgetls-function.md) avec JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="a4782-170">The application can purge the cache using a call to [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="a4782-171">Si le moteur de base de données vide le cache, un rappel d’exécution sera généré pour permettre à l’application de nettoyer ce contexte.</span><span class="sxs-lookup"><span data-stu-id="a4782-171">If the database engine purges the cache then a runtime callback will be generated to give the application a chance to cleanup that context.</span></span> <span data-ttu-id="a4782-172">Le type de rappel sera JET_cbtypFreeCursorLS pour un handle de contexte associé à un curseur et JET_cbtypFreeTableLS pour un handle de contexte associé à une table.</span><span class="sxs-lookup"><span data-stu-id="a4782-172">The callback type will be JET_cbtypFreeCursorLS for a context handle associated with a cursor and JET_cbtypFreeTableLS for a context handle associated with a table.</span></span> <span data-ttu-id="a4782-173">Dans les deux cas, le handle de contexte est passé en tant que pvArg1.</span><span class="sxs-lookup"><span data-stu-id="a4782-173">In either case, the context handle will be passed as pvArg1.</span></span> <span data-ttu-id="a4782-174">Pour plus d’informations, consultez [JET_CALLBACK](./jet-callback-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a4782-174">See [JET_CALLBACK](./jet-callback-callback-function.md) for more information.</span></span>

<span data-ttu-id="a4782-175">Le rappel d’exécution doit être configuré correctement pour l’instance associée à la session donnée avant que le stockage local puisse être utilisé.</span><span class="sxs-lookup"><span data-stu-id="a4782-175">The runtime callback must be properly configured for the instance associated with the given session before Local Storage can be used.</span></span> <span data-ttu-id="a4782-176">Ce rappel peut être défini à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramRuntimeCallback](./callback-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a4782-176">This callback can be set using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramRuntimeCallback](./callback-parameters.md).</span></span> <span data-ttu-id="a4782-177">Pour plus d’informations, consultez [JetSetSystemParameter](./jetsetsystemparameter-function.md) et [JET_paramRuntimeCallback](./callback-parameters.md) dans paramètres système.</span><span class="sxs-lookup"><span data-stu-id="a4782-177">See [JetSetSystemParameter](./jetsetsystemparameter-function.md) and [JET_paramRuntimeCallback](./callback-parameters.md) in System Parameters for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a4782-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4782-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4782-179"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="a4782-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a4782-180">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a4782-180">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4782-181"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="a4782-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a4782-182">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a4782-182">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4782-183"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="a4782-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a4782-184">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="a4782-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4782-185"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="a4782-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a4782-186">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a4782-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4782-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a4782-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a4782-188">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a4782-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a4782-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4782-189">See Also</span></span>

[<span data-ttu-id="a4782-190">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="a4782-190">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="a4782-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a4782-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a4782-192">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a4782-192">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a4782-193">JET_LS</span><span class="sxs-lookup"><span data-stu-id="a4782-193">JET_LS</span></span>](./jet-ls.md)  
[<span data-ttu-id="a4782-194">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a4782-194">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a4782-195">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a4782-195">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a4782-196">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="a4782-196">JetGetLS</span></span>](./jetgetls-function.md)  
[<span data-ttu-id="a4782-197">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a4782-197">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a4782-198">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="a4782-198">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
