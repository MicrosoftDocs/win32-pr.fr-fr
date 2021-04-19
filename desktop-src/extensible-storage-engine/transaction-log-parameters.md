---
description: 'En savoir plus sur : paramètres du journal des transactions'
title: Paramètres du journal des transactions
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528255"
---
# <a name="transaction-log-parameters"></a><span data-ttu-id="cf132-103">Paramètres du journal des transactions</span><span class="sxs-lookup"><span data-stu-id="cf132-103">Transaction Log Parameters</span></span>


<span data-ttu-id="cf132-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="cf132-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="cf132-105">**Dans cet article**</span><span class="sxs-lookup"><span data-stu-id="cf132-105">**In this article**</span></span>  
<span data-ttu-id="cf132-106">Paramètres du journal des transactions</span><span class="sxs-lookup"><span data-stu-id="cf132-106">Transaction Log Parameters</span></span>  
<span data-ttu-id="cf132-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cf132-107">Requirements</span></span>  
<span data-ttu-id="cf132-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf132-108">See Also</span></span>  

## <a name="transaction-log-parameters"></a><span data-ttu-id="cf132-109">Paramètres du journal des transactions</span><span class="sxs-lookup"><span data-stu-id="cf132-109">Transaction Log Parameters</span></span>

<span data-ttu-id="cf132-110">Cette rubrique contient des paramètres qui sont utilisés pour les journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="cf132-110">This topic contains parameters that are used for transaction logs.</span></span>

<span data-ttu-id="cf132-111">*JET_paramBaseName*</span><span class="sxs-lookup"><span data-stu-id="cf132-111">*JET_paramBaseName*</span></span>  
<span data-ttu-id="cf132-112">3</span><span class="sxs-lookup"><span data-stu-id="cf132-112">3</span></span>  

<span data-ttu-id="cf132-113">Ce paramètre définit le préfixe à trois lettres utilisé pour la plupart des fichiers utilisés par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-113">This parameter sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="cf132-114">Par exemple, le fichier de point de contrôle est appelé EDB. CHK par défaut, car EDB est le nom de base par défaut.</span><span class="sxs-lookup"><span data-stu-id="cf132-114">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span> <span data-ttu-id="cf132-115">Le nom de base peut être utilisé pour distinguer facilement les ensembles de fichiers qui appartiennent à différentes instances ou à différentes applications.</span><span class="sxs-lookup"><span data-stu-id="cf132-115">The base name can be used to easily distinguish between sets of files that belong to different instances or to different applications.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-116">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-116">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-117">&quot;EDB&quot;</span><span class="sxs-lookup"><span data-stu-id="cf132-117">&quot;edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-118">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-118">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-119">String</span><span class="sxs-lookup"><span data-stu-id="cf132-119">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-120">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-120">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-121">3 caractères</span><span class="sxs-lookup"><span data-stu-id="cf132-121">3 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-122">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-122">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-123">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-123">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-124">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-124">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-125">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-125">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-126">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-126">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-127">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-128">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-128">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-129">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-130">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-130">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-131">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-132">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-132">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-133">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-134">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-134">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-135">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-136">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-136">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-137">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-137">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-138">*JET_paramCircularLog*</span><span class="sxs-lookup"><span data-stu-id="cf132-138">*JET_paramCircularLog*</span></span>  
<span data-ttu-id="cf132-139">17</span><span class="sxs-lookup"><span data-stu-id="cf132-139">17</span></span>  

<span data-ttu-id="cf132-140">Ce paramètre configure la façon dont les fichiers journaux des transactions sont gérés par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-140">This parameter configures how transaction log files are managed by the database engine.</span></span>

<span data-ttu-id="cf132-141">Lorsque la journalisation circulaire est désactivée, tous les fichiers journaux des transactions générés sont conservés sur le disque jusqu’à ce qu’ils ne soient plus nécessaires, car une sauvegarde complète de la base de données a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="cf132-141">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="cf132-142">Dans ce mode, il est possible de restaurer à partir d’une sauvegarde plus ancienne et de lire par progression tous les fichiers journaux de transactions conservés de sorte qu’aucune donnée ne soit perdue à la suite de l’incident qui a forcé la restauration.</span><span class="sxs-lookup"><span data-stu-id="cf132-142">In this mode, it is possible to restore from an older backup and play forward through all the retained transaction log files such that no data is lost as a result of the disaster that forced the restore.</span></span> <span data-ttu-id="cf132-143">Des sauvegardes complètes régulières sont nécessaires pour empêcher le disque de se remplir avec les fichiers journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="cf132-143">Regular full backups are required to prevent the disk from filling up with transaction log files.</span></span>

