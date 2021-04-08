---
description: 'En savoir plus sur : fonction JetOSSnapshotEnd'
title: JetOSSnapshotEnd fonction)
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112054"
---
# <a name="jetossnapshotend-function"></a><span data-ttu-id="89acd-103">JetOSSnapshotEnd fonction)</span><span class="sxs-lookup"><span data-stu-id="89acd-103">JetOSSnapshotEnd Function</span></span>


<span data-ttu-id="89acd-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="89acd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotend-function"></a><span data-ttu-id="89acd-105">JetOSSnapshotEnd fonction)</span><span class="sxs-lookup"><span data-stu-id="89acd-105">JetOSSnapshotEnd Function</span></span>

<span data-ttu-id="89acd-106">La fonction **JetOSSnapshotEnd** informe le moteur que la session d’instantané est terminée.</span><span class="sxs-lookup"><span data-stu-id="89acd-106">The **JetOSSnapshotEnd** function notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="89acd-107">**Windows Vista :**  **JetOSSnapshotEnd** est introduit dans Windows Vista :.</span><span class="sxs-lookup"><span data-stu-id="89acd-107">**Windows Vista:**  **JetOSSnapshotEnd** is introduced in Windows Vista:.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="89acd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89acd-108">Parameters</span></span>

<span data-ttu-id="89acd-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="89acd-109">*snapId*</span></span>

<span data-ttu-id="89acd-110">Identificateur de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="89acd-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="89acd-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="89acd-111">*grbit*</span></span>

<span data-ttu-id="89acd-112">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="89acd-112">The options for this call.</span></span> <span data-ttu-id="89acd-113">Ce paramètre peut avoir une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="89acd-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89acd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="89acd-114">Value</span></span></p></th>
<th><p><span data-ttu-id="89acd-115">Signification</span><span class="sxs-lookup"><span data-stu-id="89acd-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89acd-116">0</span><span class="sxs-lookup"><span data-stu-id="89acd-116">0</span></span></p></td>
<td><p><span data-ttu-id="89acd-117">Fin de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="89acd-117">The successful end of the snapshot session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89acd-118">JET_bitAbortSnapshot</span><span class="sxs-lookup"><span data-stu-id="89acd-118">JET_bitAbortSnapshot</span></span></p></td>
<td><p><span data-ttu-id="89acd-119">La session d’instantané a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="89acd-119">The snapshot session aborted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="89acd-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89acd-120">Return Value</span></span>

<span data-ttu-id="89acd-121">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="89acd-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="89acd-122">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="89acd-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89acd-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="89acd-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="89acd-124">Description</span><span class="sxs-lookup"><span data-stu-id="89acd-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89acd-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="89acd-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="89acd-126">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="89acd-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89acd-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="89acd-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="89acd-128">L’une des options demandées n’est pas valide, est utilisée de manière incorrecte ou n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="89acd-128">One of the options requested is invalid, used incorrectly, or not implemented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89acd-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="89acd-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="89acd-130">Une session d’instantané est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="89acd-130">A snapshot session is already in progress.</span></span> <span data-ttu-id="89acd-131">Cette opération n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="89acd-131">This is not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89acd-132">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="89acd-132">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="89acd-133">L’identificateur de la session d’instantané n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="89acd-133">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89acd-134">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="89acd-134">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="89acd-135">La session d’instantané avait un délai d’expiration interne avant l’appel de cet appel.</span><span class="sxs-lookup"><span data-stu-id="89acd-135">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="89acd-136">Par conséquent, les opérations d’e/s retournées à normal avant cet appel ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="89acd-136">As a result, the IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89acd-137">Si cette fonction réussit, une session d’instantané se termine et le comportement normal du moteur reprendra.</span><span class="sxs-lookup"><span data-stu-id="89acd-137">If this function succeeds, a snapshot session will complete and the normal engine behavior will resume.</span></span> <span data-ttu-id="89acd-138">Une nouvelle session d’instantané peut être démarrée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="89acd-138">A new snapshot session can be started later.</span></span>

<span data-ttu-id="89acd-139">Si cette fonction échoue, le code de retour de la JET_errOSSnapshotTimeOut retourne et la session d’instantané en cours se termine, mais le gel d’IOs pendant la période de capture instantanée n’a pas été respecté en interne.</span><span class="sxs-lookup"><span data-stu-id="89acd-139">If this function fails, the JET_errOSSnapshotTimeOut return code returns and the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span> <span data-ttu-id="89acd-140">Pour toutes les autres erreurs, l’état de la session d’instantané ne sera pas modifié.</span><span class="sxs-lookup"><span data-stu-id="89acd-140">For all other errors, the snapshot session state will not be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="89acd-141">Notes</span><span class="sxs-lookup"><span data-stu-id="89acd-141">Remarks</span></span>

<span data-ttu-id="89acd-142">Cette fonction est appelée uniquement si [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) a été appelé avec JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="89acd-142">This function is called only if [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) was called with JET_bitContinueAfterThaw.</span></span>

<span data-ttu-id="89acd-143">La session d’instantané doit se terminer pour que la vérification de l’instantané et la troncation du journal aient lieu.</span><span class="sxs-lookup"><span data-stu-id="89acd-143">The snapshot session must complete for the snapshot verification and log truncation to take place.</span></span> <span data-ttu-id="89acd-144">Les entrées du journal des événements seront générées pour les différentes étapes de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="89acd-144">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="89acd-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89acd-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89acd-146"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="89acd-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="89acd-147">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="89acd-147">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89acd-148"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="89acd-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="89acd-149">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="89acd-149">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89acd-150"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="89acd-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="89acd-151">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="89acd-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89acd-152"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="89acd-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="89acd-153">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="89acd-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89acd-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="89acd-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="89acd-155">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="89acd-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="89acd-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89acd-156">See Also</span></span>

[<span data-ttu-id="89acd-157">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="89acd-157">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="89acd-158">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="89acd-158">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="89acd-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="89acd-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="89acd-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="89acd-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
