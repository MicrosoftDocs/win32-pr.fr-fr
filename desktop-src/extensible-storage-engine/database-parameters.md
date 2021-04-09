---
description: 'En savoir plus sur : paramètres de base de données'
title: Paramètres de base de données
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114083"
---
# <a name="database-parameters"></a><span data-ttu-id="fddbf-103">Paramètres de base de données</span><span class="sxs-lookup"><span data-stu-id="fddbf-103">Database Parameters</span></span>


<span data-ttu-id="fddbf-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="fddbf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-parameters"></a><span data-ttu-id="fddbf-105">Paramètres de base de données</span><span class="sxs-lookup"><span data-stu-id="fddbf-105">Database Parameters</span></span>

<span data-ttu-id="fddbf-106">Cette rubrique contient les paramètres utilisés pour la base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-106">This topic contains parameters that are used for the database.</span></span>

<span data-ttu-id="fddbf-107">*JET_paramCheckFormatWhenOpenFail*</span><span class="sxs-lookup"><span data-stu-id="fddbf-107">*JET_paramCheckFormatWhenOpenFail*</span></span>  
<span data-ttu-id="fddbf-108">44</span><span class="sxs-lookup"><span data-stu-id="fddbf-108">44</span></span>  

<span data-ttu-id="fddbf-109">Quand ce paramètre est défini, [JetInit](./jetinit-function.md) renvoie une erreur spéciale lorsqu’une base de données ou un journal des transactions d’une version précédente du moteur de base de données est ouvert.</span><span class="sxs-lookup"><span data-stu-id="fddbf-109">This parameter, when set, will cause [JetInit](./jetinit-function.md) to return a special error when a database or transaction log from a previous release of the database engine is opened.</span></span> <span data-ttu-id="fddbf-110">Ces erreurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="fddbf-110">These errors are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fddbf-111">Error</span><span class="sxs-lookup"><span data-stu-id="fddbf-111">Error</span></span></p></th>
<th><p><span data-ttu-id="fddbf-112">Description</span><span class="sxs-lookup"><span data-stu-id="fddbf-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-113">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="fddbf-113">JET_errDatabase200Format</span></span></p></td>
<td><p><span data-ttu-id="fddbf-114">La base de données et/ou les fichiers journaux des transactions ont été créés avec le moteur de base de données dans Windows NT 3,51.</span><span class="sxs-lookup"><span data-stu-id="fddbf-114">The database and/or transaction log files were created with the database engine in Windows NT 3.51.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-115">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="fddbf-115">JET_errDatabase400Format</span></span></p></td>
<td><p><span data-ttu-id="fddbf-116">La base de données et/ou les fichiers journaux des transactions ont été créés avec le moteur de base de données dans une version de test antérieure à Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="fddbf-116">The database and/or transaction log files were created with the database engine in a test release prior to Windows NT Server 4.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-117">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="fddbf-117">JET_errDatabase500Format</span></span></p></td>
<td><p><span data-ttu-id="fddbf-118">La base de données et/ou les fichiers journaux des transactions ont été créés avec le moteur de base de données dans Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="fddbf-118">The database and/or transaction log files were created with the database engine in Windows NT Server 4.0.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-119">**Windows Vista :**  Pour Windows Vista et versions ultérieures, ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-119">**Windows Vista:**  For Windows Vista and later, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-120">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-120">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-121">Vrai</span><span class="sxs-lookup"><span data-stu-id="fddbf-121">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-122">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-122">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="fddbf-123">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-124">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-124">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-125">False, True</span><span class="sxs-lookup"><span data-stu-id="fddbf-125">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-126">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-126">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-127">Instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-127">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-128">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-128">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-129">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-130">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-130">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-131">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-132">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-132">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-133">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-134">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-134">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-135">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-136">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-136">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-137">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-138">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-138">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-139">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-139">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-140">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-140">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-141">Tous</span><span class="sxs-lookup"><span data-stu-id="fddbf-141">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-142">*JET_paramDatabasePageSize*</span><span class="sxs-lookup"><span data-stu-id="fddbf-142">*JET_paramDatabasePageSize*</span></span>  
<span data-ttu-id="fddbf-143">64</span><span class="sxs-lookup"><span data-stu-id="fddbf-143">64</span></span>  

