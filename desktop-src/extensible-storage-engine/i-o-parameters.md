---
description: En savoir plus sur les paramètres d’e/s
title: Paramètres d’e/s
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
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
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753988"
---
# <a name="io-parameters"></a><span data-ttu-id="71335-103">Paramètres d’e/s</span><span class="sxs-lookup"><span data-stu-id="71335-103">I/O Parameters</span></span>


<span data-ttu-id="71335-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="71335-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="io-parameters"></a><span data-ttu-id="71335-105">Paramètres d’e/s</span><span class="sxs-lookup"><span data-stu-id="71335-105">I/O Parameters</span></span>

<span data-ttu-id="71335-106">Cette rubrique contient des paramètres qui sont utilisés pour l’entrée et la sortie (e/s).</span><span class="sxs-lookup"><span data-stu-id="71335-106">This topic contains parameters that are used for input and output (I/O).</span></span>

<span data-ttu-id="71335-107">*JET_paramAccessDeniedRetryPeriod*</span><span class="sxs-lookup"><span data-stu-id="71335-107">*JET_paramAccessDeniedRetryPeriod*</span></span>  
<span data-ttu-id="71335-108">53</span><span class="sxs-lookup"><span data-stu-id="71335-108">53</span></span>  

<span data-ttu-id="71335-109">**Windows XP et versions ultérieures :**  Ce paramètre configure la durée (en millisecondes) pendant laquelle le moteur de base de données utilisera pour accéder à un fichier verrouillé avant l’échec avec JET_errFileAccessDenied.</span><span class="sxs-lookup"><span data-stu-id="71335-109">**Windows XP and later:**  This parameter configures the duration of time (in milliseconds) that the database engine will use to access a file that is locked before failing with JET_errFileAccessDenied.</span></span> <span data-ttu-id="71335-110">Ce délai est conçu pour contourner les logiciels antivirus qui peuvent contenir certains des fichiers du moteur de base de données ouverts brièvement après leur fermeture.</span><span class="sxs-lookup"><span data-stu-id="71335-110">This time delay is designed to work around anti-virus software that may hold some of the database engine's files open briefly after they are closed.</span></span>

<span data-ttu-id="71335-111">**Remarque**  En raison de la logique de nouvelle tentative ci-dessus, toute tentative d’attachement à une base de données ou d’utilisation d’un fichier journal qui est déjà utilisé par le moteur de base de données entraîne un délai de cette taille avant que l’appel d’API ne retourne un échec (légitime).</span><span class="sxs-lookup"><span data-stu-id="71335-111">**Note**  As a result of the above retry logic, any attempt to attach to a database or use a log file that is already in use by the database engine will result in a delay of this size before the API call returns a (legitimate) failure.</span></span> <span data-ttu-id="71335-112">Ce paramètre peut être utilisé pour désactiver ce délai au cas où il s’agit d’un scénario courant.</span><span class="sxs-lookup"><span data-stu-id="71335-112">This parameter can be used to turn down that delay in case this is a common scenario.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-113">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-113">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-114">10000</span><span class="sxs-lookup"><span data-stu-id="71335-114">10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-115">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-115">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-116">Integer</span><span class="sxs-lookup"><span data-stu-id="71335-116">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-117">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-117">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-118">0 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="71335-118">0 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-119">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-119">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-120">Global</span><span class="sxs-lookup"><span data-stu-id="71335-120">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-121">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-121">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-122">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-123">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-123">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-124">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-124">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-125">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-125">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-126">Non</span><span class="sxs-lookup"><span data-stu-id="71335-126">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-127">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-127">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-128">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-128">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-129">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-129">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-130">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-130">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-131">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-131">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-132">Non</span><span class="sxs-lookup"><span data-stu-id="71335-132">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-133">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-133">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-134">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="71335-134">Windows XP and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71335-135">*JET_paramCreatePathIfNotExist*</span><span class="sxs-lookup"><span data-stu-id="71335-135">*JET_paramCreatePathIfNotExist*</span></span>  
<span data-ttu-id="71335-136">100</span><span class="sxs-lookup"><span data-stu-id="71335-136">100</span></span>  

