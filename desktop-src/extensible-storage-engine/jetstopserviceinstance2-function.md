---
description: 'En savoir plus sur : fonction JetStopServiceInstance2'
title: JetStopServiceInstance2 fonction)
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752277"
---
# <a name="jetstopserviceinstance2-function"></a><span data-ttu-id="6cc52-103">JetStopServiceInstance2 fonction)</span><span class="sxs-lookup"><span data-stu-id="6cc52-103">JetStopServiceInstance2 Function</span></span>


<span data-ttu-id="6cc52-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="6cc52-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="6cc52-105">La fonction **JetStopServiceInstance2** prépare une instance avant de suspendre et prépare une instance après la reprise.</span><span class="sxs-lookup"><span data-stu-id="6cc52-105">The **JetStopServiceInstance2** function prepares an instance prior to Suspend, and prepares an instance after Resume.</span></span> <span data-ttu-id="6cc52-106">Les États d’interruption et de reprise sont les États d’exécution du modèle de cycle de vie des applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6cc52-106">Suspend and Resume are execution states of the Windows Store App lifecycle model.</span></span>

<span data-ttu-id="6cc52-107">La fonction **JetStopServiceInstance2** a été introduite dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6cc52-107">The **JetStopServiceInstance2** function was introduced in Windows 8.</span></span>

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a><span data-ttu-id="6cc52-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cc52-108">Parameters</span></span>

<span data-ttu-id="6cc52-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="6cc52-109">*instance*</span></span>

