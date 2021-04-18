---
description: 'En savoir plus sur : méta-paramètres'
title: Paramètres méta
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
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
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542892"
---
# <a name="meta-parameters"></a><span data-ttu-id="352a7-103">Paramètres méta</span><span class="sxs-lookup"><span data-stu-id="352a7-103">Meta Parameters</span></span>


<span data-ttu-id="352a7-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="352a7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="meta-parameters"></a><span data-ttu-id="352a7-105">Paramètres méta</span><span class="sxs-lookup"><span data-stu-id="352a7-105">Meta Parameters</span></span>

<span data-ttu-id="352a7-106">Cette rubrique contient des paramètres qui permettent de contrôler d’autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="352a7-106">This topic contains parameters that are used to control other parameters.</span></span>

<span data-ttu-id="352a7-107">JET_paramConfiguration</span><span class="sxs-lookup"><span data-stu-id="352a7-107">JET_paramConfiguration</span></span>  
<span data-ttu-id="352a7-108">129</span><span class="sxs-lookup"><span data-stu-id="352a7-108">129</span></span>  
<span data-ttu-id="352a7-109">Ce paramètre expose plusieurs jeux de valeurs par défaut pour l’ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="352a7-109">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="352a7-110">Quand ce paramètre est défini sur une configuration spécifique, toutes les valeurs des paramètres système sont réinitialisées à leurs valeurs par défaut pour cette configuration.</span><span class="sxs-lookup"><span data-stu-id="352a7-110">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="352a7-111">Si la configuration est définie pour une instance spécifique, les valeurs par défaut des paramètres système globaux ne sont pas réinitialisées.</span><span class="sxs-lookup"><span data-stu-id="352a7-111">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span>

<span data-ttu-id="352a7-112">En outre, le paramètre lui-même peut avoir d’autres effets sur le comportement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="352a7-112">In addition, the parameter itself can have other effects on the behavior of the database engine.</span></span>

<span data-ttu-id="352a7-113">À ce stade, il existe deux configurations prises en charge :</span><span class="sxs-lookup"><span data-stu-id="352a7-113">At this time, there are two supported configurations:</span></span>

  - <span data-ttu-id="352a7-114">Petite configuration (0) : le moteur de base de données est optimisé pour l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="352a7-114">Small Configuration (0): The database engine is optimized for memory use.</span></span>

  - <span data-ttu-id="352a7-115">Configuration héritée (1) : le moteur de base de données a ses valeurs par défaut traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="352a7-115">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="352a7-116">Une petite configuration modifie les valeurs par défaut des paramètres système suivants pour les valeurs spécifiées :</span><span class="sxs-lookup"><span data-stu-id="352a7-116">Small Configuration changes the defaults of the following system parameters to the specified values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="352a7-117">Paramètre système</span><span class="sxs-lookup"><span data-stu-id="352a7-117">System Parameter</span></span></p></th>
