---
description: 'En savoir plus sur : fonction JetOSSnapshotPrepare'
title: Fonction JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536533"
---
# <a name="jetossnapshotprepare-function"></a><span data-ttu-id="c84bb-103">Fonction JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="c84bb-103">JetOSSnapshotPrepare Function</span></span>


<span data-ttu-id="c84bb-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c84bb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepare-function"></a><span data-ttu-id="c84bb-105">Fonction JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="c84bb-105">JetOSSnapshotPrepare Function</span></span>

<span data-ttu-id="c84bb-106">La fonction **JetOSSnapshotPrepare** commence les préparations pour une session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="c84bb-106">The **JetOSSnapshotPrepare** function begins the preparations for a snapshot session.</span></span> <span data-ttu-id="c84bb-107">Une session d’instantané est un intervalle de temps dans lequel le moteur n’émet pas d’e/s d’écriture sur le disque, de sorte que le moteur peut participer à une session d’instantané de volume (lorsqu’il est piloté par un enregistreur d’instantané).</span><span class="sxs-lookup"><span data-stu-id="c84bb-107">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="c84bb-108">**Windows XP :**  **JetOSSnapshotPrepare** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c84bb-108">**Windows XP:**  **JetOSSnapshotPrepare** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c84bb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c84bb-109">Parameters</span></span>

<span data-ttu-id="c84bb-110">*psnapId*</span><span class="sxs-lookup"><span data-stu-id="c84bb-110">*psnapId*</span></span>

<span data-ttu-id="c84bb-111">Identificateur de la session d’instantané à démarrer.</span><span class="sxs-lookup"><span data-stu-id="c84bb-111">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="c84bb-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c84bb-112">*grbit*</span></span>

<span data-ttu-id="c84bb-113">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="c84bb-113">The options for this call.</span></span> <span data-ttu-id="c84bb-114">Ce paramètre peut avoir une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c84bb-114">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c84bb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c84bb-115">Value</span></span></p></th>
<th><p><span data-ttu-id="c84bb-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c84bb-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c84bb-117">0</span><span class="sxs-lookup"><span data-stu-id="c84bb-117">0</span></span></p></td>
<td><p><span data-ttu-id="c84bb-118">Instantané normal.</span><span class="sxs-lookup"><span data-stu-id="c84bb-118">Normal snapshot.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84bb-119">JET_bitIncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="c84bb-119">JET_bitIncrementalSnapshot</span></span></p></td>
<td><p><span data-ttu-id="c84bb-120">Seuls les fichiers journaux seront pris.</span><span class="sxs-lookup"><span data-stu-id="c84bb-120">Only log files will be taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84bb-121">JET_bitCopySnapshot</span><span class="sxs-lookup"><span data-stu-id="c84bb-121">JET_bitCopySnapshot</span></span></p></td>
<td><p><span data-ttu-id="c84bb-122">Instantané de copie (normal ou incrémentiel) sans troncation du journal.</span><span class="sxs-lookup"><span data-stu-id="c84bb-122">A copy snapshot (normal or incremental) with no log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84bb-123">JET_bitContinueAfterThaw</span><span class="sxs-lookup"><span data-stu-id="c84bb-123">JET_bitContinueAfterThaw</span></span></p></td>
<td><p><span data-ttu-id="c84bb-124">La session d’instantané se produit après <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> et nécessite un appel de fonction <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> .</span><span class="sxs-lookup"><span data-stu-id="c84bb-124">The snapshot session occurs after <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> and will require a <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> function call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84bb-125">JET_bitExplicitPrepare</span><span class="sxs-lookup"><span data-stu-id="c84bb-125">JET_bitExplicitPrepare</span></span></p></td>
<td><p><span data-ttu-id="c84bb-126">Aucune instance ne sera préparée par défaut.</span><span class="sxs-lookup"><span data-stu-id="c84bb-126">No instances will be prepared by default.</span></span></p>
<p><span data-ttu-id="c84bb-127"><strong>Windows 7 :</strong>  JET_bitExplicitPrepare est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c84bb-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c84bb-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c84bb-128">Return Value</span></span>