<span data-ttu-id="6cc52-110">Instance cible.</span><span class="sxs-lookup"><span data-stu-id="6cc52-110">The target instance.</span></span> <span data-ttu-id="6cc52-111">Le type de données **JET_INSTANCE** est un descripteur de l’instance de la base de données à utiliser pour un appel à l’API jet.</span><span class="sxs-lookup"><span data-stu-id="6cc52-111">The **JET_INSTANCE** data type is a handle to the instance of the database to use for a call to the JET API.</span></span> <span data-ttu-id="6cc52-112">Ce descripteur est obtenu lorsque vous créez une instance de la base de données en appelant les fonctions [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)ou [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6cc52-112">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="6cc52-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6cc52-113">*grbit*</span></span>

<span data-ttu-id="6cc52-114">Groupe de bits qui spécifie une ou plusieurs des valeurs énumérées et définies dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6cc52-114">A group of bits that specifies one or more of the values listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cc52-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cc52-115">Value</span></span></p></th>
<th><p><span data-ttu-id="6cc52-116">Description</span><span class="sxs-lookup"><span data-stu-id="6cc52-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cc52-117">JET_bitStopServiceAll</span><span class="sxs-lookup"><span data-stu-id="6cc52-117">JET_bitStopServiceAll</span></span></p></td>
<td><p><span data-ttu-id="6cc52-118">Arrête tous les services ESE (Extensible Storage Engine) pour l’instance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6cc52-118">Stops all Extensible Storage Engine (ESE) services for the specified instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc52-119">JET_bitStopServiceBackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="6cc52-119">JET_bitStopServiceBackgroundUserTasks</span></span></p></td>
<td><p><span data-ttu-id="6cc52-120">Arrête les tâches de maintenance en arrière-plan du client redémarrables (par exemple, la défragmentation B + Tree).</span><span class="sxs-lookup"><span data-stu-id="6cc52-120">Stops restartable client-specified background maintenance tasks (B+ Tree Defrag, for example).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cc52-121">JET_bitStopServiceQuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="6cc52-121">JET_bitStopServiceQuiesceCaches</span></span></p></td>
<td><p><span data-ttu-id="6cc52-122">Quiesces tous les caches modifiés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="6cc52-122">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="6cc52-123">Cette valeur est asynchrone et peut être annulée.</span><span class="sxs-lookup"><span data-stu-id="6cc52-123">This value is asynchronous and can be canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc52-124">JET_bitStopServiceResume</span><span class="sxs-lookup"><span data-stu-id="6cc52-124">JET_bitStopServiceResume</span></span></p></td>
<td><p><span data-ttu-id="6cc52-125">Reprend les opérations StopService précédemment émises ; autrement dit, il redémarre le service.</span><span class="sxs-lookup"><span data-stu-id="6cc52-125">Resumes previously issued StopService operations; that is, it restarts the service.</span></span> <span data-ttu-id="6cc52-126">Cette valeur peut être combinée avec le paramètre <em>grbits</em> pour reprendre des services spécifiques, ou avec JET_bitStopServiceAll pour reprendre tous les services précédemment arrêtés.</span><span class="sxs-lookup"><span data-stu-id="6cc52-126">This value can be combined with the <em>grbits</em> parameter to resume specific services, or with JET_bitStopServiceAll to Resume all previously stopped services.</span></span> <span data-ttu-id="6cc52-127">Ce bit ne peut être utilisé que pour reprendre StopServiceBackgroundUserTasks et JET_bitStopServiceQuiesceCaches.</span><span class="sxs-lookup"><span data-stu-id="6cc52-127">This bit can only be used to resume StopServiceBackgroundUserTasks and JET_bitStopServiceQuiesceCaches.</span></span> <span data-ttu-id="6cc52-128">Si vous avez précédemment appelé avec JET_bitStopServiceAll, une tentative d’utilisation de JET_bitStopServiceResume échouera.</span><span class="sxs-lookup"><span data-stu-id="6cc52-128">If you previously called with JET_bitStopServiceAll, an attempt to use JET_bitStopServiceResume will fail.</span></span> <span data-ttu-id="6cc52-129">Si la deuxième étape de reprise n’est pas appelée, l’application aura une dégradation des performances.</span><span class="sxs-lookup"><span data-stu-id="6cc52-129">If the second resume step does not get called, the application will have degraded performance.</span></span> <span data-ttu-id="6cc52-130">Dans ce cas, le point de contrôle est conservé à zéro.</span><span class="sxs-lookup"><span data-stu-id="6cc52-130">In this situation the checkpoint is kept at zero.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6cc52-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cc52-131">Return value</span></span>

<span data-ttu-id="6cc52-132">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="6cc52-132">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="6cc52-133">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6cc52-133">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cc52-134">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6cc52-134">Return code</span></span></p></th>
<th><p><span data-ttu-id="6cc52-135">Description</span><span class="sxs-lookup"><span data-stu-id="6cc52-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cc52-136">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6cc52-136">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6cc52-137">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6cc52-137">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6cc52-138">Notes</span><span class="sxs-lookup"><span data-stu-id="6cc52-138">Remarks</span></span>

<span data-ttu-id="6cc52-139">Cette fonction permet à une application JET de déplacer le cache de base de données à un état propre ou presque propre (avec les e/s du système d’exploitation inactives), de sorte que si l’application doit être arrêtée, la récupération est rapide.</span><span class="sxs-lookup"><span data-stu-id="6cc52-139">This function allows a JET application to move the database cache to a clean or nearly clean state (with the operating system I/O idle), such that if the application were to be terminated, recovery would be quick.</span></span> <span data-ttu-id="6cc52-140">Cette approche est préférable à l’arrêt de JET en appelant les fonctions [JetTerm](./jetterm-function.md) ou [JetDetachDatabase](./jetdetachdatabase-function.md) , de sorte que dans le scénario le plus courant, l’application n’est pas suspendue, et par la suite, l’application dispose de l’ensemble du cache et est prête à être utilisée dès que possible.</span><span class="sxs-lookup"><span data-stu-id="6cc52-140">This approach is preferred over terminating JET by calling the [JetTerm](./jetterm-function.md) or [JetDetachDatabase](./jetdetachdatabase-function.md) functions, so that in the more common scenario, the application is just unsuspended, and later the application has the whole cache and is ready to go as soon as possible.</span></span>

<span data-ttu-id="6cc52-141">Si cette fonction est réussie, elle prépare le cache de base de données pour une suspension imminente.</span><span class="sxs-lookup"><span data-stu-id="6cc52-141">If this function succeeds, it prepares the database cache for an imminent suspension.</span></span> <span data-ttu-id="6cc52-142">Cette fonction met en file d’attente le travail sur un thread de travail en arrière-plan et retourne immédiatement à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="6cc52-142">This function queues work to a background worker thread and returns to the caller immediately.</span></span> <span data-ttu-id="6cc52-143">La fonction doit être appelée en fonction de l’VisibilityNotice de PLM, plutôt que d’appeler à partir du gestionnaire d’événements de suspension de l’application pour s’assurer que JET a le temps de vider les tampons modifiés avant que la gestion PLM interrompe/arrête le processus.</span><span class="sxs-lookup"><span data-stu-id="6cc52-143">The function should be called based on the PLM VisibilityNotice as opposed to calling from the application's suspension event handler to ensure that JET has time to flush dirty buffers before PLM suspends/terminates the process.</span></span> <span data-ttu-id="6cc52-144">En interne, JET déclenche une distribution immédiate de la maintenance des points de contrôle lors de la modification de la configuration (soit la mise à jour des points de contrôle, soit le nouveau bit de suspension des caches).</span><span class="sxs-lookup"><span data-stu-id="6cc52-144">Internally, JET triggers an immediate dispatch of checkpoint maintenance upon configuration change (either checkpoint update or this new quiesce caches bit).</span></span> <span data-ttu-id="6cc52-145">Pour plus d’informations sur les événements VisibilityNotice, consultez [classe VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span><span class="sxs-lookup"><span data-stu-id="6cc52-145">For more information about VisibilityNotice events, see [VisibilityChangedEventArgs class](/uwp/api/windows.ui.core.visibilitychangedeventargs).</span></span>

<span data-ttu-id="6cc52-146">Cette fonction doit être appelée deux fois.</span><span class="sxs-lookup"><span data-stu-id="6cc52-146">This function must be called twice.</span></span> <span data-ttu-id="6cc52-147">Elle est appelée une fois que l’application a reçu l’avis de suspension du système d’exploitation, mais avant que l’application ne soit interrompue.</span><span class="sxs-lookup"><span data-stu-id="6cc52-147">It is called after the application receives the suspension notice from the operating system, but before the application has been suspended.</span></span> <span data-ttu-id="6cc52-148">Ensuite, il est à nouveau appelé après que le système d’exploitation a repris l’application.</span><span class="sxs-lookup"><span data-stu-id="6cc52-148">Then it is called again after the operating system resumes the application.</span></span> <span data-ttu-id="6cc52-149">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="6cc52-149">For example:</span></span>

<span data-ttu-id="6cc52-150">En cas d’appel pour suspendre : JET_ERR JET_API JetStopServiceInstance2 (instance, JET_bitStopServiceQuiesceCaches);</span><span class="sxs-lookup"><span data-stu-id="6cc52-150">When called to Suspend: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches);</span></span>

