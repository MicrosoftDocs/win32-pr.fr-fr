---
description: 'En savoir plus sur : paramètres de ressource'
title: Paramètres de ressource
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534542"
---
# <a name="resource-parameters"></a><span data-ttu-id="aa16d-103">Paramètres de ressource</span><span class="sxs-lookup"><span data-stu-id="aa16d-103">Resource Parameters</span></span>


<span data-ttu-id="aa16d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="aa16d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="resource-parameters"></a><span data-ttu-id="aa16d-105">Paramètres de ressource</span><span class="sxs-lookup"><span data-stu-id="aa16d-105">Resource Parameters</span></span>

<span data-ttu-id="aa16d-106">Cette rubrique contient des paramètres qui sont utilisés pour les ressources.</span><span class="sxs-lookup"><span data-stu-id="aa16d-106">This topic contains parameters that are used for resources.</span></span>

<span data-ttu-id="aa16d-107">*JET_paramCachedClosedTables*</span><span class="sxs-lookup"><span data-stu-id="aa16d-107">*JET_paramCachedClosedTables*</span></span>  
<span data-ttu-id="aa16d-108">125</span><span class="sxs-lookup"><span data-stu-id="aa16d-108">125</span></span>  

<span data-ttu-id="aa16d-109">Ce paramètre contrôle le nombre de ressources de l’arborescence B + mises en cache par l’instance une fois que les tables qu’elles représentent ont été fermées par l’application.</span><span class="sxs-lookup"><span data-stu-id="aa16d-109">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span>

<span data-ttu-id="aa16d-110">Des valeurs élevées pour ce paramètre forcent le moteur de base de données à utiliser plus de mémoire, mais augmentent la vitesse avec laquelle un grand nombre de tables peut être ouvert de façon aléatoire par l’application.</span><span class="sxs-lookup"><span data-stu-id="aa16d-110">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="aa16d-111">Cela est utile pour les applications qui ont un schéma avec un très grand nombre de tables.</span><span class="sxs-lookup"><span data-stu-id="aa16d-111">This is useful for applications that have a schema with a very large number of tables.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-112">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-113">64</span><span class="sxs-lookup"><span data-stu-id="aa16d-113">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-114">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-115">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-116">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-117">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-117">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-118">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-119">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-119">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-120">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-121">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-121">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-122">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-123">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-124">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-125">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-126">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-127">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-128">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-129">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-130">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-131">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-132">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-133">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aa16d-133">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-134">*JET_paramDisablePerfmon*</span><span class="sxs-lookup"><span data-stu-id="aa16d-134">*JET_paramDisablePerfmon*</span></span>  
<span data-ttu-id="aa16d-135">107</span><span class="sxs-lookup"><span data-stu-id="aa16d-135">107</span></span>  

<span data-ttu-id="aa16d-136">Ce paramètre peut être utilisé pour empêcher le moteur de base de données de publier des données sur ses performances sur Windows.</span><span class="sxs-lookup"><span data-stu-id="aa16d-136">This parameter can be used to prevent the database engine from publishing data about its performance to Windows.</span></span> <span data-ttu-id="aa16d-137">Cela peut être fait pour réduire l’activité de thread de service du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="aa16d-137">This can be done to reduce the service thread activity of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-138">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-138">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-139">Faux</span><span class="sxs-lookup"><span data-stu-id="aa16d-139">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-140">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-140">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="aa16d-141">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-142">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-142">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-143">False, True</span><span class="sxs-lookup"><span data-stu-id="aa16d-143">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-144">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-144">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-145">Global</span><span class="sxs-lookup"><span data-stu-id="aa16d-145">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-146">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-146">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-147">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-148">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-148">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-149">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-149">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-150">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-150">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-151">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-152">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-152">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-153">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-154">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-154">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-155">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-156">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-156">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-157">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-157">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-158">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-158">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-159">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aa16d-159">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-160">*JET_paramGlobalMinVerPages*</span><span class="sxs-lookup"><span data-stu-id="aa16d-160">*JET_paramGlobalMinVerPages*</span></span>  
<span data-ttu-id="aa16d-161">81</span><span class="sxs-lookup"><span data-stu-id="aa16d-161">81</span></span>  

