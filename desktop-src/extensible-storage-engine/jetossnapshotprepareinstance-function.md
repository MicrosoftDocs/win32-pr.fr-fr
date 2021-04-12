---
description: 'En savoir plus sur : fonction JetOSSnapshotPrepareInstance'
title: JetOSSnapshotPrepareInstance fonction)
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104394283"
---
# <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="0df25-103">JetOSSnapshotPrepareInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="0df25-103">JetOSSnapshotPrepareInstance Function</span></span>


<span data-ttu-id="0df25-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="0df25-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="0df25-105">JetOSSnapshotPrepareInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="0df25-105">JetOSSnapshotPrepareInstance Function</span></span>

<span data-ttu-id="0df25-106">La fonction **JetOSSnapshotPrepareInstance** sélectionne une instance spécifique pour faire partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="0df25-106">The **JetOSSnapshotPrepareInstance** function selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="0df25-107">**Windows Vista :** **JetOSSnapshotPrepareInstance** a été introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0df25-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** was introduced in Windows Vista.</span></span>

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="0df25-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0df25-108">Parameters</span></span>

<span data-ttu-id="0df25-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="0df25-109">*snapId*</span></span>

<span data-ttu-id="0df25-110">Identificateur de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="0df25-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="0df25-111">*instancié*</span><span class="sxs-lookup"><span data-stu-id="0df25-111">*instance*</span></span>

<span data-ttu-id="0df25-112">Instance qui sera utilisée pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="0df25-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="0df25-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0df25-113">*grbit*</span></span>

<span data-ttu-id="0df25-114">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="0df25-114">The options for this call.</span></span> <span data-ttu-id="0df25-115">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="0df25-115">This parameter is reserved for future use.</span></span> <span data-ttu-id="0df25-116">La seule valeur valide est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="0df25-116">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="0df25-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0df25-117">Return Value</span></span>

<span data-ttu-id="0df25-118">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="0df25-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0df25-119">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0df25-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0df25-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0df25-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="0df25-121">Description</span><span class="sxs-lookup"><span data-stu-id="0df25-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0df25-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0df25-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0df25-123">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0df25-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0df25-124">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0df25-124">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0df25-125">Le pointeur d’ID d’instantané a la <strong>valeur null</strong> ou le paramètre <em>Grbit</em> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0df25-125">The snapshot id pointer is <strong>NULL</strong> or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0df25-126">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="0df25-126">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="0df25-127">Une session d’instantané est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="0df25-127">A snapshot session is already in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0df25-128">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="0df25-128">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="0df25-129">L’identificateur de la session d’instantané n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0df25-129">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0df25-130">Si cette fonction est réussie, l’instance spécifiée fera partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="0df25-130">If this function succeeds, the specified instance will be part of the snapshot session.</span></span>

<span data-ttu-id="0df25-131">Si cette fonction échoue, aucune modification de l’état du moteur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="0df25-131">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0df25-132">Notes</span><span class="sxs-lookup"><span data-stu-id="0df25-132">Remarks</span></span>

<span data-ttu-id="0df25-133">L’appel de séquence d’API normal est : [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), éventuellement suivi d’un ou plusieurs appels à **JetOSSnapshotPrepareInstance**, puis de [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="0df25-133">The normal API sequence call is: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optionally followed by one or more calls to **JetOSSnapshotPrepareInstance**, then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="0df25-134">Une fois le blocage démarré, il peut être arrêté à l’aide de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="0df25-134">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="0df25-135">À tout moment après la préparation, la session d’instantané peut être interrompue soudainement avec [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="0df25-135">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span> <span data-ttu-id="0df25-136">Les entrées du journal des événements seront générées pour les différentes étapes de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="0df25-136">Event log entries will be generated for the different steps of the snapshot.</span></span>

<span data-ttu-id="0df25-137">Si **JetOSSnapshotPrepareInstance** n’est pas appelé entre le début de la session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) et le moment du blocage ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), toutes les instances en cours d’exécution dans le moteur se figeront et feront partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="0df25-137">If **JetOSSnapshotPrepareInstance** is not called between the start of the session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) and the freeze moment ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), all the running instances in the engine will freeze and become part of the snapshot session.</span></span> <span data-ttu-id="0df25-138">Cela se produit pour deux raisons :</span><span class="sxs-lookup"><span data-stu-id="0df25-138">This occurs for two reasons:</span></span>

  - <span data-ttu-id="0df25-139">Il simplifie le code pour les utilisateurs qui souhaitent toutes les instances.</span><span class="sxs-lookup"><span data-stu-id="0df25-139">It simplifies the code for users who want all instances.</span></span>

  - <span data-ttu-id="0df25-140">Il permet la compatibilité descendante pour les appelants des API d’instantané.</span><span class="sxs-lookup"><span data-stu-id="0df25-140">It allows backward compatibility for the callers of the snapshot APIs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0df25-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0df25-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0df25-142"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0df25-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0df25-143">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0df25-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0df25-144"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="0df25-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0df25-145">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0df25-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0df25-146"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="0df25-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0df25-147">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="0df25-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0df25-148"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="0df25-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0df25-149">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0df25-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0df25-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0df25-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0df25-151">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0df25-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0df25-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0df25-152">See Also</span></span>

[<span data-ttu-id="0df25-153">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="0df25-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="0df25-154">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="0df25-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="0df25-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0df25-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0df25-156">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="0df25-156">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="0df25-157">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="0df25-157">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="0df25-158">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="0df25-158">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="0df25-159">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="0df25-159">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="0df25-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="0df25-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