<span data-ttu-id="71335-137">Lorsque ce paramètre est défini sur true, tout dossier manquant dans un chemin d’accès du système de fichiers utilisé par le moteur de base de données sera créé sans assistance.</span><span class="sxs-lookup"><span data-stu-id="71335-137">When this parameter is set to true then any folder that is missing in a file system path in use by the database engine will be silently created.</span></span> <span data-ttu-id="71335-138">Dans le cas contraire, l’opération qui utilise le chemin d’accès au système de fichiers manquant échouera avec JET_errInvalidPath.</span><span class="sxs-lookup"><span data-stu-id="71335-138">Otherwise, the operation that uses the missing file system path will fail with JET_errInvalidPath.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-139">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-140">Faux</span><span class="sxs-lookup"><span data-stu-id="71335-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-141">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="71335-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-143">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-144">False, True</span><span class="sxs-lookup"><span data-stu-id="71335-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-145">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-146">Instance</span><span class="sxs-lookup"><span data-stu-id="71335-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-147">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-148">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-149">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-150">Non</span><span class="sxs-lookup"><span data-stu-id="71335-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-151">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-152">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-153">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-154">Non</span><span class="sxs-lookup"><span data-stu-id="71335-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-155">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-156">Non</span><span class="sxs-lookup"><span data-stu-id="71335-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-157">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-158">Non</span><span class="sxs-lookup"><span data-stu-id="71335-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-159">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-160">Tous</span><span class="sxs-lookup"><span data-stu-id="71335-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71335-161">*JET_paramEnableFileCache*</span><span class="sxs-lookup"><span data-stu-id="71335-161">*JET_paramEnableFileCache*</span></span>  
<span data-ttu-id="71335-162">126</span><span class="sxs-lookup"><span data-stu-id="71335-162">126</span></span>  

<span data-ttu-id="71335-163">Lorsque ce paramètre a la **valeur true**, le moteur de base de données utilise le cache de fichiers Windows comme cache de lecture pour tous ses différents fichiers.</span><span class="sxs-lookup"><span data-stu-id="71335-163">When this parameter is **True**, the database engine will use the Windows file cache as a read cache for all of its various files.</span></span> <span data-ttu-id="71335-164">Il l’utilise également comme cache d’écriture pour la base de données temporaire ou pour les bases de données ouvertes avec la récupération désactivée.</span><span class="sxs-lookup"><span data-stu-id="71335-164">It will also use it as a write cache for the temporary database or for databases that are opened with recovery disabled.</span></span> <span data-ttu-id="71335-165">Le moteur de base de données doit désactiver le cache d’écriture pour les bases de données ordinaires, les fichiers journaux des transactions et les fichiers de point de contrôle pour protéger l’intégrité transactionnelle des bases de données.</span><span class="sxs-lookup"><span data-stu-id="71335-165">The database engine must disable write caching for ordinary databases, transaction log files, and checkpoint files to protect the transactional integrity of the databases.</span></span>

<span data-ttu-id="71335-166">Il est important de noter que l’utilisation du cache de fichiers Windows ajoute une deuxième superposition de la mise en cache des fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="71335-166">It is important to note that the use of the Windows file cache will add a second layering of caching for database files.</span></span> <span data-ttu-id="71335-167">Le cache de base de données utilisera toujours sa propre mémoire pour mettre en cache les fichiers de base de données.</span><span class="sxs-lookup"><span data-stu-id="71335-167">The database cache will still use its own memory to cache the database files.</span></span> <span data-ttu-id="71335-168">L’objectif de ce mode est de permettre à l’application de configurer le moteur de base de données avec un petit cache dédié et de permettre à Windows de faire don de mémoire Spare pour améliorer la mise en cache des données de la base de données.</span><span class="sxs-lookup"><span data-stu-id="71335-168">The intent of this mode is to allow the application to configure the database engine with a small dedicated cache and to allow Windows to donate spare memory to further improve the caching of database data.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-169">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-170">Faux</span><span class="sxs-lookup"><span data-stu-id="71335-170">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-171">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="71335-172">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-173">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-174">False, True</span><span class="sxs-lookup"><span data-stu-id="71335-174">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-175">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-176">Global</span><span class="sxs-lookup"><span data-stu-id="71335-176">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-177">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-178">Non</span><span class="sxs-lookup"><span data-stu-id="71335-178">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-179">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-180">Non</span><span class="sxs-lookup"><span data-stu-id="71335-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-181">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-182">Non</span><span class="sxs-lookup"><span data-stu-id="71335-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-183">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-184">Non</span><span class="sxs-lookup"><span data-stu-id="71335-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-185">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-186">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-187">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-188">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-188">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-189">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-190">Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="71335-190">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71335-191">*JET_paramIOPriority*</span><span class="sxs-lookup"><span data-stu-id="71335-191">*JET_paramIOPriority*</span></span>  
<span data-ttu-id="71335-192">152</span><span class="sxs-lookup"><span data-stu-id="71335-192">152</span></span>  

