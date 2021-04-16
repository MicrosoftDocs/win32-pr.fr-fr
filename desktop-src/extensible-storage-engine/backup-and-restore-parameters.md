---
description: En savoir plus sur les paramètres de sauvegarde et de restauration
title: Paramètres de sauvegarde et de restauration
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530117"
---
# <a name="backup-and-restore-parameters"></a><span data-ttu-id="84851-103">Paramètres de sauvegarde et de restauration</span><span class="sxs-lookup"><span data-stu-id="84851-103">Backup and Restore Parameters</span></span>


<span data-ttu-id="84851-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="84851-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="backup-and-restore-parameters"></a><span data-ttu-id="84851-105">Paramètres de sauvegarde et de restauration</span><span class="sxs-lookup"><span data-stu-id="84851-105">Backup and Restore Parameters</span></span>

<span data-ttu-id="84851-106">Cette rubrique contient les paramètres utilisés pour la sauvegarde et la restauration.</span><span class="sxs-lookup"><span data-stu-id="84851-106">This topic contains parameters that are used for backup and restore.</span></span>

<span data-ttu-id="84851-107">*JET_paramAlternateDatabaseRecoveryPath*</span><span class="sxs-lookup"><span data-stu-id="84851-107">*JET_paramAlternateDatabaseRecoveryPath*</span></span>  
<span data-ttu-id="84851-108">113</span><span class="sxs-lookup"><span data-stu-id="84851-108">113</span></span>  

<span data-ttu-id="84851-109">Le chemin d’accès complet à chaque base de données est conservé dans les journaux des transactions au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="84851-109">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="84851-110">En règle générale, ces bases de données doivent rester à l’emplacement d’origine pour que la relecture des transactions fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="84851-110">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="84851-111">Ce paramètre peut être utilisé pour forcer la récupération après incident ou une opération de restauration pour rechercher les bases de données référencées dans le journal des transactions dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="84851-111">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84851-112">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="84851-112">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="84851-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="84851-114">Chemin d’accès au dossier (String)</span><span class="sxs-lookup"><span data-stu-id="84851-114">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-115">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="84851-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="84851-116">0 – 246 caractères</span><span class="sxs-lookup"><span data-stu-id="84851-116">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-117">Étendue :</span><span class="sxs-lookup"><span data-stu-id="84851-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="84851-118">Instance</span><span class="sxs-lookup"><span data-stu-id="84851-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-119">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-120">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-121">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-122">Non</span><span class="sxs-lookup"><span data-stu-id="84851-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-123">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="84851-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="84851-124">Non</span><span class="sxs-lookup"><span data-stu-id="84851-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-125">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="84851-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="84851-126">Non</span><span class="sxs-lookup"><span data-stu-id="84851-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-127">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="84851-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="84851-128">Non</span><span class="sxs-lookup"><span data-stu-id="84851-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-129">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="84851-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="84851-130">Non</span><span class="sxs-lookup"><span data-stu-id="84851-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-131">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="84851-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="84851-132">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="84851-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84851-133">*JET_paramCleanupMismatchedLogFiles*</span><span class="sxs-lookup"><span data-stu-id="84851-133">*JET_paramCleanupMismatchedLogFiles*</span></span>  
<span data-ttu-id="84851-134">77</span><span class="sxs-lookup"><span data-stu-id="84851-134">77</span></span>  

<span data-ttu-id="84851-135">Ce paramètre contrôle le résultat de [JetInit](./jetinit-function.md) lorsque le moteur de base de données est configuré pour commencer à utiliser des fichiers du journal des transactions sur un disque d’une taille différente de celle configurée.</span><span class="sxs-lookup"><span data-stu-id="84851-135">This parameter controls the outcome of [JetInit](./jetinit-function.md) when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="84851-136">Normalement, [JetInit](./jetinit-function.md) récupère correctement les bases de données, mais échoue avec JET_errLogFileSizeMismatchDatabasesConsistent pour indiquer que la taille du fichier journal est mal configurée.</span><span class="sxs-lookup"><span data-stu-id="84851-136">Normally, [JetInit](./jetinit-function.md) will successfully recover the databases but will fail with JET_errLogFileSizeMismatchDatabasesConsistent to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="84851-137">Toutefois, lorsque ce paramètre est défini sur true, le moteur de base de données supprime silencieusement tous les anciens fichiers journaux, démarre un nouvel ensemble de fichiers journaux de transactions à l’aide de la taille de fichier journal configurée et retourne JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="84851-137">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size, and return JET_errSuccess.</span></span>

