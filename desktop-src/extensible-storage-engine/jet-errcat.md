---
description: 'En savoir plus sur : JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523240"
---
# <a name="jet_errcat"></a><span data-ttu-id="3edfa-103">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="3edfa-103">JET_ERRCAT</span></span>


<span data-ttu-id="3edfa-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="3edfa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errcat"></a><span data-ttu-id="3edfa-105">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="3edfa-105">JET_ERRCAT</span></span>

<span data-ttu-id="3edfa-106">Le **JET_ERRCAT** groupe de constantes décrit les classifications ou les catégories d’erreurs de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="3edfa-106">The **JET_ERRCAT** group of constants describes higher-level classifications or categories of errors.</span></span> <span data-ttu-id="3edfa-107">Ce groupe de constantes permet aux applications de définir le traitement par défaut pour une classification des erreurs, au lieu de gérer chaque cas d’erreur individuellement.</span><span class="sxs-lookup"><span data-stu-id="3edfa-107">This group of constants enables applications to define default treatment for a classification of errors, rather than handling each error case individually.</span></span> <span data-ttu-id="3edfa-108">Elle garantit également que l’application n’a pas à gérer les nouvelles conditions d’erreur incluses dans les classifications existantes.</span><span class="sxs-lookup"><span data-stu-id="3edfa-108">It also ensures that the application does not have to handle new error conditions that are included in existing classifications.</span></span>

<span data-ttu-id="3edfa-109">Remarque : cette documentation est basée sur une version préliminaire du moteur de stockage extensible.</span><span class="sxs-lookup"><span data-stu-id="3edfa-109">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="3edfa-110">Ces informations sont susceptibles d’être modifiées.</span><span class="sxs-lookup"><span data-stu-id="3edfa-110">This information is subject to change.</span></span>

<span data-ttu-id="3edfa-111">Les constantes de **JET_ERRCAT** sont organisées dans une hiérarchie spécifique de conditions et de sous-conditions, comme suit :</span><span class="sxs-lookup"><span data-stu-id="3edfa-111">The **JET_ERRCAT** constants are arranged in a specific hierarchy of conditions and subconditions, as follows:</span></span>

<span data-ttu-id="3edfa-112">| Erreur---| opération de---(Al) | |---irrécupérable | |---e/s | |---ressource | |---de la mémoire | |---quota | |---disque | |---des données | |---de l’altération | |---incohérent | |---de la fragmentation | |---l’API | utilisation de---</span><span class="sxs-lookup"><span data-stu-id="3edfa-112">|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- Api |--- Usage |--- State</span></span>

