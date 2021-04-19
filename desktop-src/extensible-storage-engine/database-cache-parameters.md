---
description: 'En savoir plus sur : paramètres de cache de base de données'
title: Paramètres du cache de base de données
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543469"
---
# <a name="database-cache-parameters"></a><span data-ttu-id="f1edd-103">Paramètres du cache de base de données</span><span class="sxs-lookup"><span data-stu-id="f1edd-103">Database Cache Parameters</span></span>


<span data-ttu-id="f1edd-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f1edd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-cache-parameters"></a><span data-ttu-id="f1edd-105">Paramètres du cache de base de données</span><span class="sxs-lookup"><span data-stu-id="f1edd-105">Database Cache Parameters</span></span>

<span data-ttu-id="f1edd-106">Cette rubrique contient des paramètres qui sont utilisés pour le cache de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-106">This topic contains parameters that are used for the database cache.</span></span>

<span data-ttu-id="f1edd-107">*JET_paramBatchIOBufferMax*</span><span class="sxs-lookup"><span data-stu-id="f1edd-107">*JET_paramBatchIOBufferMax*</span></span>  
<span data-ttu-id="f1edd-108">22</span><span class="sxs-lookup"><span data-stu-id="f1edd-108">22</span></span>  

<span data-ttu-id="f1edd-109">Ce paramètre contrôle la taille d’une partie auxiliaire du cache des pages de base de données qui est utilisé pour simuler des e/s de regroupement de nuages de points lorsqu’il n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="f1edd-109">This parameter controls the size of an auxiliary part of the database page cache that is used to simulate scatter gather I/O when it is otherwise not available.</span></span> <span data-ttu-id="f1edd-110">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-110">The size is in database pages.</span></span>

<span data-ttu-id="f1edd-111">**Windows XP et versions ultérieures :**  Ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-111">**Windows XP and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-112">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-113">256</span><span class="sxs-lookup"><span data-stu-id="f1edd-113">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-114">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-115">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-116">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-117">0, 2 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="f1edd-117">0, 2 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-118">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-119">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-119">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-120">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-121">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-121">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-122">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-123">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-124">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-125">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-126">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-127">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-128">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-129">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-130">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-131">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-132">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-133">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-133">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-134">*JET_paramCacheSize*</span><span class="sxs-lookup"><span data-stu-id="f1edd-134">*JET_paramCacheSize*</span></span>  
<span data-ttu-id="f1edd-135">41</span><span class="sxs-lookup"><span data-stu-id="f1edd-135">41</span></span>  

<span data-ttu-id="f1edd-136">Ce paramètre peut être utilisé pour contrôler la taille du cache de la page de base de données au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f1edd-136">This parameter can be used to control the size of the database page cache at run time.</span></span> <span data-ttu-id="f1edd-137">En règle générale, le cache ajuste automatiquement sa taille en fonction des niveaux d’activité de la base de données et de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f1edd-137">Ordinarily, the cache will automatically tune its size as a function of database and machine activity levels.</span></span> <span data-ttu-id="f1edd-138">Si l’application définit ce paramètre sur zéro, le cache ajuste sa propre taille de cette manière.</span><span class="sxs-lookup"><span data-stu-id="f1edd-138">If the application sets this parameter to zero, then the cache will tune its own size in this manner.</span></span> <span data-ttu-id="f1edd-139">Toutefois, si l’application définit ce paramètre sur une valeur différente de zéro, le cache s’ajuste à cette taille cible (dans les pages de base de données).</span><span class="sxs-lookup"><span data-stu-id="f1edd-139">However, if the application sets this parameter to a non-zero value then the cache will adjust itself to that target size (in database pages).</span></span> <span data-ttu-id="f1edd-140">Le cache conserve sa taille à ce seuil jusqu’à ce qu’une nouvelle taille soit donnée ou jusqu’à ce qu’il soit relâché pour choisir sa propre taille.</span><span class="sxs-lookup"><span data-stu-id="f1edd-140">The cache will then hold its size at that threshold until given a new size or until it is released to choose its own size.</span></span>