<span data-ttu-id="71335-193">Ce paramètre contrôle la manière dont ESE gère les opérations d’e/s.</span><span class="sxs-lookup"><span data-stu-id="71335-193">This parameter controls how ESE handles I/O operations.</span></span> <span data-ttu-id="71335-194">Les valeurs peuvent être définies sur 0 (JET_IOPriorityNormal) pour une opération normale, ou sur 1 (JET_IOPriorityLow) pour une opération de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="71335-194">The values can be set to 0 (JET_IOPriorityNormal) for normal operation, or 1 (JET_IOPriorityLow) for low priority operation.</span></span> <span data-ttu-id="71335-195">Lorsque la priorité est définie sur JET_IOPriorityLow, le moteur ESE utilise la nouvelle fonctionnalité de priorité d’e/s de thread disponible dans Windows Vista pour réduire la priorité d’e/s sur le thread afin que les opérations d’e/s ultérieures soient émises au niveau de la nouvelle priorité basse.</span><span class="sxs-lookup"><span data-stu-id="71335-195">When the priority is set to JET_IOPriorityLow, ESE uses the new thread I/O priority functionality available in Windows Vista to reduce the I/O priority on the thread so that subsequent I/O operations are issued at the new low priority.</span></span>

<span data-ttu-id="71335-196">**Windows Vista :**  JET_paramIOPriority est introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="71335-196">**Windows Vista:**  JET_paramIOPriority is introduced in Windows Vista.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-197">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-197">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-198">0</span><span class="sxs-lookup"><span data-stu-id="71335-198">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-199">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-199">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-200">Integer</span><span class="sxs-lookup"><span data-stu-id="71335-200">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-201">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-201">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-202">0 - 1</span><span class="sxs-lookup"><span data-stu-id="71335-202">0 - 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-203">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-203">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-204">Instance</span><span class="sxs-lookup"><span data-stu-id="71335-204">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-205">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-205">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-206">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-206">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-207">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-207">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-208">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-208">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-209">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-209">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-210">Non</span><span class="sxs-lookup"><span data-stu-id="71335-210">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-211">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-211">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-212">Non</span><span class="sxs-lookup"><span data-stu-id="71335-212">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-213">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-213">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-214">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-214">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-215">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-215">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-216">Non</span><span class="sxs-lookup"><span data-stu-id="71335-216">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-217">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-217">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71335-218">Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71335-219">*JET_paramOutstandingIOMax*</span><span class="sxs-lookup"><span data-stu-id="71335-219">*JET_paramOutstandingIOMax*</span></span>  
<span data-ttu-id="71335-220">30</span><span class="sxs-lookup"><span data-stu-id="71335-220">30</span></span> 

<span data-ttu-id="71335-221">Ce paramètre contrôle le nombre d’e/s de fichier de base de données qui peuvent être mises en file d’attente dans le système d’exploitation hôte à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="71335-221">This parameter controls how many database file I/Os can be queued in the host operating system at one time.</span></span>

