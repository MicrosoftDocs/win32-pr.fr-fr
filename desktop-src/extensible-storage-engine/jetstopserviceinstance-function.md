---
description: 'En savoir plus sur : fonction JetStopServiceInstance'
title: JetStopServiceInstance fonction)
TOCTitle: JetStopServiceInstance Function
ms:assetid: d8d3d047-91d6-4054-b3e1-44174666900e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294108(v=EXCHG.10)
ms:contentKeyID: 32765723
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopServiceInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9b2e3307f13a63d00cbbaf33f491750bbfcdb9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532079"
---
# <a name="jetstopserviceinstance-function"></a><span data-ttu-id="cc360-103">JetStopServiceInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="cc360-103">JetStopServiceInstance Function</span></span>


<span data-ttu-id="cc360-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="cc360-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopserviceinstance-function"></a><span data-ttu-id="cc360-105">JetStopServiceInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="cc360-105">JetStopServiceInstance Function</span></span>

<span data-ttu-id="cc360-106">La fonction **JetStopServiceInstance** prépare une instance pour l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="cc360-106">The **JetStopServiceInstance** function prepares an instance for termination.</span></span>

<span data-ttu-id="cc360-107">**Windows XP :**  **JetStopServiceInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc360-107">**Windows XP:**  **JetStopServiceInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetStopServiceInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="cc360-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc360-108">Parameters</span></span>

<span data-ttu-id="cc360-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="cc360-109">*instance*</span></span>

<span data-ttu-id="cc360-110">Instance en cours d’exécution à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="cc360-110">The running instance to use for the API call.</span></span>

### <a name="return-value"></a><span data-ttu-id="cc360-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc360-111">Return Value</span></span>

<span data-ttu-id="cc360-112">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="cc360-112">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cc360-113">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cc360-113">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc360-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cc360-114">Return code</span></span></p></th>
<th><p><span data-ttu-id="cc360-115">Description</span><span class="sxs-lookup"><span data-stu-id="cc360-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc360-116">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cc360-116">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cc360-117">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="cc360-117">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc360-118">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="cc360-118">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="cc360-119">Le paramètre d’instance spécifié a une valeur non valide (pas une instance en cours d’exécution).</span><span class="sxs-lookup"><span data-stu-id="cc360-119">The specified instance parameter has an invalid value (not an instance that is currently running).</span></span></p>
<p><span data-ttu-id="cc360-120"><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc360-120"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cc360-121">Si cette fonction est réussie, elle se prépare à un arrêt ultérieur.</span><span class="sxs-lookup"><span data-stu-id="cc360-121">If this function succeeds, it prepares for a future termination.</span></span> <span data-ttu-id="cc360-122">Les étapes à suivre pour préparer un arrêt sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc360-122">The steps taken to prepare for a termination include the following:</span></span>

  - <span data-ttu-id="cc360-123">Arrêtez la défragmentation en ligne si elle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cc360-123">Stop online defragmentation if it is running.</span></span>

  - <span data-ttu-id="cc360-124">Démarrez un nettoyage de la Banque des versions.</span><span class="sxs-lookup"><span data-stu-id="cc360-124">Start a version store clean-up.</span></span>

  - <span data-ttu-id="cc360-125">Réduisez la profondeur du point de contrôle en commençant à vider les pages incorrectes dans le gestionnaire de tampons.</span><span class="sxs-lookup"><span data-stu-id="cc360-125">Reduce the checkpoint depth by starting to flush dirty pages in the buffer manager.</span></span>

  - <span data-ttu-id="cc360-126">Empêcher les appels ultérieurs à la plupart des fonctions pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="cc360-126">Prevent future calls to most functions for that instance.</span></span>

<span data-ttu-id="cc360-127">Si cette fonction échoue, aucune des étapes de préparation d’un arrêt de l’instance n’est effectuée, donc aucune modification de l’état de l’instance ne se produit.</span><span class="sxs-lookup"><span data-stu-id="cc360-127">If this function fails, none of the steps to prepare for an instance termination will be taken, so no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="cc360-128">Notes</span><span class="sxs-lookup"><span data-stu-id="cc360-128">Remarks</span></span>

<span data-ttu-id="cc360-129">Cette fonction permet de réduire le travail que l’instance doit effectuer une fois terminé, mais ne met pas fin à l’instance.</span><span class="sxs-lookup"><span data-stu-id="cc360-129">This function will reduce the work the instance will have to do when terminated but will not terminate the instance.</span></span> <span data-ttu-id="cc360-130">Par conséquent, cette fonction est simplement une optimisation et n’est pas obligatoire pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="cc360-130">As a result, this function is just an optimization and is not mandatory to use.</span></span> <span data-ttu-id="cc360-131">Notez que la quantité de travail effectuée en préparation était moins importante dans Windows 2000 et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc360-131">Note that the amount of work done in preparation was less in Windows 2000 and Windows XP.</span></span> <span data-ttu-id="cc360-132">Une fois la fonction réussie, l’appel de fonctions qui ne sont plus autorisées retourne JET_errClientRequestToStopJetService.</span><span class="sxs-lookup"><span data-stu-id="cc360-132">Once the function succeeds, calling functions that are no longer allowed will return JET_errClientRequestToStopJetService.</span></span> <span data-ttu-id="cc360-133">Les fonctions qui sont toujours autorisées après cet appel sont les suivantes : [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="cc360-133">Functions that are still allowed after this call are: [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="cc360-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc360-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc360-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cc360-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cc360-136">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc360-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc360-137"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="cc360-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cc360-138">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cc360-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc360-139"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="cc360-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cc360-140">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="cc360-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc360-141"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="cc360-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cc360-142">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cc360-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc360-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cc360-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cc360-144">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cc360-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cc360-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc360-145">See Also</span></span>

[<span data-ttu-id="cc360-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cc360-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cc360-147">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cc360-147">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="cc360-148">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="cc360-148">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="cc360-149">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="cc360-149">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="cc360-150">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="cc360-150">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="cc360-151">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="cc360-151">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="cc360-152">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="cc360-152">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="cc360-153">JetRollback</span><span class="sxs-lookup"><span data-stu-id="cc360-153">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="cc360-154">JetTerm</span><span class="sxs-lookup"><span data-stu-id="cc360-154">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="cc360-155">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="cc360-155">JetTerm2</span></span>](./jetterm2-function.md)
