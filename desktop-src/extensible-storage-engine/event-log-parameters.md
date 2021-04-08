---
description: En savoir plus sur les paramètres du journal des événements
title: Paramètres du journal des événements
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
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
ms.openlocfilehash: 912dc3e1e8588e18ef0d1db8fbf7edccfca7bdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034695"
---
# <a name="event-log-parameters"></a><span data-ttu-id="aa535-103">Paramètres du journal des événements</span><span class="sxs-lookup"><span data-stu-id="aa535-103">Event Log Parameters</span></span>


<span data-ttu-id="aa535-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="aa535-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-log-parameters"></a><span data-ttu-id="aa535-105">Paramètres du journal des événements</span><span class="sxs-lookup"><span data-stu-id="aa535-105">Event Log Parameters</span></span>

<span data-ttu-id="aa535-106">Cette rubrique contient des paramètres qui sont utilisés pour le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="aa535-106">This topic contains parameters that are used for the event log.</span></span>

<span data-ttu-id="aa535-107">JET_paramEventLogCache</span><span class="sxs-lookup"><span data-stu-id="aa535-107">JET_paramEventLogCache</span></span>  
<span data-ttu-id="aa535-108">Ce paramètre contrôle la taille (en octets) d’un cache de messages EventLog qui contiendra les messages EventLog émis par le moteur de base de données pendant l’arrêt du service EventLog.</span><span class="sxs-lookup"><span data-stu-id="aa535-108">This parameter controls the size (in bytes) of an eventlog message cache that will hold eventlog messages emitted by the database engine while the eventlog service is stopped.</span></span> <span data-ttu-id="aa535-109">Ces messages mis en cache seront vidés dans le journal des événements lorsque le service devient opérationnel.</span><span class="sxs-lookup"><span data-stu-id="aa535-109">These cached messages will be flushed to the eventlog when the service becomes operational.</span></span> <span data-ttu-id="aa535-110">Tous les messages qui dépassent le cache sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="aa535-110">Any messages that overflow the cache will be dropped.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa535-111">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa535-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa535-112">0</span><span class="sxs-lookup"><span data-stu-id="aa535-112">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-113">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa535-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa535-114">Integer</span><span class="sxs-lookup"><span data-stu-id="aa535-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-115">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa535-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa535-116">0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="aa535-116">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-117">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa535-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa535-118">Global</span><span class="sxs-lookup"><span data-stu-id="aa535-118">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-119">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-120">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-121">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-122">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-123">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa535-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa535-124">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-125">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-126">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-127">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa535-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa535-128">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-129">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa535-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa535-130">Oui</span><span class="sxs-lookup"><span data-stu-id="aa535-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-131">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-132">Tous</span><span class="sxs-lookup"><span data-stu-id="aa535-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa535-133">*JET_paramEventLoggingLevel*</span><span class="sxs-lookup"><span data-stu-id="aa535-133">*JET_paramEventLoggingLevel*</span></span>  
  
<span data-ttu-id="aa535-134">Ce paramètre configure le niveau de détail des messages EventLog émis dans le journal des événements par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="aa535-134">This parameter configures the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="aa535-135">Des numéros plus élevés entraînent des messages EventLog plus détaillés.</span><span class="sxs-lookup"><span data-stu-id="aa535-135">Higher numbers will result in more detailed eventlog messages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa535-136">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa535-136">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa535-137">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="aa535-137">JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-138">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa535-138">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa535-139">Integer</span><span class="sxs-lookup"><span data-stu-id="aa535-139">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-140">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa535-140">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa535-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="aa535-141">JET_EventLoggingDisable – JET_EventLoggingLevelMax</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-142">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa535-142">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa535-143">Instance</span><span class="sxs-lookup"><span data-stu-id="aa535-143">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-144">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-144">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-145">Oui</span><span class="sxs-lookup"><span data-stu-id="aa535-145">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-146">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-146">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-147">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-147">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-148">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa535-148">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa535-149">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-149">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-150">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-150">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-151">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-151">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-152">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa535-152">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa535-153">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-153">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-154">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa535-154">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa535-155">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-155">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-156">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-156">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-157">Windows XP et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="aa535-157">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa535-158">*JET_paramEventSource*</span><span class="sxs-lookup"><span data-stu-id="aa535-158">*JET_paramEventSource*</span></span>  
<span data-ttu-id="aa535-159">4</span><span class="sxs-lookup"><span data-stu-id="aa535-159">4</span></span>  