<span data-ttu-id="71335-222">Une valeur plus élevée pour ce paramètre peut améliorer considérablement les performances d’une application de base de données volumineuse.</span><span class="sxs-lookup"><span data-stu-id="71335-222">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="71335-223">**Windows XP et Windows Server 2003 :**  Ce paramètre est ignoré sur Windows XP et Windows Server 2003 et n’affecte pas le fonctionnement du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="71335-223">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-224">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-224">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-225"><strong>Windows 2000 : </strong>  64</span><span class="sxs-lookup"><span data-stu-id="71335-225"><strong>Windows 2000: </strong>  64</span></span></p>
<p><span data-ttu-id="71335-226"><strong>Windows Vista :</strong>   1024</span><span class="sxs-lookup"><span data-stu-id="71335-226"><strong>Windows Vista:</strong>   1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-227">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-227">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-228">Integer</span><span class="sxs-lookup"><span data-stu-id="71335-228">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-229">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-229">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-230"><strong>Windows 2000 :</strong>  8 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="71335-230"><strong>Windows 2000:</strong>  8 – 2147483647</span></span></p>
<p><span data-ttu-id="71335-231"><strong>Windows Vista :</strong>  0 – 65536</span><span class="sxs-lookup"><span data-stu-id="71335-231"><strong>Windows Vista:</strong>  0 – 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-232">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-232">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-233">Global</span><span class="sxs-lookup"><span data-stu-id="71335-233">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-234">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-234">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-235">Non</span><span class="sxs-lookup"><span data-stu-id="71335-235">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-236">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-236">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-237">Non</span><span class="sxs-lookup"><span data-stu-id="71335-237">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-238">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-238">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-239">Non</span><span class="sxs-lookup"><span data-stu-id="71335-239">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-240">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-240">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-241">Non</span><span class="sxs-lookup"><span data-stu-id="71335-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-242">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-242">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-243">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-243">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-244">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-244">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-245">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-246">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-246">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-247">Tous</span><span class="sxs-lookup"><span data-stu-id="71335-247">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71335-248">*JET_paramMaxCoalesceReadSize*</span><span class="sxs-lookup"><span data-stu-id="71335-248">*JET_paramMaxCoalesceReadSize*</span></span>  
<span data-ttu-id="71335-249">164</span><span class="sxs-lookup"><span data-stu-id="71335-249">164</span></span>  

<span data-ttu-id="71335-250">Nombre maximal d’octets pouvant être regroupés pour une opération de lecture fusionnée.</span><span class="sxs-lookup"><span data-stu-id="71335-250">Maximum number of bytes that can be grouped for a coalesced read operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-251">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-251">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-252">262 144</span><span class="sxs-lookup"><span data-stu-id="71335-252">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-253">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-253">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-254">Integer</span><span class="sxs-lookup"><span data-stu-id="71335-254">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-255">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-255">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-256">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="71335-256">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-257">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-257">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-258">Global</span><span class="sxs-lookup"><span data-stu-id="71335-258">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-259">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-259">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-260">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-260">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-261">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-261">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-262">Non</span><span class="sxs-lookup"><span data-stu-id="71335-262">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-263">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-263">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-264">Non</span><span class="sxs-lookup"><span data-stu-id="71335-264">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-265">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-265">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-266">Non</span><span class="sxs-lookup"><span data-stu-id="71335-266">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-267">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-267">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-268">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-268">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-269">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-269">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-270">Non</span><span class="sxs-lookup"><span data-stu-id="71335-270">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-271">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-271">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71335-272">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71335-273">*JET_paramMaxCoalesceWriteSize*</span><span class="sxs-lookup"><span data-stu-id="71335-273">*JET_paramMaxCoalesceWriteSize*</span></span>  
<span data-ttu-id="71335-274">165</span><span class="sxs-lookup"><span data-stu-id="71335-274">165</span></span>  

<span data-ttu-id="71335-275">Nombre maximal d’octets pouvant être regroupés pour une opération d’écriture fusionnée.</span><span class="sxs-lookup"><span data-stu-id="71335-275">Maximum number of bytes that can be grouped for a coalesced write operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-276">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-276">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-277">393216</span><span class="sxs-lookup"><span data-stu-id="71335-277">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-278">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-278">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-279">Integer</span><span class="sxs-lookup"><span data-stu-id="71335-279">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-280">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-280">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-281">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="71335-281">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-282">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-282">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-283">Global</span><span class="sxs-lookup"><span data-stu-id="71335-283">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-284">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-284">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-285">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-285">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-286">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-286">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-287">Non</span><span class="sxs-lookup"><span data-stu-id="71335-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-288">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-288">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-289">Non</span><span class="sxs-lookup"><span data-stu-id="71335-289">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-290">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-290">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-291">Non</span><span class="sxs-lookup"><span data-stu-id="71335-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-292">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-292">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-293">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-293">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-294">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-294">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-295">Non</span><span class="sxs-lookup"><span data-stu-id="71335-295">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-296">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-296">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-297">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71335-297">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71335-298">*JET_paramMaxCoalesceReadGapSize*</span><span class="sxs-lookup"><span data-stu-id="71335-298">*JET_paramMaxCoalesceReadGapSize*</span></span>  
<span data-ttu-id="71335-299">166</span><span class="sxs-lookup"><span data-stu-id="71335-299">166</span></span>  

