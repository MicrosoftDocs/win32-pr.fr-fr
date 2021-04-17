---
description: 'En savoir plus sur : fonction JetBeginExternalBackupInstance'
title: JetBeginExternalBackupInstance fonction)
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484241"
---
# <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="f58b1-103">JetBeginExternalBackupInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="f58b1-103">JetBeginExternalBackupInstance Function</span></span>


<span data-ttu-id="f58b1-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f58b1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="f58b1-105">JetBeginExternalBackupInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="f58b1-105">JetBeginExternalBackupInstance Function</span></span>

<span data-ttu-id="f58b1-106">La fonction **JetBeginExternalBackupInstance** lance une sauvegarde externe alors que le moteur et la base de données sont en ligne et actifs.</span><span class="sxs-lookup"><span data-stu-id="f58b1-106">The **JetBeginExternalBackupInstance** function initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="f58b1-107">**Windows XP : JetBeginExternalBackupInstance** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f58b1-107">**Windows XP:  JetBeginExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="f58b1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f58b1-108">Parameters</span></span>

<span data-ttu-id="f58b1-109">*instancié*</span><span class="sxs-lookup"><span data-stu-id="f58b1-109">*instance*</span></span>

<span data-ttu-id="f58b1-110">Instance de base de données à utiliser pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="f58b1-110">The database instance to use for this call.</span></span>

<span data-ttu-id="f58b1-111">Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f58b1-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="f58b1-112">L’utilisation de cette instance globale est implicitement dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="f58b1-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="f58b1-113">Pour Windows XP et les versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f58b1-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="f58b1-114">Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="f58b1-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="f58b1-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f58b1-115">*grbit*</span></span>

<span data-ttu-id="f58b1-116">Groupe de bits spécifiant zéro ou plusieurs des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="f58b1-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f58b1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f58b1-117">Value</span></span></p></th>
<th><p><span data-ttu-id="f58b1-118">Signification</span><span class="sxs-lookup"><span data-stu-id="f58b1-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f58b1-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="f58b1-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="f58b1-120">Cet indicateur est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="f58b1-120">This flag is deprecated.</span></span> <span data-ttu-id="f58b1-121">L’utilisation de ce bit entraîne le retour de JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="f58b1-121">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f58b1-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="f58b1-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="f58b1-123">Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète.</span><span class="sxs-lookup"><span data-stu-id="f58b1-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="f58b1-124">Cela signifie que seuls les fichiers journaux depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="f58b1-124">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f58b1-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="f58b1-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="f58b1-126">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="f58b1-126">Reserved for future use.</span></span> <span data-ttu-id="f58b1-127">Défini pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f58b1-127">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f58b1-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f58b1-128">Return Value</span></span>

<span data-ttu-id="f58b1-129">Le système peut générer des codes de réussite ou d’échec à la suite d’un appel à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f58b1-129">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="f58b1-130">Pour obtenir la liste complète des erreurs pour cette API, consultez [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f58b1-130">For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="f58b1-131">Consultez [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="f58b1-131">See [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="f58b1-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f58b1-132">Remarks</span></span>

<span data-ttu-id="f58b1-133">**JetBeginExternalBackupInstance** est la première fonction d’une série de fonctions qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).</span><span class="sxs-lookup"><span data-stu-id="f58b1-133">**JetBeginExternalBackupInstance** is the first function in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span> <span data-ttu-id="f58b1-134">Voir aussi [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) et [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="f58b1-134">See also [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) and [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span></span>

<span data-ttu-id="f58b1-135">Une sauvegarde externe peut être utilisée pour implémenter des sauvegardes complètes, incrémentielles ou différentielles.</span><span class="sxs-lookup"><span data-stu-id="f58b1-135">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="f58b1-136">La sauvegarde sera approximative, car la sauvegarde sera cohérente à un point unique dans le temps dans l’historique des transactions, mais le contrôle du point exact dans le temps n’est pas possible pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="f58b1-136">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible at this time.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f58b1-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f58b1-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f58b1-138"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f58b1-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f58b1-139">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f58b1-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f58b1-140"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f58b1-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f58b1-141">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f58b1-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f58b1-142"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f58b1-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f58b1-143">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f58b1-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f58b1-144"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="f58b1-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f58b1-145">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f58b1-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f58b1-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f58b1-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f58b1-147">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f58b1-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f58b1-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f58b1-148">See Also</span></span>

[<span data-ttu-id="f58b1-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f58b1-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f58b1-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f58b1-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f58b1-151">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f58b1-151">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f58b1-152">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="f58b1-152">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="f58b1-153">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="f58b1-153">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="f58b1-154">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="f58b1-154">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="f58b1-155">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="f58b1-155">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="f58b1-156">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="f58b1-156">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="f58b1-157">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="f58b1-157">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="f58b1-158">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="f58b1-158">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="f58b1-159">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="f58b1-159">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="f58b1-160">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="f58b1-160">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="f58b1-161">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="f58b1-161">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="f58b1-162">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="f58b1-162">JetTruncateLog</span></span>](./jettruncatelog-function.md)