<span data-ttu-id="cf132-144">Lorsque la journalisation circulaire est activée, seuls les fichiers journaux des transactions qui sont plus récents que le point de contrôle actuel sont conservés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="cf132-144">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="cf132-145">L’avantage de ce mode est que les sauvegardes ne sont pas nécessaires pour supprimer les anciens fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="cf132-145">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span> <span data-ttu-id="cf132-146">Le compromis est qu’il n’est plus possible de restaurer une perte de données nulle.</span><span class="sxs-lookup"><span data-stu-id="cf132-146">The tradeoff is that a zero data loss restore is no longer possible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-147">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-147">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-148">Faux</span><span class="sxs-lookup"><span data-stu-id="cf132-148">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-149">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-149">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="cf132-150">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-151">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-151">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-152">False, True</span><span class="sxs-lookup"><span data-stu-id="cf132-152">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-153">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-153">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-154">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-154">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-155">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-155">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-156">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-156">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-157">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-157">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-158">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-159">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-160">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-160">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-161">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-162">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-163">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-164">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-165">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-166">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-167">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-168">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-168">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-169">*JET_paramCommitDefault*</span><span class="sxs-lookup"><span data-stu-id="cf132-169">*JET_paramCommitDefault*</span></span>  
<span data-ttu-id="cf132-170">16</span><span class="sxs-lookup"><span data-stu-id="cf132-170">16</span></span>  

