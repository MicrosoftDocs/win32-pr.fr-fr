---
description: 'En savoir plus sur : fonction JetOSSnapshotTruncateLogInstance'
title: JetOSSnapshotTruncateLogInstance fonction)
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749701"
---
# <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="ddcd8-103">JetOSSnapshotTruncateLogInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="ddcd8-103">JetOSSnapshotTruncateLogInstance Function</span></span>


<span data-ttu-id="ddcd8-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ddcd8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="ddcd8-105">JetOSSnapshotTruncateLogInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="ddcd8-105">JetOSSnapshotTruncateLogInstance Function</span></span>

<span data-ttu-id="ddcd8-106">La fonction **JetOSSnapshotTruncateLogInstance** tronque le journal pour une instance spécifiée pendant une session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-106">The **JetOSSnapshotTruncateLogInstance** function truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="ddcd8-107">**Windows Vista :**  **JetOSSnapshotTruncateLogInstance** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="ddcd8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddcd8-108">Parameters</span></span>

<span data-ttu-id="ddcd8-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="ddcd8-109">*snapId*</span></span>

<span data-ttu-id="ddcd8-110">Identificateur de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="ddcd8-111">*instancié*</span><span class="sxs-lookup"><span data-stu-id="ddcd8-111">*instance*</span></span>

<span data-ttu-id="ddcd8-112">Instance qui sera utilisée pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="ddcd8-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="ddcd8-113">*grbit*</span></span>

<span data-ttu-id="ddcd8-114">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-114">The options for this call.</span></span> <span data-ttu-id="ddcd8-115">Ce paramètre peut avoir une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-115">This parameter can have a combination of the following values.</span></span>

<span data-ttu-id="ddcd8-116">*Grbit* peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ddcd8-116">*grbit* can be one of the following values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ddcd8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddcd8-117">Value</span></span></p></th>
<th><p><span data-ttu-id="ddcd8-118">Signification</span><span class="sxs-lookup"><span data-stu-id="ddcd8-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ddcd8-119">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ddcd8-119">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="ddcd8-120">Toutes les bases de données sont attachées afin que le moteur de stockage puisse calculer et effectuer la troncation du journal.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-120">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddcd8-121">0 (zéro)</span><span class="sxs-lookup"><span data-stu-id="ddcd8-121">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="ddcd8-122">Aucune troncation ne se produit.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-122">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="ddcd8-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ddcd8-123">Return Value</span></span>

<span data-ttu-id="ddcd8-124">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="ddcd8-125">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ddcd8-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ddcd8-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ddcd8-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="ddcd8-127">Description</span><span class="sxs-lookup"><span data-stu-id="ddcd8-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ddcd8-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="ddcd8-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="ddcd8-129">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddcd8-130">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="ddcd8-130">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="ddcd8-131">Le paramètre <em>Grbit</em> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-131">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddcd8-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="ddcd8-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="ddcd8-133">La session d’instantané n’est pas dans l’État dans lequel une troncation peut se produire.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-133">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="ddcd8-134">Les causes possibles sont :</span><span class="sxs-lookup"><span data-stu-id="ddcd8-134">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="ddcd8-135">L’appel se termine après le délai d’expiration de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-135">The call completes after the snapshot session timed out.</span></span></p></li>
<li><p><span data-ttu-id="ddcd8-136">La session a été spécifiée en tant qu’instantané de copie.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-136">The session was specified as a copy snapshot.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ddcd8-137">Si cette fonction est réussie, les fichiers journaux d’une ou de toutes les instances qui font partie de la session d’instantané seront tronqués, si possible.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-137">If this function succeeds, the log files for one or all of the instances that are part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="ddcd8-138">Notes</span><span class="sxs-lookup"><span data-stu-id="ddcd8-138">Remarks</span></span>

<span data-ttu-id="ddcd8-139">Cette fonction doit être appelée uniquement si l’instantané a été créé avec l’option JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-139">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="ddcd8-140">Dans le cas contraire, la session d’instantané se termine après l’appel à [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="ddcd8-140">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="ddcd8-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddcd8-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ddcd8-142"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ddcd8-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ddcd8-143">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddcd8-144"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="ddcd8-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ddcd8-145">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddcd8-146"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="ddcd8-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ddcd8-147">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ddcd8-148"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="ddcd8-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="ddcd8-149">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ddcd8-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="ddcd8-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="ddcd8-151">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="ddcd8-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="ddcd8-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddcd8-152">See Also</span></span>

[<span data-ttu-id="ddcd8-153">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="ddcd8-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="ddcd8-154">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="ddcd8-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="ddcd8-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="ddcd8-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="ddcd8-156">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="ddcd8-156">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="ddcd8-157">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="ddcd8-157">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="ddcd8-158">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="ddcd8-158">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="ddcd8-159">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="ddcd8-159">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