<span data-ttu-id="aa535-160">Ce paramètre fournit une chaîne spécifique à l’application qui sera ajoutée à tous les messages du journal des événements émis par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="aa535-160">This parameter supplies an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="aa535-161">Cela permet de corréler facilement les messages du journal des événements avec l’application source.</span><span class="sxs-lookup"><span data-stu-id="aa535-161">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="aa535-162">Si une chaîne vide est spécifiée (comme c’est le cas par défaut), le nom de l’exécutable de l’application hôte sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="aa535-162">If an empty string is specified (as is the default) then the host application executable name will be used.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa535-163">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa535-163">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-164">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa535-164">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa535-165">String</span><span class="sxs-lookup"><span data-stu-id="aa535-165">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-166">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa535-166">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa535-167">0 – 259 caractères</span><span class="sxs-lookup"><span data-stu-id="aa535-167">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-168">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa535-168">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa535-169">Instance</span><span class="sxs-lookup"><span data-stu-id="aa535-169">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-170">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-170">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-171">Oui</span><span class="sxs-lookup"><span data-stu-id="aa535-171">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-172">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-172">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-173">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-173">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-174">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa535-174">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa535-175">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-175">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-176">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-176">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-177">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-178">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa535-178">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa535-179">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-180">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa535-180">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa535-181">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-182">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-182">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-183">Tous</span><span class="sxs-lookup"><span data-stu-id="aa535-183">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa535-184">*JET_paramEventSourceKey*</span><span class="sxs-lookup"><span data-stu-id="aa535-184">*JET_paramEventSourceKey*</span></span>  
<span data-ttu-id="aa535-185">49</span><span class="sxs-lookup"><span data-stu-id="aa535-185">49</span></span>  

<span data-ttu-id="aa535-186">Ce paramètre peut être utilisé pour contrôler le journal des événements que le moteur de base de données utilise pour ses messages de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="aa535-186">This parameter can be used to control which event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="aa535-187">Par défaut, tous les messages du journal des événements sont envoyés dans le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="aa535-187">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="aa535-188">Si le nom de la clé de registre d’un autre journal des événements est configuré, les messages du journal des événements y seront à la place.</span><span class="sxs-lookup"><span data-stu-id="aa535-188">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa535-189">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa535-189">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-190">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa535-190">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa535-191">String</span><span class="sxs-lookup"><span data-stu-id="aa535-191">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-192">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa535-192">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa535-193">0 – 259 caractères</span><span class="sxs-lookup"><span data-stu-id="aa535-193">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-194">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa535-194">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa535-195">Instance</span><span class="sxs-lookup"><span data-stu-id="aa535-195">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-196">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-196">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-197">Oui</span><span class="sxs-lookup"><span data-stu-id="aa535-197">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-198">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-198">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-199">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-199">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-200">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa535-200">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa535-201">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-201">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-202">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-202">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-203">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-203">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-204">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa535-204">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa535-205">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-205">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-206">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa535-206">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa535-207">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-208">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-208">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-209">Tous</span><span class="sxs-lookup"><span data-stu-id="aa535-209">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa535-210">*JET_paramNoInformationEvent*</span><span class="sxs-lookup"><span data-stu-id="aa535-210">*JET_paramNoInformationEvent*</span></span>  
<span data-ttu-id="aa535-211">50</span><span class="sxs-lookup"><span data-stu-id="aa535-211">50</span></span>  

<span data-ttu-id="aa535-212">Lorsque ce paramètre a la valeur true, les messages du journal des événements d’information qui seraient normalement générés par le moteur de base de données seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="aa535-212">When this parameter is true, informational event log messages that would ordinarily be generated by the database engine will be suppressed.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa535-213">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="aa535-213">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="aa535-214">Faux</span><span class="sxs-lookup"><span data-stu-id="aa535-214">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-215">Tapez :</span><span class="sxs-lookup"><span data-stu-id="aa535-215">Type:</span></span></p></td>
<td><p><span data-ttu-id="aa535-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="aa535-216">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-217">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="aa535-217">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="aa535-218">False, True</span><span class="sxs-lookup"><span data-stu-id="aa535-218">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-219">Étendue :</span><span class="sxs-lookup"><span data-stu-id="aa535-219">Scope:</span></span></p></td>
<td><p><span data-ttu-id="aa535-220">Instance</span><span class="sxs-lookup"><span data-stu-id="aa535-220">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-221">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-221">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-222">Oui</span><span class="sxs-lookup"><span data-stu-id="aa535-222">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-223">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="aa535-223">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="aa535-224">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-224">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-225">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="aa535-225">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="aa535-226">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-226">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-227">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-227">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-228">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-228">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-229">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="aa535-229">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="aa535-230">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-231">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="aa535-231">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="aa535-232">Non</span><span class="sxs-lookup"><span data-stu-id="aa535-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-233">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="aa535-233">Availability:</span></span></p></td>
<td><p><span data-ttu-id="aa535-234">Tous</span><span class="sxs-lookup"><span data-stu-id="aa535-234">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="aa535-235">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa535-235">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa535-236"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="aa535-236"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aa535-237">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="aa535-237">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa535-238"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="aa535-238"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aa535-239">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="aa535-239">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa535-240"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="aa535-240"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aa535-241">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="aa535-241">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="aa535-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa535-242">See Also</span></span>

[<span data-ttu-id="aa535-243">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="aa535-243">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="aa535-244">JetInit</span><span class="sxs-lookup"><span data-stu-id="aa535-244">JetInit</span></span>](./jetinit-function.md)