<span data-ttu-id="71335-300">Nombre maximal d’octets pouvant être utilisé pour une opération d’e/s d’écriture fusionnée.</span><span class="sxs-lookup"><span data-stu-id="71335-300">Maximum number of bytes that can be gapped for a coalesced write I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-301">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-301">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-302">262 144</span><span class="sxs-lookup"><span data-stu-id="71335-302">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-303">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-303">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-304">Integer</span><span class="sxs-lookup"><span data-stu-id="71335-304">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-305">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-305">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-306">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="71335-306">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-307">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-307">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-308">Global</span><span class="sxs-lookup"><span data-stu-id="71335-308">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-309">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-309">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-310">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-310">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-311">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-311">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-312">Non</span><span class="sxs-lookup"><span data-stu-id="71335-312">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-313">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-313">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-314">Non</span><span class="sxs-lookup"><span data-stu-id="71335-314">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-315">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-315">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-316">Non</span><span class="sxs-lookup"><span data-stu-id="71335-316">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-317">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-317">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-318">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-318">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-319">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-319">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-320">Non</span><span class="sxs-lookup"><span data-stu-id="71335-320">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-321">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-321">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71335-322">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71335-323">*JET_paramMaxCoalesceWriteGapSize*</span><span class="sxs-lookup"><span data-stu-id="71335-323">*JET_paramMaxCoalesceWriteGapSize*</span></span>  
<span data-ttu-id="71335-324">167</span><span class="sxs-lookup"><span data-stu-id="71335-324">167</span></span>  

<span data-ttu-id="71335-325">Nombre maximal d’octets pouvant être utilisé pour une opération d’e/s de lecture fusionnée.</span><span class="sxs-lookup"><span data-stu-id="71335-325">Max number of bytes that can be gapped for a coalesced read I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-326">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="71335-326">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="71335-327">393216</span><span class="sxs-lookup"><span data-stu-id="71335-327">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-328">Tapez :</span><span class="sxs-lookup"><span data-stu-id="71335-328">Type:</span></span></p></td>
<td><p><span data-ttu-id="71335-329">Integer</span><span class="sxs-lookup"><span data-stu-id="71335-329">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-330">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="71335-330">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="71335-331">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="71335-331">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-332">Étendue :</span><span class="sxs-lookup"><span data-stu-id="71335-332">Scope:</span></span></p></td>
<td><p><span data-ttu-id="71335-333">Global</span><span class="sxs-lookup"><span data-stu-id="71335-333">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-334">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-334">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-335">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-335">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-336">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="71335-336">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="71335-337">Non</span><span class="sxs-lookup"><span data-stu-id="71335-337">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-338">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="71335-338">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="71335-339">Non</span><span class="sxs-lookup"><span data-stu-id="71335-339">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-340">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="71335-340">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="71335-341">Non</span><span class="sxs-lookup"><span data-stu-id="71335-341">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-342">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="71335-342">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="71335-343">Oui</span><span class="sxs-lookup"><span data-stu-id="71335-343">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-344">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="71335-344">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="71335-345">Non</span><span class="sxs-lookup"><span data-stu-id="71335-345">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-346">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="71335-346">Availability:</span></span></p></td>
<td><p><span data-ttu-id="71335-347">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71335-347">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="71335-348">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71335-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71335-349"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="71335-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="71335-350">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="71335-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71335-351"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="71335-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="71335-352">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="71335-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71335-353"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="71335-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="71335-354">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="71335-354">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="71335-355">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71335-355">See Also</span></span>

[<span data-ttu-id="71335-356">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="71335-356">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="71335-357">JetInit</span><span class="sxs-lookup"><span data-stu-id="71335-357">JetInit</span></span>](./jetinit-function.md)