<span data-ttu-id="6cc52-151">En cas de reprise : JET_ERR JET_API JetStopServiceInstance2 (instance, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);</span><span class="sxs-lookup"><span data-stu-id="6cc52-151">When Resumed: JET_ERR JET_API JetStopServiceInstance2( instance, JET_bitStopServiceQuiesceCaches|JET_bitStopServiceResume );</span></span>

#### <a name="requirements"></a><span data-ttu-id="6cc52-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cc52-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cc52-153"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6cc52-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc52-154">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6cc52-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc52-155"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="6cc52-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc52-156">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6cc52-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cc52-157"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="6cc52-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc52-158">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="6cc52-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc52-159"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="6cc52-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc52-160">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6cc52-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cc52-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6cc52-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc52-162">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6cc52-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6cc52-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cc52-163">See also</span></span>

[<span data-ttu-id="6cc52-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6cc52-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6cc52-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6cc52-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="6cc52-166">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="6cc52-166">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="6cc52-167">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="6cc52-167">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="6cc52-168">JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="6cc52-168">JetDetachDatabase</span></span>](./jetdetachdatabase-function.md)  
[<span data-ttu-id="6cc52-169">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="6cc52-169">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="6cc52-170">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="6cc52-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="6cc52-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="6cc52-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="6cc52-172">JetTerm</span><span class="sxs-lookup"><span data-stu-id="6cc52-172">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="6cc52-173">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="6cc52-173">JetTerm2</span></span>](./jetterm2-function.md)
