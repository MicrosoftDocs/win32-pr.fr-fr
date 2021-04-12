---
description: En savoir plus sur les paramètres de base de données temporaires
title: Paramètres de base de données temporaires
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: c137472d03f1088da061c20b52050ae1a1f6629e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210096"
---
# <a name="temporary-database-parameters"></a><span data-ttu-id="f35f4-103">Paramètres de base de données temporaires</span><span class="sxs-lookup"><span data-stu-id="f35f4-103">Temporary Database Parameters</span></span>


<span data-ttu-id="f35f4-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="f35f4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="temporary-database-parameters"></a><span data-ttu-id="f35f4-105">Paramètres de base de données temporaires</span><span class="sxs-lookup"><span data-stu-id="f35f4-105">Temporary Database Parameters</span></span>

<span data-ttu-id="f35f4-106">Cette rubrique contient les paramètres utilisés pour la base de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="f35f4-106">This topic contains parameters that are used for the temporary database.</span></span>

<span data-ttu-id="f35f4-107">*JET_paramEnableTempTableVersioning*</span><span class="sxs-lookup"><span data-stu-id="f35f4-107">*JET_paramEnableTempTableVersioning*</span></span>  
<span data-ttu-id="f35f4-108">46</span><span class="sxs-lookup"><span data-stu-id="f35f4-108">46</span></span>  

<span data-ttu-id="f35f4-109">Ce paramètre contrôle l’utilisation des transactions dans les tables temporaires.</span><span class="sxs-lookup"><span data-stu-id="f35f4-109">This parameter controls the use of transactions in temporary tables.</span></span> <span data-ttu-id="f35f4-110">Lorsque ce paramètre a la valeur false, les tables temporaires sont plus rapides, mais il n’est pas possible de restaurer les mises à jour effectuées dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="f35f4-110">When this parameter is false, temporary tables will be faster but it will not be possible to rollback any updates made in a transaction.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-111">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f35f4-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-112">Vrai</span><span class="sxs-lookup"><span data-stu-id="f35f4-112">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f35f4-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="f35f4-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-115">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f35f4-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-116">False, True</span><span class="sxs-lookup"><span data-stu-id="f35f4-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-117">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f35f4-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-118">Instance</span><span class="sxs-lookup"><span data-stu-id="f35f4-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-119">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f35f4-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-120">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-121">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f35f4-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-122">Non</span><span class="sxs-lookup"><span data-stu-id="f35f4-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-123">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f35f4-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-124">Non</span><span class="sxs-lookup"><span data-stu-id="f35f4-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-125">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f35f4-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-126">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-126">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-127">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f35f4-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-128">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-129">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f35f4-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-130">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-131">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f35f4-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-132">Tous</span><span class="sxs-lookup"><span data-stu-id="f35f4-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f35f4-133">*JET_paramPageTempDBMin*</span><span class="sxs-lookup"><span data-stu-id="f35f4-133">*JET_paramPageTempDBMin*</span></span>  
<span data-ttu-id="f35f4-134">19</span><span class="sxs-lookup"><span data-stu-id="f35f4-134">19</span></span>  

<span data-ttu-id="f35f4-135">Ce paramètre contrôle la taille initiale de la base de données temporaire.</span><span class="sxs-lookup"><span data-stu-id="f35f4-135">This parameter controls the initial size of the temporary database.</span></span> <span data-ttu-id="f35f4-136">La taille est dans les pages de base de données.</span><span class="sxs-lookup"><span data-stu-id="f35f4-136">The size is in database pages.</span></span> <span data-ttu-id="f35f4-137">Une taille de zéro indique que la taille par défaut d’une base de données ordinaire doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f35f4-137">A size of zero indicates that the default size of an ordinary database should be used.</span></span>

