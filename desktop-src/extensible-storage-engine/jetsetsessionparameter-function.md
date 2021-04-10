---
description: 'En savoir plus sur : fonction JetSetSessionParameter'
title: JetSetSessionParameter fonction)
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951041"
---
# <a name="jetsetsessionparameter-function"></a><span data-ttu-id="16e60-103">JetSetSessionParameter fonction)</span><span class="sxs-lookup"><span data-stu-id="16e60-103">JetSetSessionParameter Function</span></span>


<span data-ttu-id="16e60-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="16e60-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="16e60-105">La fonction **JetSetSessionParameter** configure le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="16e60-105">The **JetSetSessionParameter** function configures the database engine.</span></span>

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a><span data-ttu-id="16e60-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16e60-106">Parameters</span></span>

<span data-ttu-id="16e60-107">*sesid*</span><span class="sxs-lookup"><span data-stu-id="16e60-107">*sesid*</span></span>

<span data-ttu-id="16e60-108">Spécifie la session à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="16e60-108">Specifies the session to use for this call.</span></span>

<span data-ttu-id="16e60-109">Lorsqu’il est spécifié, l’instance spécifiée est ignorée et l’instance associée à la session est utilisée.</span><span class="sxs-lookup"><span data-stu-id="16e60-109">When specified, the specified instance is ignored and the instance associated with the session will be used.</span></span>

<span data-ttu-id="16e60-110">*sesparamid*</span><span class="sxs-lookup"><span data-stu-id="16e60-110">*sesparamid*</span></span>

<span data-ttu-id="16e60-111">ID du paramètre de session à définir.</span><span class="sxs-lookup"><span data-stu-id="16e60-111">The ID of the session parameter to set.</span></span>

<span data-ttu-id="16e60-112">*pvParam*</span><span class="sxs-lookup"><span data-stu-id="16e60-112">*pvParam*</span></span>

<span data-ttu-id="16e60-113">Données à définir dans ce paramètre de session.</span><span class="sxs-lookup"><span data-stu-id="16e60-113">The data to set in this session parameter.</span></span>

<span data-ttu-id="16e60-114">*cbParam*</span><span class="sxs-lookup"><span data-stu-id="16e60-114">*cbParam*</span></span>

<span data-ttu-id="16e60-115">Taille des données fournies.</span><span class="sxs-lookup"><span data-stu-id="16e60-115">The size of the data provided.</span></span>

### <a name="return-value"></a><span data-ttu-id="16e60-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16e60-116">Return value</span></span>

