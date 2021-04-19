---
description: 'En savoir plus sur : fonction JetCreateInstance2'
title: Fonction JetCreateInstance2
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af31e7e66d92cf7ebbc238ac54a9b331e6dc5362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521090"
---
# <a name="jetcreateinstance2-function"></a><span data-ttu-id="c96cf-103">Fonction JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="c96cf-103">JetCreateInstance2 Function</span></span>


<span data-ttu-id="c96cf-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c96cf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance2-function"></a><span data-ttu-id="c96cf-105">Fonction JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="c96cf-105">JetCreateInstance2 Function</span></span>

<span data-ttu-id="c96cf-106">La fonction **JetCreateInstance2** est utilisée pour allouer une nouvelle instance du moteur de base de données pour une utilisation dans un processus unique, avec un nom d’affichage spécifié.</span><span class="sxs-lookup"><span data-stu-id="c96cf-106">The **JetCreateInstance2** function is used to allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="c96cf-107">**Windows XP :**  **JetCreateInstance2** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c96cf-107">**Windows XP:**  **JetCreateInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c96cf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c96cf-108">Parameters</span></span>

<span data-ttu-id="c96cf-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="c96cf-109">*pinstance*</span></span>

<span data-ttu-id="c96cf-110">Mémoire tampon de sortie qui recevra l’instance nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="c96cf-110">The output buffer that will receive the newly created instance.</span></span>

<span data-ttu-id="c96cf-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="c96cf-111">*szInstanceName*</span></span>

<span data-ttu-id="c96cf-112">Spécifie un identificateur de chaîne unique pour l’instance à créer.</span><span class="sxs-lookup"><span data-stu-id="c96cf-112">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="c96cf-113">Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="c96cf-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="c96cf-114">**Remarque** Une valeur NULL est traitée comme un identificateur de chaîne valide pour une instance.</span><span class="sxs-lookup"><span data-stu-id="c96cf-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="c96cf-115">Une seule instance peut avoir un identificateur de chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="c96cf-115">Only one instance may have a NULL string identifier.</span></span>

<span data-ttu-id="c96cf-116">*szDisplayName*</span><span class="sxs-lookup"><span data-stu-id="c96cf-116">*szDisplayName*</span></span>

<span data-ttu-id="c96cf-117">Nom complet de l’instance à créer.</span><span class="sxs-lookup"><span data-stu-id="c96cf-117">A display name for the instance to be created.</span></span> <span data-ttu-id="c96cf-118">Lorsque ce paramètre n’est pas présent, sa valeur est supposée être NULL.</span><span class="sxs-lookup"><span data-stu-id="c96cf-118">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="c96cf-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c96cf-119">*grbit*</span></span>

<span data-ttu-id="c96cf-120">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="c96cf-120">Reserved for future use.</span></span> <span data-ttu-id="c96cf-121">Quand ce paramètre n’est pas présent, sa valeur est supposée être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c96cf-121">When this parameter is not present, its value is presumed to be zero.</span></span>

### <a name="return-value"></a><span data-ttu-id="c96cf-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c96cf-122">Return Value</span></span>

<span data-ttu-id="c96cf-123">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="c96cf-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c96cf-124">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c96cf-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c96cf-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c96cf-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="c96cf-126">Description</span><span class="sxs-lookup"><span data-stu-id="c96cf-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c96cf-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c96cf-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c96cf-128">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="c96cf-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c96cf-129">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="c96cf-129">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="c96cf-130">Le nom d’instance spécifié est déjà utilisé pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="c96cf-130">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c96cf-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c96cf-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c96cf-132">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="c96cf-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="c96cf-133">Cela peut se produire pour <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> lorsque <em>pinstance</em> a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="c96cf-133">This can happen for <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> when <em>pinstance</em> is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c96cf-134">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="c96cf-134">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="c96cf-135">L’opération a échoué, car elle ne peut pas être utilisée lorsque le moteur de base de données fonctionne en mode d’instance unique (mode de compatibilité Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="c96cf-135">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c96cf-136">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="c96cf-136">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="c96cf-137">Impossible de créer une nouvelle instance, car le nombre maximal d’instances a été atteint.</span><span class="sxs-lookup"><span data-stu-id="c96cf-137">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="c96cf-138">Le nombre maximal d’instances prises en charge est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> à l’aide de <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="c96cf-138">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c96cf-139">En cas de réussite, une nouvelle instance sera allouée et l’identificateur correspondant sera retourné.</span><span class="sxs-lookup"><span data-stu-id="c96cf-139">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="c96cf-140">À ce stade, tous les paramètres système de l’instance auront les valeurs des paramètres système par défaut globaux.</span><span class="sxs-lookup"><span data-stu-id="c96cf-140">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="c96cf-141">Une fois qu’une instance sera allouée, elle doit être arrêtée et/ou libérée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="c96cf-141">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="c96cf-142">En cas d’échec, une erreur qui représente la cause de l’échec est retournée et aucune instance n’est allouée.</span><span class="sxs-lookup"><span data-stu-id="c96cf-142">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c96cf-143">Notes</span><span class="sxs-lookup"><span data-stu-id="c96cf-143">Remarks</span></span>