<span data-ttu-id="cf132-171">Ce paramètre contrôle l’action par défaut entreprise lorsque la transaction la plus à l’extérieur est validée sur une session.</span><span class="sxs-lookup"><span data-stu-id="cf132-171">This parameter controls the default action taken when the outermost transaction is committed on a session.</span></span> <span data-ttu-id="cf132-172">Toute option valide pouvant être passée à [JetCommitTransaction](./jetcommittransaction-function.md) peut également être définie comme étant la valeur par défaut pour toutes les sessions dans une instance et/ou pour une session spécifique.</span><span class="sxs-lookup"><span data-stu-id="cf132-172">Any valid option that can be passed to [JetCommitTransaction](./jetcommittransaction-function.md) can also be made to be the default for all sessions in an instance and/or for a specific session.</span></span> <span data-ttu-id="cf132-173">Pour plus d’informations sur ces options, consultez [JetCommitTransaction](./jetcommittransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cf132-173">See [JetCommitTransaction](./jetcommittransaction-function.md) for more details on these options.</span></span>

<span data-ttu-id="cf132-174">Ce paramètre a un impact sur la fiabilité et les performances des transactions.</span><span class="sxs-lookup"><span data-stu-id="cf132-174">This parameter has an impact on the reliability and performance of transactions.</span></span> <span data-ttu-id="cf132-175">Pour plus d’informations, consultez [JetCommitTransaction](./jetcommittransaction-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cf132-175">Please see [JetCommitTransaction](./jetcommittransaction-function.md) for more details.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-176">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-176">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-177">0</span><span class="sxs-lookup"><span data-stu-id="cf132-177">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-178">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-179">JET_GRBIT (entier)</span><span class="sxs-lookup"><span data-stu-id="cf132-179">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-180">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-181">Une option valide pour JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="cf132-181">A valid option for JetCommitTransaction</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-182">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-182">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-183">Instance ou session</span><span class="sxs-lookup"><span data-stu-id="cf132-183">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-184">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-184">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-185">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-185">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-186">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-186">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-187">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-187">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-188">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-189">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-190">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-191">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-191">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-192">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-193">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-194">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-195">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-195">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-196">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-197">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-198">*JET_paramDeleteOldLogs*</span><span class="sxs-lookup"><span data-stu-id="cf132-198">*JET_paramDeleteOldLogs*</span></span>  
<span data-ttu-id="cf132-199">48</span><span class="sxs-lookup"><span data-stu-id="cf132-199">48</span></span>  

<span data-ttu-id="cf132-200">Lorsque ce paramètre a la valeur true et que les fichiers journaux des transactions désignés par le chemin d’accès au fichier journal (**JET_paramLogFilePath**) sont tous des versions obsolètes, ces fichiers journaux des transactions sont automatiquement supprimés.</span><span class="sxs-lookup"><span data-stu-id="cf132-200">When this parameter is true and the transaction log files pointed to by the log file path (**JET_paramLogFilePath**) are all of an obsolete version then those transaction log files will be automatically deleted.</span></span>

<span data-ttu-id="cf132-201">**Windows 2000 :**  Vous devez veiller à utiliser ce paramètre lors de la mise à niveau d’une base de données de Windows NT vers Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="cf132-201">**Windows 2000:**  Care must be taken with the use of this parameter when upgrading a database from Windows NT to Windows 2000.</span></span> <span data-ttu-id="cf132-202">Si la base de données n’est pas dans un état cohérent et que les anciens fichiers journaux sont supprimés, le contenu de la base de données sera perdu.</span><span class="sxs-lookup"><span data-stu-id="cf132-202">If the database is not in a consistent state and the old log files are deleted then the contents of the database will be lost.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-203">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-203">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-204"><strong>Windows 2000 :</strong>  Fausses</span><span class="sxs-lookup"><span data-stu-id="cf132-204"><strong>Windows 2000:</strong>  False</span></span></p>
<p><span data-ttu-id="cf132-205"><strong>Windows XP :</strong>  :</span><span class="sxs-lookup"><span data-stu-id="cf132-205"><strong>Windows XP:</strong>  True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-206">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-206">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="cf132-207">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-208">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-208">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-209">False, True</span><span class="sxs-lookup"><span data-stu-id="cf132-209">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-210">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-210">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-211">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-211">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-212">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-212">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-213">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-213">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-214">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-214">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-215">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-215">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-216">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-216">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-217">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-217">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-218">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-218">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-219">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-219">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-220">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-220">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-221">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-221">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-222">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-222">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-223">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-223">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-224">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-224">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-225">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-225">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-226">*JET_paramIgnoreLogVersion*</span><span class="sxs-lookup"><span data-stu-id="cf132-226">*JET_paramIgnoreLogVersion*</span></span>  
<span data-ttu-id="cf132-227">47</span><span class="sxs-lookup"><span data-stu-id="cf132-227">47</span></span>  

<span data-ttu-id="cf132-228">Si ce paramètre a la valeur true, le moteur de base de données ne valide pas le numéro de version du fichier journal des transactions pendant la [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="cf132-228">If this parameter is true then the database engine will not validate the transaction log file version number during [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="cf132-229">**Windows XP :**  À compter de Windows XP, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-229">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-230">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-230">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-231">Faux</span><span class="sxs-lookup"><span data-stu-id="cf132-231">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-232">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-232">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-233">Boolean</span><span class="sxs-lookup"><span data-stu-id="cf132-233">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-234">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-234">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-235">False, True</span><span class="sxs-lookup"><span data-stu-id="cf132-235">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-236">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-236">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-237">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-237">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-238">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-238">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-239">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-239">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-240">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-240">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-241">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-242">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-242">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-243">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-243">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-244">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-244">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-245">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-246">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-246">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-247">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-247">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-248">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-248">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-249">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-249">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-250">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-250">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-251">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-251">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-252">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="cf132-252">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="cf132-253">136</span><span class="sxs-lookup"><span data-stu-id="cf132-253">136</span></span>  

<span data-ttu-id="cf132-254">Ce paramètre offre une compatibilité descendante avec les conventions d’affectation des noms de fichiers des versions antérieures du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-254">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span>

<span data-ttu-id="cf132-255">Les options suivantes sont actuellement prises en charge :</span><span class="sxs-lookup"><span data-stu-id="cf132-255">The following options are currently supported:</span></span>

<span data-ttu-id="cf132-256">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="cf132-256">JET_bitESE98FileNames</span></span>

<span data-ttu-id="cf132-257">Lorsque cette option est présente, le moteur de base de données utilise les conventions d’affectation de noms suivantes pour ses fichiers :</span><span class="sxs-lookup"><span data-stu-id="cf132-257">When this option is present then the database engine will use the following naming conventions for its files:</span></span>

  - <span data-ttu-id="cf132-258">Les fichiers journaux des transactions vont utiliser. Journal pour l’extension de fichier</span><span class="sxs-lookup"><span data-stu-id="cf132-258">Transaction Log files will use .LOG for their file extension</span></span>

  - <span data-ttu-id="cf132-259">Les fichiers de point de contrôle seront utilisés. CHK pour leur extension de fichier</span><span class="sxs-lookup"><span data-stu-id="cf132-259">Checkpoint files will use .CHK for their file extension</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-260">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-261">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="cf132-261">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-262">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-263">JET_GRBIT (entier)</span><span class="sxs-lookup"><span data-stu-id="cf132-263">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-264">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-265">0, JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="cf132-265">0, JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-266">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-267">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-268">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-269">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-270">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-271">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-272">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-273">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-273">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-274">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-275">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-276">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-277">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-278">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-279">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-280">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-281">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="cf132-281">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-282">*JET_paramLogBuffers*</span><span class="sxs-lookup"><span data-stu-id="cf132-282">*JET_paramLogBuffers*</span></span>  
<span data-ttu-id="cf132-283">12</span><span class="sxs-lookup"><span data-stu-id="cf132-283">12</span></span>  

<span data-ttu-id="cf132-284">Ce paramètre permet de configurer la quantité de mémoire utilisée pour mettre en cache les enregistrements de journal avant leur écriture dans le fichier journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="cf132-284">This parameter will configure the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="cf132-285">L’unité de ce paramètre correspond à la taille de secteur du volume qui contient les fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="cf132-285">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="cf132-286">La taille des secteurs étant presque toujours de 512 octets, il est possible de supposer en toute sécurité la taille de l’unité.</span><span class="sxs-lookup"><span data-stu-id="cf132-286">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span>

<span data-ttu-id="cf132-287">Ce paramètre a un impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="cf132-287">This parameter has an impact on performance.</span></span> <span data-ttu-id="cf132-288">Lorsque le moteur de base de données subit une charge de mise à jour importante, cette mémoire tampon peut être entièrement très rapide.</span><span class="sxs-lookup"><span data-stu-id="cf132-288">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="cf132-289">Une plus grande taille de cache pour le fichier journal des transactions est essentielle pour garantir une bonne performance des mises à jour dans une condition de charge élevée.</span><span class="sxs-lookup"><span data-stu-id="cf132-289">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="cf132-290">La valeur par défaut est trop petite pour ce cas.</span><span class="sxs-lookup"><span data-stu-id="cf132-290">The default is known to be too small for this case.</span></span>

<span data-ttu-id="cf132-291">**Windows XP et windows 2000 :**  Sur Windows XP et les versions antérieures, il n’est pas recommandé de définir ce paramètre sur un nombre de mémoires tampons plus grand (en octets) que la moitié de la taille d’un fichier journal de transactions.</span><span class="sxs-lookup"><span data-stu-id="cf132-291">**Windows XP and Windows 2000:**  On Windows XP and previous releases, it is not recommended to set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-292">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-292">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-293"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  80</span><span class="sxs-lookup"><span data-stu-id="cf132-293"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80</span></span></p>
<p><span data-ttu-id="cf132-294"><strong>Windows Vista :</strong>  126</span><span class="sxs-lookup"><span data-stu-id="cf132-294"><strong>Windows Vista:</strong>  126</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-295">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-295">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-296">Integer</span><span class="sxs-lookup"><span data-stu-id="cf132-296">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-297">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-297">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-298"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  80 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="cf132-298"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80 – 2147483647</span></span></p>
<p><span data-ttu-id="cf132-299"><strong>Windows Vista :</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="cf132-299"><strong>Windows Vista:</strong>  1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-300">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-300">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-301">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-301">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-302">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-302">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-303">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-303">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-304">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-304">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-305">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-305">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-306">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-306">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-307">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-307">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-308">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-308">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-309">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-309">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-310">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-310">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-311">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-311">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-312">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-312">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-313">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-313">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-314">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-314">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-315">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-315">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-316">*JET_paramLogCheckpointPeriod*</span><span class="sxs-lookup"><span data-stu-id="cf132-316">*JET_paramLogCheckpointPeriod*</span></span>  
<span data-ttu-id="cf132-317">14</span><span class="sxs-lookup"><span data-stu-id="cf132-317">14</span></span>  

<span data-ttu-id="cf132-318">Ce paramètre configure le moteur de base de données pour qu’il prenne un point de contrôle lorsque le nombre spécifié de secteurs de fichier journal a été généré.</span><span class="sxs-lookup"><span data-stu-id="cf132-318">This parameter configures the database engine to take a checkpoint when the specified number of log file sectors has been generated.</span></span>

<span data-ttu-id="cf132-319">**Windows XP :**  À compter de Windows XP, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-319">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-320">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-320">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-321">1 024</span><span class="sxs-lookup"><span data-stu-id="cf132-321">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-322">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-322">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-323">Integer</span><span class="sxs-lookup"><span data-stu-id="cf132-323">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-324">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-324">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-325">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="cf132-325">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-326">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-327">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-328">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-329">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-330">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-331">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-331">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-332">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-333">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-334">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-335">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-336">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-337">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-338">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-339">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-340">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-341">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-342">*JET_paramLogFileCreateAsynch*</span><span class="sxs-lookup"><span data-stu-id="cf132-342">*JET_paramLogFileCreateAsynch*</span></span>  
<span data-ttu-id="cf132-343">69</span><span class="sxs-lookup"><span data-stu-id="cf132-343">69</span></span>  

<span data-ttu-id="cf132-344">Lorsque ce paramètre est défini sur true, le moteur de base de données crée le prochain fichier journal des transactions, car le fichier journal des transactions en cours est consommé.</span><span class="sxs-lookup"><span data-stu-id="cf132-344">When this parameter is set to true, the database engine will create the next transaction log file as the current transaction log file is consumed.</span></span> <span data-ttu-id="cf132-345">L’objectif est de réduire le temps passé à passer d’un fichier journal de transactions à l’autre sous une charge de mise à jour importante.</span><span class="sxs-lookup"><span data-stu-id="cf132-345">The intent is to minimize the time spent switching from one transaction log file to the next under a heavy update load.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-346">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-347">Vrai</span><span class="sxs-lookup"><span data-stu-id="cf132-347">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-348">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-349">Boolean</span><span class="sxs-lookup"><span data-stu-id="cf132-349">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-350">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-351">False, True</span><span class="sxs-lookup"><span data-stu-id="cf132-351">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-352">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-353">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-354">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-355">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-356">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-357">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-358">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-359">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-359">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-360">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-361">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-362">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-363">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-364">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-365">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-366">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-367">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="cf132-367">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-368">*JET_paramLogFilePath*</span><span class="sxs-lookup"><span data-stu-id="cf132-368">*JET_paramLogFilePath*</span></span>  
<span data-ttu-id="cf132-369">2</span><span class="sxs-lookup"><span data-stu-id="cf132-369">2</span></span> 

<span data-ttu-id="cf132-370">Ce paramètre indique le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra les journaux des transactions pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="cf132-370">This parameter indicates the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span> <span data-ttu-id="cf132-371">Le chemin d’accès doit se terminer par une barre oblique inverse, ce qui indique que le chemin d’accès cible est un dossier.</span><span class="sxs-lookup"><span data-stu-id="cf132-371">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="cf132-372">Les fichiers journaux des transactions contiennent les informations requises pour ramener les fichiers de base de données à un état cohérent après un incident.</span><span class="sxs-lookup"><span data-stu-id="cf132-372">The transaction log files contain the information required to bring the database files to a consistent state after a crash.</span></span> <span data-ttu-id="cf132-373">Ils sont généralement nommés EDB \* . Sign.</span><span class="sxs-lookup"><span data-stu-id="cf132-373">They are typically named EDB\*.LOG.</span></span> <span data-ttu-id="cf132-374">Le contenu des fichiers du journal des transactions est tout aussi important (si ce n’est pas le cas) que les fichiers de base de données eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="cf132-374">The contents of the transaction log files are just as important (if not more so) than the database files themselves.</span></span> <span data-ttu-id="cf132-375">Chaque effort doit être effectué pour les protéger.</span><span class="sxs-lookup"><span data-stu-id="cf132-375">Every effort should be made to protect them.</span></span>

<span data-ttu-id="cf132-376">Il y aura également des fichiers journaux de réserve supplémentaires nommés RES1. LOG et RES2. JOURNAL stocké avec les fichiers journaux ordinaires.</span><span class="sxs-lookup"><span data-stu-id="cf132-376">There will also be additional reserve log files named RES1.LOG and RES2.LOG stored along with the ordinary log files.</span></span> <span data-ttu-id="cf132-377">Le contenu de ces fichiers n’est pas important car leur seul objectif est de réserver de l’espace disque pour permettre au moteur de s’arrêter correctement dans un scénario à faible disque.</span><span class="sxs-lookup"><span data-stu-id="cf132-377">The contents of these files are not important as their only purpose is to reserve disk space to allow the engine to shut down gracefully in a low disk scenario.</span></span> <span data-ttu-id="cf132-378">Il s’agit également d’un fichier journal temporaire appelé EDBTMP. Connectez-vous au même dossier.</span><span class="sxs-lookup"><span data-stu-id="cf132-378">These will also be a temporary log file typically named EDBTMP.LOG in this same folder.</span></span> <span data-ttu-id="cf132-379">Le contenu de ce fichier n’a pas d’importance.</span><span class="sxs-lookup"><span data-stu-id="cf132-379">The contents of this file are not important either.</span></span> <span data-ttu-id="cf132-380">Ce fichier est un nouveau fichier journal préparé pour être utilisé.</span><span class="sxs-lookup"><span data-stu-id="cf132-380">This file is a new log file being prepared for use.</span></span>

<span data-ttu-id="cf132-381">Les propriétés du volume hôte des fichiers journaux des transactions et leur emplacement par rapport aux autres fichiers utilisés par le moteur de base de données peuvent avoir un impact considérable sur les performances.</span><span class="sxs-lookup"><span data-stu-id="cf132-381">The properties of the host volume of the transaction log files and their placement relative to the other files used by the database engine can dramatically impact performance.</span></span>

<span data-ttu-id="cf132-382">**Remarque**  Si un chemin d’accès relatif est spécifié, il est relatif au répertoire de travail actuel du processus qui héberge l’application qui utilise le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-382">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-383">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-384">&quot;.\& tenu</span><span class="sxs-lookup"><span data-stu-id="cf132-384">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-385">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-386">Chemin d’accès au dossier (String)</span><span class="sxs-lookup"><span data-stu-id="cf132-386">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-387">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-388">0 – 246 caractères</span><span class="sxs-lookup"><span data-stu-id="cf132-388">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-389">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-390">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-390">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-391">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-392">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-392">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-393">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-394">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-395">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-396">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-396">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-397">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-398">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-398">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-399">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-400">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-401">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-402">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-403">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-404">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-405">*JET_paramLogFileSize*</span><span class="sxs-lookup"><span data-stu-id="cf132-405">*JET_paramLogFileSize*</span></span>  
<span data-ttu-id="cf132-406">11</span><span class="sxs-lookup"><span data-stu-id="cf132-406">11</span></span>  

<span data-ttu-id="cf132-407">Ce paramètre permet de configurer la taille des fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="cf132-407">This parameter will configure the size of the transaction log files.</span></span> <span data-ttu-id="cf132-408">Chaque fichier journal de transactions a une taille fixe.</span><span class="sxs-lookup"><span data-stu-id="cf132-408">Each transaction log file is a fixed size.</span></span> <span data-ttu-id="cf132-409">La taille est égale à la valeur de ce paramètre système, en unités de 1024 octets.</span><span class="sxs-lookup"><span data-stu-id="cf132-409">The size is equal to the setting of this system parameter in units of 1024 bytes.</span></span>

<span data-ttu-id="cf132-410">Ce paramètre a un impact sur la fiabilité.</span><span class="sxs-lookup"><span data-stu-id="cf132-410">This parameter has an impact on reliability.</span></span> <span data-ttu-id="cf132-411">Si le paramètre est trop petit, le nombre maximal de fichiers journaux (1048575) sera atteint beaucoup plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="cf132-411">If the setting is too small then the maximum number of log files (1048575) will be reached much faster.</span></span> <span data-ttu-id="cf132-412">Dans ce cas, l’instance doit être arrêtée correctement, les fichiers journaux existants doivent être supprimés et l’instance doit être redémarrée.</span><span class="sxs-lookup"><span data-stu-id="cf132-412">When this happens, the instance must be shutdown cleanly, the existing log files must be deleted, and the instance must be restarted.</span></span> <span data-ttu-id="cf132-413">Cette action permet non seulement de réduire la disponibilité de l’application, mais également d’invalider les sauvegardes précédentes de la base de données de l’application.</span><span class="sxs-lookup"><span data-stu-id="cf132-413">This action will not only reduce the availability of the application but it will also invalidate any previous backups of the application's database.</span></span>

<span data-ttu-id="cf132-414">Ce paramètre a un impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="cf132-414">This parameter has an impact on performance.</span></span> <span data-ttu-id="cf132-415">Si le paramètre est très important, [JetInit](./jetinit-function.md) est lent, car le moteur de base de données doit lire le fichier journal le plus récent (au minimum) au moment de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="cf132-415">If the setting is very large then [JetInit](./jetinit-function.md) will be slow because the database engine must read the youngest log file (at a minimum) when it initializes.</span></span> <span data-ttu-id="cf132-416">Si le paramètre est très volumineux, le basculement entre les fichiers journaux prendra également plus de temps.</span><span class="sxs-lookup"><span data-stu-id="cf132-416">If the setting is very large then it will also take longer to switch between log files.</span></span> <span data-ttu-id="cf132-417">Si le paramètre est très petit, vous devrez créer des fichiers journaux pour un nombre donné de mises à jour, ce qui entraînera une surcharge supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="cf132-417">If the setting is very small then more log files will need to be created for a given number of updates which will add more overhead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-418">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-418">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-419">5120</span><span class="sxs-lookup"><span data-stu-id="cf132-419">5120</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-420">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-420">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-421">Integer</span><span class="sxs-lookup"><span data-stu-id="cf132-421">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-422">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-422">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-423"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  128 – 32768</span><span class="sxs-lookup"><span data-stu-id="cf132-423"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  128 – 32768</span></span></p>
<p><span data-ttu-id="cf132-424"><strong>Windows Vista :</strong>  64 – 32768</span><span class="sxs-lookup"><span data-stu-id="cf132-424"><strong>Windows Vista:</strong>  64 – 32768</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-425">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-425">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-426">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-426">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-427">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-427">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-428">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-429">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-429">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-430">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-430">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-431">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-431">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-432">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-432">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-433">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-433">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-434">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-434">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-435">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-435">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-436">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-436">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-437">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-437">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-438">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-438">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-439">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-439">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-440">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-440">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-441">*JET_paramLogWaitingUserMax*</span><span class="sxs-lookup"><span data-stu-id="cf132-441">*JET_paramLogWaitingUserMax*</span></span>  
<span data-ttu-id="cf132-442">15</span><span class="sxs-lookup"><span data-stu-id="cf132-442">15</span></span>  

<span data-ttu-id="cf132-443">Ce paramètre tente d’optimiser le vidage du tampon du journal provoqué par une validation durable en attendant qu’un nombre spécifié de sessions attendent une validation durable avant de forcer un vidage à se produire dans l’espoir qu’une autre transaction partage le vidage.</span><span class="sxs-lookup"><span data-stu-id="cf132-443">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified number of sessions to wait for a durable commit prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="cf132-444">**Windows XP :**  À compter de Windows XP, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-444">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-445">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-445">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-446">3</span><span class="sxs-lookup"><span data-stu-id="cf132-446">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-447">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-447">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-448">Integer</span><span class="sxs-lookup"><span data-stu-id="cf132-448">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-449">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-449">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-450">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="cf132-450">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-451">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-451">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-452">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-452">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-453">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-453">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-454">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-454">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-455">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-455">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-456">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-456">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-457">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-457">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-458">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-458">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-459">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-459">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-460">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-461">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-461">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-462">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-463">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-463">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-464">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-465">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-465">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-466">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-466">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-467">*JET_paramRecovery*</span><span class="sxs-lookup"><span data-stu-id="cf132-467">*JET_paramRecovery*</span></span>  
<span data-ttu-id="cf132-468">34</span><span class="sxs-lookup"><span data-stu-id="cf132-468">34</span></span>  

<span data-ttu-id="cf132-469">Ce paramètre est le commutateur maître qui contrôle la récupération après incident pour une instance.</span><span class="sxs-lookup"><span data-stu-id="cf132-469">This parameter is the master switch that controls crash recovery for an instance.</span></span> <span data-ttu-id="cf132-470">Si ce paramètre a la valeur « on », la récupération de type ARIES sera utilisée pour ramener toutes les bases de données de l’instance dans un état cohérent en cas de panne d’un processus ou d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cf132-470">If this parameter is set to "On" then ARIES style recovery will be used to bring all databases in the instance to a consistent state in the event of a process or machine crash.</span></span> <span data-ttu-id="cf132-471">Si ce paramètre est défini sur « désactivé », toutes les bases de données de l’instance seront gérées sans l’avantage de la récupération après incident.</span><span class="sxs-lookup"><span data-stu-id="cf132-471">If this parameter is set to "Off" then all databases in the instance will be managed without the benefit of crash recovery.</span></span> <span data-ttu-id="cf132-472">Autrement dit, si l’instance n’est pas fermée correctement à l’aide de [JetTerm](./jetterm-function.md) avant la sortie du processus ou de l’arrêt de l’ordinateur, le contenu de toutes les bases de données de cette instance est endommagé.</span><span class="sxs-lookup"><span data-stu-id="cf132-472">That is to say, that if the instance is not shut down cleanly using [JetTerm](./jetterm-function.md) prior to the process exiting or machine shutdown then the contents of all databases in that instance will be corrupted.</span></span>

<span data-ttu-id="cf132-473">La désactivation de la récupération est utile dans des circonstances particulières où l’on sait que le contenu d’une base de données n’est pas utile en cas de panne.</span><span class="sxs-lookup"><span data-stu-id="cf132-473">Disabling recovery is useful in special circumstances where it is known that the contents of a database are not useful in the event of a crash.</span></span> <span data-ttu-id="cf132-474">La récupération doit être activée pour tous les autres cas.</span><span class="sxs-lookup"><span data-stu-id="cf132-474">Recovery should be enabled for all other cases.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-475">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-475">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-476">&quot;Actif&quot;</span><span class="sxs-lookup"><span data-stu-id="cf132-476">&quot;On&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-477">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-477">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-478">String</span><span class="sxs-lookup"><span data-stu-id="cf132-478">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-479">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-479">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-480">0 – 259 caractères</span><span class="sxs-lookup"><span data-stu-id="cf132-480">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-481">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-481">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-482">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-482">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-483">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-483">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-484">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-484">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-485">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-485">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-486">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-486">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-487">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-487">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-488">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-488">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-489">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-489">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-490">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-490">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-491">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-491">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-492">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-492">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-493">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-493">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-494">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-494">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-495">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-495">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-496">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-496">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-497">*JET_paramSystemPath*</span><span class="sxs-lookup"><span data-stu-id="cf132-497">*JET_paramSystemPath*</span></span>  
<span data-ttu-id="cf132-498">0</span><span class="sxs-lookup"><span data-stu-id="cf132-498">0</span></span>  

<span data-ttu-id="cf132-499">Ce paramètre indique le chemin d’accès relatif ou absolu du système de fichiers du dossier qui contiendra le fichier de point de contrôle de l’instance.</span><span class="sxs-lookup"><span data-stu-id="cf132-499">This parameter indicates the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span> <span data-ttu-id="cf132-500">Le chemin d’accès doit se terminer par une barre oblique inverse, ce qui indique que le chemin d’accès cible est un dossier.</span><span class="sxs-lookup"><span data-stu-id="cf132-500">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="cf132-501">Le fichier de point de contrôle est un fichier simple géré par instance qui mémorise le fichier journal des transactions le plus ancien qui doit être relu pour ramener toutes les bases de données de cette instance à un état cohérent après un incident.</span><span class="sxs-lookup"><span data-stu-id="cf132-501">The checkpoint file is a simple file maintained per instance that remembers the oldest transaction log file that must be replayed to bring all databases in that instance to a consistent state after a crash.</span></span> <span data-ttu-id="cf132-502">Le fichier de point de contrôle est généralement nommé EDB. CHK.</span><span class="sxs-lookup"><span data-stu-id="cf132-502">The checkpoint file is typically named EDB.CHK.</span></span>

<span data-ttu-id="cf132-503">**Remarque**  Si un chemin d’accès relatif est spécifié, il est relatif au répertoire de travail actuel du processus qui héberge l’application qui utilise le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-503">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-504">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-504">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-505">&quot;.\& tenu</span><span class="sxs-lookup"><span data-stu-id="cf132-505">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-506">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-506">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-507">Chemin d’accès au dossier (String)</span><span class="sxs-lookup"><span data-stu-id="cf132-507">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-508">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-508">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-509">0 – 246 caractères</span><span class="sxs-lookup"><span data-stu-id="cf132-509">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-510">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-510">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-511">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-511">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-512">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-512">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-513">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-513">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-514">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-514">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-515">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-515">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-516">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-516">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-517">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-517">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-518">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-518">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-519">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-519">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-520">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-520">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-521">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-521">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-522">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-522">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-523">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-523">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-524">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-524">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-525">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-525">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-526">*JET_paramWaitLogFlush*</span><span class="sxs-lookup"><span data-stu-id="cf132-526">*JET_paramWaitLogFlush*</span></span>  
<span data-ttu-id="cf132-527">13</span><span class="sxs-lookup"><span data-stu-id="cf132-527">13</span></span> 

<span data-ttu-id="cf132-528">Ce paramètre tente d’optimiser le vidage du tampon du journal provoqué par une validation durable en attendant une période spécifiée avant de forcer un vidage à se produire dans l’espoir qu’une autre transaction partage le vidage.</span><span class="sxs-lookup"><span data-stu-id="cf132-528">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified time period prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="cf132-529">**Windows XP :**  À compter de Windows XP, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="cf132-529">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-530">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-530">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-531">0</span><span class="sxs-lookup"><span data-stu-id="cf132-531">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-532">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-532">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-533">Integer</span><span class="sxs-lookup"><span data-stu-id="cf132-533">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-534">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-534">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-535">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="cf132-535">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-536">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-536">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-537">Instance ou session</span><span class="sxs-lookup"><span data-stu-id="cf132-537">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-538">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-538">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-539">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-539">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-540">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-540">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-541">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-541">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-542">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-542">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-543">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-543">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-544">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-544">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-545">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-545">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-546">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-546">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-547">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-547">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-548">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-548">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-549">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-549">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-550">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-550">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-551">Tous</span><span class="sxs-lookup"><span data-stu-id="cf132-551">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf132-552">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="cf132-552">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="cf132-553">136</span><span class="sxs-lookup"><span data-stu-id="cf132-553">136</span></span>  

<span data-ttu-id="cf132-554">Ce paramètre est utilisé pour spécifier les fonctionnalités de compatibilité d’attribution de noms de fichiers à gérer avec Windows Server 2003 et le schéma d’affectation de noms de fichier précédent.</span><span class="sxs-lookup"><span data-stu-id="cf132-554">This parameter is used to specify the file naming compatibility features to maintain with the Windows Server 2003 and previous file naming scheme.</span></span> <span data-ttu-id="cf132-555">Pour plus d’informations sur les différents fichiers et leur affectation de noms, consultez [fichiers ESE (Extensible Storage Engine](./extensible-storage-engine-files.md)).</span><span class="sxs-lookup"><span data-stu-id="cf132-555">For more information about the different files and their naming see [Extensible Storage Engine Files](./extensible-storage-engine-files.md).</span></span>

<span data-ttu-id="cf132-556">La JET_bitESE98FileNames garantit que l’extension de fichier utilisée dans les fichiers journaux de transactions et le fichier de point de contrôle sont les mêmes que ceux utilisés dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cf132-556">The JET_bitESE98FileNames ensures the file extension used on the transaction log files and the checkpoint file are the same as that used in Windows Server 2003.</span></span> <span data-ttu-id="cf132-557">Remarque : Si vous effectuez une mise à niveau à partir de Windows Server 2003, ce bit n’a toujours pas besoin d’être spécifié, car le moteur met automatiquement à niveau les extensions de fichier si JET_paramCircularLog a la valeur **true** ou conserve l’ancienne extension de journal si JET_paramCircularLog a la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="cf132-557">Note if upgrading from Windows Server 2003, this bit still need not be specified, as the engine will automatically upgrade the file extensions if JET_paramCircularLog is set to **true**, or maintain the older log extension if JET_paramCircularLog is **false**.</span></span>

<span data-ttu-id="cf132-558">**Remarque**  Pour définir un bit, la valeur doit d’abord être récupérée, puis « ou » dans le bit de compatibilité souhaité.</span><span class="sxs-lookup"><span data-stu-id="cf132-558">**Note**  To set a bit, the value should first be retrieved, and then "or" in the desired compatibility bit.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-559">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="cf132-559">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cf132-560">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="cf132-560">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-561">Tapez :</span><span class="sxs-lookup"><span data-stu-id="cf132-561">Type:</span></span></p></td>
<td><p><span data-ttu-id="cf132-562">JET_GRBIT (entier)</span><span class="sxs-lookup"><span data-stu-id="cf132-562">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-563">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="cf132-563">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cf132-564">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="cf132-564">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-565">Étendue :</span><span class="sxs-lookup"><span data-stu-id="cf132-565">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cf132-566">Instance</span><span class="sxs-lookup"><span data-stu-id="cf132-566">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-567">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-567">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-568">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-568">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-569">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cf132-569">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cf132-570">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-570">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-571">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="cf132-571">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cf132-572">Oui</span><span class="sxs-lookup"><span data-stu-id="cf132-572">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-573">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-573">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-574">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-574">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-575">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="cf132-575">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cf132-576">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-576">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-577">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="cf132-577">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cf132-578">Non</span><span class="sxs-lookup"><span data-stu-id="cf132-578">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-579">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="cf132-579">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cf132-580">À compter de Windows Server 2008 et Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf132-580">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a><span data-ttu-id="cf132-581">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf132-581">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf132-582"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="cf132-582"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cf132-583">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="cf132-583">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf132-584"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="cf132-584"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cf132-585">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cf132-585">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf132-586"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="cf132-586"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cf132-587">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="cf132-587">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="cf132-588">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf132-588">See Also</span></span>

[<span data-ttu-id="cf132-589">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="cf132-589">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="cf132-590">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="cf132-590">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="cf132-591">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="cf132-591">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="cf132-592">JetInit</span><span class="sxs-lookup"><span data-stu-id="cf132-592">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="cf132-593">JetTerm</span><span class="sxs-lookup"><span data-stu-id="cf132-593">JetTerm</span></span>](./jetterm-function.md)
