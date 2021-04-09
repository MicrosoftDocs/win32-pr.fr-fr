---
description: 'En savoir plus sur : fonction JetInit2'
title: Fonction JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954036"
---
# <a name="jetinit2-function"></a><span data-ttu-id="fd19d-103">Fonction JetInit2</span><span class="sxs-lookup"><span data-stu-id="fd19d-103">JetInit2 Function</span></span>


<span data-ttu-id="fd19d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="fd19d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit2-function"></a><span data-ttu-id="fd19d-105">Fonction JetInit2</span><span class="sxs-lookup"><span data-stu-id="fd19d-105">JetInit2 Function</span></span>

<span data-ttu-id="fd19d-106">La fonction **JetInit2** met le moteur de base de données dans un État où il peut prendre en charge l’utilisation des fichiers de base de données par l’application.</span><span class="sxs-lookup"><span data-stu-id="fd19d-106">The **JetInit2** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="fd19d-107">Le moteur doit déjà être correctement configuré pour l’initialisation à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="fd19d-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="fd19d-108">La récupération après incident de la base de données s’effectue automatiquement dans le cadre du processus d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="fd19d-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

<span data-ttu-id="fd19d-109">**Windows XP :**  **JetInit2** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd19d-109">**Windows XP:**  **JetInit2** is introduced in Windows XP.</span></span>

<span data-ttu-id="fd19d-110">Cette fonction est obsolète.</span><span class="sxs-lookup"><span data-stu-id="fd19d-110">This function is obsolete.</span></span> <span data-ttu-id="fd19d-111">Utilisez [JetInit3](./jetinit3-function.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="fd19d-111">Use [JetInit3](./jetinit3-function.md) instead.</span></span>

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="fd19d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd19d-112">Parameters</span></span>

<span data-ttu-id="fd19d-113">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="fd19d-113">*pinstance*</span></span>

<span data-ttu-id="fd19d-114">Instance à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="fd19d-114">The instance to use for this call.</span></span>

<span data-ttu-id="fd19d-115">Pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="fd19d-115">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="fd19d-116">Pour Windows XP et versions ultérieures, l’utilisation de ce paramètre dépend du mode de fonctionnement du moteur.</span><span class="sxs-lookup"><span data-stu-id="fd19d-116">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="fd19d-117">Si le moteur fonctionne en mode hérité (mode de compatibilité de Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la valeur NULL ou il peut être défini sur une mémoire tampon de sortie valide contenant la valeur NULL ou JET_instanceNil qui retourne le handle d’instance global créé comme un effet secondaire de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="fd19d-117">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil which returns the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="fd19d-118">Ce descripteur d’instance peut ensuite être passé à toute autre API qui prend une instance.</span><span class="sxs-lookup"><span data-stu-id="fd19d-118">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="fd19d-119">Si le moteur fonctionne en mode multi-instance, ce paramètre doit être défini sur une mémoire tampon d’entrée valide qui contient le handle d’instance retourné par le [JetCreateInstance](./jetcreateinstance-function.md) en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="fd19d-119">If the engine is operating in multi-instance mode, this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="fd19d-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="fd19d-120">*grbit*</span></span>

<span data-ttu-id="fd19d-121">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="fd19d-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd19d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd19d-122">Value</span></span></p></th>
<th><p><span data-ttu-id="fd19d-123">Signification</span><span class="sxs-lookup"><span data-stu-id="fd19d-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd19d-124">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="fd19d-124">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="fd19d-125">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="fd19d-125">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd19d-126">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="fd19d-126">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="fd19d-127">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="fd19d-127">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd19d-128">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="fd19d-128">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="fd19d-129">Cette option permet à l’utilisateur d’exécuter la récupération sur un ensemble de fichiers journaux, sans que toutes les bases de données présentes, soient attachées à un point du jeu de journaux.</span><span class="sxs-lookup"><span data-stu-id="fd19d-129">This option allows the user to run recovery on a set of log files, without all of the databases being present, that were attached at one point of the log set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd19d-130">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="fd19d-130">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="fd19d-131">Effectuer la récupération, mais s’arrêter à la phase de restauration.</span><span class="sxs-lookup"><span data-stu-id="fd19d-131">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="fd19d-132">Cela permet la copie et l’application des journaux de transactions supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fd19d-132">This allows additional transaction logs to copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd19d-133">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="fd19d-133">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="fd19d-134">En cas de récupération logicielle réussie, tronquez les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="fd19d-134">On successful soft recovery, truncate log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd19d-135">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="fd19d-135">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="fd19d-136">L’entrée de mappage de base de données est manquante par défaut au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="fd19d-136">Missing database map entry default to same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd19d-137">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="fd19d-137">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="fd19d-138">Ignorer les journaux perdus à la fin du flux de journal.</span><span class="sxs-lookup"><span data-stu-id="fd19d-138">Ignore logs lost from the end of the log stream.</span></span></p>
<p><span data-ttu-id="fd19d-139"><strong>Windows 7 : JET_bitReplayIgnoreLostLogs</strong> est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fd19d-139"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="fd19d-140">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd19d-140">Return Value</span></span>

<span data-ttu-id="fd19d-141">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="fd19d-141">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fd19d-142">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fd19d-142">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="fd19d-143">Notes</span><span class="sxs-lookup"><span data-stu-id="fd19d-143">Remarks</span></span>

<span data-ttu-id="fd19d-144">Une instance doit être initialisée avec un appel à **JetInit2** avant de pouvoir être utilisée par une autre chose que [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="fd19d-144">An instance must be initialized with a call to **JetInit2** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="fd19d-145">Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="fd19d-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="fd19d-146">Une instance est l’unité de récupérabilité pour le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="fd19d-146">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="fd19d-147">Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="fd19d-147">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="fd19d-148">Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="fd19d-148">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="fd19d-149">Si la récupération s’exécute sur un ensemble de journaux, pour lesquels toutes les bases de données ne sont pas présentes (ce qui renvoie l’erreur JET_errAttachedDatabaseMismatch dans des conditions normales), et que le client souhaite que la récupération se poursuive malgré les bases de données manquantes, le JET_ bitReplayIgnoreMissingDB est utilisé pour poursuivre la récupération des bases de données disponibles.</span><span class="sxs-lookup"><span data-stu-id="fd19d-149">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="fd19d-150">Pour plus d’informations, consultez la section Notes dans [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="fd19d-150">See the Remarks section in [JetInit](./jetinit-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fd19d-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd19d-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd19d-152"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fd19d-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fd19d-153">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd19d-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd19d-154"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="fd19d-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fd19d-155">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fd19d-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd19d-156"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="fd19d-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fd19d-157">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="fd19d-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd19d-158"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="fd19d-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fd19d-159">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fd19d-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd19d-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fd19d-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fd19d-161">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fd19d-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fd19d-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd19d-162">See Also</span></span>

[<span data-ttu-id="fd19d-163">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="fd19d-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="fd19d-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fd19d-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fd19d-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fd19d-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fd19d-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="fd19d-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="fd19d-167">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="fd19d-167">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="fd19d-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="fd19d-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="fd19d-169">JetInit3</span><span class="sxs-lookup"><span data-stu-id="fd19d-169">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="fd19d-170">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="fd19d-170">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="fd19d-171">Paramètres de ressource</span><span class="sxs-lookup"><span data-stu-id="fd19d-171">Resource Parameters</span></span>](./resource-parameters.md)