<span data-ttu-id="f1edd-141">**Remarque**  La taille du cache est toujours soumise aux limites imposées par **JET_paramCacheSizeMin** et **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="f1edd-141">**Note**  The cache size is still subject to the limits imposed by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="f1edd-142">Lorsque ce paramètre est lu, la taille réelle du cache dans les pages de la base de données est retournée.</span><span class="sxs-lookup"><span data-stu-id="f1edd-142">When this parameter is read, the actual size of the cache in database pages is returned.</span></span> <span data-ttu-id="f1edd-143">Cette taille peut être utilisée par l’application comme entrée pour conduire son ajustement manuel de la taille du cache.</span><span class="sxs-lookup"><span data-stu-id="f1edd-143">This size can be used by the application as an input to drive its manual adjustment of the cache size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-144">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-144">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-145">Spécial</span><span class="sxs-lookup"><span data-stu-id="f1edd-145">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-146">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-146">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-147">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-147">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-148">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-148">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-149"><strong>Windows 2000 :</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="f1edd-149"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="f1edd-150"><strong>Windows XP :</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="f1edd-150"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-151">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-152">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-153">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-154">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-155">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-155">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-156">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-157">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-157">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-158">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-159">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-159">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-160">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-161">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-161">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-162">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-163">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-163">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-164">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-164">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-165">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-165">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-166">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-166">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-167">*JET_paramCacheSizeMin*</span><span class="sxs-lookup"><span data-stu-id="f1edd-167">*JET_paramCacheSizeMin*</span></span>  
<span data-ttu-id="f1edd-168">60</span><span class="sxs-lookup"><span data-stu-id="f1edd-168">60</span></span>  

<span data-ttu-id="f1edd-169">Ce paramètre configure la taille minimale du cache des pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-169">This parameter configures the minimum size of the database page cache.</span></span> <span data-ttu-id="f1edd-170">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-170">The size is in database pages.</span></span>

<span data-ttu-id="f1edd-171">Par défaut, le cache de base de données ajuste automatiquement sa taille entre les limites définies par **JET_paramCacheSizeMin** et **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="f1edd-171">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="f1edd-172">**Windows 2000 :**  Sur Windows 2000, ce paramètre doit être défini sur une valeur à peu près égal à quatre fois le nombre de threads qui se trouveront à l’intérieur de l’API ESE en même temps.</span><span class="sxs-lookup"><span data-stu-id="f1edd-172">**Windows 2000:**  On Windows 2000, this parameter should be set to a value roughly equal to four times the number of threads that will be inside the ESE API at the same time.</span></span> <span data-ttu-id="f1edd-173">Cela est nécessaire pour éviter les blocages provoqués par un nombre insuffisant de tampons de cache de pages de base de données pour effectuer des opérations complexes telles que les fractionnements d’arborescences B +.</span><span class="sxs-lookup"><span data-stu-id="f1edd-173">This is required to avoid deadlocks caused by an insufficient number of database page cache buffers to perform complex operations like B+ Tree splits.</span></span>

<span data-ttu-id="f1edd-174">**Windows XP et versions ultérieures :**  Le gestionnaire de cache définit automatiquement sa propre taille de cache minimale pour éviter les interblocages.</span><span class="sxs-lookup"><span data-stu-id="f1edd-174">**Windows XP and later:**  The cache manager will automatically set its own minimum cache size to avoid deadlocks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-175">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-176"><strong>Windows 2000 :</strong>  64</span><span class="sxs-lookup"><span data-stu-id="f1edd-176"><strong>Windows 2000:</strong>  64</span></span></p>
<p><span data-ttu-id="f1edd-177"><strong>Windows XP :</strong>  1</span><span class="sxs-lookup"><span data-stu-id="f1edd-177"><strong>Windows XP:</strong>  1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-178">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-179">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-179">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-180">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-181"><strong>Windows 2000 :</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="f1edd-181"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="f1edd-182"><strong>Windows XP :</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="f1edd-182"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-183">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-184">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-184">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-185">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-186"><strong>Windows 2000 :</strong>  º</span><span class="sxs-lookup"><span data-stu-id="f1edd-186"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="f1edd-187"><strong>Windows XP :</strong>  Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-187"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-188">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-188">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-189"><strong>Windows 2000 :</strong>  º</span><span class="sxs-lookup"><span data-stu-id="f1edd-189"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="f1edd-190"><strong>Windows XP :</strong>  Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-190"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-191">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-191">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-192">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-192">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-193">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-193">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-194">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-195">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-195">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-196">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-196">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-197">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-197">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-198">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-199">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-199">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-200">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-200">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-201">*JET_paramCacheSizeMax*</span><span class="sxs-lookup"><span data-stu-id="f1edd-201">*JET_paramCacheSizeMax*</span></span>  
<span data-ttu-id="f1edd-202">23</span><span class="sxs-lookup"><span data-stu-id="f1edd-202">23</span></span>  

