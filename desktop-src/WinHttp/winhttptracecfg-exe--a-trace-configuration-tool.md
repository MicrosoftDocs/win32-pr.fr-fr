---
description: L’outil de configuration de trace Microsoft Windows HTTP Services (WinHTTP), WinHttpTraceCfg.exe, est utilisé pour configurer les fonctionnalités de trace à des fins de débogage et de détection de paquets.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, outil de configuration de trace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543084"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a><span data-ttu-id="260bd-103">WinHttpTraceCfg.exe, outil de configuration de trace</span><span class="sxs-lookup"><span data-stu-id="260bd-103">WinHttpTraceCfg.exe, a Trace Configuration Tool</span></span>

<span data-ttu-id="260bd-104">L’outil de configuration de trace [Microsoft Windows http services (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, est utilisé pour configurer les fonctionnalités de trace à des fins de débogage et de détection de paquets.</span><span class="sxs-lookup"><span data-stu-id="260bd-104">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) trace configuration tool, WinHttpTraceCfg.exe, is used to configure trace capabilities for debugging and packet-sniffing purposes.</span></span> <span data-ttu-id="260bd-105">Il est important de pouvoir surveiller les fonctions WinHTTP et le trafic réseau correspondant.</span><span class="sxs-lookup"><span data-stu-id="260bd-105">The ability to monitor WinHTTP functions and their corresponding network traffic is important.</span></span> <span data-ttu-id="260bd-106">Le débogage des applications qui utilisent des protocoles de transmission chiffrés, tels que les SSL (Secure Sockets Layer) (SSL), empêche la détection de paquets au niveau de la couche de transport réseau et nécessite la possibilité d’intercepter le trafic entre le client et le serveur après qu’il a été déchiffré.</span><span class="sxs-lookup"><span data-stu-id="260bd-106">Debugging applications that utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="260bd-107">Les services HTTP Microsoft Windows (WinHTTP) fournissent une fonctionnalité de trace qui offre un éventail de fonctionnalités pour intercepter le flux de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="260bd-107">Microsoft Windows HTTP Services (WinHTTP) provides a trace facility that has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

<span data-ttu-id="260bd-108">Cette fonctionnalité de trace peut être un outil précieux pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="260bd-108">This trace facility can be a valuable tool for debugging.</span></span> <span data-ttu-id="260bd-109">Il peut être utilisé, par exemple, pour afficher les paramètres passés à différents appels de fonction, ainsi que pour afficher les données réelles envoyées et reçues par une application WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="260bd-109">It can be used, for example, to view parameters passed to various function calls, as well as to view actual data sent and received by a WinHTTP application.</span></span>

-   [<span data-ttu-id="260bd-110">Utilisation de la fonction de trace</span><span class="sxs-lookup"><span data-stu-id="260bd-110">Using the Trace Facility</span></span>](#using-the-trace-facility)
-   [<span data-ttu-id="260bd-111">Interprétation des données de trace</span><span class="sxs-lookup"><span data-stu-id="260bd-111">Interpreting Trace Data</span></span>](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a><span data-ttu-id="260bd-112">Utilisation de la fonction de trace</span><span class="sxs-lookup"><span data-stu-id="260bd-112">Using the Trace Facility</span></span>

<span data-ttu-id="260bd-113">WinHTTP obtient des paramètres de contrôle de traçage à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="260bd-113">WinHTTP obtains tracing control parameters from the registry.</span></span> <span data-ttu-id="260bd-114">Ces paramètres de contrôle affectent la manière dont WinHTTP produit la sortie de trace et comment cette sortie est mise en forme.</span><span class="sxs-lookup"><span data-stu-id="260bd-114">These control parameters affect how WinHTTP produces trace output, and how that output is formatted.</span></span> <span data-ttu-id="260bd-115">Toutes les applications qui utilisent WinHTTP partagent les mêmes paramètres.</span><span class="sxs-lookup"><span data-stu-id="260bd-115">All applications that use WinHTTP share the same settings.</span></span>

<span data-ttu-id="260bd-116">Un outil de configuration de trace, WinHttpTraceCfg.exe, est disponible en téléchargement sur le site Web des [outils du kit de ressources Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="260bd-116">A trace facility configuration tool, WinHttpTraceCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="260bd-117">L’outil de configuration définit ou récupère les paramètres du registre de la fonctionnalité de trace en fonction des paramètres de ligne de commande spécifiés.</span><span class="sxs-lookup"><span data-stu-id="260bd-117">The configuration tool sets or retrieves the trace facility registry settings based on the specified command line parameters.</span></span>

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

<span data-ttu-id="260bd-118">Le tableau suivant répertorie les paramètres possibles pour l’outil de configuration de.</span><span class="sxs-lookup"><span data-stu-id="260bd-118">The following table lists possible parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="260bd-119">Paramètre</span><span class="sxs-lookup"><span data-stu-id="260bd-119">Parameter</span></span></th>
<th><span data-ttu-id="260bd-120">Description</span><span class="sxs-lookup"><span data-stu-id="260bd-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="260bd-121">-?</span><span class="sxs-lookup"><span data-stu-id="260bd-121">-?</span></span></td>
<td><span data-ttu-id="260bd-122">Affiche les données de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="260bd-122">Displays syntax data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="260bd-123">-E</span><span class="sxs-lookup"><span data-stu-id="260bd-123">-e</span></span></td>
<td><span data-ttu-id="260bd-124">Spécifie si la fonctionnalité de trace est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="260bd-124">Specifies whether the trace facility is enabled or disabled.</span></span> <br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="260bd-125">0</span><span class="sxs-lookup"><span data-stu-id="260bd-125">0</span></span></td>
<td><span data-ttu-id="260bd-126">Paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="260bd-126">Default setting.</span></span> <span data-ttu-id="260bd-127">Désactive le suivi.</span><span class="sxs-lookup"><span data-stu-id="260bd-127">Disables tracing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="260bd-128">1</span><span class="sxs-lookup"><span data-stu-id="260bd-128">1</span></span></td>
<td><span data-ttu-id="260bd-129">Active le suivi.</span><span class="sxs-lookup"><span data-stu-id="260bd-129">Enables tracing.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="260bd-130">-l</span><span class="sxs-lookup"><span data-stu-id="260bd-130">-l</span></span></td>
<td><p><span data-ttu-id="260bd-131">Spécifie un préfixe pour le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="260bd-131">Specifies a prefix for the log file.</span></span> <span data-ttu-id="260bd-132">Le préfixe peut inclure un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="260bd-132">The prefix can include a path.</span></span> <span data-ttu-id="260bd-133">Le fichier journal est écrit dans le répertoire actif ou dans le répertoire spécifié dans le préfixe et a le format suivant.</span><span class="sxs-lookup"><span data-stu-id="260bd-133">The log file is written to the current directory or the directory specified in the prefix and has the following format.</span></span></p>
<p><span data-ttu-id="260bd-134"><<em>préfixe</em> > -< <em>nom de l’application</em> > . <<em>Time</em> > . log</span><span class="sxs-lookup"><span data-stu-id="260bd-134"><<em>prefix</em>>-<<em>application name</em>>.<<em>time</em>>.log</span></span></p>
<p><span data-ttu-id="260bd-135">Si aucun préfixe n’est spécifié, une chaîne vide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="260bd-135">If a prefix is not specified, an empty string is used.</span></span> <span data-ttu-id="260bd-136">Spécifiez &quot; \* &quot; pour supprimer un préfixe existant.</span><span class="sxs-lookup"><span data-stu-id="260bd-136">Specify &quot;\*&quot; to delete an existing prefix.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="260bd-137">-d</span><span class="sxs-lookup"><span data-stu-id="260bd-137">-d</span></span></td>
<td><p><span data-ttu-id="260bd-138">Spécifie si la sortie de trace est affichée dans un débogueur ou écrite dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="260bd-138">Specifies whether the trace output is displayed in a debugger or written to a file.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="260bd-139">0</span><span class="sxs-lookup"><span data-stu-id="260bd-139">0</span></span></td>
<td><span data-ttu-id="260bd-140">Paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="260bd-140">Default setting.</span></span> <span data-ttu-id="260bd-141">Écrit dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="260bd-141">Writes to log file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="260bd-142">1</span><span class="sxs-lookup"><span data-stu-id="260bd-142">1</span></span></td>
<td><span data-ttu-id="260bd-143">S’affiche dans un débogueur.</span><span class="sxs-lookup"><span data-stu-id="260bd-143">Displays in a debugger.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="260bd-144">-S</span><span class="sxs-lookup"><span data-stu-id="260bd-144">-s</span></span></td>
<td><p><span data-ttu-id="260bd-145">Spécifie comment le trafic réseau (requêtes et réponses) est affiché.</span><span class="sxs-lookup"><span data-stu-id="260bd-145">Specifies how network traffic (requests and responses) is displayed.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="260bd-146">0</span><span class="sxs-lookup"><span data-stu-id="260bd-146">0</span></span></td>
<td><span data-ttu-id="260bd-147">Affiche uniquement les en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="260bd-147">Only displays HTTP headers.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="260bd-148">1</span><span class="sxs-lookup"><span data-stu-id="260bd-148">1</span></span></td>
<td><span data-ttu-id="260bd-149">Paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="260bd-149">Default setting.</span></span> <span data-ttu-id="260bd-150">Affiche le trafic réseau au format American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="260bd-150">Shows network traffic in American National Standards Institute (ANSI) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="260bd-151">2</span><span class="sxs-lookup"><span data-stu-id="260bd-151">2</span></span></td>
<td><span data-ttu-id="260bd-152">Affiche le trafic réseau au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="260bd-152">Shows network traffic in hexadecimal format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="260bd-153">-T</span><span class="sxs-lookup"><span data-stu-id="260bd-153">-t</span></span></td>
<td><p><span data-ttu-id="260bd-154">Spécifie si les appels de fonction de niveau supérieur sont enregistrés dans la trace.</span><span class="sxs-lookup"><span data-stu-id="260bd-154">Specifies whether top-level function calls are recorded in the trace.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="260bd-155">0</span><span class="sxs-lookup"><span data-stu-id="260bd-155">0</span></span></td>
<td><span data-ttu-id="260bd-156">Paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="260bd-156">Default setting.</span></span> <span data-ttu-id="260bd-157">Les appels de fonction ne sont pas enregistrés.</span><span class="sxs-lookup"><span data-stu-id="260bd-157">Function calls are not recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="260bd-158">1</span><span class="sxs-lookup"><span data-stu-id="260bd-158">1</span></span></td>
<td><span data-ttu-id="260bd-159">Les appels de fonction de niveau supérieur sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="260bd-159">Top-level function calls are recorded.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="260bd-160">-M</span><span class="sxs-lookup"><span data-stu-id="260bd-160">-m</span></span></td>
<td><p><span data-ttu-id="260bd-161">Spécifie la taille maximale, en octets, d’un fichier journal généré par la fonction de suivi.</span><span class="sxs-lookup"><span data-stu-id="260bd-161">Specifies the maximum size, in bytes, of a log file generated by the tracing facility.</span></span> <span data-ttu-id="260bd-162">Si cette option est spécifiée sans taille, la valeur minimale est de 65 535 octets.</span><span class="sxs-lookup"><span data-stu-id="260bd-162">If this option is specified without a size, the minimum value is 65,535 bytes.</span></span> <span data-ttu-id="260bd-163">Si un fichier journal atteint la taille maximale, le contenu du fichier est effacé.</span><span class="sxs-lookup"><span data-stu-id="260bd-163">If a log file reaches the maximum size, the contents of the file are erased.</span></span> <span data-ttu-id="260bd-164">Les données de trace continuent à être écrites dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="260bd-164">Trace data continues to be written to the log file.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="260bd-165">L’exécution de l’outil de configuration de trace et la spécification d’aucun paramètre permet de récupérer et d’afficher les paramètres de registre actuels.</span><span class="sxs-lookup"><span data-stu-id="260bd-165">Running the trace facility configuration tool and specifying no parameters retrieves and displays the current registry settings.</span></span>

> [!Note]  
> <span data-ttu-id="260bd-166">Les fichiers journaux augmentent rapidement et dégradent les performances de l’application.</span><span class="sxs-lookup"><span data-stu-id="260bd-166">Log files grow rapidly and degrade application performance.</span></span> <span data-ttu-id="260bd-167">Assurez-vous que l’espace disque requis est disponible avant d’activer la fonction de trace.</span><span class="sxs-lookup"><span data-stu-id="260bd-167">Ensure that the required hard disk drive space is available before enabling the trace facility.</span></span>

 

## <a name="interpreting-trace-data"></a><span data-ttu-id="260bd-168">Interprétation des données de trace</span><span class="sxs-lookup"><span data-stu-id="260bd-168">Interpreting Trace Data</span></span>

<span data-ttu-id="260bd-169">Le flux de données de la fonction de trace reflète les fonctions WinHTTP appelées dans l’application et toutes les données HTTP envoyées ou reçues.</span><span class="sxs-lookup"><span data-stu-id="260bd-169">The trace facility data stream reflects WinHTTP functions called in the application and any HTTP data sent or received.</span></span> <span data-ttu-id="260bd-170">Dans certains cas, les fonctions appelées en interne par WinHTTP sont également affichées.</span><span class="sxs-lookup"><span data-stu-id="260bd-170">In some cases, functions called internally by WinHTTP are also shown.</span></span>

<span data-ttu-id="260bd-171">L’illustration suivante montre une partie d’un fichier journal généré par la fonction de trace.</span><span class="sxs-lookup"><span data-stu-id="260bd-171">The following image shows a portion of a log file generated by the trace facility.</span></span> <span data-ttu-id="260bd-172">Plusieurs éléments sont mis en surbrillance et étiquetés.</span><span class="sxs-lookup"><span data-stu-id="260bd-172">Several items are highlighted and labeled.</span></span>

![exemple de suivi](images/ss-tracer-wco.png)

<span data-ttu-id="260bd-174">Chaque ligne de la sortie de trace contient des informations dans trois colonnes.</span><span class="sxs-lookup"><span data-stu-id="260bd-174">Each line of trace output contains information in three columns.</span></span> <span data-ttu-id="260bd-175">La première colonne affiche la date et l’heure d’enregistrement de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="260bd-175">The first column shows the date and time when the entry was recorded.</span></span> <span data-ttu-id="260bd-176">La deuxième colonne affiche un identificateur de demande (ID) qui peut être utilisé pour différencier plusieurs demandes.</span><span class="sxs-lookup"><span data-stu-id="260bd-176">The second column shows a request identifier (ID) that can be used to differentiate between multiple requests.</span></span> <span data-ttu-id="260bd-177">Si l’entrée de journal ne correspond pas à une demande spécifique, « \* session \* » s’affiche dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="260bd-177">If the log entry does not correspond to a specific request, "\*Session\*" is displayed in this column.</span></span> <span data-ttu-id="260bd-178">Il peut être utile de trier le fichier journal en fonction de cet ID pour afficher uniquement les événements qui se produisent pour une requête unique.</span><span class="sxs-lookup"><span data-stu-id="260bd-178">It can be useful to sort the log file based on this ID to see only events that occur for a single request.</span></span> <span data-ttu-id="260bd-179">L’exemple suivant montre une commande que vous pouvez utiliser pour trier le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="260bd-179">The following example shows a command you can use to sort the log file.</span></span>

<span data-ttu-id="260bd-180">**findstr 00000001 LogFile. log**</span><span class="sxs-lookup"><span data-stu-id="260bd-180">**findstr 00000001 LogFile.log**</span></span>

<span data-ttu-id="260bd-181">La troisième colonne affiche un appel de fonction, le trafic HTTP ou un message d’État inclus pour aider à interpréter la trace.</span><span class="sxs-lookup"><span data-stu-id="260bd-181">The third column shows a function call, HTTP traffic, or a status message included to help interpret the trace.</span></span>

<span data-ttu-id="260bd-182">Lorsqu’une entrée de journal correspond à un appel de fonction, les paramètres de la fonction sont également enregistrés.</span><span class="sxs-lookup"><span data-stu-id="260bd-182">When a log entry corresponds to a function call, the parameters of the function are also recorded.</span></span> <span data-ttu-id="260bd-183">Les adresses mémoire sont affichées au format hexadécimal, tandis que toutes les autres valeurs sont affichées sous forme de chaîne ASCII.</span><span class="sxs-lookup"><span data-stu-id="260bd-183">Memory addresses are displayed in hexadecimal while all other values are displayed as an ASCII string.</span></span> <span data-ttu-id="260bd-184">La fonction de trace enregistre également l’heure et la valeur de retour pour chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="260bd-184">The trace facility also records the return time and value for each function.</span></span>

<span data-ttu-id="260bd-185">Le format des données HTTP dépend des paramètres du Registre spécifiés avec l’outil de configuration de trace.</span><span class="sxs-lookup"><span data-stu-id="260bd-185">The format of HTTP data depends on the registry settings specified with the trace facility configuration tool.</span></span> <span data-ttu-id="260bd-186">Lorsque les données HTTP sont chiffrées, les données déchiffrées sont également affichées dans la sortie de trace.</span><span class="sxs-lookup"><span data-stu-id="260bd-186">When HTTP data is encrypted, the decrypted data is also shown in the trace output.</span></span>

 

 




