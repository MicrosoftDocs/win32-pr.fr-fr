---
description: 'En savoir plus sur : fonction JetTerm2'
title: Fonction JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113602"
---
# <a name="jetterm2-function"></a><span data-ttu-id="3d532-103">Fonction JetTerm2</span><span class="sxs-lookup"><span data-stu-id="3d532-103">JetTerm2 Function</span></span>


<span data-ttu-id="3d532-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="3d532-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm2-function"></a><span data-ttu-id="3d532-105">Fonction JetTerm2</span><span class="sxs-lookup"><span data-stu-id="3d532-105">JetTerm2 Function</span></span>

<span data-ttu-id="3d532-106">La fonction **JetTerm2** lance l’arrêt d’une instance qui a été initialisée par [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="3d532-106">The **JetTerm2** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="3d532-107">**JetTerm2** peut également détruire une instance non initialisée qui a été créée par [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="3d532-107">**JetTerm2** can also destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="3d532-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d532-108">Parameters</span></span>

<span data-ttu-id="3d532-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="3d532-109">*instance*</span></span>

<span data-ttu-id="3d532-110">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="3d532-110">The instance to use for this call.</span></span>

<span data-ttu-id="3d532-111">**Windows 2000 :**  Ce paramètre est ignoré et doit toujours avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3d532-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="3d532-112">**Windows XP et versions ultérieures :**  Ce paramètre est surchargé.</span><span class="sxs-lookup"><span data-stu-id="3d532-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="3d532-113">Si le moteur fonctionne en mode hérité (mode de compatibilité de Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur null** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="3d532-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="3d532-114">Si le moteur fonctionne en mode multi-instance, ce paramètre doit être un pointeur vers une instance créée à l’aide de [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="3d532-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="3d532-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="3d532-115">*grbit*</span></span>

<span data-ttu-id="3d532-116">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d532-116">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d532-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d532-117">Value</span></span></p></th>
<th><p><span data-ttu-id="3d532-118">Signification</span><span class="sxs-lookup"><span data-stu-id="3d532-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d532-119">JET_bitTermComplete</span><span class="sxs-lookup"><span data-stu-id="3d532-119">JET_bitTermComplete</span></span></p></td>
<td><p><span data-ttu-id="3d532-120">Demande que l’instance soit arrêtée proprement.</span><span class="sxs-lookup"><span data-stu-id="3d532-120">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="3d532-121">Tout travail de nettoyage facultatif qui serait normalement effectué en arrière-plan au moment de l’exécution est immédiatement effectué.</span><span class="sxs-lookup"><span data-stu-id="3d532-121">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d532-122">JET_bitTermAbrupt</span><span class="sxs-lookup"><span data-stu-id="3d532-122">JET_bitTermAbrupt</span></span></p></td>
<td><p><span data-ttu-id="3d532-123">Demande que l’instance soit arrêtée aussi rapidement que possible.</span><span class="sxs-lookup"><span data-stu-id="3d532-123">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="3d532-124">Tout travail facultatif qui serait normalement effectué en arrière-plan au moment de l’exécution est abandonné.</span><span class="sxs-lookup"><span data-stu-id="3d532-124">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></p>
<p><span data-ttu-id="3d532-125"><strong>Remarque</strong>  Cette option peut entraîner une perte d’espace temporaire ou permanente dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="3d532-125"><strong>Note</strong>  This option can cause temporary or permanent space loss in the database.</span></span> <span data-ttu-id="3d532-126">Cet espace perdu peut toujours être récupéré via une défragmentation hors connexion de la base de données.</span><span class="sxs-lookup"><span data-stu-id="3d532-126">This lost space can always be recovered through an offline defragmentation of the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d532-127">JET_bitTermStopBackup</span><span class="sxs-lookup"><span data-stu-id="3d532-127">JET_bitTermStopBackup</span></span></p></td>
<td><p><span data-ttu-id="3d532-128">Demande que l’instance soit arrêtée même si une sauvegarde est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="3d532-128">Requests that the instance be shut down even if there is currently a backup in progress.</span></span> <span data-ttu-id="3d532-129">En règle générale, une sauvegarde en attente provoquerait l’échec de <a href="gg269298(v=exchg.10).md">JetTerm</a> avec JET_errBackupInProgress.</span><span class="sxs-lookup"><span data-stu-id="3d532-129">Ordinarily, a pending backup would cause <a href="gg269298(v=exchg.10).md">JetTerm</a> to fail with JET_errBackupInProgress.</span></span> <span data-ttu-id="3d532-130">Quand ce paramètre n’est pas présent, sa valeur est supposée être JET_bitTermAbrupt.</span><span class="sxs-lookup"><span data-stu-id="3d532-130">When this parameter is not present, its value is presumed to be JET_bitTermAbrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d532-131">JET_bitTermDirty</span><span class="sxs-lookup"><span data-stu-id="3d532-131">JET_bitTermDirty</span></span></p></td>
<td><p><span data-ttu-id="3d532-132">Demande que l’instance soit arrêtée avec toutes les bases de données attachées laissées dans un état modifié.</span><span class="sxs-lookup"><span data-stu-id="3d532-132">Requests that the instance be shut down with all the attached databases left in a dirty state.</span></span></p>
<p><span data-ttu-id="3d532-133">Windows 7 : JET_bitTermDirty est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3d532-133">Windows 7: JET_bitTermDirty is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="3d532-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3d532-134">Return Value</span></span>

<span data-ttu-id="3d532-135">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="3d532-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="3d532-136">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="3d532-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d532-137">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3d532-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="3d532-138">Description</span><span class="sxs-lookup"><span data-stu-id="3d532-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d532-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="3d532-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="3d532-140">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3d532-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d532-141">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="3d532-141">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="3d532-142">Impossible de terminer l’opération, car une opération de sauvegarde est en cours sur l’instance.</span><span class="sxs-lookup"><span data-stu-id="3d532-142">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d532-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="3d532-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="3d532-144">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs paramètres a généré un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="3d532-144">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="3d532-145">Cette erreur est retournée par <a href="gg269298(v=exchg.10).md">JetTerm</a> lorsque le moteur est en mode multi-instance et lorsque <em>pinstance</em> fait référence à une instance non valide.</span><span class="sxs-lookup"><span data-stu-id="3d532-145">This error will be returned by <a href="gg269298(v=exchg.10).md">JetTerm</a> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="3d532-146"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3d532-146"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d532-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="3d532-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="3d532-148">L’opération ne peut pas se terminer car l’instance n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="3d532-148">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d532-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="3d532-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="3d532-150">L’opération ne peut pas se terminer car l’instance est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="3d532-150">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d532-151">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="3d532-151">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="3d532-152">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance.</span><span class="sxs-lookup"><span data-stu-id="3d532-152">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d532-153">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="3d532-153">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="3d532-154">L’instance ne peut pas être arrêtée, car il existe actuellement des sessions avec des transactions actives pour l’instance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3d532-154">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="3d532-155">Cette erreur se produit uniquement si le JET_bitTermComplete est utilisé.</span><span class="sxs-lookup"><span data-stu-id="3d532-155">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3d532-156">Si cette fonction est réussie, l’instance spécifiée est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="3d532-156">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="3d532-157">Le descripteur d’instance est également fermé et rendu non disponible pour toute API qui accepte un handle d’instance.</span><span class="sxs-lookup"><span data-stu-id="3d532-157">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="3d532-158">Tous les autres objets associés à l’instance, tels que les sessions, sont également fermés.</span><span class="sxs-lookup"><span data-stu-id="3d532-158">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="3d532-159">L’état du fichier de point de contrôle, des fichiers journaux des transactions et des fichiers de base de données attachés à l’instance sera modifié au cours du processus d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="3d532-159">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="3d532-160">Si cette fonction échoue en raison d’une erreur d’utilisation, l’instance reste dans un état initialisé et rien ne change.</span><span class="sxs-lookup"><span data-stu-id="3d532-160">If this function fails as a result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="3d532-161">Dans le cas contraire, l’instance est toujours arrêtée comme indiqué dans le cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="3d532-161">Otherwise, the instance is still shut down as stated for the success case.</span></span> <span data-ttu-id="3d532-162">La différence est que l’instance doit passer par la récupération après incident lorsqu’elle est ensuite initialisée.</span><span class="sxs-lookup"><span data-stu-id="3d532-162">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="3d532-163">Le moteur essaiera de vider le plus de données possible pour réduire la quantité de récupération requise.</span><span class="sxs-lookup"><span data-stu-id="3d532-163">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="3d532-164">Conceptuellement, un tel échec de [JetTerm](./jetterm-function.md) n’est pas différent d’un blocage de processus.</span><span class="sxs-lookup"><span data-stu-id="3d532-164">Conceptually, such a failure of [JetTerm](./jetterm-function.md) is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="3d532-165">Notes</span><span class="sxs-lookup"><span data-stu-id="3d532-165">Remarks</span></span>

<span data-ttu-id="3d532-166">Consultez [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="3d532-166">See [JetTerm](./jetterm-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="3d532-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d532-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d532-168"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3d532-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3d532-169">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="3d532-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d532-170"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="3d532-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3d532-171">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3d532-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d532-172"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="3d532-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3d532-173">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="3d532-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d532-174"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="3d532-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="3d532-175">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="3d532-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d532-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="3d532-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="3d532-177">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="3d532-177">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="3d532-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d532-178">See Also</span></span>

[<span data-ttu-id="3d532-179">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="3d532-179">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="3d532-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="3d532-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="3d532-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="3d532-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="3d532-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="3d532-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="3d532-183">JetInit</span><span class="sxs-lookup"><span data-stu-id="3d532-183">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="3d532-184">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="3d532-184">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="3d532-185">JetTerm</span><span class="sxs-lookup"><span data-stu-id="3d532-185">JetTerm</span></span>](./jetterm-function.md)