<span data-ttu-id="aa16d-162">Ce paramètre permet aux applications qui fonctionnent en mode multi-instance de préallouer de la mémoire pour les pages de version dans un pool global afin d’émuler l’ancien comportement.</span><span class="sxs-lookup"><span data-stu-id="aa16d-162">This parameter allows applications that operate in multi-instance mode to pre-allocate memory for version pages in a global pool to emulate the older behavior.</span></span> <span data-ttu-id="aa16d-163">Cela est utile si l’application souhaite garantir que les transactions d’une certaine taille peuvent être effectuées plus tard, même si la mémoire devient rare.</span><span class="sxs-lookup"><span data-stu-id="aa16d-163">This is useful in case the application wishes to guarantee that transactions of a certain size can succeed later on even if memory becomes scarce.</span></span>

<span data-ttu-id="aa16d-164">**Windows 2000 :**  Une quantité suffisante de mémoire pour sauvegarder toutes les pages de version est toujours réservée à l’heure [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="aa16d-164">**Windows 2000:**  Enough memory to back all version pages is always reserved at [JetInit](./jetinit-function.md) time.</span></span>

<span data-ttu-id="aa16d-165">**Windows XP :**  À compter de Windows XP, cela est toujours vrai en mode d’instance unique.</span><span class="sxs-lookup"><span data-stu-id="aa16d-165">**Windows XP:**  As of Windows XP, this is still true when in single instance mode.</span></span> <span data-ttu-id="aa16d-166">Toutefois, la mémoire de page de version est allouée dynamiquement en mode multi-instance.</span><span class="sxs-lookup"><span data-stu-id="aa16d-166">However, version page memory is dynamically allocated when in multi-instance mode.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-167">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-167">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-168">64</span><span class="sxs-lookup"><span data-stu-id="aa16d-168">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-169">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-170">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-171">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-172">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-172">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-173">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-173">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-174">Global</span><span class="sxs-lookup"><span data-stu-id="aa16d-174">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-175">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-175">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-176">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-176">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-177">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-177">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-178">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-178">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-179">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-179">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-180">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-180">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-181">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-181">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-182">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-182">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-183">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-183">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-184">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-185">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-185">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-186">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-187">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-187">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-188">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aa16d-188">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-189">*JET_paramMaxCursors*</span><span class="sxs-lookup"><span data-stu-id="aa16d-189">*JET_paramMaxCursors*</span></span>  
<span data-ttu-id="aa16d-190">8</span><span class="sxs-lookup"><span data-stu-id="aa16d-190">8</span></span>  

<span data-ttu-id="aa16d-191">Ce paramètre réserve le nombre demandé de ressources de curseur pour une utilisation par une instance.</span><span class="sxs-lookup"><span data-stu-id="aa16d-191">This parameter reserves the requested number of cursor resources for use by an instance.</span></span> <span data-ttu-id="aa16d-192">Une ressource de curseur correspond directement à un type de données [JET_TABLEID](./jet-tableid.md) .</span><span class="sxs-lookup"><span data-stu-id="aa16d-192">A cursor resource directly corresponds to a [JET_TABLEID](./jet-tableid.md) data type.</span></span> <span data-ttu-id="aa16d-193">Ce paramètre affecte le nombre de curseurs qui peuvent être utilisés en même temps.</span><span class="sxs-lookup"><span data-stu-id="aa16d-193">This setting will affect how many cursors can be used at the same time.</span></span> <span data-ttu-id="aa16d-194">Une ressource de curseur ne peut pas être partagée par différentes sessions, de sorte que ce paramètre doit être défini sur une valeur suffisamment élevée afin que chaque session puisse utiliser autant de curseurs que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="aa16d-194">A cursor resource cannot be shared by different sessions so this parameter must be set to a large enough value so that each session can use as many cursors as are required.</span></span>

<span data-ttu-id="aa16d-195">**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="aa16d-195">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-196">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-196">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-197">1 024</span><span class="sxs-lookup"><span data-stu-id="aa16d-197">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-198">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-198">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-199">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-199">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-200">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-200">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-201">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-201">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-202">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-202">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-203">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-203">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-204">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-204">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-205">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-205">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-206">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-206">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-207">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-208">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-208">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-209">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-209">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-210">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-210">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-211">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-211">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-212">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-212">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-213">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-213">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-214">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-214">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-215">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-215">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-216">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-216">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-217">Tous</span><span class="sxs-lookup"><span data-stu-id="aa16d-217">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-218">*JET_paramMaxInstances*</span><span class="sxs-lookup"><span data-stu-id="aa16d-218">*JET_paramMaxInstances*</span></span>  
<span data-ttu-id="aa16d-219">104</span><span class="sxs-lookup"><span data-stu-id="aa16d-219">104</span></span>  

<span data-ttu-id="aa16d-220">Ce paramètre contrôle le nombre maximal d’instances qui peuvent être créées dans un processus unique.</span><span class="sxs-lookup"><span data-stu-id="aa16d-220">This parameter controls the maximum number of instances that can be created in a single process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-221">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-222">16</span><span class="sxs-lookup"><span data-stu-id="aa16d-222">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-223">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-224">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-224">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-225">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-226">1-1024</span><span class="sxs-lookup"><span data-stu-id="aa16d-226">1-1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-227">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-228">Global</span><span class="sxs-lookup"><span data-stu-id="aa16d-228">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-229">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-230">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-231">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-232">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-233">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-234">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-235">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-236">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-237">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-238">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-239">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-240">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-240">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-241">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-242">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aa16d-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-243">*JET_paramMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="aa16d-243">*JET_paramMaxOpenTables*</span></span>  
<span data-ttu-id="aa16d-244">6</span><span class="sxs-lookup"><span data-stu-id="aa16d-244">6</span></span>  

<span data-ttu-id="aa16d-245">Ce paramètre réserve le nombre demandé de ressources de l’arborescence B + pour une utilisation par une instance.</span><span class="sxs-lookup"><span data-stu-id="aa16d-245">This parameter reserves the requested number of B+ Tree resources for use by an instance.</span></span> <span data-ttu-id="aa16d-246">Ce paramètre affecte le nombre de tables qui peuvent être utilisées en même temps.</span><span class="sxs-lookup"><span data-stu-id="aa16d-246">This setting will affect how many tables can be used at the same time.</span></span> <span data-ttu-id="aa16d-247">Ce paramètre doit être défini par rapport au schéma physique des bases de données utilisées par le moteur de base de données. par conséquent, ce paramètre n’est pas aussi simple que possible.</span><span class="sxs-lookup"><span data-stu-id="aa16d-247">This parameter needs to be set relative to the physical schema of the databases in use by the database engine, so this setting is not as straightforward as it could be.</span></span>

<span data-ttu-id="aa16d-248">En général, vous avez besoin de deux ressources, plus une ressource par index secondaire par table, dans l’utilisation simultanée par l’application.</span><span class="sxs-lookup"><span data-stu-id="aa16d-248">In general, you will need two resources plus one resource per secondary index per table in concurrent use by the application.</span></span>

<span data-ttu-id="aa16d-249">**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="aa16d-249">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-250">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-250">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-251">300</span><span class="sxs-lookup"><span data-stu-id="aa16d-251">300</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-252">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-252">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-253">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-253">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-254">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-254">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-255">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-255">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-256">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-256">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-257">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-257">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-258">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-258">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-259">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-259">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-260">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-260">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-261">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-261">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-262">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-262">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-263">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-263">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-264">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-264">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-265">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-265">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-266">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-266">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-267">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-267">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-268">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-268">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-269">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-269">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-270">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-270">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-271">Tous</span><span class="sxs-lookup"><span data-stu-id="aa16d-271">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-272">*JET_paramMaxSessions*</span><span class="sxs-lookup"><span data-stu-id="aa16d-272">*JET_paramMaxSessions*</span></span>  
<span data-ttu-id="aa16d-273">5</span><span class="sxs-lookup"><span data-stu-id="aa16d-273">5</span></span>  

<span data-ttu-id="aa16d-274">Ce paramètre réserve le nombre demandé de ressources de session pour une utilisation par une instance.</span><span class="sxs-lookup"><span data-stu-id="aa16d-274">This parameter reserves the requested number of session resources for use by an instance.</span></span> <span data-ttu-id="aa16d-275">Une ressource de session correspond directement à un type de données [JET_SESID](./jet-sesid.md) .</span><span class="sxs-lookup"><span data-stu-id="aa16d-275">A session resource directly corresponds to a [JET_SESID](./jet-sesid.md) data type.</span></span> <span data-ttu-id="aa16d-276">Ce paramètre affecte le nombre de sessions qui peuvent être utilisées en même temps.</span><span class="sxs-lookup"><span data-stu-id="aa16d-276">This setting will affect how many sessions can be used at the same time.</span></span>

<span data-ttu-id="aa16d-277">**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="aa16d-277">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-278">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-278">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-279">16</span><span class="sxs-lookup"><span data-stu-id="aa16d-279">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-280">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-280">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-281">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-281">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-282">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-282">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-283">0 – 30000</span><span class="sxs-lookup"><span data-stu-id="aa16d-283">0 – 30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-284">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-284">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-285">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-285">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-286">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-286">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-287">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-287">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-288">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-288">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-289">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-289">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-290">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-290">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-291">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-291">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-292">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-292">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-293">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-293">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-294">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-294">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-295">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-295">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-296">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-296">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-297">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-297">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-298">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-298">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-299">Tous</span><span class="sxs-lookup"><span data-stu-id="aa16d-299">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-300">*JET_paramMaxTemporaryTables*</span><span class="sxs-lookup"><span data-stu-id="aa16d-300">*JET_paramMaxTemporaryTables*</span></span>  
<span data-ttu-id="aa16d-301">10</span><span class="sxs-lookup"><span data-stu-id="aa16d-301">10</span></span>  

<span data-ttu-id="aa16d-302">Ce paramètre réserve le nombre demandé de ressources de table temporaire pour une utilisation par une instance.</span><span class="sxs-lookup"><span data-stu-id="aa16d-302">This parameter reserves the requested number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="aa16d-303">Ce paramètre affecte le nombre de tables temporaires qui peuvent être utilisées en même temps.</span><span class="sxs-lookup"><span data-stu-id="aa16d-303">This setting will affect how many temporary tables can be used at the same time.</span></span>

<span data-ttu-id="aa16d-304">**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="aa16d-304">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="aa16d-305">**Windows XP et versions ultérieures :**  Si ce paramètre système est défini à zéro, aucune base de données temporaire n’est créée et toute activité nécessitant l’utilisation de la base de données temporaire échoue.</span><span class="sxs-lookup"><span data-stu-id="aa16d-305">**Windows XP and later:**  If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="aa16d-306">Ce paramètre peut être utile pour éviter les e/s nécessaires à la création de la base de données temporaire si elle est connue qu’elle ne sera pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="aa16d-306">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="aa16d-307">**Remarque**  L’utilisation d’une table temporaire requiert également une ressource curseur.</span><span class="sxs-lookup"><span data-stu-id="aa16d-307">**Note**  The use of a temporary table also requires a cursor resource.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-308">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-308">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-309">20</span><span class="sxs-lookup"><span data-stu-id="aa16d-309">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-310">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-310">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-311">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-311">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-312">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-312">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-313">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-313">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-314">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-314">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-315">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-315">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-316">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-316">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-317">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-318">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-318">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-319">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-319">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-320">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-320">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-321">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-321">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-322">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-322">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-323">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-323">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-324">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-324">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-325">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-325">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-326">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-326">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-327">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-327">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-328">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-328">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-329">Tous</span><span class="sxs-lookup"><span data-stu-id="aa16d-329">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-330">*JET_paramMaxVerPages*</span><span class="sxs-lookup"><span data-stu-id="aa16d-330">*JET_paramMaxVerPages*</span></span>  
<span data-ttu-id="aa16d-331">9</span><span class="sxs-lookup"><span data-stu-id="aa16d-331">9</span></span>  

<span data-ttu-id="aa16d-332">Ce paramètre réserve le nombre demandé de pages du magasin de versions pour une utilisation par une instance.</span><span class="sxs-lookup"><span data-stu-id="aa16d-332">This parameter reserves the requested number of version store pages for use by an instance.</span></span> <span data-ttu-id="aa16d-333">La Banque des versions contient un enregistrement dynamique de toutes les différentes versions de chaque entrée d’enregistrement ou d’index dans la base de données qui peuvent être vues par toutes les transactions actives.</span><span class="sxs-lookup"><span data-stu-id="aa16d-333">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="aa16d-334">Ces versions sont utilisées pour prendre en charge le contrôle d’accès concurrentiel multiversion utilisé par le moteur de base de données pour prendre en charge les transactions à l’aide de l’isolation d’instantané.</span><span class="sxs-lookup"><span data-stu-id="aa16d-334">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="aa16d-335">Ce paramètre affecte le nombre de mises à jour qui peuvent être conservées en mémoire à la fois.</span><span class="sxs-lookup"><span data-stu-id="aa16d-335">This setting will affect how many updates can be held in memory at a time.</span></span> <span data-ttu-id="aa16d-336">Cela affecte à son tour le nombre maximal de mises à jour qu’une seule transaction peut effectuer, la durée maximale pendant laquelle une transaction peut être ouverte, la charge simultanée maximale de transactions de mise à jour sur le système ou une combinaison de ces opérations.</span><span class="sxs-lookup"><span data-stu-id="aa16d-336">This in turn will affect either the maximum number of updates a single transaction can perform, the maximum duration a transaction can be held open, the maximum concurrent load of updating transactions on the system, or a combination of these.</span></span>

<span data-ttu-id="aa16d-337">Chaque page de la Banque des versions telle que configurée par ce paramètre a une taille de 16 Ko sur les ordinateurs 32 bits, et 32 Ko sur des ordinateurs 64 bits.</span><span class="sxs-lookup"><span data-stu-id="aa16d-337">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="aa16d-338">**Windows Vista et versions ultérieures :**  La taille de page de la Banque des versions peut être lue et modifiée via JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="aa16d-338">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="aa16d-339">**Windows 2000, Windows XP et Windows Server 2003 :**  Les valeurs élevées de ce paramètre consomment l’espace d’adressage et peuvent augmenter l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="aa16d-339">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="aa16d-340">**Remarque**  Il s’agit de la ressource la plus couramment épuisée par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="aa16d-340">**Note**  This is by far the most common resource to be exhausted by the database engine.</span></span> <span data-ttu-id="aa16d-341">Une attention particulière doit être accordée au paramètre du système et au chargement transactionnel de l’application afin d’éviter l’épuisement de cette ressource en fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="aa16d-341">Careful attention must be paid to the setting of the system parameter and to the transactional load of the application to avoid exhausting this resource under normal operation.</span></span> <span data-ttu-id="aa16d-342">Lorsque cette ressource est épuisée, les mises à jour de la base de données seront rejetées avec JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="aa16d-342">When this resource is exhausted, updates to the database will be rejected with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="aa16d-343">Pour libérer certaines de ces ressources, la plus ancienne transaction en suspens doit être abandonnée.</span><span class="sxs-lookup"><span data-stu-id="aa16d-343">To release some of these resources, the oldest outstanding transaction must be aborted.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-344">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-344">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-345">64</span><span class="sxs-lookup"><span data-stu-id="aa16d-345">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-346">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-346">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-347">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-347">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-348">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-348">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-349">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-349">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-350">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-350">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-351">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-351">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-352">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-352">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-353">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-353">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-354">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-354">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-355">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-355">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-356">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-356">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-357">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-357">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-358">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-358">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-359">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-359">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-360">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-360">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-361">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-361">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-362">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-362">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-363">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-363">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-364">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-364">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-365">Tous</span><span class="sxs-lookup"><span data-stu-id="aa16d-365">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-366">*JET_paramPageHintCacheSize*</span><span class="sxs-lookup"><span data-stu-id="aa16d-366">*JET_paramPageHintCacheSize*</span></span>  
<span data-ttu-id="aa16d-367">101</span><span class="sxs-lookup"><span data-stu-id="aa16d-367">101</span></span>  

<span data-ttu-id="aa16d-368">Ce paramètre contrôle la taille d’un cache spécial utilisé pour accélérer la recherche de pointeurs de page enfant B + d’arborescence dans le cache de la page de base de données.</span><span class="sxs-lookup"><span data-stu-id="aa16d-368">This parameter controls the size of a special cache used to accelerate the lookup of B+ Tree child page pointers in the database page cache.</span></span> <span data-ttu-id="aa16d-369">La taille du cache est en octets.</span><span class="sxs-lookup"><span data-stu-id="aa16d-369">The size of the cache is in bytes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-370">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-370">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-371">262 144</span><span class="sxs-lookup"><span data-stu-id="aa16d-371">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-372">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-372">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-373">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-373">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-374">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-374">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-375">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-375">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-376">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-376">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-377">Global</span><span class="sxs-lookup"><span data-stu-id="aa16d-377">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-378">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-378">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-379">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-379">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-380">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-380">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-381">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-381">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-382">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-382">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-383">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-383">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-384">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-384">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-385">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-385">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-386">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-386">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-387">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-387">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-388">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-388">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-389">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-389">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-390">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-390">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-391">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aa16d-391">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-392">*JET_paramPreferredMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="aa16d-392">*JET_paramPreferredMaxOpenTables*</span></span>  
<span data-ttu-id="aa16d-393">7</span><span class="sxs-lookup"><span data-stu-id="aa16d-393">7</span></span>  

<span data-ttu-id="aa16d-394">Ce paramètre tente de conserver le nombre de ressources de l’arborescence B + en cours d’utilisation en deçà du seuil spécifié.</span><span class="sxs-lookup"><span data-stu-id="aa16d-394">This parameter attempts to keep the number of B+ Tree resources in use below the specified threshold.</span></span>

<span data-ttu-id="aa16d-395">Si ce paramètre a la valeur zéro, la valeur par défaut est 100% de **JET_paramMaxOpenTables**.</span><span class="sxs-lookup"><span data-stu-id="aa16d-395">If this parameter is set to zero then it will default to 100% of **JET_paramMaxOpenTables**.</span></span>

<span data-ttu-id="aa16d-396">**Windows Vista et versions ultérieures :**  Ce paramètre est obsolète et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="aa16d-396">**Windows Vista and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span> <span data-ttu-id="aa16d-397">Les applications doivent utiliser JET_paramMaxCachedClosedTables à la place.</span><span class="sxs-lookup"><span data-stu-id="aa16d-397">Applications should use JET_paramMaxCachedClosedTables instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-398">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-398">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-399">0 (100% de <strong>JET_paramMaxOpenTables</strong>)</span><span class="sxs-lookup"><span data-stu-id="aa16d-399">0 (100% of <strong>JET_paramMaxOpenTables</strong>)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-400">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-400">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-401">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-401">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-402">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-402">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-403">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-403">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-404">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-404">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-405">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-405">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-406">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-406">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-407">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-407">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-408">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-408">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-409">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-409">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-410">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-410">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-411">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-411">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-412">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-412">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-413">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-413">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-414">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-414">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-415">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-415">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-416">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-416">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-417">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-417">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-418">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-418">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-419">Tous</span><span class="sxs-lookup"><span data-stu-id="aa16d-419">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-420">*JET_paramPreferredVerPages*</span><span class="sxs-lookup"><span data-stu-id="aa16d-420">*JET_paramPreferredVerPages*</span></span>  
<span data-ttu-id="aa16d-421">63</span><span class="sxs-lookup"><span data-stu-id="aa16d-421">63</span></span>  

<span data-ttu-id="aa16d-422">Ce paramètre représente un seuil relatif à **JET_paramMaxVerPages** qui contrôle l’utilisation discrétionnaire des pages de version par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="aa16d-422">This parameter represents a threshold relative to **JET_paramMaxVerPages** that controls the discretionary use of version pages by the database engine.</span></span> <span data-ttu-id="aa16d-423">Si la taille de la Banque des versions dépasse ce seuil, toutes les informations qui sont utilisées uniquement pour les tâches en arrière-plan facultatives, telles que la récupération de l’espace supprimé dans la base de données, sont sacrifiées pour conserver de l’espace pour les informations transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="aa16d-423">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="aa16d-424">**Windows 2000, Windows XP et Windows Server 2003 :**  Si vous affectez la valeur zéro à ce paramètre, le seuil est de 90% de **JET_paramMaxVerPages**.</span><span class="sxs-lookup"><span data-stu-id="aa16d-424">**Windows 2000, Windows XP and Windows Server 2003:**  Setting this parameter to zero would set the threshold to be 90% of **JET_paramMaxVerPages**.</span></span>

<span data-ttu-id="aa16d-425">**Windows Vista et versions ultérieures :**  Cela n’est plus pris en charge et la valeur par défaut de ce paramètre a été modifiée pour clarifier son comportement.</span><span class="sxs-lookup"><span data-stu-id="aa16d-425">**Windows Vista and later:**  This is no longer supported and the default value of this parameter was changed to clarify its behavior.</span></span>

<span data-ttu-id="aa16d-426">Chaque page de la Banque des versions telle que configurée par ce paramètre a une taille de 16 Ko sur les ordinateurs 32 bits, et 32 Ko sur des ordinateurs 64 bits.</span><span class="sxs-lookup"><span data-stu-id="aa16d-426">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="aa16d-427">**Windows Vista et versions ultérieures :**  La taille de page de la Banque des versions peut être lue et modifiée via JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="aa16d-427">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="aa16d-428">**Remarque**  Si le moteur de base de données fonctionne trop souvent au-dessus de ce seuil, il est possible que la base de données se dégrade en performances.</span><span class="sxs-lookup"><span data-stu-id="aa16d-428">**Note**  If the database engine operates above this threshold too often then it is possible for the database to degrade in performance.</span></span> <span data-ttu-id="aa16d-429">Cela se produit parce que les processus d’arrière-plan qui nettoient la base de données ne peuvent pas fonctionner sans les informations facultatives qui sont rejetées dans ce scénario.</span><span class="sxs-lookup"><span data-stu-id="aa16d-429">This happens because the background processes that clean up the database cannot function without the optional information that is thrown away in this scenario.</span></span> <span data-ttu-id="aa16d-430">La défragmentation en ligne ou hors connexion contrecarre cet effet.</span><span class="sxs-lookup"><span data-stu-id="aa16d-430">Online or offline defragmentation will counteract this effect.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-431">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-431">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-432"><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  0 (90% de JET_paramMaxVerPages)</span><span class="sxs-lookup"><span data-stu-id="aa16d-432"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 (90% of JET_paramMaxVerPages)</span></span></p>
<p><span data-ttu-id="aa16d-433"><strong>Windows Vista :</strong>  58</span><span class="sxs-lookup"><span data-stu-id="aa16d-433"><strong>Windows Vista:</strong>  58</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-434">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-434">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-435">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-435">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-436">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-436">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-437">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa16d-437">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-438">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-438">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-439">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-439">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-440">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-440">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-441">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-442">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-442">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-443">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-444">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-444">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-445">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-445">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-446">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-446">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-447">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-447">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-448">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-448">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-449">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-449">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-450">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-450">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-451">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-451">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-452">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-452">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-453">Tous</span><span class="sxs-lookup"><span data-stu-id="aa16d-453">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-454">*JET_paramVerPageSize*</span><span class="sxs-lookup"><span data-stu-id="aa16d-454">*JET_paramVerPageSize*</span></span>  
<span data-ttu-id="aa16d-455">128</span><span class="sxs-lookup"><span data-stu-id="aa16d-455">128</span></span>  

<span data-ttu-id="aa16d-456">Ce paramètre contrôle la taille des pages de la Banque des versions utilisées par le moteur de base de données pour stocker les informations transactionnelles.</span><span class="sxs-lookup"><span data-stu-id="aa16d-456">This parameter controls the size of the version store pages used by the database engine to hold transactional information.</span></span> <span data-ttu-id="aa16d-457">La valeur de ce paramètre est la taille d’unité pour tous les autres paramètres système en termes de pages de version (par exemple, JET_paramMaxVerPages).</span><span class="sxs-lookup"><span data-stu-id="aa16d-457">The value of this parameter is the unit size for all the other system parameters that are in terms of version pages (e.g. JET_paramMaxVerPages).</span></span>

<span data-ttu-id="aa16d-458">Le moteur de base de données peut choisir d’utiliser une plus grande taille de page de la Banque des versions que celle demandée.</span><span class="sxs-lookup"><span data-stu-id="aa16d-458">The database engine may choose to use a larger version store page size than requested.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-459">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-459">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-460">16384</span><span class="sxs-lookup"><span data-stu-id="aa16d-460">16384</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-461">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-461">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-462">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-462">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-463">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-463">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span><span class="sxs-lookup"><span data-stu-id="aa16d-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-465">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-465">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-466">Global</span><span class="sxs-lookup"><span data-stu-id="aa16d-466">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-467">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-467">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-468">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-468">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-469">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-469">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-470">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-470">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-471">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-471">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-472">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-472">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-473">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-473">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-474">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-474">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-475">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-475">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-476">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-476">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-477">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-477">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-478">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-478">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-479">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-479">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-480">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aa16d-480">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa16d-481">*JET_paramVersionStoreTaskQueueMax*</span><span class="sxs-lookup"><span data-stu-id="aa16d-481">*JET_paramVersionStoreTaskQueueMax*</span></span>  
<span data-ttu-id="aa16d-482">105</span><span class="sxs-lookup"><span data-stu-id="aa16d-482">105</span></span>  

<span data-ttu-id="aa16d-483">Ce paramètre contrôle le nombre d’éléments de travail de nettoyage en arrière-plan qui peuvent être mis en file d’attente dans le pool de threads du moteur de base de données à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="aa16d-483">This parameter controls the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-484">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa16d-484">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-485">32</span><span class="sxs-lookup"><span data-stu-id="aa16d-485">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-486">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa16d-486">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-487">Integer</span><span class="sxs-lookup"><span data-stu-id="aa16d-487">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-488">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa16d-488">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-489"><strong>Windows XP et Windows Server 2003 :  </strong>  1 – 63</span><span class="sxs-lookup"><span data-stu-id="aa16d-489"><strong>Windows XP and Windows Server 2003:  </strong>  1 – 63</span></span></p>
<p><span data-ttu-id="aa16d-490"><strong>Windows Vista :</strong>  1 – 127</span><span class="sxs-lookup"><span data-stu-id="aa16d-490"><strong>Windows Vista:</strong>  1 – 127</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-491">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa16d-491">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-492">Instance</span><span class="sxs-lookup"><span data-stu-id="aa16d-492">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-493">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-493">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-494">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-494">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-495">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa16d-495">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-496"><strong>Windows XP et Windows Server 2003 :  </strong>  º</span><span class="sxs-lookup"><span data-stu-id="aa16d-496"><strong>Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="aa16d-497"><strong>Windows Vista :</strong>  Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-497"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-498">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa16d-498">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-499">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-499">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-500">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-500">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-501">Non</span><span class="sxs-lookup"><span data-stu-id="aa16d-501">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-502">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa16d-502">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-503">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-503">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-504">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa16d-504">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-505">Oui</span><span class="sxs-lookup"><span data-stu-id="aa16d-505">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-506">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa16d-506">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa16d-507">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aa16d-507">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="aa16d-508">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa16d-508">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-509"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="aa16d-509"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aa16d-510">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="aa16d-510">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa16d-511"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="aa16d-511"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aa16d-512">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="aa16d-512">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa16d-513"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="aa16d-513"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aa16d-514">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="aa16d-514">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="aa16d-515">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa16d-515">See Also</span></span>

[<span data-ttu-id="aa16d-516">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="aa16d-516">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="aa16d-517">JetInit</span><span class="sxs-lookup"><span data-stu-id="aa16d-517">JetInit</span></span>](./jetinit-function.md)
