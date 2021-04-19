---
description: 'En savoir plus sur : fonction JetCreateInstance'
title: Fonction JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529472"
---
# <a name="jetcreateinstance-function"></a><span data-ttu-id="7b7b6-103">Fonction JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="7b7b6-103">JetCreateInstance Function</span></span>


<span data-ttu-id="7b7b6-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="7b7b6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance-function"></a><span data-ttu-id="7b7b6-105">Fonction JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="7b7b6-105">JetCreateInstance Function</span></span>

<span data-ttu-id="7b7b6-106">La fonction **JetCreateInstance** alloue une nouvelle instance du moteur de base de données pour une utilisation dans un processus unique.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-106">The **JetCreateInstance** function allocates a new instance of the database engine for use in a single process.</span></span>

<span data-ttu-id="7b7b6-107">**Windows XP : JetCreateInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-107">**Windows XP:  JetCreateInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a><span data-ttu-id="7b7b6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b7b6-108">Parameters</span></span>

<span data-ttu-id="7b7b6-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="7b7b6-109">*pinstance*</span></span>

<span data-ttu-id="7b7b6-110">Mémoire tampon de sortie qui reçoit l’instance nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-110">The output buffer that receives the newly-created instance.</span></span>

<span data-ttu-id="7b7b6-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="7b7b6-111">*szInstanceName*</span></span>

<span data-ttu-id="7b7b6-112">Identificateur de chaîne unique pour l’instance à créer.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-112">A unique string identifier for the instance to be created.</span></span> <span data-ttu-id="7b7b6-113">Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="7b7b6-114">**Remarque** Une valeur NULL est traitée comme un identificateur de chaîne valide pour une instance.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="7b7b6-115">Une seule instance peut avoir un identificateur de chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-115">Only one instance may have a NULL string identifier.</span></span>

### <a name="return-value"></a><span data-ttu-id="7b7b6-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7b7b6-116">Return Value</span></span>

