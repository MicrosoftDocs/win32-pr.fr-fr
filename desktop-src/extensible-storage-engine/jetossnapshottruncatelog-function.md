---
description: 'En savoir plus sur : fonction JetOSSnapshotTruncateLog'
title: JetOSSnapshotTruncateLog fonction)
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520098"
---
# <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="35c4d-103">JetOSSnapshotTruncateLog fonction)</span><span class="sxs-lookup"><span data-stu-id="35c4d-103">JetOSSnapshotTruncateLog Function</span></span>


<span data-ttu-id="35c4d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="35c4d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="35c4d-105">JetOSSnapshotTruncateLog fonction)</span><span class="sxs-lookup"><span data-stu-id="35c4d-105">JetOSSnapshotTruncateLog Function</span></span>

<span data-ttu-id="35c4d-106">La fonction **JetOSSnapshotTruncateLog** active la troncation du journal pour toutes les instances qui font partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="35c4d-106">The **JetOSSnapshotTruncateLog** function enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="35c4d-107">**Windows Vista :**  **JetOSSnapshotTruncateLog** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35c4d-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="35c4d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35c4d-108">Parameters</span></span>

<span data-ttu-id="35c4d-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="35c4d-109">*snapId*</span></span>

<span data-ttu-id="35c4d-110">Identificateur de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="35c4d-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="35c4d-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="35c4d-111">*grbit*</span></span>

<span data-ttu-id="35c4d-112">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="35c4d-112">The options for this call.</span></span> <span data-ttu-id="35c4d-113">Ce paramètre peut avoir une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="35c4d-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35c4d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="35c4d-114">Value</span></span></p></th>
<th><p><span data-ttu-id="35c4d-115">Signification</span><span class="sxs-lookup"><span data-stu-id="35c4d-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35c4d-116">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="35c4d-116">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="35c4d-117">Toutes les bases de données sont attachées afin que le moteur de stockage puisse calculer et effectuer la troncation du journal.</span><span class="sxs-lookup"><span data-stu-id="35c4d-117">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35c4d-118">0 (zéro)</span><span class="sxs-lookup"><span data-stu-id="35c4d-118">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="35c4d-119">Aucune troncation ne se produit.</span><span class="sxs-lookup"><span data-stu-id="35c4d-119">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="35c4d-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="35c4d-120">Return Value</span></span>

<span data-ttu-id="35c4d-121">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="35c4d-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="35c4d-122">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="35c4d-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35c4d-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="35c4d-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="35c4d-124">Description</span><span class="sxs-lookup"><span data-stu-id="35c4d-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35c4d-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="35c4d-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="35c4d-126">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="35c4d-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35c4d-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="35c4d-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="35c4d-128">Le paramètre <em>Grbit</em> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="35c4d-128">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35c4d-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="35c4d-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="35c4d-130">La session d’instantané n’est pas dans l’État dans lequel une troncation peut se produire.</span><span class="sxs-lookup"><span data-stu-id="35c4d-130">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="35c4d-131">Les causes possibles sont :</span><span class="sxs-lookup"><span data-stu-id="35c4d-131">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="35c4d-132">l’appel est effectué après le délai d’expiration de la session d’instantané</span><span class="sxs-lookup"><span data-stu-id="35c4d-132">the call is done after the snapshot session timed-out</span></span></p></li>
<li><p><span data-ttu-id="35c4d-133">la session a été spécifiée en tant qu’instantané de copie</span><span class="sxs-lookup"><span data-stu-id="35c4d-133">the session was specified as a copy snapshot</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="35c4d-134">En cas de réussite, les fichiers journaux pour une partie ou l’ensemble des instances de la session d’instantané seront tronqués, si possible.</span><span class="sxs-lookup"><span data-stu-id="35c4d-134">On success, the log files for one or all the instances part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="35c4d-135">Notes</span><span class="sxs-lookup"><span data-stu-id="35c4d-135">Remarks</span></span>

<span data-ttu-id="35c4d-136">Cette fonction doit être appelée uniquement si l’instantané a été créé avec l’option JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="35c4d-136">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="35c4d-137">Dans le cas contraire, la session d’instantané se terminera après l’appel de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="35c4d-137">Otherwise, the snapshot session would have ended after the [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) call.</span></span>

#### <a name="requirements"></a><span data-ttu-id="35c4d-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35c4d-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35c4d-139"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="35c4d-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="35c4d-140">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35c4d-140">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35c4d-141"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="35c4d-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="35c4d-142">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="35c4d-142">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35c4d-143"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="35c4d-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="35c4d-144">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="35c4d-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35c4d-145"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="35c4d-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="35c4d-146">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="35c4d-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="35c4d-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="35c4d-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="35c4d-148">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="35c4d-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="35c4d-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35c4d-149">See Also</span></span>

[<span data-ttu-id="35c4d-150">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="35c4d-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="35c4d-151">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="35c4d-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="35c4d-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="35c4d-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="35c4d-153">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="35c4d-153">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="35c4d-154">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="35c4d-154">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="35c4d-155">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="35c4d-155">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="35c4d-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="35c4d-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
