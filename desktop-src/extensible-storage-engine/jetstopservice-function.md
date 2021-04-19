---
description: 'En savoir plus sur : fonction JetStopService'
title: Fonction JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516693"
---
# <a name="jetstopservice-function"></a><span data-ttu-id="0fb4f-103">Fonction JetStopService</span><span class="sxs-lookup"><span data-stu-id="0fb4f-103">JetStopService Function</span></span>


<span data-ttu-id="0fb4f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="0fb4f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopservice-function"></a><span data-ttu-id="0fb4f-105">Fonction JetStopService</span><span class="sxs-lookup"><span data-stu-id="0fb4f-105">JetStopService Function</span></span>

<span data-ttu-id="0fb4f-106">La fonction **JetStopService** prépare une instance pour l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-106">The **JetStopService** function prepares an instance for termination.</span></span>

<span data-ttu-id="0fb4f-107">**JetStopService** est l’appel hérité lorsqu’une seule instance est autorisée.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-107">**JetStopService** is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="0fb4f-108">Dans ce cas, la seule instance active est celle qui est préparée pour l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-108">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a><span data-ttu-id="0fb4f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fb4f-109">Parameters</span></span>

<span data-ttu-id="0fb4f-110">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-110">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="0fb4f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0fb4f-111">Return Value</span></span>

<span data-ttu-id="0fb4f-112">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0fb4f-113">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0fb4f-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0fb4f-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0fb4f-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="0fb4f-115">Description</span><span class="sxs-lookup"><span data-stu-id="0fb4f-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fb4f-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0fb4f-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0fb4f-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fb4f-118">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="0fb4f-118">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="0fb4f-119">Il n’est pas évident de déterminer l’instance à préparer pour l’arrêt lors de l’utilisation de <strong>JetStopService</strong> avec plusieurs modes d’instance.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-119">It is not clear which instance to prepare for termination when using <strong>JetStopService</strong> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="0fb4f-120"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0fb4f-121">Si cette fonction est réussie, elle se prépare à un arrêt ultérieur.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="0fb4f-122">Les étapes à suivre pour préparer un arrêt sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0fb4f-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="0fb4f-123">Arrêtez la défragmentation en ligne si elle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="0fb4f-124">Démarrez un nettoyage de la Banque des versions.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="0fb4f-125">Réduisez la profondeur du point de contrôle en commençant à vider les pages incorrectes dans le gestionnaire de tampons.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="0fb4f-126">Empêcher les appels ultérieurs à la plupart des fonctions pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="0fb4f-127">Si cette fonction échoue, aucune des étapes de préparation d’un arrêt de l’instance n’est effectuée, donc aucune modification de l’état de l’instance ne se produit.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0fb4f-128">Notes</span><span class="sxs-lookup"><span data-stu-id="0fb4f-128">Remarks</span></span>

<span data-ttu-id="0fb4f-129">Cette fonction réduit le travail que l’instance doit effectuer une fois qu’elle est terminée, mais ne met pas fin à l’instance.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-129">This function reduces the work the instance will have to do when terminated, but will not terminate the instance.</span></span> <span data-ttu-id="0fb4f-130">Par conséquent, cette fonction est simplement une optimisation et n’est pas obligatoire pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="0fb4f-131">Notez que la quantité de travail effectuée en préparation était moins importante dans Windows 2000 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="0fb4f-132">Une fois la fonction réussie, l’appel de fonctions qui ne sont plus autorisées retourne JET_errClientRequestToStopJetService.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="0fb4f-133">Les fonctions qui sont toujours autorisées après cet appel sont les suivantes : [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="0fb4f-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="0fb4f-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fb4f-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0fb4f-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="0fb4f-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0fb4f-136">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fb4f-137"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="0fb4f-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0fb4f-138">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fb4f-139"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="0fb4f-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0fb4f-140">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0fb4f-141"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="0fb4f-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0fb4f-142">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0fb4f-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0fb4f-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0fb4f-144">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0fb4f-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0fb4f-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fb4f-145">See Also</span></span>

[<span data-ttu-id="0fb4f-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0fb4f-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0fb4f-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0fb4f-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0fb4f-148">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="0fb4f-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="0fb4f-149">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="0fb4f-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="0fb4f-150">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="0fb4f-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="0fb4f-151">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="0fb4f-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="0fb4f-152">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="0fb4f-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="0fb4f-153">JetRollback</span><span class="sxs-lookup"><span data-stu-id="0fb4f-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="0fb4f-154">JetTerm</span><span class="sxs-lookup"><span data-stu-id="0fb4f-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="0fb4f-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="0fb4f-155">JetTerm2</span></span>](./jetterm2-function.md)