<span data-ttu-id="7b7b6-117">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7b7b6-118">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b7b6-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7b7b6-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="7b7b6-120">Description</span><span class="sxs-lookup"><span data-stu-id="7b7b6-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b7b6-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7b7b6-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7b7b6-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b7b6-123">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="7b7b6-123">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="7b7b6-124">Le nom d’instance spécifié est déjà utilisé pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-124">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b7b6-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7b7b6-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7b7b6-126">L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-126">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="7b7b6-127">Cela peut se produire pour <strong>JetCreateInstance</strong> lorsque <em>Pinstance</em> a la <strong>valeur null</strong>.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-127">This can happen for <strong>JetCreateInstance</strong> when <em>pinstance</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b7b6-128">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="7b7b6-128">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="7b7b6-129">L’opération a échoué, car elle ne peut pas être utilisée lorsque le moteur de base de données fonctionne en mode d’instance unique (mode de compatibilité Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-129">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b7b6-130">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="7b7b6-130">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="7b7b6-131">Impossible de créer une nouvelle instance, car le nombre maximal d’instances a été atteint.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-131">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="7b7b6-132">Le nombre maximal d’instances prises en charge est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> à l’aide de <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-132">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7b7b6-133">En cas de réussite, une nouvelle instance sera allouée et l’identificateur correspondant sera retourné.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-133">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="7b7b6-134">À ce stade, tous les paramètres système de l’instance auront les valeurs des paramètres système par défaut globaux.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-134">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="7b7b6-135">Une fois qu’une instance sera allouée, elle doit être arrêtée et/ou libérée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-135">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="7b7b6-136">En cas d’échec, une erreur qui représente la cause de l’échec est retournée et aucune instance n’est allouée.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-136">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7b7b6-137">Notes</span><span class="sxs-lookup"><span data-stu-id="7b7b6-137">Remarks</span></span>

<span data-ttu-id="7b7b6-138">Une instance doit être initialisée avec un appel à [JetInit](./jetinit-function.md) avant de pouvoir être utilisée par une autre chose que [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-138">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="7b7b6-139">Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-139">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="7b7b6-140">Le nombre maximal d’instances pouvant être créées à un moment donné est contrôlé par [JET_paramMaxInstances](./resource-parameters.md), qui peut être configurée par un appel à [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-140">The maximum number of instances that may be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="7b7b6-141">Une instance est l’unité de récupérabilité pour le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-141">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="7b7b6-142">Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-142">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="7b7b6-143">Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-143">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="7b7b6-144">Si la fonction s’exécute correctement, le moteur de base de données est automatiquement remplacé par le mode multi-instance comme un effet secondaire de cet appel.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-144">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="7b7b6-145">Si l’application souhaite autoriser une seule instance du processus, [JetInit](./jetinit-function.md) doit être utilisé pour démarrer le moteur de base de données en mode de compatibilité Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-145">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="7b7b6-146">S’il est présent, le *szDisplayName* sera utilisé pour identifier l’instance dans des emplacements tels que le journal des événements ou vers d’autres appelants comme des applications de sauvegarde (via des fonctions telles que [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-146">If present, the *szDisplayName* will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="7b7b6-147">Si le nom complet n’est pas fourni, le *szInstanceName* unique est utilisé à la place, s’il est présent ; sinon, une chaîne vide est retournée.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-147">If the display name is not provided, the unique *szInstanceName* will be used instead if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="7b7b6-148">Si le mode d’exécution n’a pas été défini pour le moteur, après cet appel, il sera défini en mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-148">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="7b7b6-149">La séquence de démarrage classique d’un processus potentiellement exécutant plusieurs instances de jet serait la suivante :</span><span class="sxs-lookup"><span data-stu-id="7b7b6-149">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="7b7b6-150">Un appel à [JetCreateInstance2](./jetcreateinstance2-function.md) , qui allouera et nommera l’instance.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-150">A call to [JetCreateInstance2](./jetcreateinstance2-function.md) which will allocate and name the instance.</span></span>

  - <span data-ttu-id="7b7b6-151">Plusieurs appels à [JetSetSystemParameter](./jetsetsystemparameter-function.md) pour cette instance afin de définir différents paramètres système.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-151">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="7b7b6-152">Notez que certains paramètres système doivent être uniques par instance (comme [JET_paramSystemPath](./transaction-log-parameters.md) ou [JET_paramLogFilePath](./transaction-log-parameters.md)). il est donc très probable que vous deviez définir chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-152">Note that some system parameters need to be unique per instance (like [JET_paramSystemPath](./transaction-log-parameters.md) or [JET_paramLogFilePath](./transaction-log-parameters.md)) so most likely one will need to set each of those.</span></span>

  - <span data-ttu-id="7b7b6-153">Démarrez l’instance à l’aide de [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-153">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="7b7b6-154">Pour arrêter et/ou libérer une instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-154">In order to terminate and/or free an instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) needs to be used.</span></span>

<span data-ttu-id="7b7b6-155">S’il s’agit de la première instance à démarrer, il existe un certain nombre d’étapes supplémentaires qui seront exécutées au cours de cet appel afin d’effectuer une initialisation et une configuration de base du système.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-155">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="7b7b6-156">Un certain nombre de ces étapes peuvent entraîner des erreurs spécifiques à partir de JET_errOutOfMemory mais d’autres également (voir les erreurs ci-dessus).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-156">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see errors above).</span></span>

#### <a name="requirements"></a><span data-ttu-id="7b7b6-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b7b6-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b7b6-158"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="7b7b6-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7b7b6-159">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b7b6-160"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="7b7b6-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7b7b6-161">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b7b6-162"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="7b7b6-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7b7b6-163">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b7b6-164"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="7b7b6-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7b7b6-165">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b7b6-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7b7b6-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7b7b6-167">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7b7b6-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b7b6-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="7b7b6-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="7b7b6-169">Implémenté en tant que <strong>JetCreateInstanceW</strong> (Unicode) et <strong>JetCreateInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="7b7b6-169">Implemented as <strong>JetCreateInstanceW</strong> (Unicode) and <strong>JetCreateInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7b7b6-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b7b6-170">See Also</span></span>

[<span data-ttu-id="7b7b6-171">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="7b7b6-171">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="7b7b6-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7b7b6-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7b7b6-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="7b7b6-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="7b7b6-174">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="7b7b6-174">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="7b7b6-175">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="7b7b6-175">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="7b7b6-176">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="7b7b6-176">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="7b7b6-177">JetInit</span><span class="sxs-lookup"><span data-stu-id="7b7b6-177">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="7b7b6-178">JetInit2</span><span class="sxs-lookup"><span data-stu-id="7b7b6-178">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="7b7b6-179">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="7b7b6-179">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="7b7b6-180">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="7b7b6-180">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="7b7b6-181">JetTerm</span><span class="sxs-lookup"><span data-stu-id="7b7b6-181">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="7b7b6-182">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="7b7b6-182">JetTerm2</span></span>](./jetterm2-function.md)