<span data-ttu-id="fddbf-144">Ce paramètre configure la taille de page pour la base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-144">This parameter configures the page size for the database.</span></span> <span data-ttu-id="fddbf-145">La taille de la page est la plus petite unité d’allocation d’espace possible pour un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-145">The page size is the smallest unit of space allocation possible for a database file.</span></span> <span data-ttu-id="fddbf-146">La taille de la page de base de données est également très importante, car elle définit la limite supérieure de la taille d’un enregistrement individuel dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-146">The database page size is also very important because it sets the upper limit on the size of an individual record in the database.</span></span>

<span data-ttu-id="fddbf-147">**Remarque** Une seule taille de page de base de données est prise en charge par processus pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="fddbf-147">**Note** Only one database page size is supported per process at this time.</span></span> <span data-ttu-id="fddbf-148">Cela signifie que si vous êtes dans un processus unique qui contient des applications qui utilisent le moteur de base de données, elles doivent toutes accepter sur une taille de page de base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-148">This means that if you are in a single process that contains different applications that use the database engine then they must all agree on a database page size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-149">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-149">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-150">4096</span><span class="sxs-lookup"><span data-stu-id="fddbf-150">4096</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-151">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-151">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-152">Integer</span><span class="sxs-lookup"><span data-stu-id="fddbf-152">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-153">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-153">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-154">2048, 4096, 8192</span><span class="sxs-lookup"><span data-stu-id="fddbf-154">2048, 4096, 8192</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-155">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-155">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-156">Global</span><span class="sxs-lookup"><span data-stu-id="fddbf-156">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-157">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-157">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-158">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-159">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-159">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-160">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-161">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-161">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-162">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-163">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-163">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-164">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-164">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-165">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-165">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-166">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-166">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-167">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-167">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-168">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-168">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-169">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-169">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-170">Tous</span><span class="sxs-lookup"><span data-stu-id="fddbf-170">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-171">*JET_paramDbExtensionSize*</span><span class="sxs-lookup"><span data-stu-id="fddbf-171">*JET_paramDbExtensionSize*</span></span>  
<span data-ttu-id="fddbf-172">18</span><span class="sxs-lookup"><span data-stu-id="fddbf-172">18</span></span>  

<span data-ttu-id="fddbf-173">Ce paramètre contrôle la quantité d’espace qui est ajoutée à un fichier de base de données chaque fois qu’il doit croître pour accueillir davantage de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-173">This parameter controls the amount of space that is added to a database file each time it needs to grow to accommodate more data.</span></span> <span data-ttu-id="fddbf-174">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-174">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-175">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-176">256</span><span class="sxs-lookup"><span data-stu-id="fddbf-176">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-177">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-177">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-178">Integer</span><span class="sxs-lookup"><span data-stu-id="fddbf-178">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-179">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-179">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-180">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="fddbf-180">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-181">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-181">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-182">Instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-182">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-183">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-183">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-184">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-184">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-185">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-185">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-186">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-186">No</span></span></p>
<p><span data-ttu-id="fddbf-187"><strong>Windows Vista :</strong>  Pour Windows Vista et versions ultérieures : Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-187"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-188">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-189">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-190">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-191">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-191">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-192">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-193">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-194">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-195">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-195">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-196">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-197">Tous</span><span class="sxs-lookup"><span data-stu-id="fddbf-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-198">*JET_paramEnableIndexChecking*</span><span class="sxs-lookup"><span data-stu-id="fddbf-198">*JET_paramEnableIndexChecking*</span></span>  
<span data-ttu-id="fddbf-199">45</span><span class="sxs-lookup"><span data-stu-id="fddbf-199">45</span></span>  

<span data-ttu-id="fddbf-200">Lorsque ce paramètre a la valeur true, chaque base de données est vérifiée au moment de la [JetAttachDatabase](./jetattachdatabase-function.md) pour les index sur les colonnes clés Unicode qui ont été créées à l’aide d’une version antérieure de la bibliothèque NLS dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fddbf-200">When this parameter is true, every database is checked at [JetAttachDatabase](./jetattachdatabase-function.md) time for indexes over Unicode key columns that were built using an older version of the NLS library in the operating system.</span></span> <span data-ttu-id="fddbf-201">Cela doit être fait parce que le moteur de base de données conserve les clés de tri générées par [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) et que la valeur de ces clés de tri passe de Release à Release.</span><span class="sxs-lookup"><span data-stu-id="fddbf-201">This must be done because the database engine persists the sort keys generated by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) and the value of these sort keys change from release to release.</span></span>