<span data-ttu-id="84851-138">Ce paramètre est utile lorsque l’application souhaite modifier en toute transparence la taille du fichier journal des transactions, tout en continuant à travailler de manière transparente dans les scénarios de mise à niveau et de restauration.</span><span class="sxs-lookup"><span data-stu-id="84851-138">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84851-139">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="84851-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="84851-140">Faux</span><span class="sxs-lookup"><span data-stu-id="84851-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-141">Tapez :</span><span class="sxs-lookup"><span data-stu-id="84851-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="84851-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="84851-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-143">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="84851-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="84851-144">False, True</span><span class="sxs-lookup"><span data-stu-id="84851-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-145">Étendue :</span><span class="sxs-lookup"><span data-stu-id="84851-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="84851-146">Instance</span><span class="sxs-lookup"><span data-stu-id="84851-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-147">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-148">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-149">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-150">Non</span><span class="sxs-lookup"><span data-stu-id="84851-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-151">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="84851-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="84851-152">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-153">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="84851-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="84851-154">Non</span><span class="sxs-lookup"><span data-stu-id="84851-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-155">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="84851-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="84851-156">Non</span><span class="sxs-lookup"><span data-stu-id="84851-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-157">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="84851-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="84851-158">Non</span><span class="sxs-lookup"><span data-stu-id="84851-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-159">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="84851-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="84851-160">Tous</span><span class="sxs-lookup"><span data-stu-id="84851-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84851-161">*JET_paramDeleteOutOfRangeLogs*</span><span class="sxs-lookup"><span data-stu-id="84851-161">*JET_paramDeleteOutOfRangeLogs*</span></span>  
<span data-ttu-id="84851-162">52</span><span class="sxs-lookup"><span data-stu-id="84851-162">52</span></span>  

