---
description: 'En savoir plus sur : fonction JetOSSnapshotThaw'
title: JetOSSnapshotThaw fonction)
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868941"
---
# <a name="jetossnapshotthaw-function"></a><span data-ttu-id="64ca9-103">JetOSSnapshotThaw fonction)</span><span class="sxs-lookup"><span data-stu-id="64ca9-103">JetOSSnapshotThaw Function</span></span>


<span data-ttu-id="64ca9-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="64ca9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotthaw-function"></a><span data-ttu-id="64ca9-105">JetOSSnapshotThaw fonction)</span><span class="sxs-lookup"><span data-stu-id="64ca9-105">JetOSSnapshotThaw Function</span></span>

<span data-ttu-id="64ca9-106">La fonction **JetOSSnapshotThaw** avertit le moteur qu’il peut reprendre des opérations d’e/s normales après une période de blocage et une capture instantanée réussie.</span><span class="sxs-lookup"><span data-stu-id="64ca9-106">The **JetOSSnapshotThaw** function notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="64ca9-107">**Windows XP :**  **JetOSSnapshotThaw** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="64ca9-107">**Windows XP:**  **JetOSSnapshotThaw** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="64ca9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64ca9-108">Parameters</span></span>

<span data-ttu-id="64ca9-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="64ca9-109">*snapId*</span></span>

<span data-ttu-id="64ca9-110">Identificateur de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="64ca9-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="64ca9-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="64ca9-111">*grbit*</span></span>

<span data-ttu-id="64ca9-112">Ce paramètre est réservé pour une utilisation ultérieure et la seule valeur valide prise en charge est 0.</span><span class="sxs-lookup"><span data-stu-id="64ca9-112">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="64ca9-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="64ca9-113">Return Value</span></span>

<span data-ttu-id="64ca9-114">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="64ca9-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="64ca9-115">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="64ca9-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64ca9-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="64ca9-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="64ca9-117">Description</span><span class="sxs-lookup"><span data-stu-id="64ca9-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64ca9-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="64ca9-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="64ca9-119">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="64ca9-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ca9-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="64ca9-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="64ca9-121">La session d’instantané n’est pas valide ou le paramètre <em>Grbit</em> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="64ca9-121">The snapshot session is invalid or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ca9-122">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="64ca9-122">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="64ca9-123">La session d’instantané avait un délai d’expiration interne avant l’appel de cet appel.</span><span class="sxs-lookup"><span data-stu-id="64ca9-123">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="64ca9-124">Par conséquent, les opérations d’e/s retournées à normal avant cet appel ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="64ca9-124">Consequently, IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ca9-125">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="64ca9-125">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="64ca9-126">L’identificateur pour la session d’instantané n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="64ca9-126">The identifier for snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="64ca9-127">Si cette fonction aboutit, une session d’instantané se termine et le comportement normal du moteur reprend.</span><span class="sxs-lookup"><span data-stu-id="64ca9-127">If this function succeeds, a snapshot session ends and the normal engine behavior resumes.</span></span> <span data-ttu-id="64ca9-128">Une nouvelle session d’instantané peut être démarrée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="64ca9-128">A new snapshot session can be started later.</span></span>

<span data-ttu-id="64ca9-129">Si cette fonction échoue, la session d’instantané en cours se termine, mais le gel d’IOs pendant la période de capture instantanée n’a pas été respecté en interne.</span><span class="sxs-lookup"><span data-stu-id="64ca9-129">If this function fails, the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span>

#### <a name="remarks"></a><span data-ttu-id="64ca9-130">Notes</span><span class="sxs-lookup"><span data-stu-id="64ca9-130">Remarks</span></span>

<span data-ttu-id="64ca9-131">Les entrées du journal des événements seront générées pour les différentes étapes de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="64ca9-131">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="64ca9-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64ca9-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64ca9-133"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="64ca9-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="64ca9-134">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="64ca9-134">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ca9-135"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="64ca9-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="64ca9-136">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="64ca9-136">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ca9-137"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="64ca9-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="64ca9-138">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="64ca9-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64ca9-139"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="64ca9-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="64ca9-140">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="64ca9-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64ca9-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="64ca9-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="64ca9-142">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="64ca9-142">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="64ca9-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64ca9-143">See Also</span></span>

[<span data-ttu-id="64ca9-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="64ca9-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="64ca9-145">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="64ca9-145">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="64ca9-146">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="64ca9-146">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="64ca9-147">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="64ca9-147">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="64ca9-148">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="64ca9-148">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)
