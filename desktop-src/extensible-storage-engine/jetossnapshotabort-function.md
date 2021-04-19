---
description: 'En savoir plus sur : fonction JetOSSnapshotAbort'
title: JetOSSnapshotAbort fonction)
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521872"
---
# <a name="jetossnapshotabort-function"></a><span data-ttu-id="7c0ae-103">JetOSSnapshotAbort fonction)</span><span class="sxs-lookup"><span data-stu-id="7c0ae-103">JetOSSnapshotAbort Function</span></span>


<span data-ttu-id="7c0ae-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="7c0ae-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotabort-function"></a><span data-ttu-id="7c0ae-105">JetOSSnapshotAbort fonction)</span><span class="sxs-lookup"><span data-stu-id="7c0ae-105">JetOSSnapshotAbort Function</span></span>

<span data-ttu-id="7c0ae-106">La fonction **JetOSSnapshotAbort** avertit le moteur qu’il peut reprendre des opérations d’e/s normales après la fin d’une période de blocage avec un instantané ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-106">The **JetOSSnapshotAbort** function notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="7c0ae-107">**Windows server 2003 :**  **JetOSSnapshotAbort** est introduit dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-107">**Windows Server 2003:**  **JetOSSnapshotAbort** is introduced in Windows Server 2003.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7c0ae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c0ae-108">Parameters</span></span>

<span data-ttu-id="7c0ae-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="7c0ae-109">*snapId*</span></span>

<span data-ttu-id="7c0ae-110">Identificateur de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="7c0ae-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7c0ae-111">*grbit*</span></span>

<span data-ttu-id="7c0ae-112">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-112">The options for this call.</span></span> <span data-ttu-id="7c0ae-113">Ce paramètre est réservé pour une utilisation ultérieure et la seule valeur valide prise en charge est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="7c0ae-113">This parameter is reserved for future use and the only valid value supported is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="7c0ae-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7c0ae-114">Return Value</span></span>

<span data-ttu-id="7c0ae-115">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7c0ae-116">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7c0ae-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c0ae-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7c0ae-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="7c0ae-118">Description</span><span class="sxs-lookup"><span data-stu-id="7c0ae-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c0ae-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7c0ae-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7c0ae-120">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c0ae-121">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7c0ae-121">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7c0ae-122">La session d’instantané n’est pas valide ou le paramètre Grbit n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-122">The snapshot session is invalid or the grbit parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c0ae-123">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="7c0ae-123">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="7c0ae-124">L’identificateur de la session d’instantané n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-124">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7c0ae-125">Si cette fonction est exécutée correctement, la session d’instantané se termine et le comportement normal du moteur reprend.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-125">If this function succeeds, the snapshot session will end and the normal engine behavior will resume.</span></span> <span data-ttu-id="7c0ae-126">Une nouvelle session d’instantané peut être démarrée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-126">A new snapshot session can be started at a later point.</span></span>

<span data-ttu-id="7c0ae-127">Si cette fonction échoue, la session d’instantané n’est pas abandonnée.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-127">If this function fails, the snapshot session will not be aborted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7c0ae-128">Notes</span><span class="sxs-lookup"><span data-stu-id="7c0ae-128">Remarks</span></span>

<span data-ttu-id="7c0ae-129">Cette fonction doit être appelée à la place de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) pour informer le moteur que l’instantané a été abandonné pour des raisons qui ne sont pas liées au moteur.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-129">This function should be called instead of [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) to inform the engine that the snapshot was aborted for reasons that don't relate to the engine.</span></span> <span data-ttu-id="7c0ae-130">Ces informations peuvent être utilisées ultérieurement pour aider à émettre des messages du journal des événements concernant la session d’instantané ou pour aider à déterminer d’autres actions appropriées.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-130">This information can be used later to help issue event log messages about the snapshot session or to help determine other appropriate actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7c0ae-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c0ae-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c0ae-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7c0ae-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7c0ae-133">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-133">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c0ae-134"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="7c0ae-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7c0ae-135">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-135">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c0ae-136"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="7c0ae-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7c0ae-137">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c0ae-138"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="7c0ae-138"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7c0ae-139">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-139">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c0ae-140"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7c0ae-140"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7c0ae-141">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7c0ae-141">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7c0ae-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c0ae-142">See Also</span></span>

[<span data-ttu-id="7c0ae-143">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7c0ae-143">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7c0ae-144">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="7c0ae-144">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="7c0ae-145">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="7c0ae-145">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="7c0ae-146">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="7c0ae-146">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="7c0ae-147">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="7c0ae-147">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
