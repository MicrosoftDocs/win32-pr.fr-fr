---
description: 'En savoir plus sur : fonction JetOSSnapshotGetFreezeInfo'
title: JetOSSnapshotGetFreezeInfo fonction)
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536532"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="df050-103">JetOSSnapshotGetFreezeInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="df050-103">JetOSSnapshotGetFreezeInfo Function</span></span>


<span data-ttu-id="df050-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="df050-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="df050-105">JetOSSnapshotGetFreezeInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="df050-105">JetOSSnapshotGetFreezeInfo Function</span></span>

<span data-ttu-id="df050-106">La fonction **JetOSSnapshotGetFreezeInfo** récupère la liste des instances et des bases de données qui font partie de la session d’instantané à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="df050-106">The **JetOSSnapshotGetFreezeInfo** function retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="df050-107">**Windows Vista :**  **JetOSSnapshotGetFreezeInfo** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df050-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="df050-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df050-108">Parameters</span></span>

<span data-ttu-id="df050-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="df050-109">*snapId*</span></span>

<span data-ttu-id="df050-110">Identificateur de la session d’instantané à démarrer.</span><span class="sxs-lookup"><span data-stu-id="df050-110">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="df050-111">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="df050-111">*pcInstanceInfo*</span></span>

<span data-ttu-id="df050-112">Nombre d’instances en cours d’exécution qui font partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="df050-112">The number of instances currently running that are part of the snapshot session.</span></span>

<span data-ttu-id="df050-113">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="df050-113">*paInstanceInfo*</span></span>

<span data-ttu-id="df050-114">Tableau de structures, une pour chaque instance en cours d’exécution, décrivant l’instance et les bases de données qui en font partie.</span><span class="sxs-lookup"><span data-stu-id="df050-114">An array of structures, one for each running instance, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="df050-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="df050-115">*grbit*</span></span>

<span data-ttu-id="df050-116">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="df050-116">The options for this call.</span></span> <span data-ttu-id="df050-117">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="df050-117">This parameter is reserved for future use.</span></span> <span data-ttu-id="df050-118">La seule valeur valide est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="df050-118">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="df050-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df050-119">Return Value</span></span>

<span data-ttu-id="df050-120">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="df050-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="df050-121">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="df050-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="df050-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="df050-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="df050-123">Description</span><span class="sxs-lookup"><span data-stu-id="df050-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df050-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="df050-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="df050-125">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="df050-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df050-126">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="df050-126">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="df050-127">La fonction a échoué en raison d’une condition de mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="df050-127">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df050-128">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="df050-128">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="df050-129"><em>pcInstanceInfo</em> ou <em>PaInstanceInfo</em> a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="df050-129"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df050-130">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="df050-130">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="df050-131">L’identificateur de la session d’instantané n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="df050-131">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df050-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="df050-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="df050-133">Une session d’instantané n’est pas en cours.</span><span class="sxs-lookup"><span data-stu-id="df050-133">A snapshot session is not in progress.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="df050-134">Si cette fonction est réussie, les informations d’instance sont correctement remplies et doivent être libérées ultérieurement en appelant [JetFreeBuffer](./jetfreebuffer-function.md) avec le pointeur vers le tableau d’informations d’instance retourné.</span><span class="sxs-lookup"><span data-stu-id="df050-134">If this function succeeds, the instance information is properly filled and it must be freed later by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="df050-135">Si cette fonction échoue, aucune modification de l’état du moteur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="df050-135">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="df050-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df050-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df050-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="df050-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="df050-138">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df050-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df050-139"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="df050-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="df050-140">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="df050-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df050-141"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="df050-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="df050-142">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="df050-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df050-143"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="df050-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="df050-144">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="df050-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="df050-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="df050-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="df050-146">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="df050-146">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="df050-147"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="df050-147"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="df050-148">Implémenté en tant que <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) et <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="df050-148">Implemented as <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) and <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="df050-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df050-149">See Also</span></span>

[<span data-ttu-id="df050-150">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="df050-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="df050-151">Erreurs du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="df050-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="df050-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="df050-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="df050-153">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="df050-153">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)  
[<span data-ttu-id="df050-154">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="df050-154">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="df050-155">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="df050-155">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="df050-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="df050-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
