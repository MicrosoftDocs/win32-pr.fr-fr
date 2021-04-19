---
description: 'En savoir plus sur : fonction JetTerm'
title: Fonction JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ce78ea12dfa61265a12b3858cc1e859adcae6e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515215"
---
# <a name="jetterm-function"></a><span data-ttu-id="f52db-103">Fonction JetTerm</span><span class="sxs-lookup"><span data-stu-id="f52db-103">JetTerm Function</span></span>


<span data-ttu-id="f52db-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f52db-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm-function"></a><span data-ttu-id="f52db-105">Fonction JetTerm</span><span class="sxs-lookup"><span data-stu-id="f52db-105">JetTerm Function</span></span>

<span data-ttu-id="f52db-106">La fonction **JetTerm** lance l’arrêt d’une instance qui a été initialisée par [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="f52db-106">The **JetTerm** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="f52db-107">**JetTerm** peut également être utilisé pour détruire une instance non initialisée qui a été créée par [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="f52db-107">**JetTerm** can also be used to destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="f52db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f52db-108">Parameters</span></span>

<span data-ttu-id="f52db-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="f52db-109">*instance*</span></span>

<span data-ttu-id="f52db-110">Spécifie l’instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="f52db-110">Specifies the instance to use for this call.</span></span>

<span data-ttu-id="f52db-111">**Windows 2000 :**  Ce paramètre est ignoré et doit toujours avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f52db-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="f52db-112">**Windows XP et versions ultérieures :**  Ce paramètre est surchargé.</span><span class="sxs-lookup"><span data-stu-id="f52db-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="f52db-113">Si le moteur fonctionne en mode hérité (mode de compatibilité de Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur null** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="f52db-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="f52db-114">Si le moteur fonctionne en mode multi-instance, ce paramètre doit être un pointeur vers une instance créée à l’aide de [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="f52db-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="f52db-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f52db-115">Return Value</span></span>

<span data-ttu-id="f52db-116">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="f52db-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f52db-117">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f52db-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f52db-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f52db-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="f52db-119">Description</span><span class="sxs-lookup"><span data-stu-id="f52db-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f52db-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f52db-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f52db-121">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f52db-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f52db-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f52db-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f52db-123">L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs paramètres a généré un résultat inattendu.</span><span class="sxs-lookup"><span data-stu-id="f52db-123">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="f52db-124">Cette erreur est retournée par <strong>JetTerm</strong> lorsque le moteur est en mode multi-instance et lorsque <em>pinstance</em> fait référence à une instance non valide.</span><span class="sxs-lookup"><span data-stu-id="f52db-124">This error will be returned by <strong>JetTerm</strong> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="f52db-125"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f52db-125"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f52db-126">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f52db-126">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f52db-127">L’opération ne peut pas se terminer car l’instance n’a pas encore été initialisée.</span><span class="sxs-lookup"><span data-stu-id="f52db-127">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f52db-128">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f52db-128">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f52db-129">L’opération ne peut pas se terminer car l’instance est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f52db-129">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f52db-130">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f52db-130">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f52db-131">Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance.</span><span class="sxs-lookup"><span data-stu-id="f52db-131">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f52db-132">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="f52db-132">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="f52db-133">Impossible de terminer l’opération, car une opération de sauvegarde est en cours sur l’instance.</span><span class="sxs-lookup"><span data-stu-id="f52db-133">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f52db-134">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="f52db-134">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="f52db-135">L’instance ne peut pas être arrêtée, car il existe actuellement des sessions avec des transactions actives pour l’instance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f52db-135">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="f52db-136">Cette erreur se produit uniquement si le JET_bitTermComplete est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f52db-136">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f52db-137">Si cette fonction est réussie, l’instance spécifiée est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="f52db-137">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="f52db-138">Le descripteur d’instance est également fermé et rendu non disponible pour toute API qui accepte un handle d’instance.</span><span class="sxs-lookup"><span data-stu-id="f52db-138">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="f52db-139">Tous les autres objets associés à l’instance, tels que les sessions, sont également fermés.</span><span class="sxs-lookup"><span data-stu-id="f52db-139">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="f52db-140">L’état du fichier de point de contrôle, des fichiers journaux des transactions et des fichiers de base de données attachés à l’instance sera modifié au cours du processus d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f52db-140">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="f52db-141">Si cette fonction échoue en raison d’une erreur d’utilisation, l’instance reste dans un état initialisé et rien ne change.</span><span class="sxs-lookup"><span data-stu-id="f52db-141">If this function fails as the result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="f52db-142">Dans le cas contraire, l’instance est toujours arrêtée en fonction de la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="f52db-142">Otherwise, the instance is still shut down as per the success case.</span></span> <span data-ttu-id="f52db-143">La différence est que l’instance doit passer par la récupération après incident lorsqu’elle est ensuite initialisée.</span><span class="sxs-lookup"><span data-stu-id="f52db-143">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="f52db-144">Le moteur essaiera de vider le plus de données possible pour réduire la quantité de récupération requise.</span><span class="sxs-lookup"><span data-stu-id="f52db-144">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="f52db-145">Conceptuellement, un tel échec de **JetTerm** n’est pas différent d’un blocage de processus.</span><span class="sxs-lookup"><span data-stu-id="f52db-145">Conceptually, such a failure of **JetTerm** is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f52db-146">Notes</span><span class="sxs-lookup"><span data-stu-id="f52db-146">Remarks</span></span>

<span data-ttu-id="f52db-147">Si le processus hôte d’une instance se ferme pour une raison quelconque avant que **JetTerm** soit appelé avec succès sur cette instance, l’instance est considérée comme étant dans un état de blocage.</span><span class="sxs-lookup"><span data-stu-id="f52db-147">If the host process of an instance quits for any reason before **JetTerm** is successfully called on that instance then the instance is considered to be in a crashed state.</span></span> <span data-ttu-id="f52db-148">La récupération après incident se produira lors de la prochaine tentative d’initialisation de cette instance.</span><span class="sxs-lookup"><span data-stu-id="f52db-148">Crash recovery will occur on the next attempt to initialize that instance.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f52db-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f52db-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f52db-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f52db-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f52db-151">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f52db-151">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f52db-152"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f52db-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f52db-153">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f52db-153">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f52db-154"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f52db-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f52db-155">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f52db-155">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f52db-156"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f52db-156"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f52db-157">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f52db-157">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f52db-158"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f52db-158"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f52db-159">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f52db-159">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f52db-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f52db-160">See Also</span></span>

[<span data-ttu-id="f52db-161">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="f52db-161">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="f52db-162">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="f52db-162">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="f52db-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f52db-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f52db-164">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f52db-164">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f52db-165">JetInit</span><span class="sxs-lookup"><span data-stu-id="f52db-165">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="f52db-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f52db-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f52db-167">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="f52db-167">JetTerm2</span></span>](./jetterm2-function.md)