<span data-ttu-id="c84bb-129">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c84bb-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c84bb-130">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c84bb-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c84bb-131">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c84bb-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="c84bb-132">Description</span><span class="sxs-lookup"><span data-stu-id="c84bb-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c84bb-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c84bb-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c84bb-134">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c84bb-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84bb-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c84bb-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c84bb-136">Le pointeur d’ID d’instantané a la valeur NULL ou le paramètre <em>Grbit</em> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c84bb-136">The snapshot ID pointer is NULL or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84bb-137">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="c84bb-137">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="c84bb-138">Une session d’instantané est déjà en cours et l’opération n’est pas autorisée à avoir plus d’une session d’instantané à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="c84bb-138">A snapshot session is already in progress and the operation is not allowed to have more then one snapshot session at any given time.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c84bb-139">Si cette fonction réussit, une session d’instantané est en mesure de démarrer à tout moment avec la phase d’interruption des e/s.</span><span class="sxs-lookup"><span data-stu-id="c84bb-139">If this function succeeds, a snapshot session will be able to start at any time with the IO freeze phase.</span></span> <span data-ttu-id="c84bb-140">L’identificateur de la session est retourné et doit être utilisé dans les appels suivants pour la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="c84bb-140">The identifier for the session will be returned and must be used in the subsequent calls for the snapshot session.</span></span>

<span data-ttu-id="c84bb-141">Les instances en cours d’exécution du moteur seront désormais considérées comme faisant partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="c84bb-141">The running instances of the engine will now be considered part of the snapshot session.</span></span>

<span data-ttu-id="c84bb-142">**Windows Vista :**  Pour spécifier un sous-ensemble différent d’instances, [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) peut être appelé.</span><span class="sxs-lookup"><span data-stu-id="c84bb-142">**Windows Vista:**  To specify a different subset of instances, the [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) can be called.</span></span>

<span data-ttu-id="c84bb-143">L’appel de séquence d’API normal est : **JetOSSnapshotPrepare**, éventuellement suivi d’un ou plusieurs appels à [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), puis de [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="c84bb-143">The normal API sequence call is: **JetOSSnapshotPrepare**, optionally followed by one or more calls to [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="c84bb-144">Une fois le blocage démarré, il peut être arrêté à l’aide de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="c84bb-144">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="c84bb-145">À tout moment après la préparation, la session d’instantané peut être interrompue soudainement avec [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="c84bb-145">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span>

<span data-ttu-id="c84bb-146">Si JET_bitContinueAfterThaw est spécifié après [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), la session d’instantané est conservée (bien que l’e/s reprenne).</span><span class="sxs-lookup"><span data-stu-id="c84bb-146">If JET_bitContinueAfterThaw is specified after [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), the snapshot session will remain (although the I/O will resume).</span></span> <span data-ttu-id="c84bb-147">Cela permet de vérifier la capture instantanée et, si nécessaire, d’activer la troncation du journal à l’aide de [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) et de demander un appel à [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span><span class="sxs-lookup"><span data-stu-id="c84bb-147">This will enable a verification of the snapshot, and if needed, will enable log truncation using [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) and will require a call to [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span></span>

<span data-ttu-id="c84bb-148">Si cette fonction échoue, aucune modification de l’état du moteur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="c84bb-148">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c84bb-149">Notes</span><span class="sxs-lookup"><span data-stu-id="c84bb-149">Remarks</span></span>

<span data-ttu-id="c84bb-150">Les entrées du journal des événements seront générées pour les différentes étapes de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="c84bb-150">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c84bb-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c84bb-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c84bb-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c84bb-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c84bb-153">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c84bb-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84bb-154"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c84bb-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c84bb-155">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c84bb-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84bb-156"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c84bb-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c84bb-157">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c84bb-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c84bb-158"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="c84bb-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c84bb-159">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c84bb-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c84bb-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c84bb-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c84bb-161">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c84bb-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c84bb-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c84bb-162">See Also</span></span>

[<span data-ttu-id="c84bb-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c84bb-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c84bb-164">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="c84bb-164">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="c84bb-165">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="c84bb-165">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="c84bb-166">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="c84bb-166">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="c84bb-167">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="c84bb-167">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="c84bb-168">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="c84bb-168">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="c84bb-169">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="c84bb-169">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)  
[<span data-ttu-id="c84bb-170">JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="c84bb-170">JetOSSnapshotTruncateLog</span></span>](./jetossnapshottruncatelog-function.md)
