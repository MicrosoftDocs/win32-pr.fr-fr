---
description: 'En savoir plus sur : fonction JetInit3'
title: Fonction JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321145"
---
# <a name="jetinit3-function"></a><span data-ttu-id="cc761-103">Fonction JetInit3</span><span class="sxs-lookup"><span data-stu-id="cc761-103">JetInit3 Function</span></span>


<span data-ttu-id="cc761-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="cc761-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit3-function"></a><span data-ttu-id="cc761-105">Fonction JetInit3</span><span class="sxs-lookup"><span data-stu-id="cc761-105">JetInit3 Function</span></span>

<span data-ttu-id="cc761-106">La fonction **JetInit3** place le moteur de base de données dans un État dans lequel il peut prendre en charge l’utilisation des fichiers de base de données par l’application.</span><span class="sxs-lookup"><span data-stu-id="cc761-106">The **JetInit3** function puts the database engine into a state in which it can support application use of database files.</span></span> <span data-ttu-id="cc761-107">Le moteur doit déjà être correctement configuré pour l’initialisation, ce que vous effectuez à l’aide de la fonction [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cc761-107">The engine must already be properly configured for initialization, which you accomplish by using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span> <span data-ttu-id="cc761-108">Notez que la récupération après incident de la base de données se produit automatiquement dans le cadre du processus d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="cc761-108">Note that database crash recovery occurs automatically as a part of the initialization process.</span></span>

<span data-ttu-id="cc761-109">**Windows Vista :**  **JetInit3** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc761-109">**Windows Vista:**  **JetInit3** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="cc761-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc761-110">Parameters</span></span>

<span data-ttu-id="cc761-111">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="cc761-111">*pinstance*</span></span>

<span data-ttu-id="cc761-112">Instance que vous utilisez pour un appel particulier.</span><span class="sxs-lookup"><span data-stu-id="cc761-112">The instance that you use for a particular call.</span></span> <span data-ttu-id="cc761-113">L’utilisation de ce paramètre dépend du mode de fonctionnement du moteur.</span><span class="sxs-lookup"><span data-stu-id="cc761-113">The use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="cc761-114">Si le moteur fonctionne en mode hérité (mode de compatibilité Windows 2000), dans lequel une seule instance est prise en charge, vous pouvez définir ce paramètre sur **null** ou sur une mémoire tampon de sortie valide contenant **null** ou JET_instanceNil, qui retourne le handle d’instance global créé comme un effet secondaire de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="cc761-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode), in which only one instance is supported, you can set this parameter either to **NULL** or to a valid output buffer containing either **NULL** or JET_instanceNil, which returns the global instance handle created as a side-effect of the initialization.</span></span> <span data-ttu-id="cc761-115">Ce descripteur d’instance peut ensuite être passé à toute autre API qui prend une instance.</span><span class="sxs-lookup"><span data-stu-id="cc761-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="cc761-116">Si le moteur fonctionne en mode multi-instance, vous devez définir ce paramètre sur une mémoire tampon d’entrée valide qui contient le handle d’instance retourné par la fonction [JetCreateInstance](./jetcreateinstance-function.md) qui est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="cc761-116">If the engine is operating in multi-instance mode, you must set this parameter to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function that is being initialized.</span></span>

<span data-ttu-id="cc761-117">*prstInfo*</span><span class="sxs-lookup"><span data-stu-id="cc761-117">*prstInfo*</span></span>

<span data-ttu-id="cc761-118">Paramètres de récupération supplémentaires utilisés pour le remappage des bases de données lors de la récupération, pour définir la position d’arrêt de la récupération ou pour déterminer l’état actuel de la récupération.</span><span class="sxs-lookup"><span data-stu-id="cc761-118">Additional recovery parameters used for remapping databases during recovery, for setting the position where recovery will stop, or for determining the current recovery status.</span></span>

<span data-ttu-id="cc761-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="cc761-119">*grbit*</span></span>

<span data-ttu-id="cc761-120">Groupe de bits qui spécifie zéro, une ou plusieurs des options énumérées et définies dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cc761-120">A group of bits that specifies zero or more of the options listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cc761-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc761-121">Value</span></span></p></th>
<th><p><span data-ttu-id="cc761-122">Signification</span><span class="sxs-lookup"><span data-stu-id="cc761-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc761-123">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="cc761-123">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="cc761-124">Cette valeur est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cc761-124">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc761-125">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="cc761-125">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="cc761-126">Cette valeur est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cc761-126">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc761-127">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="cc761-127">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="cc761-128">Cette valeur permet à l’utilisateur d’exécuter la récupération sur un ensemble de fichiers journaux, même en l’absence de bases de données attachées au fichier journal défini à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="cc761-128">This value enables the user to run recovery on a set of log files, even in the absence of the databases that were attached to the log file set at some point.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc761-129">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="cc761-129">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="cc761-130">Cette valeur permet à l’utilisateur d’effectuer la récupération, mais uniquement jusqu’à la phase d’annulation (sans inclure).</span><span class="sxs-lookup"><span data-stu-id="cc761-130">This value enables the user to perform recovery, but only up to (and not including) the Undo phase.</span></span> <span data-ttu-id="cc761-131">À l’aide de cette valeur, les journaux de transactions supplémentaires peuvent être copiés et appliqués.</span><span class="sxs-lookup"><span data-stu-id="cc761-131">Using this value, additional transaction logs can be copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc761-132">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="cc761-132">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="cc761-133">Cette valeur entraîne la troncation des fichiers journaux au cours d’une récupération logicielle réussie.</span><span class="sxs-lookup"><span data-stu-id="cc761-133">This value causes log files to be truncated during a successful soft recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc761-134">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="cc761-134">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="cc761-135">Cette valeur entraîne l’absence d’une entrée de mappage de base de données par défaut au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="cc761-135">This value causes a missing database map entry to default to the same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc761-136">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="cc761-136">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="cc761-137">Cette valeur entraîne l’ignorance des journaux perdus à partir de la fin du flux de journal au cours d’une récupération.</span><span class="sxs-lookup"><span data-stu-id="cc761-137">This value causes logs lost from the end of the log stream to be ignored during a recovery.</span></span></p>
<p><span data-ttu-id="cc761-138"><strong>Windows 7 : JET_bitReplayIgnoreLostLogs</strong> est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cc761-138"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="cc761-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc761-139">Return Value</span></span>

<span data-ttu-id="cc761-140">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="cc761-140">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="cc761-141">Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cc761-141">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="cc761-142">Notes</span><span class="sxs-lookup"><span data-stu-id="cc761-142">Remarks</span></span>

<span data-ttu-id="cc761-143">Une instance doit être initialisée avec un appel à la fonction **JetInit3** avant de pouvoir être utilisée par autre chose que la fonction [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cc761-143">An instance must be initialized with a call to the **JetInit3** function before it can be used by anything other than the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span>

<span data-ttu-id="cc761-144">Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de la fonction [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cc761-144">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized by using the [JetInit](./jetinit-function.md) function.</span></span> <span data-ttu-id="cc761-145">Une instance est l’unité de récupérabilité pour le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cc761-145">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="cc761-146">Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="cc761-146">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="cc761-147">Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="cc761-147">These files include the checkpoint file and the transaction log files.</span></span> <span data-ttu-id="cc761-148">Notez que [JetTerm](./jetterm-function.md) ne doit pas être appelé si la fonction **JetInit3** échoue.</span><span class="sxs-lookup"><span data-stu-id="cc761-148">Note that [JetTerm](./jetterm-function.md) should not be called if the **JetInit3** function fails.</span></span> <span data-ttu-id="cc761-149">Toutefois, [JetTerm](./jetterm-function.md) doit toujours être appelé pour toutes les instances créées par **JetCreateInstance2** si **JetInit3** n’a jamais été appelé ou si **JetInit3** s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="cc761-149">However, [JetTerm](./jetterm-function.md) should still be called for all instances created by **JetCreateInstance2** if **JetInit3** was never called or if **JetInit3** succeeds.</span></span>

<span data-ttu-id="cc761-150">Si la récupération s’exécute sur un ensemble de journaux pour lesquels toutes les bases de données associées ne sont pas présentes (ce qui renvoie l’erreur JET_errAttachedDatabaseMismatch dans des conditions normales) et que le client souhaite que la récupération continue malgré les bases de données manquantes, l’erreur JET_bitReplayIgnoreMissingDB est utilisée pour poursuivre la récupération des bases de données disponibles.</span><span class="sxs-lookup"><span data-stu-id="cc761-150">If recovery is running on a set of logs for which not all of the related databases are present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wants recovery to continue despite the missing databases, the JET_bitReplayIgnoreMissingDB error is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="cc761-151">Comme la récupération après incident ne se produit généralement pas sur le même ordinateur (et avec la même configuration) qu’au moment de l’incident, une base de données ne change pas d’emplacement en général.</span><span class="sxs-lookup"><span data-stu-id="cc761-151">Because crash recovery doesn't usually happen on the same machine (and with the same configuration) as at the time of the crash, a database typically doesn't change location.</span></span> <span data-ttu-id="cc761-152">Dans certains scénarios, tels que le déplacement de fichiers vers un autre ordinateur ou la restauration d’une sauvegarde d’instantané vers différents emplacements, ce n’est plus le cas.</span><span class="sxs-lookup"><span data-stu-id="cc761-152">In certain scenarios, such as moving files to a different machine or restoring snapshot backup to different locations, this is no longer true.</span></span> <span data-ttu-id="cc761-153">La fonction **JetInit3** vous permet de spécifier un mappage (à l’aide des structures [JET_RSTINFO](./jet-rstinfo-structure.md) et [JET_RSTMAP](./jet-rstmap-structure.md) ) entre l’ancien emplacement de base de données et son nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="cc761-153">The **JetInit3** function enables you to specify a mapping (using the [JET_RSTINFO](./jet-rstinfo-structure.md) and [JET_RSTMAP](./jet-rstmap-structure.md) structures) between the old database location and its new location.</span></span> <span data-ttu-id="cc761-154">En fait, vous n’avez besoin que du nouvel emplacement tant que les fichiers de base de données sont présents à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="cc761-154">In fact, you need only the new location as long as the database files are present at that location.</span></span> <span data-ttu-id="cc761-155">Dès que vous connaissez l’emplacement des bases de données restaurées, la signature de base de données est utilisée pour identifier la base de données par le biais du processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="cc761-155">As soon as you know the locations of the restored databases, the database signature will be used to identify the database through the restore process.</span></span> <span data-ttu-id="cc761-156">Vous aurez besoin de l’emplacement de la base de données d’origine uniquement si vous devez recréer une base de données, auquel cas la signature est connue.</span><span class="sxs-lookup"><span data-stu-id="cc761-156">You'll need the original database location only if you need to re-create a database, in which case the signature is known.</span></span>

<span data-ttu-id="cc761-157">En outre, si vous devez arrêter une récupération après une opération d’annulation, vous pouvez spécifier une position de journal particulière à laquelle la récupération s’arrêtera.</span><span class="sxs-lookup"><span data-stu-id="cc761-157">In addition, if you need to stop a recovery after an Undo operation, you can specify a particular log position at which recovery will stop.</span></span> <span data-ttu-id="cc761-158">Notez que cela comprend la possibilité de s’arrêter à la fin d’une génération de journal particulière si la position spécifiée fait partie de la génération, mais au-delà de la fin du journal réel.</span><span class="sxs-lookup"><span data-stu-id="cc761-158">Note that this includes the ability to stop at the end of a particular log generation if the specified position is part of the generation but past the end of the actual log.</span></span>

<span data-ttu-id="cc761-159">Pour plus d’informations, consultez la section « Notes » de la rubrique [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cc761-159">For more information, see the "Remarks" section in the [JetInit](./jetinit-function.md) topic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cc761-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc761-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cc761-161">Client</span><span class="sxs-lookup"><span data-stu-id="cc761-161">Client</span></span></p></td>
<td><p><span data-ttu-id="cc761-162">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc761-162">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc761-163">Serveur</span><span class="sxs-lookup"><span data-stu-id="cc761-163">Server</span></span></p></td>
<td><p><span data-ttu-id="cc761-164">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cc761-164">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc761-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc761-165">Header</span></span></p></td>
<td><p><span data-ttu-id="cc761-166">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="cc761-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc761-167">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc761-167">Library</span></span></p></td>
<td><p><span data-ttu-id="cc761-168">Utilise ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cc761-168">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cc761-169">DLL</span><span class="sxs-lookup"><span data-stu-id="cc761-169">DLL</span></span></p></td>
<td><p><span data-ttu-id="cc761-170">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cc761-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cc761-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="cc761-171">Unicode</span></span></p></td>
<td><p><span data-ttu-id="cc761-172">Implémenté en tant que <strong>JetInit3W</strong> (Unicode) et <strong>JetInit3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="cc761-172">Implemented as <strong>JetInit3W</strong> (Unicode) and <strong>JetInit3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cc761-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc761-173">See Also</span></span>

[<span data-ttu-id="cc761-174">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="cc761-174">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="cc761-175">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cc761-175">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cc761-176">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="cc761-176">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="cc761-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="cc761-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="cc761-178">JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="cc761-178">JET_RSTINFO</span></span>](./jet-rstinfo-structure.md)  
[<span data-ttu-id="cc761-179">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="cc761-179">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="cc761-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="cc761-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="cc761-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="cc761-181">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="cc761-182">JetInit2</span><span class="sxs-lookup"><span data-stu-id="cc761-182">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="cc761-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="cc761-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="cc761-184">Paramètres de ressource</span><span class="sxs-lookup"><span data-stu-id="cc761-184">Resource Parameters</span></span>](./resource-parameters.md)