<span data-ttu-id="3edfa-113">Le tableau suivant répertorie les constantes d' **JET_ERRCAT** et fournit une description et des informations de récupération, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3edfa-113">The following table lists the **JET_ERRCAT** constants and provides a description and recovery information, as applicable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3edfa-114">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="3edfa-114">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="3edfa-115">Description</span><span class="sxs-lookup"><span data-stu-id="3edfa-115">Description</span></span></p></th>
<th><p><span data-ttu-id="3edfa-116">Récupération</span><span class="sxs-lookup"><span data-stu-id="3edfa-116">Recovery</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-117">JET_errcatUnknown 0</span><span class="sxs-lookup"><span data-stu-id="3edfa-117">JET_errcatUnknown 0</span></span></p></td>
<td><p><span data-ttu-id="3edfa-118">Catégorie d’erreur non valide.</span><span class="sxs-lookup"><span data-stu-id="3edfa-118">An invalid error category.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-119">N/A.</span><span class="sxs-lookup"><span data-stu-id="3edfa-119">N/A.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-120">JET_errcatError 1</span><span class="sxs-lookup"><span data-stu-id="3edfa-120">JET_errcatError 1</span></span></p></td>
<td><p><span data-ttu-id="3edfa-121">Catégorie de niveau supérieur (aucune erreur ne doit être de cette classe).</span><span class="sxs-lookup"><span data-stu-id="3edfa-121">The top level category (no errors should be of this class).</span></span></p></td>
<td><p><span data-ttu-id="3edfa-122">Consultez les constantes d’erreur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3edfa-122">See the specific error constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-123">JET_errcatOperation 2</span><span class="sxs-lookup"><span data-stu-id="3edfa-123">JET_errcatOperation 2</span></span></p></td>
<td><p><span data-ttu-id="3edfa-124">Représente les erreurs qui peuvent se produire à tout moment en raison de conditions incontrôlables et qui sont souvent temporaires.</span><span class="sxs-lookup"><span data-stu-id="3edfa-124">Represents errors that can happen at any time due to uncontrollable conditions and are often temporary.</span></span> <span data-ttu-id="3edfa-125">Consultez les sous-catégories si elles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="3edfa-125">See subcategories if specified.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-126">Réessayez et si l’erreur persiste, Informez l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="3edfa-126">Retry and if the error continues, inform the operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-127">JET_errcatFatal 3</span><span class="sxs-lookup"><span data-stu-id="3edfa-127">JET_errcatFatal 3</span></span></p></td>
<td><p><span data-ttu-id="3edfa-128">Représente des erreurs irrécupérables qui, lorsqu’elles se produisent, créent un risque que ESE ne puisse pas continuer en toute sécurité (souvent transactionnelle), et les données peuvent être endommagées.</span><span class="sxs-lookup"><span data-stu-id="3edfa-128">Represents fatal errors that, when they occur, create a risk that ESE cannot continue in a safe (often transactional) way, and data may become corrupted.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-129">Redémarrez l’instance ou le processus.</span><span class="sxs-lookup"><span data-stu-id="3edfa-129">Restart the instance or process.</span></span> <span data-ttu-id="3edfa-130">Si le problème persiste, Informez l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="3edfa-130">If the problem persists, inform the operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-131">JET_errcatIO 4</span><span class="sxs-lookup"><span data-stu-id="3edfa-131">JET_errcatIO 4</span></span></p></td>
<td><p><span data-ttu-id="3edfa-132">Représente les erreurs d’e/s qui proviennent du système d’exploitation et qui sont hors du contrôle de ESE.</span><span class="sxs-lookup"><span data-stu-id="3edfa-132">Represents IO errors, which come from the operating system, and are out of ESE's control.</span></span> <span data-ttu-id="3edfa-133">Ce type d’erreur peut être temporaire.</span><span class="sxs-lookup"><span data-stu-id="3edfa-133">This type of error may be temporary.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-134">Réessayez, et si l’erreur persiste, demandez à l’opérateur de vérifier le disque.</span><span class="sxs-lookup"><span data-stu-id="3edfa-134">Retry, and if the error continues, ask the operator to check the disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-135">JET_errcatResource 5</span><span class="sxs-lookup"><span data-stu-id="3edfa-135">JET_errcatResource 5</span></span></p></td>
<td><p><span data-ttu-id="3edfa-136">Représente une catégorie d’erreurs liées à des conditions de ressources insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="3edfa-136">Represents a category of errors related to lack of resource conditions.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-137">Consultez sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="3edfa-137">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-138">JET_errcatMemory 6</span><span class="sxs-lookup"><span data-stu-id="3edfa-138">JET_errcatMemory 6</span></span></p></td>
<td><p><span data-ttu-id="3edfa-139">Représente une erreur provoquée par un manque de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3edfa-139">Represents an error caused by lack of memory.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-140">Réessayez au bout d’un certain temps, libérez de la mémoire ou quittez.</span><span class="sxs-lookup"><span data-stu-id="3edfa-140">Retry after a period of time, free up memory, or quit.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-141">JET_errcatQuota 7</span><span class="sxs-lookup"><span data-stu-id="3edfa-141">JET_errcatQuota 7</span></span></p></td>
<td><p><span data-ttu-id="3edfa-142">Certaines &quot; &quot; ressources spécialisées se trouvent dans des pools d’une certaine taille, ce qui facilite la détection des fuites de ces ressources.</span><span class="sxs-lookup"><span data-stu-id="3edfa-142">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-143">L’application doit <strong>déclarer ()</strong> pour détecter ces problèmes lors du développement.</span><span class="sxs-lookup"><span data-stu-id="3edfa-143">The application should <strong>Assert()</strong> to detect these issues during development .</span></span> <span data-ttu-id="3edfa-144">Toutefois, dans le code de vente au détail, l’application doit traiter ceci comme une erreur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3edfa-144">However, in retail code, the application should treat this as a memory error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-145">JET_errcatDisk 8</span><span class="sxs-lookup"><span data-stu-id="3edfa-145">JET_errcatDisk 8</span></span></p></td>
<td><p><span data-ttu-id="3edfa-146">Représente une erreur provoquée par un manque d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="3edfa-146">Represents an error caused by lack of disk space.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-147">Réessayez ultérieurement pour déterminer si de l’espace disque est disponible ou demandez à l’opérateur de libérer de l’espace disque.</span><span class="sxs-lookup"><span data-stu-id="3edfa-147">Retry later to determine whether more disk space is available, or ask the operator to free some disk space.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-148">JET_errcatData 9</span><span class="sxs-lookup"><span data-stu-id="3edfa-148">JET_errcatData 9</span></span></p></td>
<td><p><span data-ttu-id="3edfa-149">Représente une catégorie de niveau supérieur pour les erreurs liées aux données.</span><span class="sxs-lookup"><span data-stu-id="3edfa-149">Represents a top-level category for errors related to data.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-150">Consultez sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="3edfa-150">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-151">JET_errcatCorruption 10</span><span class="sxs-lookup"><span data-stu-id="3edfa-151">JET_errcatCorruption 10</span></span></p></td>
<td><p><span data-ttu-id="3edfa-152">Représente un problème d’endommagement, qui est souvent permanent sans action corrective.</span><span class="sxs-lookup"><span data-stu-id="3edfa-152">Represents a corruption issue, which is often permanent without corrective action.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-153">Restauration à partir d’une sauvegarde à l’aide de l’opération de réparation des utilitaires ESE (cette opération restaure uniquement les données qui sont conservées/perdues).</span><span class="sxs-lookup"><span data-stu-id="3edfa-153">Restore from backup by using the ESE utilities repair operation (this operation restores only the data that is left/lossy).</span></span> <span data-ttu-id="3edfa-154">En outre, lorsque la méthode Recovery (JetInit) est utilisée, la récupération peut être effectuée en autorisant la perte de données (pour plus d’informations, consultez <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="3edfa-154">Also when the recovery(JetInit) method is used, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-155">JET_errcatInconsistent 11</span><span class="sxs-lookup"><span data-stu-id="3edfa-155">JET_errcatInconsistent 11</span></span></p></td>
<td><p><span data-ttu-id="3edfa-156">Représente une erreur dans laquelle la base de données et/ou les fichiers journaux sont dans un état incohérent et ne peuvent pas être conciliés.</span><span class="sxs-lookup"><span data-stu-id="3edfa-156">Represents an error in which the database and/or log files are in a state that is inconsistent and cannot be reconciled.</span></span> <span data-ttu-id="3edfa-157">Cette erreur peut être due à une mauvaise administration de l’application/de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="3edfa-157">This error might be caused by application/administrator mishandling.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-158">Restaurez à partir d’une sauvegarde à l’aide de l’opération de réparation des utilitaires ESE (qui restaure uniquement les données qui sont conservées/perdues).</span><span class="sxs-lookup"><span data-stu-id="3edfa-158">Restore from backup by using the ESE utilities repair operation (which only restores the data that is left/lossy).</span></span> <span data-ttu-id="3edfa-159">En outre, dans le cas de l’opération de <strong>récupération (JetInit)</strong> , la récupération peut être effectuée en autorisant la perte de données (pour plus d’informations, consultez <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="3edfa-159">Also in the case of the <strong>recovery(JetInit)</strong> operation, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-160">JET_errcatFragmentation 12</span><span class="sxs-lookup"><span data-stu-id="3edfa-160">JET_errcatFragmentation 12</span></span></p></td>
<td><p><span data-ttu-id="3edfa-161">Représente une classe d’erreurs dans laquelle une ressource interne persistante s’est exécutée.</span><span class="sxs-lookup"><span data-stu-id="3edfa-161">Represents a class of errors in which some persisted internal resource ran out.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-162">Pour les erreurs de base de données, la défragmentation hors connexion permet de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="3edfa-162">For database errors, offline defragmentation will fix the problem.</span></span> <span data-ttu-id="3edfa-163">Pour les fichiers journaux, récupérez d’abord toutes les bases de données attachées à un arrêt correct, puis supprimez tous les fichiers journaux et le point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="3edfa-163">For the log files, first recover all attached databases to a clean shutdown, and then delete all the log files and the checkpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-164">JET_errcatApi 13</span><span class="sxs-lookup"><span data-stu-id="3edfa-164">JET_errcatApi 13</span></span></p></td>
<td><p><span data-ttu-id="3edfa-165">Consultez sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="3edfa-165">See subcategories.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-166">Consultez sous-catégories.</span><span class="sxs-lookup"><span data-stu-id="3edfa-166">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-167">JET_errcatUsage 14</span><span class="sxs-lookup"><span data-stu-id="3edfa-167">JET_errcatUsage 14</span></span></p></td>
<td><p><span data-ttu-id="3edfa-168">Représente une erreur d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3edfa-168">Represents a usage error.</span></span> <span data-ttu-id="3edfa-169">Le code client n’a pas transmis les arguments corrects à l’API <strong>Jet</strong> .</span><span class="sxs-lookup"><span data-stu-id="3edfa-169">The client code did not pass the correct arguments to the <strong>JET</strong> API.</span></span> <span data-ttu-id="3edfa-170">Cette erreur persiste avec une nouvelle tentative.</span><span class="sxs-lookup"><span data-stu-id="3edfa-170">This error will persist with retry.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-171">Le code client doit utiliser la méthode <strong>Assert ()</strong> pour s’assurer que cette classe d’erreurs n’est pas retournée, de sorte que les problèmes peuvent être détectés pendant le développement.</span><span class="sxs-lookup"><span data-stu-id="3edfa-171">Client code should use the <strong>Assert()</strong> method to ensure that this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="3edfa-172">Dans la version commerciale, l’application doit avertir l’opérateur de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="3edfa-172">In retail, the application should notify the operator about the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-173">JET_errcatState 15</span><span class="sxs-lookup"><span data-stu-id="3edfa-173">JET_errcatState 15</span></span></p></td>
<td><p><span data-ttu-id="3edfa-174">Représente une classe de messages que l’API peut retourner pour décrire l’état de la base de données.</span><span class="sxs-lookup"><span data-stu-id="3edfa-174">Represents a class of messages that the API can return to describe the state of the database.</span></span> <span data-ttu-id="3edfa-175">Par exemple, la méthode <a href="gg294103(v=exchg.10).md">JetSeek ()</a> peut retourner <strong>JET_errRecordNotFound</strong> lorsque l’enregistrement demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="3edfa-175">For example, the <a href="gg294103(v=exchg.10).md">JetSeek()</a> method might return <strong>JET_errRecordNotFound</strong> when the requested record was not found.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-176">Varie en fonction de l’API.</span><span class="sxs-lookup"><span data-stu-id="3edfa-176">Varies based on the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-177">JET_errcatObsolete 16</span><span class="sxs-lookup"><span data-stu-id="3edfa-177">JET_errcatObsolete 16</span></span></p></td>
<td><p><span data-ttu-id="3edfa-178">Représente les erreurs qui proviennent d’une version antérieure du moteur.</span><span class="sxs-lookup"><span data-stu-id="3edfa-178">Represents errors that are from a previous version of the engine.</span></span> <span data-ttu-id="3edfa-179">Ces erreurs ne doivent pas être retournées par le moteur actuel.</span><span class="sxs-lookup"><span data-stu-id="3edfa-179">These errors should not be returned by the current engine.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-180">Inconnu.</span><span class="sxs-lookup"><span data-stu-id="3edfa-180">Unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-181">JET_errcatMax 17</span><span class="sxs-lookup"><span data-stu-id="3edfa-181">JET_errcatMax 17</span></span></p></td>
<td><p><span data-ttu-id="3edfa-182">Constante qui indique la fin de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="3edfa-182">A constant that indicates the end of the enumeration.</span></span></p></td>
<td><p><span data-ttu-id="3edfa-183">N/A.</span><span class="sxs-lookup"><span data-stu-id="3edfa-183">N/A.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="3edfa-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3edfa-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-185"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3edfa-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3edfa-186">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3edfa-186">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edfa-187"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="3edfa-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3edfa-188">Nécessite Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="3edfa-188">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edfa-189"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="3edfa-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3edfa-190">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="3edfa-190">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