<span data-ttu-id="fddbf-202">Si un index principal est détecté comme étant dans cet État, [JetAttachDatabase](./jetattachdatabase-function.md) échouera toujours avec JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="fddbf-202">If a primary index is detected to be in this state then [JetAttachDatabase](./jetattachdatabase-function.md) will always fail with JET_errPrimaryIndexCorrupted.</span></span>

<span data-ttu-id="fddbf-203">Si des index secondaires sont détectés comme étant dans cet État, il existe deux résultats possibles.</span><span class="sxs-lookup"><span data-stu-id="fddbf-203">If any secondary indexes are detected to be in this state then there are two possible outcomes.</span></span> <span data-ttu-id="fddbf-204">Si JET_bitDbDeleteCorruptIndexes a été passé à [JetAttachDatabase](./jetattachdatabase-function.md) , ces index seront supprimés et JET_wrnCorruptIndexDeleted sera retourné à partir de [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="fddbf-204">If JET_bitDbDeleteCorruptIndexes was passed to [JetAttachDatabase](./jetattachdatabase-function.md) then these indexes will be deleted and JET_wrnCorruptIndexDeleted will be returned from [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="fddbf-205">Ces index doivent être recréés par votre application.</span><span class="sxs-lookup"><span data-stu-id="fddbf-205">These indexes will need to be recreated by your application.</span></span> <span data-ttu-id="fddbf-206">Si JET_bitDbDeleteCorruptIndexes n’a pas été passé à [JetAttachDatabase](./jetattachdatabase-function.md) , l’appel échoue avec JET_errSecondaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="fddbf-206">If JET_bitDbDeleteCorruptIndexes was not passed to [JetAttachDatabase](./jetattachdatabase-function.md) then the call will fail with JET_errSecondaryIndexCorrupted.</span></span>

<span data-ttu-id="fddbf-207">**Remarque** Il est fortement recommandé de définir ce paramètre sur true par votre application.</span><span class="sxs-lookup"><span data-stu-id="fddbf-207">**Note** It is strongly recommended that this parameter be set to True by your application.</span></span>

<span data-ttu-id="fddbf-208">**Remarque** Il est fortement recommandé que les applications évitent l’utilisation de colonnes clés Unicode dans leurs index de clé primaire (en cluster).</span><span class="sxs-lookup"><span data-stu-id="fddbf-208">**Note** It is very strongly recommended that applications avoid the use of Unicode key columns in their primary key (clustered) indexes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-209">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-209">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-210">Faux</span><span class="sxs-lookup"><span data-stu-id="fddbf-210">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-211">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-212">Boolean</span><span class="sxs-lookup"><span data-stu-id="fddbf-212">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-213">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-214">False, True</span><span class="sxs-lookup"><span data-stu-id="fddbf-214">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-215">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-215">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-216">Global</span><span class="sxs-lookup"><span data-stu-id="fddbf-216">Global</span></span></p>
<p><span data-ttu-id="fddbf-217"><strong>Windows Vista :</strong>  Pour Windows Vista et versions ultérieures : instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-217"><strong>Windows Vista:</strong>  For Windows Vista and later: Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-218">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-219">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-219">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-220">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-220">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-221">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-221">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-222">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-222">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-223">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-223">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-224">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-224">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-225">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-225">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-226">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-226">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-227">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-227">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-228">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-228">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-229">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-229">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-230">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-230">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-231">Tous</span><span class="sxs-lookup"><span data-stu-id="fddbf-231">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-232">*JET_paramEnableIndexCleanup*</span><span class="sxs-lookup"><span data-stu-id="fddbf-232">*JET_paramEnableIndexCleanup*</span></span>  
<span data-ttu-id="fddbf-233">54</span><span class="sxs-lookup"><span data-stu-id="fddbf-233">54</span></span>  

<span data-ttu-id="fddbf-234">Lorsque ce paramètre est défini sur true, le moteur de base de données peut nettoyer automatiquement les index sur les colonnes de clés Unicode au moment [JetInit](./jetinit-function.md) pour éviter les modifications de format de base de données dues à des modifications apportées à la bibliothèque NLS dans Windows.</span><span class="sxs-lookup"><span data-stu-id="fddbf-234">When this parameter is set to true, then the database engine may automatically clean up indexes over Unicode key columns at [JetInit](./jetinit-function.md) time as necessary to avoid database format changes caused by changes to the NLS library in Windows.</span></span> <span data-ttu-id="fddbf-235">Ces modifications sont régulièrement apportées à la bibliothèque NLS pour ajouter la prise en charge de nouvelles langues, pour ajouter des caractères manquants à une langue, pour ajouter un ordre de classement à une langue ou pour corriger les bogues dans l’ordre de classement d’une langue.</span><span class="sxs-lookup"><span data-stu-id="fddbf-235">Such changes are made routinely to the NLS library to add support for new languages, to add missing characters to a language, to add a collation order to a language, or to fix bugs in the collation order of a language.</span></span> <span data-ttu-id="fddbf-236">Ces modifications affectent les clés de tri produites par [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) qui sont rendues persistantes par le moteur de base de données en tant que composants des clés d’index.</span><span class="sxs-lookup"><span data-stu-id="fddbf-236">These changes affect the sort keys produced by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) which are persisted by the database engine as components of index keys.</span></span>

<span data-ttu-id="fddbf-237">Il est important de comprendre qu’il est possible que les modifications apportées à l’index soient tellement importantes qu’un nettoyage incrémentiel n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="fddbf-237">It is important to realize that it is possible for the changes to the index to be so great that an incremental cleanup is not possible.</span></span> <span data-ttu-id="fddbf-238">Dans ce cas, l’index sera géré conformément aux indications de **JET_paramEnableIndexChecking**.</span><span class="sxs-lookup"><span data-stu-id="fddbf-238">In this case, the index will be handled as prescribed by **JET_paramEnableIndexChecking**.</span></span>

<span data-ttu-id="fddbf-239">**Remarque** Il est fortement recommandé de définir ce paramètre et d' **JET_paramEnableIndexChecking** avoir la valeur **true** par votre application.</span><span class="sxs-lookup"><span data-stu-id="fddbf-239">**Note** It is strongly recommended that this parameter and **JET_paramEnableIndexChecking** be set to **True** by your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-240">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-240">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-241">Vrai</span><span class="sxs-lookup"><span data-stu-id="fddbf-241">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-242">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-242">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="fddbf-243">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-244">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-244">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-245">False, True</span><span class="sxs-lookup"><span data-stu-id="fddbf-245">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-246">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-246">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-247">Instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-247">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-248">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-248">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-249">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-249">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-250">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-250">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-251">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-251">No</span></span></p>
<p><span data-ttu-id="fddbf-252"><strong>Windows Vista :</strong>  Pour Windows Vista et versions ultérieures : Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-252"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-253">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-253">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-254">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-254">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-255">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-255">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-256">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-256">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-257">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-257">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-258">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-258">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-259">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-259">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-260">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-260">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-261">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-261">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-262">Windows Server 2003 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="fddbf-262">Windows Server 2003 and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-263">*JET_paramOneDatabasePerSession*</span><span class="sxs-lookup"><span data-stu-id="fddbf-263">*JET_paramOneDatabasePerSession*</span></span>  
<span data-ttu-id="fddbf-264">102</span><span class="sxs-lookup"><span data-stu-id="fddbf-264">102</span></span>  

<span data-ttu-id="fddbf-265">Lorsque ce paramètre a la valeur true, une seule base de données peut être ouverte à l’aide de [JetOpenDatabase](./jetopendatabase-function.md) par une session donnée à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="fddbf-265">When this parameter is true then only one database is allowed to be opened using [JetOpenDatabase](./jetopendatabase-function.md) by a given session at one time.</span></span> <span data-ttu-id="fddbf-266">La base de données temporaire est exclue de cette restriction.</span><span class="sxs-lookup"><span data-stu-id="fddbf-266">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="fddbf-267">**Windows XP et Windows Server 2003 :**  Ce paramètre est écrit uniquement sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fddbf-267">**Windows XP and Windows Server 2003:**  This parameter is write only on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="fddbf-268">**Windows Vista :**  Ce paramètre se comporte normalement à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fddbf-268">**Windows Vista:**  This parameter behaves normally as of Windows Vista.</span></span>

<span data-ttu-id="fddbf-269">**Remarque**  Ce paramètre est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="fddbf-269">**Note**  This parameter is write only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-270">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-270">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-271">Faux</span><span class="sxs-lookup"><span data-stu-id="fddbf-271">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-272">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-272">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="fddbf-273">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-274">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-274">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-275">False, True</span><span class="sxs-lookup"><span data-stu-id="fddbf-275">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-276">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-276">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-277">Global</span><span class="sxs-lookup"><span data-stu-id="fddbf-277">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-278">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-278">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-279">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-279">No</span></span></p>
<p><span data-ttu-id="fddbf-280"><strong>Windows Vista :</strong>  Pour Windows Vista et versions ultérieures : Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-280"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-281">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-281">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-282">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-282">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-283">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-283">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-284">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-284">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-285">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-285">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-286">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-286">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-287">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-287">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-288">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-288">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-289">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-289">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-290">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-290">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-291">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-291">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-292">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="fddbf-292">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-293">*JET_paramEnableOnlineDefrag*</span><span class="sxs-lookup"><span data-stu-id="fddbf-293">*JET_paramEnableOnlineDefrag*</span></span>  
<span data-ttu-id="fddbf-294">35</span><span class="sxs-lookup"><span data-stu-id="fddbf-294">35</span></span>  

<span data-ttu-id="fddbf-295">Ce paramètre contrôle le comportement de la défragmentation en ligne lorsqu’elle est lancée à l’aide de [JetDefragment](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="fddbf-295">This parameter controls the behavior of online defragmentation when initiated using [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="fddbf-296">Pour plus d’informations, consultez [JetDefragment](./jetdefragment-function.md) .</span><span class="sxs-lookup"><span data-stu-id="fddbf-296">Please see [JetDefragment](./jetdefragment-function.md) for more information.</span></span>

<span data-ttu-id="fddbf-297">Windows 2000 : sur Windows 2000, ce paramètre était une valeur booléenne simple qui porterait sur la défragmentation en ligne lorsqu’elle était initiée par [JetDefragment](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="fddbf-297">Windows 2000:  On Windows 2000, this parameter was a simple Boolean that would gate online defragmentation when initiated by [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="fddbf-298">Lorsque la valeur est **true**, la défragmentation en ligne est effectuée sur les enregistrements de chaque table de la base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-298">When set to **TRUE**, online defragmentation will be performed on the records of each table in the database.</span></span>

<span data-ttu-id="fddbf-299">**Windows XP :**  Sur Windows XP et versions ultérieures, ce paramètre peut être défini sur une ou plusieurs des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="fddbf-299">**Windows XP:**  On Windows XP and later releases, this parameter can be set to one or more of the following options:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fddbf-300">Option</span><span class="sxs-lookup"><span data-stu-id="fddbf-300">Option</span></span></p></th>
<th><p><span data-ttu-id="fddbf-301">Description</span><span class="sxs-lookup"><span data-stu-id="fddbf-301">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-302">JET_OnlineDefragDisable</span><span class="sxs-lookup"><span data-stu-id="fddbf-302">JET_OnlineDefragDisable</span></span></p></td>
<td><p><span data-ttu-id="fddbf-303">N’effectuez pas de défragmentation en ligne.</span><span class="sxs-lookup"><span data-stu-id="fddbf-303">Do not perform online defragmentation.</span></span> <span data-ttu-id="fddbf-304">Il s’agit du binaire équivalent au paramètre Windows 2000 de la valeur false pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="fddbf-304">This is the binary equivalent to the Windows 2000 setting of False for this parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-305">JET_OnlineDefragAllOBSOLETE</span><span class="sxs-lookup"><span data-stu-id="fddbf-305">JET_OnlineDefragAllOBSOLETE</span></span></p></td>
<td><p><span data-ttu-id="fddbf-306">Effectuez une défragmentation en ligne complète.</span><span class="sxs-lookup"><span data-stu-id="fddbf-306">Perform full online defragmentation.</span></span> <span data-ttu-id="fddbf-307">Il s’agit du binaire équivalent au paramètre Windows 2000 de true pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="fddbf-307">This is the binary equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-308">JET_OnlineDefragDatabases</span><span class="sxs-lookup"><span data-stu-id="fddbf-308">JET_OnlineDefragDatabases</span></span></p></td>
<td><p><span data-ttu-id="fddbf-309">Effectuez une défragmentation en ligne des enregistrements de chaque table dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-309">Perform online defragmentation of the records of each table in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-310">JET_OnlineDefragSpaceTrees</span><span class="sxs-lookup"><span data-stu-id="fddbf-310">JET_OnlineDefragSpaceTrees</span></span></p></td>
<td><p><span data-ttu-id="fddbf-311">Effectuez une défragmentation en ligne des arborescences d’espaces de chaque table dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-311">Perform online defragmentation of the space trees of each table in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-312">JET_OnlineDefragStreamingFiles</span><span class="sxs-lookup"><span data-stu-id="fddbf-312">JET_OnlineDefragStreamingFiles</span></span></p></td>
<td><p><span data-ttu-id="fddbf-313">Ce paramètre est utilisé pour prendre en charge l’infrastructure Microsoft Exchange et n’est pas destiné à être utilisé dans votre application.</span><span class="sxs-lookup"><span data-stu-id="fddbf-313">This parameter is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-314">JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="fddbf-314">JET_OnlineDefragAll</span></span></p></td>
<td><p><span data-ttu-id="fddbf-315">Effectuez une défragmentation en ligne complète.</span><span class="sxs-lookup"><span data-stu-id="fddbf-315">Perform full online defragmentation.</span></span> <span data-ttu-id="fddbf-316">Il s’agit du concept conceptuel équivalent au paramètre Windows 2000 de true pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="fddbf-316">This is the conceptual equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-317">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-317">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-318"><strong>Windows 2000 :</strong>  :</span><span class="sxs-lookup"><span data-stu-id="fddbf-318"><strong>Windows 2000:</strong>  True</span></span></p>
<p><span data-ttu-id="fddbf-319"><strong>Windows XP : pour Windows XP et versions ultérieures :</strong> JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="fddbf-319"><strong>Windows XP:  For Windows XP and later:</strong> JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-320">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-320">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-321"><strong>Windows 2000 :</strong>  Expression</span><span class="sxs-lookup"><span data-stu-id="fddbf-321"><strong>Windows 2000:</strong>  Boolean</span></span></p>
<p><span data-ttu-id="fddbf-322"><strong>Windows XP et versions ultérieures :</strong>  JET_GRBIT (entier)</span><span class="sxs-lookup"><span data-stu-id="fddbf-322"><strong>Windows XP and later:</strong>  JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-323">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-323">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-324"><strong>Windows 2000 :</strong>  False, true</span><span class="sxs-lookup"><span data-stu-id="fddbf-324"><strong>Windows 2000:</strong>  False, True</span></span></p>
<p><span data-ttu-id="fddbf-325"><strong>Windows XP et versions ultérieures :</strong>  0 – JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="fddbf-325"><strong>Windows XP and later:</strong>  0 – JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-326">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-327">Instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-328">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-329">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-330">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-331">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-331">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-332">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-333">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-334">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-335">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-336">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-337">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-338">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-339">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-340">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-341">Tous</span><span class="sxs-lookup"><span data-stu-id="fddbf-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-342">*JET_paramPageFragment*</span><span class="sxs-lookup"><span data-stu-id="fddbf-342">*JET_paramPageFragment*</span></span>  
<span data-ttu-id="fddbf-343">20</span><span class="sxs-lookup"><span data-stu-id="fddbf-343">20</span></span>  

<span data-ttu-id="fddbf-344">Ce paramètre correspond au seuil utilisé par le moteur de base de données pour contrôler la fragmentation de l’espace libre.</span><span class="sxs-lookup"><span data-stu-id="fddbf-344">This parameter is the threshold that the database engine uses to control free space fragmentation.</span></span> <span data-ttu-id="fddbf-345">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-345">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-346">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-347">8</span><span class="sxs-lookup"><span data-stu-id="fddbf-347">8</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-348">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-349">Integer</span><span class="sxs-lookup"><span data-stu-id="fddbf-349">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-350">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-351">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="fddbf-351">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-352">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-353">Instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-354">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-355">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-356">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-357">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-358">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-359">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-359">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-360">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-361">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-362">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-363">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-364">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-365">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-366">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-367">Tous</span><span class="sxs-lookup"><span data-stu-id="fddbf-367">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-368">*JET_paramRecordUpgradeDirtyLevel*</span><span class="sxs-lookup"><span data-stu-id="fddbf-368">*JET_paramRecordUpgradeDirtyLevel*</span></span>  
<span data-ttu-id="fddbf-369">78</span><span class="sxs-lookup"><span data-stu-id="fddbf-369">78</span></span>

<span data-ttu-id="fddbf-370">Ce paramètre contrôle la manière dont le gestionnaire de cache de la page de base de données écrira une page de base de données qui a subi une conversion de format en place.</span><span class="sxs-lookup"><span data-stu-id="fddbf-370">This parameter controls how aggressively the database page cache manager will write a database page that has undergone an in place format conversion.</span></span> <span data-ttu-id="fddbf-371">Ces conversions de format se produisent à la volée Lorsque les pages sont chargées à partir d’une base de données créée avec le moteur de base de données Windows 2000, mais utilisées par Windows XP ou une version ultérieure du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="fddbf-371">These format conversions occur on the fly as pages are loaded from a database that was created with the Windows 2000 database engine but used by a Windows XP or later release of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-372">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-372">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-373">1</span><span class="sxs-lookup"><span data-stu-id="fddbf-373">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-374">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-374">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-375">Integer</span><span class="sxs-lookup"><span data-stu-id="fddbf-375">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-376">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-376">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-377">0-3</span><span class="sxs-lookup"><span data-stu-id="fddbf-377">0-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-378">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-378">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-379">Global</span><span class="sxs-lookup"><span data-stu-id="fddbf-379">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-380">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-380">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-381">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-382">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-382">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-383">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-384">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-384">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-385">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-385">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-386">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-386">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-387">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-387">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-388">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-388">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-389">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-389">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-390">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-390">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-391">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-391">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-392">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-392">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-393">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="fddbf-393">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-394">*JET_paramWaypointLatency*</span><span class="sxs-lookup"><span data-stu-id="fddbf-394">*JET_paramWaypointLatency*</span></span>  
<span data-ttu-id="fddbf-395">153</span><span class="sxs-lookup"><span data-stu-id="fddbf-395">153</span></span>  

<span data-ttu-id="fddbf-396">Latence (dans les journaux) en arrière-plan des vidages de pages de la page de base de données pour différer le vidage.</span><span class="sxs-lookup"><span data-stu-id="fddbf-396">The latency (in logs) behind the tip / highest committed log to defer database page flushes.</span></span> <span data-ttu-id="fddbf-397">L’activation de cette latence peut permettre la récupération de la base de données en cas de perte irrémédiable du fichier journal le plus récent.</span><span class="sxs-lookup"><span data-stu-id="fddbf-397">Enabling this latency can allow database recovery in the case of catastrophic loss of the most recent logfile.</span></span> <span data-ttu-id="fddbf-398">Consultez JET_bitReplayIgnoreLostLogs.</span><span class="sxs-lookup"><span data-stu-id="fddbf-398">See JET_bitReplayIgnoreLostLogs.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-399">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-399">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-400">0</span><span class="sxs-lookup"><span data-stu-id="fddbf-400">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-401">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-401">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-402">Integer</span><span class="sxs-lookup"><span data-stu-id="fddbf-402">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-403">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-403">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-404">0-1023</span><span class="sxs-lookup"><span data-stu-id="fddbf-404">0-1023</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-405">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-405">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-406">Instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-406">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-407">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-407">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-408">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-409">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-409">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-410">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-410">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-411">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-411">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-412">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-412">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-413">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-413">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-414">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-414">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-415">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-415">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-416">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-416">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-417">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-417">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-418">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-418">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-419">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-419">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fddbf-420">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-421">*JET_paramDefragmentSequentialBTrees*</span><span class="sxs-lookup"><span data-stu-id="fddbf-421">*JET_paramDefragmentSequentialBTrees*</span></span>  
<span data-ttu-id="fddbf-422">160</span><span class="sxs-lookup"><span data-stu-id="fddbf-422">160</span></span>  

<span data-ttu-id="fddbf-423">Activez/désactivez la défragmentation séquentielle automatique de l’arbre B.</span><span class="sxs-lookup"><span data-stu-id="fddbf-423">Turn on/off automatic sequential B-tree defragmentation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-424">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-424">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-425">1</span><span class="sxs-lookup"><span data-stu-id="fddbf-425">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-426">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-426">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-427">Boolean</span><span class="sxs-lookup"><span data-stu-id="fddbf-427">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-428">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-428">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-429">0-1</span><span class="sxs-lookup"><span data-stu-id="fddbf-429">0-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-430">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-430">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-431">Instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-431">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-432">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-432">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-433">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-433">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-434">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-434">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-435">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-435">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-436">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-436">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-437">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-437">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-438">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-438">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-439">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-439">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-440">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-440">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-441">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-442">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-442">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-443">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-443">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-444">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-444">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fddbf-445">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span><span class="sxs-lookup"><span data-stu-id="fddbf-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span></span>  
<span data-ttu-id="fddbf-447">161</span><span class="sxs-lookup"><span data-stu-id="fddbf-447">161</span></span>  

<span data-ttu-id="fddbf-448">Détermine la fréquence de vérification de la densité de l’arbre B.</span><span class="sxs-lookup"><span data-stu-id="fddbf-448">Determines how frequently B-tree density is checked.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-449">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-449">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-450">10</span><span class="sxs-lookup"><span data-stu-id="fddbf-450">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-451">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-451">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-452">Integer</span><span class="sxs-lookup"><span data-stu-id="fddbf-452">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-453">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-453">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-454">0-entier maximal</span><span class="sxs-lookup"><span data-stu-id="fddbf-454">0-Max Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-455">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-455">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-456">Instance</span><span class="sxs-lookup"><span data-stu-id="fddbf-456">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-457">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-457">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-458">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-459">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-459">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-460">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-461">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-461">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-462">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-463">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-463">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-464">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-465">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-465">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-466">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-466">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-467">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-467">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-468">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-468">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-469">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-469">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-470">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fddbf-470">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fddbf-471">*JET_paramIOThrottlingTimeQuanta*</span><span class="sxs-lookup"><span data-stu-id="fddbf-471">*JET_paramIOThrottlingTimeQuanta*</span></span>  
<span data-ttu-id="fddbf-472">162</span><span class="sxs-lookup"><span data-stu-id="fddbf-472">162</span></span>  

<span data-ttu-id="fddbf-473">Durée maximale, en millisecondes, pendant laquelle le mécanisme de limitation des e/s permet à une tâche de s’exécuter pour qu’elle soit considérée comme « terminée ».</span><span class="sxs-lookup"><span data-stu-id="fddbf-473">Max time, in milliseconds, that the I/O throttling mechanism gives a task to run for it to be considered 'completed'.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-474">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="fddbf-474">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-475">125</span><span class="sxs-lookup"><span data-stu-id="fddbf-475">125</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-476">Tapez :</span><span class="sxs-lookup"><span data-stu-id="fddbf-476">Type:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-477">Integer</span><span class="sxs-lookup"><span data-stu-id="fddbf-477">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-478">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="fddbf-478">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-479">0-10000</span><span class="sxs-lookup"><span data-stu-id="fddbf-479">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-480">Étendue :</span><span class="sxs-lookup"><span data-stu-id="fddbf-480">Scope:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-481">Global</span><span class="sxs-lookup"><span data-stu-id="fddbf-481">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-482">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-482">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-483">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-483">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-484">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="fddbf-484">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-485">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-485">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-486">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="fddbf-486">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-487">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-487">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-488">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-488">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-489">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-489">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-490">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="fddbf-490">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-491">Oui</span><span class="sxs-lookup"><span data-stu-id="fddbf-491">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-492">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="fddbf-492">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-493">Non</span><span class="sxs-lookup"><span data-stu-id="fddbf-493">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-494">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="fddbf-494">Availability:</span></span></p></td>
<td><p><span data-ttu-id="fddbf-495">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fddbf-495">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="fddbf-496">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fddbf-496">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-497"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="fddbf-497"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fddbf-498">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="fddbf-498">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fddbf-499"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="fddbf-499"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fddbf-500">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fddbf-500">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fddbf-501"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="fddbf-501"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fddbf-502">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="fddbf-502">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fddbf-503">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fddbf-503">See Also</span></span>

[<span data-ttu-id="fddbf-504">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="fddbf-504">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="fddbf-505">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="fddbf-505">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="fddbf-506">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="fddbf-506">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="fddbf-507">JetInit</span><span class="sxs-lookup"><span data-stu-id="fddbf-507">JetInit</span></span>](./jetinit-function.md)