<span data-ttu-id="f35f4-138">Il est souvent souhaitable que les petites applications configurent la base de données temporaire aussi petite que possible.</span><span class="sxs-lookup"><span data-stu-id="f35f4-138">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="f35f4-139">L’affectation de la valeur 14 à ce paramètre permet d’obtenir la plus petite base de données temporaire possible.</span><span class="sxs-lookup"><span data-stu-id="f35f4-139">Setting this parameter to 14 will achieve the smallest temporary database possible.</span></span> <span data-ttu-id="f35f4-140">Notez qu’il est également possible d’éliminer entièrement la base de données temporaire en affectant à **JET_paramMaxTemporaryTables** la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="f35f4-140">Note that one can also entirely eliminate the temporary database by setting **JET_paramMaxTemporaryTables** to zero.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-141">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f35f4-141">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-142">0</span><span class="sxs-lookup"><span data-stu-id="f35f4-142">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-143">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f35f4-143">Type:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-144">Integer</span><span class="sxs-lookup"><span data-stu-id="f35f4-144">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-145">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f35f4-145">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-146">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="f35f4-146">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-147">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f35f4-147">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-148">Instance</span><span class="sxs-lookup"><span data-stu-id="f35f4-148">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-149">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f35f4-149">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-150">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-150">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-151">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f35f4-151">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-152">Non</span><span class="sxs-lookup"><span data-stu-id="f35f4-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-153">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f35f4-153">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-154">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-155">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f35f4-155">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-156">Non</span><span class="sxs-lookup"><span data-stu-id="f35f4-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-157">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f35f4-157">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-158">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-159">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f35f4-159">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-160">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-160">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-161">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f35f4-161">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-162">Tous</span><span class="sxs-lookup"><span data-stu-id="f35f4-162">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f35f4-163">*JET_paramTempPath*</span><span class="sxs-lookup"><span data-stu-id="f35f4-163">*JET_paramTempPath*</span></span>  
<span data-ttu-id="f35f4-164">1</span><span class="sxs-lookup"><span data-stu-id="f35f4-164">1</span></span>  

<span data-ttu-id="f35f4-165">Ce paramètre indique le chemin d’accès relatif ou absolu du système de fichiers du dossier ou du fichier qui contiendra la base de données temporaire de l’instance.</span><span class="sxs-lookup"><span data-stu-id="f35f4-165">This parameter indicates the relative or absolute file system path of the folder or file that will contain the temporary database for the instance.</span></span> <span data-ttu-id="f35f4-166">Si le chemin d’accès correspond à un dossier qui contiendra la base de données temporaire, il doit se terminer par une barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="f35f4-166">If the path is to a folder that will contain the temporary database then it must be terminated with a backslash character.</span></span> <span data-ttu-id="f35f4-167">La base de données temporaire est utilisée pour stocker les données volatiles générées dans le processus de gestion des appels d’informations de l’API ESE, de création d’index ou de stockage du contenu d’une table temporaire.</span><span class="sxs-lookup"><span data-stu-id="f35f4-167">The temporary database is used to hold volatile data that is generated in the process of handling ESE API info calls, creating indexes, or storing the contents of a temporary table.</span></span>

<span data-ttu-id="f35f4-168">**Remarque**  Si un chemin d’accès relatif est spécifié, il est relatif au répertoire de travail actuel du processus qui héberge l’application qui utilise le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="f35f4-168">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-169">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="f35f4-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-170">&quot;tmp. edb&quot;</span><span class="sxs-lookup"><span data-stu-id="f35f4-170">&quot;tmp.edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-171">Tapez :</span><span class="sxs-lookup"><span data-stu-id="f35f4-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-172">Path (chaîne)</span><span class="sxs-lookup"><span data-stu-id="f35f4-172">Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-173">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="f35f4-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-174">0 – 247 caractères</span><span class="sxs-lookup"><span data-stu-id="f35f4-174">0 – 247 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-175">Étendue :</span><span class="sxs-lookup"><span data-stu-id="f35f4-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-176">Instance</span><span class="sxs-lookup"><span data-stu-id="f35f4-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-177">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="f35f4-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-178">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-179">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="f35f4-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-180">Non</span><span class="sxs-lookup"><span data-stu-id="f35f4-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-181">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="f35f4-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-182">Oui</span><span class="sxs-lookup"><span data-stu-id="f35f4-182">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-183">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="f35f4-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-184">Non</span><span class="sxs-lookup"><span data-stu-id="f35f4-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-185">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="f35f4-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-186">Non</span><span class="sxs-lookup"><span data-stu-id="f35f4-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-187">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="f35f4-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-188">Non</span><span class="sxs-lookup"><span data-stu-id="f35f4-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-189">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="f35f4-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="f35f4-190">Tous</span><span class="sxs-lookup"><span data-stu-id="f35f4-190">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="f35f4-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f35f4-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-192"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="f35f4-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f35f4-193">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="f35f4-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f35f4-194"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="f35f4-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f35f4-195">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f35f4-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f35f4-196"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="f35f4-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f35f4-197">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="f35f4-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f35f4-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f35f4-198">See Also</span></span>

[<span data-ttu-id="f35f4-199">Fichiers ESE (Extensible Storage Engine)</span><span class="sxs-lookup"><span data-stu-id="f35f4-199">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="f35f4-200">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="f35f4-200">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="f35f4-201">JetInit</span><span class="sxs-lookup"><span data-stu-id="f35f4-201">JetInit</span></span>](./jetinit-function.md)