<span data-ttu-id="84851-163">Lorsque ce paramètre a la valeur true, tous les fichiers journaux des transactions trouvés sur le disque qui ne font pas partie de la séquence actuelle des fichiers journaux seront supprimés par [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="84851-163">When this parameter is true, then any transaction log files found on disk that are not part of the current sequence of log files will be deleted by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="84851-164">Cela peut être utilisé pour nettoyer automatiquement les fichiers journaux superflus après une opération de restauration.</span><span class="sxs-lookup"><span data-stu-id="84851-164">This may be used to automatically clean up extraneous log files after a restore operation.</span></span>

<span data-ttu-id="84851-165">**Windows XP :**  Introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="84851-165">**Windows XP:**  Introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84851-166">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="84851-166">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="84851-167">Faux</span><span class="sxs-lookup"><span data-stu-id="84851-167">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-168">Tapez :</span><span class="sxs-lookup"><span data-stu-id="84851-168">Type:</span></span></p></td>
<td><p><span data-ttu-id="84851-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="84851-169">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-170">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="84851-170">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="84851-171">False, True</span><span class="sxs-lookup"><span data-stu-id="84851-171">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-172">Étendue :</span><span class="sxs-lookup"><span data-stu-id="84851-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="84851-173">Instance</span><span class="sxs-lookup"><span data-stu-id="84851-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-174">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-175">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-176">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-177">Non</span><span class="sxs-lookup"><span data-stu-id="84851-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-178">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="84851-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="84851-179">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-179">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-180">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="84851-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="84851-181">Non</span><span class="sxs-lookup"><span data-stu-id="84851-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-182">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="84851-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="84851-183">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-183">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-184">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="84851-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="84851-185">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-185">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-186">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="84851-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="84851-187">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="84851-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84851-188">*JET_paramOSSnapshotTimeout*</span><span class="sxs-lookup"><span data-stu-id="84851-188">*JET_paramOSSnapshotTimeout*</span></span>  
<span data-ttu-id="84851-189">82</span><span class="sxs-lookup"><span data-stu-id="84851-189">82</span></span>  

<span data-ttu-id="84851-190">Ce paramètre configure la durée autorisée entre un appel à [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) et [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) avant qu’un délai d’attente ne se produise.</span><span class="sxs-lookup"><span data-stu-id="84851-190">This parameter configures the amount of time allowed between a call to [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) before a timeout occurs.</span></span> <span data-ttu-id="84851-191">Pour plus d’informations, consultez [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) et [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="84851-191">Please see [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) for more information.</span></span> <span data-ttu-id="84851-192">Le délai d’attente est exprimé en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="84851-192">The timeout is in milliseconds.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84851-193">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="84851-193">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="84851-194">20000 (Windows XP et Windows Server 2003);</span><span class="sxs-lookup"><span data-stu-id="84851-194">20000 (Windows XP and Windows Server 2003);</span></span></p>
<p><span data-ttu-id="84851-195">70000 (Windows Server 2003 SP1)</span><span class="sxs-lookup"><span data-stu-id="84851-195">70000 (Windows Server 2003 SP1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-196">Tapez :</span><span class="sxs-lookup"><span data-stu-id="84851-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="84851-197">Integer</span><span class="sxs-lookup"><span data-stu-id="84851-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-198">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="84851-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="84851-199">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="84851-199">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-200">Étendue :</span><span class="sxs-lookup"><span data-stu-id="84851-200">Scope:</span></span></p></td>
<td><p><span data-ttu-id="84851-201">Global</span><span class="sxs-lookup"><span data-stu-id="84851-201">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-202">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-202">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-203">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-204">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-204">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-205">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-206">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="84851-206">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="84851-207">Non</span><span class="sxs-lookup"><span data-stu-id="84851-207">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-208">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="84851-208">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="84851-209">Non</span><span class="sxs-lookup"><span data-stu-id="84851-209">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-210">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="84851-210">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="84851-211">Non</span><span class="sxs-lookup"><span data-stu-id="84851-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-212">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="84851-212">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="84851-213">Non</span><span class="sxs-lookup"><span data-stu-id="84851-213">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-214">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="84851-214">Availability:</span></span></p></td>
<td><p><span data-ttu-id="84851-215">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="84851-215">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84851-216">*JET_paramZeroDatabaseDuringBackup*</span><span class="sxs-lookup"><span data-stu-id="84851-216">*JET_paramZeroDatabaseDuringBackup*</span></span>  
<span data-ttu-id="84851-217">71</span><span class="sxs-lookup"><span data-stu-id="84851-217">71</span></span>  

<span data-ttu-id="84851-218">Lorsque ce paramètre a la valeur true, toutes les pages d’une base de données qui subit une sauvegarde en continu sont nettoyées des données supprimées.</span><span class="sxs-lookup"><span data-stu-id="84851-218">When this parameter is true then every page in a database that is undergoing a streaming backup will be scrubbed of deleted data.</span></span> <span data-ttu-id="84851-219">Il est important de noter que les pages de la base de données qui sont en cours de nettoyage sont sur le disque.</span><span class="sxs-lookup"><span data-stu-id="84851-219">It is important to note that the database pages that are being scrubbed are on disk.</span></span> <span data-ttu-id="84851-220">Le jeu de données complet est sauvegardé avant le processus de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="84851-220">The full data set is backed up prior to the scrub process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84851-221">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="84851-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="84851-222">Faux</span><span class="sxs-lookup"><span data-stu-id="84851-222">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-223">Tapez :</span><span class="sxs-lookup"><span data-stu-id="84851-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="84851-224">Boolean</span><span class="sxs-lookup"><span data-stu-id="84851-224">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-225">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="84851-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="84851-226">False, True</span><span class="sxs-lookup"><span data-stu-id="84851-226">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-227">Étendue :</span><span class="sxs-lookup"><span data-stu-id="84851-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="84851-228">Instance</span><span class="sxs-lookup"><span data-stu-id="84851-228">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-229">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-230">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-230">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-231">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="84851-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="84851-232">Non</span><span class="sxs-lookup"><span data-stu-id="84851-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-233">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="84851-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="84851-234">Non</span><span class="sxs-lookup"><span data-stu-id="84851-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-235">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="84851-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="84851-236">Non</span><span class="sxs-lookup"><span data-stu-id="84851-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-237">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="84851-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="84851-238">Oui</span><span class="sxs-lookup"><span data-stu-id="84851-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-239">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="84851-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="84851-240">Non</span><span class="sxs-lookup"><span data-stu-id="84851-240">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-241">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="84851-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="84851-242">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="84851-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="84851-243">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84851-243">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84851-244"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="84851-244"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="84851-245">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="84851-245">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84851-246"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="84851-246"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="84851-247">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="84851-247">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84851-248"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="84851-248"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="84851-249">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="84851-249">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="84851-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84851-250">See Also</span></span>

[<span data-ttu-id="84851-251">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="84851-251">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="84851-252">JetInit</span><span class="sxs-lookup"><span data-stu-id="84851-252">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="84851-253">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="84851-253">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="84851-254">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="84851-254">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