<span data-ttu-id="c96cf-144">Une instance doit être initialisée avec un appel à [JetInit](./jetinit-function.md) avant de pouvoir être utilisée par une autre chose que [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="c96cf-144">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="c96cf-145">Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="c96cf-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="c96cf-146">Le nombre maximal d’instances pouvant être créées à un moment donné est contrôlé par *JET_paramMaxInstances*, qui peut être configurée par un appel à [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="c96cf-146">The maximum number of instances that may be created at any one time is controlled by *JET_paramMaxInstances*, which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="c96cf-147">Une instance est l’unité de récupérabilité pour le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="c96cf-147">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="c96cf-148">Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="c96cf-148">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="c96cf-149">Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="c96cf-149">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="c96cf-150">Si la fonction s’exécute correctement, le moteur de base de données est automatiquement remplacé par le mode multi-instance comme un effet secondaire de cet appel.</span><span class="sxs-lookup"><span data-stu-id="c96cf-150">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="c96cf-151">Si l’application souhaite autoriser une seule instance du processus, [JetInit](./jetinit-function.md) doit être utilisé pour démarrer le moteur de base de données en mode de compatibilité Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c96cf-151">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="c96cf-152">S’il est présent, le paramètre *szDisplayName* sera utilisé pour identifier l’instance dans des emplacements tels que le journal des événements ou vers d’autres appelants comme des applications de sauvegarde (via des fonctions telles que [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="c96cf-152">If present, the *szDisplayName* parameter will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="c96cf-153">Si le nom complet n’est pas fourni, le paramètre *szInstanceName* unique sera utilisé à la place, s’il existe, dans le cas contraire, une chaîne vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="c96cf-153">If the display name is not provided, the unique *szInstanceName* parameter will be used instead, if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="c96cf-154">Si le mode d’exécution n’a pas été défini pour le moteur, après cet appel, il sera défini en mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="c96cf-154">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="c96cf-155">La séquence de démarrage classique d’un processus potentiellement exécutant plusieurs instances de jet serait la suivante :</span><span class="sxs-lookup"><span data-stu-id="c96cf-155">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="c96cf-156">Un appel à **JetCreateInstance2** , qui allouera et nommera l’instance.</span><span class="sxs-lookup"><span data-stu-id="c96cf-156">A call to **JetCreateInstance2** which will allocate and name the instance.</span></span>

  - <span data-ttu-id="c96cf-157">Plusieurs appels à [JetSetSystemParameter](./jetsetsystemparameter-function.md) pour cette instance afin de définir différents paramètres système.</span><span class="sxs-lookup"><span data-stu-id="c96cf-157">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="c96cf-158">Notez que certains paramètres système doivent être uniques pour chaque instance (comme *JET_paramSystemPath* ou *JET_paramLogFilePath*). il est donc très probable que chacun d’eux doive être défini.</span><span class="sxs-lookup"><span data-stu-id="c96cf-158">Note that some system parameters need to be unique for each instance (like *JET_paramSystemPath* or *JET_paramLogFilePath*) so most likely, each of these will need to be set.</span></span>

  - <span data-ttu-id="c96cf-159">Démarrez l’instance à l’aide de [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="c96cf-159">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="c96cf-160">Pour arrêter et/ou libérer une instance, utilisez [JetTerm](./jetterm-function.md) ou [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="c96cf-160">In order to terminate and/or free an instance, use [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="c96cf-161">S’il s’agit de la première instance à démarrer, il existe un certain nombre d’étapes supplémentaires qui seront exécutées au cours de cet appel afin d’effectuer une initialisation et une configuration de base du système.</span><span class="sxs-lookup"><span data-stu-id="c96cf-161">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="c96cf-162">Un certain nombre de ces étapes peuvent entraîner des erreurs spécifiques à partir de JET_errOutOfMemory mais d’autres encore (voir les valeurs de retour pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="c96cf-162">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see Return Values for more information).</span></span>

#### <a name="requirements"></a><span data-ttu-id="c96cf-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c96cf-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c96cf-164"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c96cf-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c96cf-165">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c96cf-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c96cf-166"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c96cf-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c96cf-167">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c96cf-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c96cf-168"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c96cf-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c96cf-169">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c96cf-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c96cf-170"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="c96cf-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c96cf-171">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c96cf-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c96cf-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c96cf-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c96cf-173">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c96cf-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c96cf-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c96cf-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c96cf-175">Implémenté en tant que <strong>JetCreateInstance2W</strong> (Unicode) et <strong>JetCreateInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c96cf-175">Implemented as <strong>JetCreateInstance2W</strong> (Unicode) and <strong>JetCreateInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c96cf-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c96cf-176">See Also</span></span>

[<span data-ttu-id="c96cf-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c96cf-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c96cf-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c96cf-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c96cf-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c96cf-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="c96cf-180">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="c96cf-180">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="c96cf-181">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="c96cf-181">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="c96cf-182">JetInit</span><span class="sxs-lookup"><span data-stu-id="c96cf-182">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="c96cf-183">JetInit2</span><span class="sxs-lookup"><span data-stu-id="c96cf-183">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="c96cf-184">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="c96cf-184">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="c96cf-185">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c96cf-185">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="c96cf-186">JetTerm</span><span class="sxs-lookup"><span data-stu-id="c96cf-186">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="c96cf-187">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="c96cf-187">JetTerm2</span></span>](./jetterm2-function.md)