<span data-ttu-id="f1edd-203">Ce paramètre configure la taille maximale du cache des pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-203">This parameter configures the maximum size of the database page cache.</span></span> <span data-ttu-id="f1edd-204">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-204">The size is in database pages.</span></span>

<span data-ttu-id="f1edd-205">Par défaut, le cache de base de données ajuste automatiquement sa taille entre les limites définies par **JET_paramCacheSizeMin** et **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="f1edd-205">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="f1edd-206">**Remarque**   Si ce paramètre est laissé à sa valeur par défaut, la taille maximale du cache sera définie sur la taille de la mémoire physique lors de l’appel de [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="f1edd-206">**Note**   If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when [JetInit](./jetinit-function.md) is called.</span></span>

<span data-ttu-id="f1edd-207">**Windows Vista :**  À compter de Windows Vista, la valeur par défaut de ce paramètre a été modifiée pour clarifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="f1edd-207">**Windows Vista:**  As of Windows Vista, the default value of this parameter was changed to clarify this behavior.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-208">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-208">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-209"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  512</span><span class="sxs-lookup"><span data-stu-id="f1edd-209"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  512</span></span></p>
<p><span data-ttu-id="f1edd-210"><strong>Windows Vista :</strong>  2 milliards</span><span class="sxs-lookup"><span data-stu-id="f1edd-210"><strong>Windows Vista:</strong>  2000000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-211">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-212">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-212">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-213">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-214"><strong>Windows 2000 :</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="f1edd-214"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="f1edd-215"><strong>Windows XP :</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="f1edd-215"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-216">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-216">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-217">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-217">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-218">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-219"><strong>Windows 2000 :</strong>  º</span><span class="sxs-lookup"><span data-stu-id="f1edd-219"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="f1edd-220"><strong>Windows XP :</strong>  Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-220"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-221">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-221">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-222"><strong>Windows XP et windows 2000 :</strong>  º</span><span class="sxs-lookup"><span data-stu-id="f1edd-222"><strong>Windows XP and Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="f1edd-223"><strong>Windows Vista et Windows Server 2003 :</strong>  Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-223"><strong>Windows Vista and Windows Server 2003:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-224">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-224">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-225">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-225">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-226">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-226">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-227">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-227">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-228">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-228">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-229">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-229">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-230">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-230">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-231">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-231">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-232">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-232">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-233">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-233">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-234">*JET_paramCheckpointDepthMax*</span><span class="sxs-lookup"><span data-stu-id="f1edd-234">*JET_paramCheckpointDepthMax*</span></span>  
<span data-ttu-id="f1edd-235">24</span><span class="sxs-lookup"><span data-stu-id="f1edd-235">24</span></span> 

<span data-ttu-id="f1edd-236">Ce paramètre contrôle le vidage des pages de base de données à partir du cache des pages de base de données afin de réduire le temps nécessaire à la récupération d’un incident.</span><span class="sxs-lookup"><span data-stu-id="f1edd-236">This parameter controls how aggressively database pages are flushed from the database page cache to minimize the amount of time it will take to recover from a crash.</span></span> <span data-ttu-id="f1edd-237">Le paramètre est un seuil en octets pour le nombre de fichiers journaux des transactions qui doivent être relus après un incident.</span><span class="sxs-lookup"><span data-stu-id="f1edd-237">The parameter is a threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span>

<span data-ttu-id="f1edd-238">Si l’enregistrement circulaire est activé à l’aide de [JET_paramCircularLog](./transaction-log-parameters.md) , ce paramètre contrôle également la quantité approximative de fichiers du journal des transactions qui seront conservés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="f1edd-238">If circular logging is enabled using [JET_paramCircularLog](./transaction-log-parameters.md) then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="f1edd-239">Il est important que ce paramètre ne soit pas défini trop bas.</span><span class="sxs-lookup"><span data-stu-id="f1edd-239">It is important that this parameter not be set too low.</span></span> <span data-ttu-id="f1edd-240">Étant donné que la valeur de ce paramètre est proche de zéro, le cache devient de plus en plus agressif lors du vidage des pages de base de données sur le disque.</span><span class="sxs-lookup"><span data-stu-id="f1edd-240">As the value of this parameter approaches zero, the cache will become more and more aggressive when flushing database pages to disk.</span></span> <span data-ttu-id="f1edd-241">Cela aboutit non seulement à un nombre accru d’écritures dans les fichiers de base de données, mais aussi à un nombre accru de lectures dans ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="f1edd-241">This not only results in an increased number of writes to the database files but it also indirectly causes an increased number of reads to those files as well.</span></span> <span data-ttu-id="f1edd-242">Cela peut entraîner des problèmes de performances très importants dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="f1edd-242">This can cause very significant performance problems in some cases.</span></span> <span data-ttu-id="f1edd-243">Malheureusement, la définition de la plus petite valeur optimale pour ce paramètre ne peut être effectuée qu’à l’aide de l’expérimentation avec l’application cible.</span><span class="sxs-lookup"><span data-stu-id="f1edd-243">Unfortunately, setting the smallest optimal value for this parameter can only be done using experimentation with the target application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-244">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-245">20971520</span><span class="sxs-lookup"><span data-stu-id="f1edd-245">20971520</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-246">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-247">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-247">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-248">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-249"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="f1edd-249"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 2147483647</span></span></p>
<p><span data-ttu-id="f1edd-250"><strong>Windows Vista :</strong>  Toutes les valeurs</span><span class="sxs-lookup"><span data-stu-id="f1edd-250"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-251">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-251">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-252"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong> Ce paramètre est global.</span><span class="sxs-lookup"><span data-stu-id="f1edd-252"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong> This parameter is global.</span></span></p>
<p><span data-ttu-id="f1edd-253"><strong>Windows Vista :</strong>  Ce paramètre est par instance.</span><span class="sxs-lookup"><span data-stu-id="f1edd-253"><strong>Windows Vista:</strong>  This parameter is per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-254">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-254">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-255">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-255">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-256">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-256">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-257">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-257">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-258">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-258">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-259">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-259">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-260">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-260">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-261">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-261">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-262">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-262">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-263">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-263">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-264">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-264">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-265">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-265">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-266">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-266">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-267">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-267">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-268">*JET_paramCheckpointIOMax*</span><span class="sxs-lookup"><span data-stu-id="f1edd-268">*JET_paramCheckpointIOMax*</span></span>  
<span data-ttu-id="f1edd-269">135</span><span class="sxs-lookup"><span data-stu-id="f1edd-269">135</span></span>  

<span data-ttu-id="f1edd-270">Ce paramètre contrôle le nombre maximal d’écritures simultanées que le moteur de base de données utilisera pour vider les pages modifiées de la base de données dans le but d’avancer le point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f1edd-270">This parameter controls the maximum number of concurrent writes that the database engine will use to flush modified database pages for the purpose of advancing the checkpoint.</span></span> <span data-ttu-id="f1edd-271">La valeur de ce paramètre peut être utilisée pour équilibrer la vitesse à laquelle le point de contrôle peut être avancé par rapport à l’impact négatif que ce processus aura sur le temps de réponse pour les autres opérations d’e/s sur les disques contenant la base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-271">The value of this parameter can be used to balance the speed with which the checkpoint can be advanced versus the negative impact this process will have on the response time for other I/O operations to the disks holding the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-272">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-272">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-273">96</span><span class="sxs-lookup"><span data-stu-id="f1edd-273">96</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-274">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-274">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-275">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-275">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-276">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-276">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-277">8 – 1024</span><span class="sxs-lookup"><span data-stu-id="f1edd-277">8 – 1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-278">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-278">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-279">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-279">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-280">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-280">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-281">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-281">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-282">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-282">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-283">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-283">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-284">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-284">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-285">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-285">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-286">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-286">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-287">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-288">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-288">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-289">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-289">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-290">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-290">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-291">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-292">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-292">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-293">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="f1edd-293">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-294">*JET_paramEnableViewCache*</span><span class="sxs-lookup"><span data-stu-id="f1edd-294">*JET_paramEnableViewCache*</span></span>  
<span data-ttu-id="f1edd-295">127</span><span class="sxs-lookup"><span data-stu-id="f1edd-295">127</span></span>  

<span data-ttu-id="f1edd-296">Lorsque ce paramètre a la **valeur true**, le moteur de base de données utilise les données de base de données directement à partir du cache de fichiers Windows au lieu de copier les données mises en cache dans sa propre mémoire privée.</span><span class="sxs-lookup"><span data-stu-id="f1edd-296">When this parameter is **True**, the database engine will use database data directly from the Windows file cache rather than copying the cached data into its own private memory.</span></span> <span data-ttu-id="f1edd-297">Toutes les données de base de données modifiées seront toujours mises en cache dans la mémoire privée.</span><span class="sxs-lookup"><span data-stu-id="f1edd-297">Any database data that is modified will still be cached in private memory.</span></span>

<span data-ttu-id="f1edd-298">L’objectif de ce mode est de réduire davantage la quantité de mémoire privée utilisée par le moteur de base de données pour mettre en cache les données de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-298">The intent of this mode is to further reduce the amount of private memory used by the database engine to cache database data.</span></span>

<span data-ttu-id="f1edd-299">Le cache de vue ne peut être utilisé que si l’utilisation du cache de fichiers Windows est activée en affectant à JET_paramEnableFileCache la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="f1edd-299">The view cache may only be used if the use of the Windows file cache is enabled by setting JET_paramEnableFileCache to **True**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-300">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-300">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-301">Faux</span><span class="sxs-lookup"><span data-stu-id="f1edd-301">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-302">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-302">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-303">Boolean</span><span class="sxs-lookup"><span data-stu-id="f1edd-303">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-304">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-304">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-305">False, True</span><span class="sxs-lookup"><span data-stu-id="f1edd-305">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-306">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-306">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-307">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-307">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-308">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-308">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-309">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-309">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-310">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-310">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-311">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-311">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-312">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-312">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-313">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-313">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-314">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-314">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-315">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-315">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-316">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-316">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-317">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-318">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-318">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-319">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-319">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-320">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-320">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-321">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="f1edd-321">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-322">*JET_paramLRUKCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="f1edd-322">*JET_paramLRUKCorrInterval*</span></span>  
<span data-ttu-id="f1edd-323">25</span><span class="sxs-lookup"><span data-stu-id="f1edd-323">25</span></span>  

<span data-ttu-id="f1edd-324">Ce paramètre définit l’intervalle de temps, en microsecondes, pendant lequel deux accès à une page de base de données sont considérés comme corrélés.</span><span class="sxs-lookup"><span data-stu-id="f1edd-324">This parameter sets the time interval in microseconds over which two database page accesses are considered to be correlated.</span></span> <span data-ttu-id="f1edd-325">Cet intervalle de corrélation contrôle la sensibilité de l’algorithme de remplacement de page (LRU-K) du cache aux accès aux pages successives.</span><span class="sxs-lookup"><span data-stu-id="f1edd-325">This correlation interval controls the sensitivity of the cache's page replacement algorithm (LRU-K) to successive page accesses.</span></span> <span data-ttu-id="f1edd-326">Cela affecte à son tour les pages qu’il choisit de conserver en cache.</span><span class="sxs-lookup"><span data-stu-id="f1edd-326">This in turn will affect which pages it chooses to keep cached.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-327">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-327">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-328">128000</span><span class="sxs-lookup"><span data-stu-id="f1edd-328">128000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-329">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-329">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-330">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-330">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-331">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-331">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-332"><strong>Windows 2000, Windows XP et Windows Server 2003 : </strong>    0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="f1edd-332"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>    0 – 2147483647</span></span></p>
<p><span data-ttu-id="f1edd-333"><strong>Windows Vista :</strong>  Toutes les valeurs</span><span class="sxs-lookup"><span data-stu-id="f1edd-333"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-334">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-334">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-335">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-335">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-336">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-336">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-337">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-337">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-338">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-338">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-339">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-340">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-340">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-341">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-341">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-342">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-342">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-343">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-343">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-344">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-344">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-345">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-345">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-346">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-346">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-347">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-347">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-348">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-348">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-349">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-349">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-350">*JET_paramLRUKHistoryMax*</span><span class="sxs-lookup"><span data-stu-id="f1edd-350">*JET_paramLRUKHistoryMax*</span></span>  
<span data-ttu-id="f1edd-351">26</span><span class="sxs-lookup"><span data-stu-id="f1edd-351">26</span></span>  

<span data-ttu-id="f1edd-352">Ce paramètre définit le nombre maximal de pages de base de données non mises en cache pour lesquelles les heures d’accès à la page de base de données sont conservées.</span><span class="sxs-lookup"><span data-stu-id="f1edd-352">This parameter sets the maximum number of non cached database pages for which database page access times will be retained.</span></span> <span data-ttu-id="f1edd-353">Ces enregistrements d’historique permettent à l’algorithme de remplacement de page (LRU-K) du cache de détecter plus précisément les pages populaires qui ont été supprimées incorrectement dans le cache des pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-353">These history records allow the cache's page replacement algorithm (LRU-K) to more accurately detect popular pages that were wrongly evicted from the database page cache.</span></span>

<span data-ttu-id="f1edd-354">**Windows XP et Windows Server 2003 :**  Ce paramètre est ignoré sur Windows XP et Windows Server 2003 et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-354">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-355">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-355">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-356"><strong>Windows 2000 :</strong>  1024</span><span class="sxs-lookup"><span data-stu-id="f1edd-356"><strong>Windows 2000:</strong>  1024</span></span></p>
<p><span data-ttu-id="f1edd-357"><strong>Windows Vista :</strong>  100000</span><span class="sxs-lookup"><span data-stu-id="f1edd-357"><strong>Windows Vista:</strong>  100000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-358">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-358">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-359">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-359">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-360">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-360">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-361"><strong>Windows 2000 :</strong>  0 – 4194303</span><span class="sxs-lookup"><span data-stu-id="f1edd-361"><strong>Windows 2000:</strong>  0 – 4194303</span></span></p>
<p><span data-ttu-id="f1edd-362"><strong>Windows Vista :</strong>  Toutes les valeurs</span><span class="sxs-lookup"><span data-stu-id="f1edd-362"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-363">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-363">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-364">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-364">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-365">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-365">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-366">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-366">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-367">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-367">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-368">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-368">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-369">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-369">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-370">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-370">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-371">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-371">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-372">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-372">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-373">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-373">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-374">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-374">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-375">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-375">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-376">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-376">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-377">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-377">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-378">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-378">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-379">*JET_paramLRUKPolicy*</span><span class="sxs-lookup"><span data-stu-id="f1edd-379">*JET_paramLRUKPolicy*</span></span>  
<span data-ttu-id="f1edd-380">27</span><span class="sxs-lookup"><span data-stu-id="f1edd-380">27</span></span>  

<span data-ttu-id="f1edd-381">Ce paramètre configure le nombre d’accès à la page de base de données qui sont pris en compte pour déterminer l’utilité de la page.</span><span class="sxs-lookup"><span data-stu-id="f1edd-381">This parameter configures the number of database page accesses that are considered for determining the usefulness of the page.</span></span> <span data-ttu-id="f1edd-382">Ce paramètre est essentiellement le K dans LRU-K, l’algorithme de remplacement de page du cache de page de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-382">This parameter is essentially the K in LRU-K, the database page cache's page replacement algorithm.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-383">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-384">2</span><span class="sxs-lookup"><span data-stu-id="f1edd-384">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-385">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-386">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-386">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-387">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-388">1-2</span><span class="sxs-lookup"><span data-stu-id="f1edd-388">1-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-389">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-390">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-390">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-391">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-392">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-392">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-393">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-394">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-395">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-396">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-396">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-397">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-398">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-398">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-399">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-400">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-401">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-402">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-403">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-404">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-405">*JET_paramLRUKTimeout*</span><span class="sxs-lookup"><span data-stu-id="f1edd-405">*JET_paramLRUKTimeout*</span></span>  
<span data-ttu-id="f1edd-406">28</span><span class="sxs-lookup"><span data-stu-id="f1edd-406">28</span></span>

<span data-ttu-id="f1edd-407">Ce paramètre indique la durée, en secondes, au terme de laquelle une page du cache de la page de base de données est considérée comme ayant perdu un accès à la page dans le but d’évaluer l’utilité de la page.</span><span class="sxs-lookup"><span data-stu-id="f1edd-407">This parameter indicates the period of time in seconds after which a page in the database page cache is considered to have lost a page access for the purpose of considering the usefulness of the page.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-408">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-408">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-409">100</span><span class="sxs-lookup"><span data-stu-id="f1edd-409">100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-410">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-410">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-411">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-411">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-412">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-412">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-413"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="f1edd-413"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  1 – 2147483647</span></span></p>
<p><span data-ttu-id="f1edd-414"><strong>Windows Vista :</strong>   1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="f1edd-414"><strong>Windows Vista:</strong>   1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-415">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-415">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-416">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-416">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-417">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-417">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-418">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-418">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-419">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-419">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-420">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-420">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-421">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-421">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-422">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-422">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-423">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-423">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-424">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-424">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-425">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-425">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-426">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-426">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-427">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-427">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-428">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-428">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-429">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-429">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-430">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-430">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-431">*JET_paramLRUKTrxCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="f1edd-431">*JET_paramLRUKTrxCorrInterval*</span></span>  
<span data-ttu-id="f1edd-432">29</span><span class="sxs-lookup"><span data-stu-id="f1edd-432">29</span></span>  

<span data-ttu-id="f1edd-433">Ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="f1edd-433">This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<span data-ttu-id="f1edd-434">*JET_paramStartFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="f1edd-434">*JET_paramStartFlushThreshold*</span></span>  
<span data-ttu-id="f1edd-435">31</span><span class="sxs-lookup"><span data-stu-id="f1edd-435">31</span></span>  

<span data-ttu-id="f1edd-436">Ce paramètre contrôle le moment où le cache de la page de base de données commence à supprimer des pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="f1edd-436">This parameter controls when the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="f1edd-437">Lorsque le nombre de tampons de page dans le cache descend sous ce seuil, un processus en arrière-plan est démarré pour réapprovisionner ce pool de mémoires tampons disponibles.</span><span class="sxs-lookup"><span data-stu-id="f1edd-437">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="f1edd-438">Ce seuil est toujours relatif à la taille maximale du cache définie par **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="f1edd-438">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="f1edd-439">Ce seuil doit également toujours être inférieur au seuil d’arrêt défini par **JET_paramStopFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="f1edd-439">This threshold must also always be less than the stop threshold as set by **JET_paramStopFlushThreshold**.</span></span>

<span data-ttu-id="f1edd-440">La hauteur de distance du seuil de démarrage détermine le temps de réponse que le cache de page de la base de données doit avoir pour produire des tampons disponibles avant que l’application en ait besoin.</span><span class="sxs-lookup"><span data-stu-id="f1edd-440">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="f1edd-441">Un seuil de démarrage élevé donnera plus de temps au processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f1edd-441">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="f1edd-442">Toutefois, un seuil de démarrage élevé implique un seuil d’arrêt plus élevé et réduit la taille effective du cache des pages de base de données pour les pages modifiées (Windows 2000) ou pour toutes les pages (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="f1edd-442">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-443">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-443">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-444"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  5 (1%)</span><span class="sxs-lookup"><span data-stu-id="f1edd-444"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  5 (1%)</span></span></p>
<p><span data-ttu-id="f1edd-445"><strong>Windows Vista :</strong>  20 millions (1%)</span><span class="sxs-lookup"><span data-stu-id="f1edd-445"><strong>Windows Vista:</strong>  20000000 (1%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-446">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-446">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-447">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-447">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-448">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-448">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-449"><strong>Windows 2000 :</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="f1edd-449"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="f1edd-450"><strong>Windows XP :</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="f1edd-450"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="f1edd-451"><strong>Windows Vista :</strong>  Toutes les valeurs</span><span class="sxs-lookup"><span data-stu-id="f1edd-451"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-452">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-452">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-453">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-453">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-454">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-454">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-455">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-455">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-456">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-456">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-457">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-457">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-458">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-458">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-459">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-459">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-460">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-460">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-461">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-461">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-462">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-462">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-463">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-463">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-464">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-464">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-465">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-465">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-466">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-466">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-467">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-467">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1edd-468">*JET_paramStopFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="f1edd-468">*JET_paramStopFlushThreshold*</span></span>  
<span data-ttu-id="f1edd-469">32</span><span class="sxs-lookup"><span data-stu-id="f1edd-469">32</span></span>  

<span data-ttu-id="f1edd-470">Ce paramètre contrôle le moment où le cache de la page de base de données met fin à la suppression des pages du cache pour libérer de l’espace pour les pages qui ne sont pas mises en cache.</span><span class="sxs-lookup"><span data-stu-id="f1edd-470">This parameter controls when the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="f1edd-471">Lorsque le nombre de tampons de page dans le cache dépasse ce seuil, le processus en arrière-plan qui a démarré pour réapprovisionner ce pool de mémoires tampons disponibles est arrêté.</span><span class="sxs-lookup"><span data-stu-id="f1edd-471">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="f1edd-472">Ce seuil est toujours relatif à la taille maximale du cache définie par **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="f1edd-472">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="f1edd-473">Ce seuil doit également être toujours supérieur au seuil de démarrage défini par **JET_paramStartFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="f1edd-473">This threshold must also always be greater than the start threshold as set by **JET_paramStartFlushThreshold**.</span></span>

<span data-ttu-id="f1edd-474">La distance entre le seuil de démarrage et le seuil d’arrêt affecte l’efficacité avec laquelle les pages de base de données sont vidées par le processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f1edd-474">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="f1edd-475">Un plus grand fossé rendra plus probable l’Association des écritures aux pages voisines.</span><span class="sxs-lookup"><span data-stu-id="f1edd-475">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="f1edd-476">Toutefois, un seuil d’arrêt élevé réduira la taille effective du cache des pages de base de données pour les pages modifiées (Windows 2000) ou pour toutes les pages (Windows XP et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="f1edd-476">However, a high stop threshold will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-477">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f1edd-477">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-478"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  10 (2%)</span><span class="sxs-lookup"><span data-stu-id="f1edd-478"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  10 (2%)</span></span></p>
<p><span data-ttu-id="f1edd-479"><strong>Windows Vista :</strong>  40 millions (2%)</span><span class="sxs-lookup"><span data-stu-id="f1edd-479"><strong>Windows Vista:</strong>  40000000 (2%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-480">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f1edd-480">Type:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-481">Integer</span><span class="sxs-lookup"><span data-stu-id="f1edd-481">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-482">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f1edd-482">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-483"><strong>Windows 2000 :</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="f1edd-483"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="f1edd-484"><strong>Windows XP :</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="f1edd-484"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="f1edd-485"><strong>Windows Vista :</strong>  Toutes les valeurs</span><span class="sxs-lookup"><span data-stu-id="f1edd-485"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-486">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f1edd-486">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-487">Global</span><span class="sxs-lookup"><span data-stu-id="f1edd-487">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-488">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-488">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-489">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-489">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-490">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f1edd-490">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-491">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-491">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-492">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f1edd-492">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-493">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-493">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-494">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-494">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-495">Non</span><span class="sxs-lookup"><span data-stu-id="f1edd-495">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-496">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f1edd-496">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-497">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-497">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-498">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f1edd-498">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-499">Oui</span><span class="sxs-lookup"><span data-stu-id="f1edd-499">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-500">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f1edd-500">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f1edd-501">Tous</span><span class="sxs-lookup"><span data-stu-id="f1edd-501">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="f1edd-502">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1edd-502">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-503"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f1edd-503"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f1edd-504">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f1edd-504">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1edd-505"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f1edd-505"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f1edd-506">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f1edd-506">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1edd-507"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f1edd-507"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f1edd-508">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f1edd-508">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f1edd-509">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1edd-509">See Also</span></span>

[<span data-ttu-id="f1edd-510">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="f1edd-510">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="f1edd-511">JetInit</span><span class="sxs-lookup"><span data-stu-id="f1edd-511">JetInit</span></span>](./jetinit-function.md)