<th><p><span data-ttu-id="352a7-118">Nouvelle valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="352a7-118">New Default Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="352a7-119">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="352a7-119">JET_paramMaxSessions</span></span></p></td>
<td><p><span data-ttu-id="352a7-120">30000</span><span class="sxs-lookup"><span data-stu-id="352a7-120">30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-121">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="352a7-121">JET_paramMaxOpenTables</span></span></p></td>
<td><p><span data-ttu-id="352a7-122">2147483647</span><span class="sxs-lookup"><span data-stu-id="352a7-122">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-123">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="352a7-123">JET_paramMaxCursors</span></span></p></td>
<td><p><span data-ttu-id="352a7-124">2147483647</span><span class="sxs-lookup"><span data-stu-id="352a7-124">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-125">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="352a7-125">JET_paramMaxVerPages</span></span></p></td>
<td><p><span data-ttu-id="352a7-126">2147483647</span><span class="sxs-lookup"><span data-stu-id="352a7-126">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-127">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="352a7-127">JET_paramMaxTemporaryTables</span></span></p></td>
<td><p><span data-ttu-id="352a7-128">2147483647</span><span class="sxs-lookup"><span data-stu-id="352a7-128">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-129">JET_paramLogFileSize</span><span class="sxs-lookup"><span data-stu-id="352a7-129">JET_paramLogFileSize</span></span></p></td>
<td><p><span data-ttu-id="352a7-130">64</span><span class="sxs-lookup"><span data-stu-id="352a7-130">64</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-131">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="352a7-131">JET_paramLogBuffers</span></span></p></td>
<td><p><span data-ttu-id="352a7-132">1</span><span class="sxs-lookup"><span data-stu-id="352a7-132">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-133">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="352a7-133">JET_paramDbExtensionSize</span></span></p></td>
<td><p><span data-ttu-id="352a7-134">16</span><span class="sxs-lookup"><span data-stu-id="352a7-134">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-135">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="352a7-135">JET_paramPageTempDBMin</span></span></p></td>
<td><p><span data-ttu-id="352a7-136">14</span><span class="sxs-lookup"><span data-stu-id="352a7-136">14</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-137">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="352a7-137">JET_paramCacheSizeMax</span></span></p></td>
<td><p><span data-ttu-id="352a7-138">16</span><span class="sxs-lookup"><span data-stu-id="352a7-138">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-139">JET_paramCheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="352a7-139">JET_paramCheckpointDepthMax</span></span></p></td>
<td><p><span data-ttu-id="352a7-140">65536</span><span class="sxs-lookup"><span data-stu-id="352a7-140">65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-141">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="352a7-141">JET_paramLRUKHistoryMax</span></span></p></td>
<td><p><span data-ttu-id="352a7-142">10</span><span class="sxs-lookup"><span data-stu-id="352a7-142">10</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-143">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="352a7-143">JET_paramOutstandingIOMax</span></span></p></td>
<td><p><span data-ttu-id="352a7-144">16</span><span class="sxs-lookup"><span data-stu-id="352a7-144">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-145">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="352a7-145">JET_paramStartFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="352a7-146">1</span><span class="sxs-lookup"><span data-stu-id="352a7-146">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-147">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="352a7-147">JET_paramStopFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="352a7-148">2</span><span class="sxs-lookup"><span data-stu-id="352a7-148">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-149">JET_paramNoInformationEvent</span><span class="sxs-lookup"><span data-stu-id="352a7-149">JET_paramNoInformationEvent</span></span></p></td>
<td><p><span data-ttu-id="352a7-150">1</span><span class="sxs-lookup"><span data-stu-id="352a7-150">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-151">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="352a7-151">JET_paramCacheSizeMin</span></span></p></td>
<td><p><span data-ttu-id="352a7-152">16</span><span class="sxs-lookup"><span data-stu-id="352a7-152">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-153">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="352a7-153">JET_paramPreferredVerPages</span></span></p></td>
<td><p><span data-ttu-id="352a7-154">2147483647</span><span class="sxs-lookup"><span data-stu-id="352a7-154">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-155">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="352a7-155">JET_paramLogFileCreateAsynch</span></span></p></td>
<td><p><span data-ttu-id="352a7-156">0</span><span class="sxs-lookup"><span data-stu-id="352a7-156">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-157">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="352a7-157">JET_paramGlobalMinVerPages</span></span></p></td>
<td><p><span data-ttu-id="352a7-158">1</span><span class="sxs-lookup"><span data-stu-id="352a7-158">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-159">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="352a7-159">JET_paramPageHintCacheSize</span></span></p></td>
<td><p><span data-ttu-id="352a7-160">32</span><span class="sxs-lookup"><span data-stu-id="352a7-160">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-161">JET_paramDisablePerfmon</span><span class="sxs-lookup"><span data-stu-id="352a7-161">JET_paramDisablePerfmon</span></span></p></td>
<td><p><span data-ttu-id="352a7-162">1</span><span class="sxs-lookup"><span data-stu-id="352a7-162">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-163">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="352a7-163">JET_paramEnableFileCache</span></span></p></td>
<td><p><span data-ttu-id="352a7-164">1</span><span class="sxs-lookup"><span data-stu-id="352a7-164">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-165">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="352a7-165">JET_paramEnableViewCache</span></span></p></td>
<td><p><span data-ttu-id="352a7-166">1</span><span class="sxs-lookup"><span data-stu-id="352a7-166">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-167">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="352a7-167">JET_paramVerPageSize</span></span></p></td>
<td><p><span data-ttu-id="352a7-168">1 024</span><span class="sxs-lookup"><span data-stu-id="352a7-168">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-169">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="352a7-169">JET_paramEnableAdvanced</span></span></p></td>
<td><p><span data-ttu-id="352a7-170">0</span><span class="sxs-lookup"><span data-stu-id="352a7-170">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-171">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="352a7-171">JET_paramCheckpointIOMax</span></span></p></td>
<td><p><span data-ttu-id="352a7-172">8</span><span class="sxs-lookup"><span data-stu-id="352a7-172">8</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="352a7-173">Une petite configuration a également plusieurs autres effets sur le moteur de base de données, notamment :</span><span class="sxs-lookup"><span data-stu-id="352a7-173">Small Configuration also has several other effects on the database engine, including:</span></span>

  - <span data-ttu-id="352a7-174">Toutes les ressources gérées par les paramètres système sont allouées à partir du segment de mémoire en fonction des besoins</span><span class="sxs-lookup"><span data-stu-id="352a7-174">All resources managed by system parameters are allocated from the heap as needed</span></span>

  - <span data-ttu-id="352a7-175">Les autres ressources internes utilisées par le moteur de base de données sont réduites en taille</span><span class="sxs-lookup"><span data-stu-id="352a7-175">Other internal resources used by the database engine are scaled down in size</span></span>

  - <span data-ttu-id="352a7-176">Diverses activités de maintenance sont mises à l’échelle pour éviter l’activité des threads en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="352a7-176">Various maintenance activities are scaled back to avoid background thread activity</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="352a7-177">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="352a7-177">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="352a7-178">1 (hérité)</span><span class="sxs-lookup"><span data-stu-id="352a7-178">1 (Legacy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-179">Tapez :</span><span class="sxs-lookup"><span data-stu-id="352a7-179">Type:</span></span></p></td>
<td><p><span data-ttu-id="352a7-180">Integer</span><span class="sxs-lookup"><span data-stu-id="352a7-180">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-181">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="352a7-181">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="352a7-182">0 – 1</span><span class="sxs-lookup"><span data-stu-id="352a7-182">0 – 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-183">Étendue :</span><span class="sxs-lookup"><span data-stu-id="352a7-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="352a7-184">Instance</span><span class="sxs-lookup"><span data-stu-id="352a7-184">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-185">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="352a7-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="352a7-186">Oui</span><span class="sxs-lookup"><span data-stu-id="352a7-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-187">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="352a7-187">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="352a7-188">Non</span><span class="sxs-lookup"><span data-stu-id="352a7-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-189">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="352a7-189">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="352a7-190">Non</span><span class="sxs-lookup"><span data-stu-id="352a7-190">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-191">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="352a7-191">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="352a7-192">Non</span><span class="sxs-lookup"><span data-stu-id="352a7-192">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-193">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="352a7-193">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="352a7-194">Oui</span><span class="sxs-lookup"><span data-stu-id="352a7-194">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-195">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="352a7-195">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="352a7-196">Oui</span><span class="sxs-lookup"><span data-stu-id="352a7-196">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-197">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="352a7-197">Availability:</span></span></p></td>
<td><p><span data-ttu-id="352a7-198">À compter de Windows Server 2008 et Windows Vista</span><span class="sxs-lookup"><span data-stu-id="352a7-198">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="352a7-199">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="352a7-199">JET_paramEnableAdvanced</span></span>  
<span data-ttu-id="352a7-200">130</span><span class="sxs-lookup"><span data-stu-id="352a7-200">130</span></span>  
<span data-ttu-id="352a7-201">Ce paramètre est utilisé pour contrôler le moment où le moteur de base de données accepte ou rejette les modifications apportées à un sous-ensemble des paramètres système.</span><span class="sxs-lookup"><span data-stu-id="352a7-201">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="352a7-202">Ce paramètre est utilisé conjointement avec JET_paramConfiguration pour empêcher la définition de certains paramètres système à partir des valeurs par défaut de la configuration sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="352a7-202">This parameter is used in conjunction with JET_paramConfiguration to prevent some system parameters from being set away from the selected configuration's defaults.</span></span>

<span data-ttu-id="352a7-203">Les paramètres système suivants seront protégés de la définition lorsque ce paramètre est défini sur false :</span><span class="sxs-lookup"><span data-stu-id="352a7-203">The following system parameters will be protected from being set when this parameter is set to False:</span></span>

  - <span data-ttu-id="352a7-204">JET_paramMaxSessionsfon</span><span class="sxs-lookup"><span data-stu-id="352a7-204">JET_paramMaxSessionsfon</span></span>

  - <span data-ttu-id="352a7-205">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="352a7-205">JET_paramMaxOpenTables</span></span>

  - <span data-ttu-id="352a7-206">JET_paramPreferredMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="352a7-206">JET_paramPreferredMaxOpenTables</span></span>

  - <span data-ttu-id="352a7-207">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="352a7-207">JET_paramMaxCursors</span></span>

  - <span data-ttu-id="352a7-208">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="352a7-208">JET_paramMaxVerPages</span></span>

  - <span data-ttu-id="352a7-209">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="352a7-209">JET_paramMaxTemporaryTables</span></span>

  - <span data-ttu-id="352a7-210">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="352a7-210">JET_paramLogBuffers</span></span>

  - <span data-ttu-id="352a7-211">JET_paramWaitLogFlush</span><span class="sxs-lookup"><span data-stu-id="352a7-211">JET_paramWaitLogFlush</span></span>

  - <span data-ttu-id="352a7-212">JET_paramLogCheckpointPeriod</span><span class="sxs-lookup"><span data-stu-id="352a7-212">JET_paramLogCheckpointPeriod</span></span>

  - <span data-ttu-id="352a7-213">JET_paramLogWaitingUserMax</span><span class="sxs-lookup"><span data-stu-id="352a7-213">JET_paramLogWaitingUserMax</span></span>

  - <span data-ttu-id="352a7-214">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="352a7-214">JET_paramDbExtensionSize</span></span>

  - <span data-ttu-id="352a7-215">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="352a7-215">JET_paramPageTempDBMin</span></span>

  - <span data-ttu-id="352a7-216">JET_paramPageFragment</span><span class="sxs-lookup"><span data-stu-id="352a7-216">JET_paramPageFragment</span></span>

  - <span data-ttu-id="352a7-217">JET_paramBatchIOBufferMax</span><span class="sxs-lookup"><span data-stu-id="352a7-217">JET_paramBatchIOBufferMax</span></span>

  - <span data-ttu-id="352a7-218">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="352a7-218">JET_paramCacheSizeMax</span></span>

  - <span data-ttu-id="352a7-219">JET_paramLRUKCorrInterval</span><span class="sxs-lookup"><span data-stu-id="352a7-219">JET_paramLRUKCorrInterval</span></span>

  - <span data-ttu-id="352a7-220">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="352a7-220">JET_paramLRUKHistoryMax</span></span>

  - <span data-ttu-id="352a7-221">JET_paramLRUKPolicy</span><span class="sxs-lookup"><span data-stu-id="352a7-221">JET_paramLRUKPolicy</span></span>

  - <span data-ttu-id="352a7-222">JET_paramLRUKTimeout</span><span class="sxs-lookup"><span data-stu-id="352a7-222">JET_paramLRUKTimeout</span></span>

  - <span data-ttu-id="352a7-223">JET_paramLRUKTrxCorrInterval</span><span class="sxs-lookup"><span data-stu-id="352a7-223">JET_paramLRUKTrxCorrInterval</span></span>

  - <span data-ttu-id="352a7-224">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="352a7-224">JET_paramOutstandingIOMax</span></span>

  - <span data-ttu-id="352a7-225">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="352a7-225">JET_paramStartFlushThreshold</span></span>

  - <span data-ttu-id="352a7-226">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="352a7-226">JET_paramStopFlushThreshold</span></span>

  - <span data-ttu-id="352a7-227">JET_paramCacheSize</span><span class="sxs-lookup"><span data-stu-id="352a7-227">JET_paramCacheSize</span></span>

  - <span data-ttu-id="352a7-228">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="352a7-228">JET_paramCacheSizeMin</span></span>

  - <span data-ttu-id="352a7-229">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="352a7-229">JET_paramPreferredVerPages</span></span>

  - <span data-ttu-id="352a7-230">JET_paramBackupChunkSize</span><span class="sxs-lookup"><span data-stu-id="352a7-230">JET_paramBackupChunkSize</span></span>

  - <span data-ttu-id="352a7-231">JET_paramBackupOutstandingReads</span><span class="sxs-lookup"><span data-stu-id="352a7-231">JET_paramBackupOutstandingReads</span></span>

  - <span data-ttu-id="352a7-232">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="352a7-232">JET_paramLogFileCreateAsynch</span></span>

  - <span data-ttu-id="352a7-233">JET_paramRecordUpgradeDirtyLevel</span><span class="sxs-lookup"><span data-stu-id="352a7-233">JET_paramRecordUpgradeDirtyLevel</span></span>

  - <span data-ttu-id="352a7-234">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="352a7-234">JET_paramGlobalMinVerPages</span></span>

  - <span data-ttu-id="352a7-235">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="352a7-235">JET_paramPageHintCacheSize</span></span>

  - <span data-ttu-id="352a7-236">JET_paramVersionStoreTaskQueueMax</span><span class="sxs-lookup"><span data-stu-id="352a7-236">JET_paramVersionStoreTaskQueueMax</span></span>

  - <span data-ttu-id="352a7-237">JET_paramDBAPageAvailMin</span><span class="sxs-lookup"><span data-stu-id="352a7-237">JET_paramDBAPageAvailMin</span></span>

  - <span data-ttu-id="352a7-238">JET_paramMaxRandomIOSize</span><span class="sxs-lookup"><span data-stu-id="352a7-238">JET_paramMaxRandomIOSize</span></span>

  - <span data-ttu-id="352a7-239">JET_paramCachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="352a7-239">JET_paramCachedClosedTables</span></span>

  - <span data-ttu-id="352a7-240">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="352a7-240">JET_paramEnableFileCache</span></span>

  - <span data-ttu-id="352a7-241">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="352a7-241">JET_paramEnableViewCache</span></span>

  - <span data-ttu-id="352a7-242">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="352a7-242">JET_paramVerPageSize</span></span>

  - <span data-ttu-id="352a7-243">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="352a7-243">JET_paramCheckpointIOMax</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="352a7-244">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="352a7-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="352a7-245">Vrai</span><span class="sxs-lookup"><span data-stu-id="352a7-245">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-246">Tapez :</span><span class="sxs-lookup"><span data-stu-id="352a7-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="352a7-247">Boolean</span><span class="sxs-lookup"><span data-stu-id="352a7-247">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-248">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="352a7-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="352a7-249">False, True</span><span class="sxs-lookup"><span data-stu-id="352a7-249">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-250">Étendue :</span><span class="sxs-lookup"><span data-stu-id="352a7-250">Scope:</span></span></p></td>
<td><p><span data-ttu-id="352a7-251">Instance</span><span class="sxs-lookup"><span data-stu-id="352a7-251">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-252">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="352a7-252">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="352a7-253">Oui</span><span class="sxs-lookup"><span data-stu-id="352a7-253">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-254">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="352a7-254">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="352a7-255">Oui</span><span class="sxs-lookup"><span data-stu-id="352a7-255">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-256">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="352a7-256">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="352a7-257">Non</span><span class="sxs-lookup"><span data-stu-id="352a7-257">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-258">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="352a7-258">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="352a7-259">Non</span><span class="sxs-lookup"><span data-stu-id="352a7-259">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-260">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="352a7-260">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="352a7-261">Non</span><span class="sxs-lookup"><span data-stu-id="352a7-261">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-262">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="352a7-262">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="352a7-263">Non</span><span class="sxs-lookup"><span data-stu-id="352a7-263">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-264">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="352a7-264">Availability:</span></span></p></td>
<td><p><span data-ttu-id="352a7-265">À compter de Windows Server 2008 et Windows Vista</span><span class="sxs-lookup"><span data-stu-id="352a7-265">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="352a7-266">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="352a7-266">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="352a7-267"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="352a7-267"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="352a7-268">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="352a7-268">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352a7-269"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="352a7-269"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="352a7-270">Requiert Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="352a7-270">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352a7-271"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="352a7-271"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="352a7-272">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="352a7-272">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="352a7-273">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="352a7-273">See Also</span></span>

[<span data-ttu-id="352a7-274">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="352a7-274">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="352a7-275">JetInit</span><span class="sxs-lookup"><span data-stu-id="352a7-275">JetInit</span></span>](./jetinit-function.md)