<span data-ttu-id="16e60-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="16e60-117">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="16e60-118">Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="16e60-118">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16e60-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="16e60-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="16e60-120">Description</span><span class="sxs-lookup"><span data-stu-id="16e60-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16e60-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="16e60-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="16e60-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="16e60-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16e60-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="16e60-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="16e60-124">L’instance a été initialisée à l’aide d’un appel à la fonction <a href="gg294068(v=exchg.10).md">JetInit</a> et cette opération ne peut pas être exécutée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="16e60-124">The instance has been initialized by using a call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function and this operation cannot be performed as a result.</span></span> <span data-ttu-id="16e60-125">Cela peut se produire lorsqu’une tentative est effectuée pour configurer un paramètre système après qu’une modification de la valeur de paramètre ne peut plus affecter l’état du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="16e60-125">This can happen when an attempt is made to configure a system parameter after a change in the parameter value can no longer affect the state of the database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16e60-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="16e60-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="16e60-127">Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="16e60-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16e60-128">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="16e60-128">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="16e60-129">Les paramètres d’index de tuple spécifiés ne sont pas conformes.</span><span class="sxs-lookup"><span data-stu-id="16e60-129">The specified tuple index parameters were illegal.</span></span> <span data-ttu-id="16e60-130">Cette erreur est retournée uniquement lorsque le paramètre <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>ou <em>JET_paramIndexTuplesToIndexMax</em> est défini sur une valeur non conforme.</span><span class="sxs-lookup"><span data-stu-id="16e60-130">This error is returned only when the <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>, or <em>JET_paramIndexTuplesToIndexMax</em> parameter is set to an illegal value.</span></span> <span data-ttu-id="16e60-131">Pour plus d’informations sur ces paramètres, consultez <a href="gg294119(v=exchg.10).md">paramètres d’index</a>.</span><span class="sxs-lookup"><span data-stu-id="16e60-131">For information about these parameters, see <a href="gg294119(v=exchg.10).md">Index Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16e60-132">JET_errInitInProgress</span><span class="sxs-lookup"><span data-stu-id="16e60-132">JET_errInitInProgress</span></span></p></td>
<td><p><span data-ttu-id="16e60-133">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="16e60-133">It is not possible to complete the operation because the instance associated with the session is being initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16e60-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="16e60-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="16e60-135">Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</span><span class="sxs-lookup"><span data-stu-id="16e60-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16e60-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="16e60-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="16e60-137">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="16e60-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="16e60-138">Cela peut se produire dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="16e60-138">This can happen when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="16e60-139">L’ID de paramètre système spécifié n’est pas valide ou n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="16e60-139">The specified system parameter ID is invalid or unsupported.</span></span></p></li>
<li><p><span data-ttu-id="16e60-140">Une tentative de définition d’un paramètre système à valeur de chaîne avec une chaîne dont la longueur était en dehors de la plage autorisée pour le paramètre a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="16e60-140">An attempt was made to set a string-valued system parameter with a string the length of which was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="16e60-141">Une tentative a été effectuée pour définir un paramètre système à valeur de chaîne avec un chemin d’accès de fichier où la longueur de sa représentation de chemin d’accès absolu était en dehors de la plage autorisée pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="16e60-141">An attempt was made to set a string-valued system parameter with a file path where the length of its absolute path representation was outside the legal range for that parameter.</span></span></p></li>
<li><p><span data-ttu-id="16e60-142">Une tentative a été effectuée pour définir un paramètre système de valeur entière avec un entier qui se trouvait en dehors de la plage autorisée pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="16e60-142">An attempt was made to set an integer-valued system parameter with an integer that was outside the legal range for the parameter.</span></span></p></li>
<li><p><span data-ttu-id="16e60-143">Une tentative a été effectuée pour définir JET_paramUnicodeIndexDefault avec un pointeur de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> null, un LCID non valide ou un jeu d’indicateurs <strong>LCMapString</strong> non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="16e60-143">An attempt was made to set JET_paramUnicodeIndexDefault with a null <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> pointer, an invalid LCID, or an unsupported set of <strong>LCMapString</strong> flags.</span></span></p></li>
<li><p><span data-ttu-id="16e60-144">Impossible de définir le paramètre système spécifié, car il est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="16e60-144">The specified system parameter cannot be set because it is read-only.</span></span></p></li>
<li><p><span data-ttu-id="16e60-145">Une tentative de définition d’un paramètre système a été effectuée après l’appel de la fonction <a href="gg294068(v=exchg.10).md">JetInit</a> , le moteur de base de données est en mode d’instance unique et aucune session n’a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="16e60-145">An attempt was made to set a system parameter after the <a href="gg294068(v=exchg.10).md">JetInit</a> function was called, the database engine is in single-instance mode, and a session was not specified.</span></span></p></li>
<li><p><span data-ttu-id="16e60-146">Le paramètre système spécifié est global uniquement et une tentative a été effectuée pour définir une valeur spécifique à l’instance pour ce paramètre système.</span><span class="sxs-lookup"><span data-stu-id="16e60-146">The specified system parameter is global only and an attempt was made to set an instance-specific value for that system parameter.</span></span></p></li>
<li><p><span data-ttu-id="16e60-147">Le paramètre système spécifié est par instance uniquement et une tentative de définition de la valeur globale pour ce paramètre système a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="16e60-147">The specified system parameter is per-instance only and an attempt was made to set the global value for that system parameter.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16e60-148">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="16e60-148">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="16e60-149">Le chemin d’accès au système de fichiers spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="16e60-149">The specified file system path was invalid.</span></span> <span data-ttu-id="16e60-150">Cette erreur peut être retournée par <strong>JetSetSessionParameter</strong> uniquement lors de la définition des paramètres système qui représentent les chemins d’accès du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="16e60-150">This error may be returned by <strong>JetSetSessionParameter</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="16e60-151">Par exemple, le paramètre <em>JET_paramSystemPath</em> peut retourner cette erreur.</span><span class="sxs-lookup"><span data-stu-id="16e60-151">For example, the <em>JET_paramSystemPath</em> parameter may return this error.</span></span> <span data-ttu-id="16e60-152">Pour plus d’informations sur ce paramètre, consultez <a href="gg269235(v=exchg.10).md">paramètres du journal des transactions</a>.</span><span class="sxs-lookup"><span data-stu-id="16e60-152">For information about this parameter, see <a href="gg269235(v=exchg.10).md">Transaction Log Parameters</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16e60-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="16e60-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="16e60-154">Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="16e60-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16e60-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="16e60-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="16e60-156">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</span><span class="sxs-lookup"><span data-stu-id="16e60-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16e60-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="16e60-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="16e60-158">Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="16e60-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16e60-159">JET_errInvalidSesid</span><span class="sxs-lookup"><span data-stu-id="16e60-159">JET_errInvalidSesid</span></span></p></td>
<td><p><span data-ttu-id="16e60-160">Le descripteur de session n’est pas valide ou fait référence à une session fermée.</span><span class="sxs-lookup"><span data-stu-id="16e60-160">The session handle is invalid or refers to a closed session.</span></span></p>
<p><span data-ttu-id="16e60-161">Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="16e60-161">This error is not returned under all circumstances.</span></span> <span data-ttu-id="16e60-162">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="16e60-162">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16e60-163">JET_errInvalidInstance</span><span class="sxs-lookup"><span data-stu-id="16e60-163">JET_errInvalidInstance</span></span></p></td>
<td><p><span data-ttu-id="16e60-164">Le descripteur d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="16e60-164">The instance handle is invalid or refers to an instance that has been shut down.</span></span></p>
<p><span data-ttu-id="16e60-165">Cette erreur n’est pas retournée dans toutes les circonstances.</span><span class="sxs-lookup"><span data-stu-id="16e60-165">This error is not returned under all circumstances.</span></span> <span data-ttu-id="16e60-166">Les handles ne sont validés qu’à titre d’effort optimal.</span><span class="sxs-lookup"><span data-stu-id="16e60-166">Handles are validated on a best effort basis only.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16e60-167">En cas de réussite, le paramètre système est défini sur la valeur fournie.</span><span class="sxs-lookup"><span data-stu-id="16e60-167">On success, the system parameter will be set to the provided value.</span></span>

<span data-ttu-id="16e60-168">En cas d’échec, la valeur du paramètre système reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="16e60-168">On failure, the system parameter value will remain unchanged.</span></span>

#### <a name="requirements"></a><span data-ttu-id="16e60-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16e60-169">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16e60-170"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="16e60-170"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="16e60-171">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="16e60-171">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16e60-172"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="16e60-172"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="16e60-173">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="16e60-173">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16e60-174"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="16e60-174"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="16e60-175">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="16e60-175">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16e60-176"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="16e60-176"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="16e60-177">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="16e60-177">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16e60-178"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="16e60-178"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="16e60-179">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="16e60-179">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="16e60-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16e60-180">See also</span></span>

[<span data-ttu-id="16e60-181">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="16e60-181">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="16e60-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="16e60-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="16e60-183">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="16e60-183">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="16e60-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="16e60-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="16e60-185">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="16e60-185">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="16e60-186">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="16e60-186">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="16e60-187">JetInit</span><span class="sxs-lookup"><span data-stu-id="16e60-187">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="16e60-188">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="16e60-188">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
