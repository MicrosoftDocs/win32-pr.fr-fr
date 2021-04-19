---
description: Wilogutl.exe aide à analyser les fichiers journaux à partir d’une installation Windows Installer et affiche les solutions suggérées aux erreurs qui se trouvent dans un fichier journal.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542062"
---
# <a name="wilogutlexe"></a><span data-ttu-id="bddf4-103">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="bddf4-103">Wilogutl.exe</span></span>

<span data-ttu-id="bddf4-104">Wilogutl.exe aide à analyser les fichiers journaux à partir d’une installation Windows Installer et affiche les solutions suggérées aux erreurs qui se trouvent dans un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bddf4-104">Wilogutl.exe assists the analysis of log files from a Windows Installer installation, and it displays suggested solutions to errors that are found in a log file.</span></span>

<span data-ttu-id="bddf4-105">Les erreurs non critiques ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="bddf4-105">Non-critical errors are not displayed.</span></span> <span data-ttu-id="bddf4-106">Wilogutl.exe peut être exécuté en mode silencieux ou à l’aide d’une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bddf4-106">Wilogutl.exe can be run in quiet mode or with a user interface (UI).</span></span> <span data-ttu-id="bddf4-107">L’outil génère des rapports en tant que fichiers texte dans l’interface utilisateur et en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="bddf4-107">The tool generates reports as text files in both the UI and quiet modes.</span></span> <span data-ttu-id="bddf4-108">Il fonctionne mieux avec les fichiers journaux de Windows Installer détaillés, mais il fonctionne également avec les journaux non détaillés.</span><span class="sxs-lookup"><span data-stu-id="bddf4-108">It works best with verbose Windows Installer log files, but also works with non-verbose logs.</span></span> <span data-ttu-id="bddf4-109">Pour plus d’informations, consultez [Journalisation](logging.md).</span><span class="sxs-lookup"><span data-stu-id="bddf4-109">For more information, see [Logging](logging.md).</span></span>

<span data-ttu-id="bddf4-110">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="bddf4-110">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bddf4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bddf4-111">Syntax</span></span>

<span data-ttu-id="bddf4-112">\**wilogutl.exe\*\*\*\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span><span class="sxs-lookup"><span data-stu-id="bddf4-112">**wilogutl.exe** *\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span></span>

<span data-ttu-id="bddf4-113">Vous pouvez utiliser les lignes de commande suivantes pour exécuter en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="bddf4-113">You can use the following command lines to run in quiet mode.</span></span>

<span data-ttu-id="bddf4-114">**Wilogutl/q/l** *c : \\ mymsilog. log* **/o** *c \\ OutputDir \\*</span><span class="sxs-lookup"><span data-stu-id="bddf4-114">**wilogutl /q /l** *c:\\mymsilog.log* **/o** *c\\outputdir\\*</span></span>

<span data-ttu-id="bddf4-115">**Wilogutl/q/l** *c : \\ mymsilog. log*</span><span class="sxs-lookup"><span data-stu-id="bddf4-115">**wilogutl /q /l** *c:\\mymsilog.log*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="bddf4-116">Options de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="bddf4-116">Command-Line Options</span></span>

<span data-ttu-id="bddf4-117">Wilogutl.exe utilise les options de ligne de commande qui ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="bddf4-117">Wilogutl.exe uses the following case insensitive command-line options.</span></span> <span data-ttu-id="bddf4-118">Un séparateur de tirets peut être utilisé à la place d’une barre oblique.</span><span class="sxs-lookup"><span data-stu-id="bddf4-118">A dash delimiter can be used in place of a slash.</span></span>



| <span data-ttu-id="bddf4-119">Option</span><span class="sxs-lookup"><span data-stu-id="bddf4-119">Option</span></span> | <span data-ttu-id="bddf4-120">Description</span><span class="sxs-lookup"><span data-stu-id="bddf4-120">Description</span></span>                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddf4-121">aucun</span><span class="sxs-lookup"><span data-stu-id="bddf4-121">none</span></span>   | <span data-ttu-id="bddf4-122">S’exécute en mode interface utilisateur, sans options de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="bddf4-122">Runs in UI mode—without command-line options.</span></span>                                                                                                                                                   |
| <span data-ttu-id="bddf4-123">/q</span><span class="sxs-lookup"><span data-stu-id="bddf4-123">/q</span></span>     | <span data-ttu-id="bddf4-124">Spécifie le mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="bddf4-124">Specifies the quiet mode.</span></span> <span data-ttu-id="bddf4-125">Wilogutl.exe génère des fichiers de rapport et n’affiche pas d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bddf4-125">Wilogutl.exe generates report files and does not display a user interface.</span></span>                                                                                            |
| <span data-ttu-id="bddf4-126">/l</span><span class="sxs-lookup"><span data-stu-id="bddf4-126">/l</span></span>     | <span data-ttu-id="bddf4-127">Spécifie le nom du fichier journal à analyser.</span><span class="sxs-lookup"><span data-stu-id="bddf4-127">Specifies the name of the log file to be analyzed.</span></span> <span data-ttu-id="bddf4-128">Cette option est requise lors de l’utilisation du mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="bddf4-128">This option is required when using the quiet mode.</span></span>                                                                                           |
| <span data-ttu-id="bddf4-129">/o</span><span class="sxs-lookup"><span data-stu-id="bddf4-129">/o</span></span>     | <span data-ttu-id="bddf4-130">Spécifie le répertoire de sortie pour les fichiers de rapport.</span><span class="sxs-lookup"><span data-stu-id="bddf4-130">Specifies the output directory for report files.</span></span> <span data-ttu-id="bddf4-131">Ce chemin de sortie est utilisé uniquement lors de l’exécution en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="bddf4-131">This output path is used only when running in quiet mode.</span></span> <span data-ttu-id="bddf4-132">Si l’option n’est pas présente, les rapports sont placés dans le répertoire C : \\ WiLogResults.</span><span class="sxs-lookup"><span data-stu-id="bddf4-132">If the option is not present, the reports are put in the C:\\WiLogResults directory.</span></span> |



 

<span data-ttu-id="bddf4-133">Quand elle est exécutée en mode interface utilisateur, Wilogutl.exe affiche les boîtes de dialogue suivantes.</span><span class="sxs-lookup"><span data-stu-id="bddf4-133">When run in UI mode, Wilogutl.exe displays the following dialog boxes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bddf4-134">Nom</span><span class="sxs-lookup"><span data-stu-id="bddf4-134">Name</span></span></th>
<th><span data-ttu-id="bddf4-135">Description</span><span class="sxs-lookup"><span data-stu-id="bddf4-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bddf4-136">Analyseur de journal détaillé Windows Installer</span><span class="sxs-lookup"><span data-stu-id="bddf4-136">Windows Installer Verbose Log Analyzer</span></span></td>
<td><span data-ttu-id="bddf4-137">La boîte de dialogue Windows Installerer l’analyseur de journal détaillé permet aux utilisateurs de sélectionner un fichier journal à analyser :</span><span class="sxs-lookup"><span data-stu-id="bddf4-137">The Windows Installer Verbose Log Analyzer dialog box enables users to select a log file for analysis:</span></span>
<ul>
<li><span data-ttu-id="bddf4-138">Le bouton <strong>ouvrir</strong> ouvre le fichier dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="bddf4-138">The <strong>Open</strong> button opens the file in Notepad.</span></span> <span data-ttu-id="bddf4-139">La zone d’aperçu peut être utilisée pour vérifier que le fichier journal correct a été sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bddf4-139">The preview area can be used to verify that the correct log file has been selected.</span></span></li>
<li><span data-ttu-id="bddf4-140">Le bouton <strong>analyser</strong> démarre l’analyse des fichiers journaux et affiche la boîte de dialogue vue détaillée du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bddf4-140">The <strong>Analyze</strong> button begins log file analysis and displays the Detailed Log File View dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bddf4-141">Affichage détaillé du fichier journal</span><span class="sxs-lookup"><span data-stu-id="bddf4-141">Detailed Log File View</span></span></td>
<td><span data-ttu-id="bddf4-142">La boîte de dialogue Affichage détaillé du fichier journal affiche les informations d’erreur journalisées.</span><span class="sxs-lookup"><span data-stu-id="bddf4-142">The Detailed Log File View dialog box displays logged error information.</span></span> <span data-ttu-id="bddf4-143">Utilisez les boutons <strong>précédent</strong> et <strong>suivant</strong> pour parcourir plusieurs erreurs.</span><span class="sxs-lookup"><span data-stu-id="bddf4-143">Use the <strong>Back</strong> and <strong>Next</strong> buttons to navigate through multiple errors.</span></span> <span data-ttu-id="bddf4-144">Pour afficher les erreurs non critiques, activez la case à cocher <strong>afficher les erreurs de débogage ignorées</strong> .</span><span class="sxs-lookup"><span data-stu-id="bddf4-144">To display non-critical errors select the <strong>Show Ignored Debug Errors</strong> check box.</span></span> <span data-ttu-id="bddf4-145">La version du programme d’installation sur l’ordinateur utilisé pour exécuter l’installation journalisée s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bddf4-145">The installer version on the computer used to run the logged installation is displayed.</span></span> <span data-ttu-id="bddf4-146">Si l’installation journalisée a été exécutée avec des autorisations élevées, la case à cocher <strong>installation élevée</strong> est activée et les informations sont fournies dans les zones de texte <strong>Détails des privilèges côté client</strong> et <strong>Détails des privilèges côté serveur</strong> .</span><span class="sxs-lookup"><span data-stu-id="bddf4-146">If the logged installation was run with elevated permissions, the <strong>Elevated install</strong> check box is selected and information is provided in the <strong>Client Side Privilege Details</strong> and <strong>Server Side Privilege Details</strong> text boxes.</span></span> <span data-ttu-id="bddf4-147">La boîte de dialogue vue détaillée du fichier journal contient les boutons suivants :</span><span class="sxs-lookup"><span data-stu-id="bddf4-147">The Detailed Log File View dialog box contains the following buttons:</span></span><br/>
<ul>
<li><span data-ttu-id="bddf4-148"><strong>États</strong> - Affiche la boîte de dialogue États des fonctionnalités et des composants.</span><span class="sxs-lookup"><span data-stu-id="bddf4-148"><strong>States</strong> - Show the Feature and Component States dialog box.</span></span></li>
<li><span data-ttu-id="bddf4-149"><strong>Propriétés</strong> - de Affiche la boîte de dialogue Propriétés.</span><span class="sxs-lookup"><span data-stu-id="bddf4-149"><strong>Properties</strong> - Show the Properties dialog box.</span></span></li>
<li><span data-ttu-id="bddf4-150"><strong>Stratégies</strong> - Affiche la boîte de dialogue stratégies.</span><span class="sxs-lookup"><span data-stu-id="bddf4-150"><strong>Policies</strong> - Show the Policies dialog box.</span></span></li>
<li><span data-ttu-id="bddf4-151"><strong>Journal</strong> - annoté html Afficher le journal comme fichier HTML annoté.</span><span class="sxs-lookup"><span data-stu-id="bddf4-151"><strong>HTML Annotated Log</strong> - Show log as annotated HTML file.</span></span></li>
<li><span data-ttu-id="bddf4-152"><strong>Enregistrer les résultats</strong> - Enregistrer les fichiers de rapport dans le répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="bddf4-152"><strong>Save Results</strong> - Save report files to specified directory.</span></span></li>
<li><span data-ttu-id="bddf4-153"><strong>Aide sur les messages d’erreur</strong> - Afficher l’aide du message d’erreur du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="bddf4-153"><strong>Error Message Help</strong> - Show installer error message help.</span></span></li>
<li><span data-ttu-id="bddf4-154"><strong>Aide</strong> - Afficher l’aide de Windows Installer analyseur de journal d’installation.</span><span class="sxs-lookup"><span data-stu-id="bddf4-154"><strong>Help</strong> - Show help for Windows Installer Setup Log Analyzer.</span></span></li>
<li><span data-ttu-id="bddf4-155"><strong>Comment lire un fichier journal</strong> - Affichez le document d’aide du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bddf4-155"><strong>How to Read a Log File</strong> - Show the log file help document.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bddf4-156">États des fonctionnalités et des composants</span><span class="sxs-lookup"><span data-stu-id="bddf4-156">Feature and Component States</span></span></td>
<td><span data-ttu-id="bddf4-157">La boîte de dialogue États des fonctionnalités <strong>et</strong> des composants affiche les États des fonctionnalités et des composants :</span><span class="sxs-lookup"><span data-stu-id="bddf4-157">The <strong>Feature and Component States</strong> dialog box displays the states of features and components:</span></span>
<ul>
<li><span data-ttu-id="bddf4-158">La colonne <strong>fonctionnalité</strong> affiche le nom de la fonctionnalité dans le package d’installation.</span><span class="sxs-lookup"><span data-stu-id="bddf4-158">The <strong>Feature</strong> column shows the name for the feature in the installation package.</span></span></li>
<li><span data-ttu-id="bddf4-159">La colonne <strong>composant</strong> indique le nom du composant dans le package d’installation.</span><span class="sxs-lookup"><span data-stu-id="bddf4-159">The <strong>Component</strong> column shows the name of the component in the installation package.</span></span></li>
<li><span data-ttu-id="bddf4-160">La colonne <strong>installé</strong> indique l’état de la fonctionnalité ou du composant à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="bddf4-160">The <strong>Installed</strong> column shows the feature or component's state at the end of the installation.</span></span></li>
<li><span data-ttu-id="bddf4-161">La colonne <strong>requête</strong> affiche la sélection de l’utilisateur au cours de l’installation pour l’état de la fonctionnalité ou du composant.</span><span class="sxs-lookup"><span data-stu-id="bddf4-161">The <strong>Request</strong> column shows the user's selection during the installation for the feature or component's state.</span></span></li>
<li><span data-ttu-id="bddf4-162">La colonne <strong>action</strong> affiche l’action entreprise par le programme d’installation de la fonctionnalité ou du composant.</span><span class="sxs-lookup"><span data-stu-id="bddf4-162">The <strong>Action</strong> column shows the action taken by the installer for the feature or component.</span></span></li>
</ul>
<span data-ttu-id="bddf4-163">Pour plus d’informations, consultez <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> et <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bddf4-163">For more information, see <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> and <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bddf4-164">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bddf4-164">Properties</span></span></td>
<td><span data-ttu-id="bddf4-165">La boîte de dialogue Propriétés affiche Windows Installer <a href="properties.md">Propriétés</a> et leurs valeurs à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="bddf4-165">The Properties dialog box shows Windows Installer <a href="properties.md">Properties</a> and their values at the end of the installation.</span></span> <span data-ttu-id="bddf4-166">Vous pouvez trier les propriétés par nom ou par valeur :</span><span class="sxs-lookup"><span data-stu-id="bddf4-166">You can sort the properties by name or by value:</span></span>
<ul>
<li><span data-ttu-id="bddf4-167">L’onglet <strong>client</strong> affiche les propriétés et les valeurs de la partie côté client de l’installation.</span><span class="sxs-lookup"><span data-stu-id="bddf4-167">The <strong>Client</strong> tab shows properties and values during the client side portion of the installation.</span></span></li>
<li><span data-ttu-id="bddf4-168">L’onglet <strong>serveur</strong> affiche les propriétés et les valeurs de la partie serveur de l’installation.</span><span class="sxs-lookup"><span data-stu-id="bddf4-168">The <strong>Server</strong> tab shows properties and values during the server portion of the installation.</span></span></li>
<li><span data-ttu-id="bddf4-169">L’onglet <strong>imbriqué</strong> affiche les propriétés et les valeurs de toutes les <a href="concurrent-installations.md">installations simultanées</a>.</span><span class="sxs-lookup"><span data-stu-id="bddf4-169">The <strong>Nested</strong> tab shows the properties and values of any <a href="concurrent-installations.md">Concurrent Installations</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bddf4-170">Stratégies</span><span class="sxs-lookup"><span data-stu-id="bddf4-170">Policies</span></span></td>
<td><span data-ttu-id="bddf4-171">La boîte de dialogue stratégies affiche la <a href="system-policy.md">stratégie système</a> définie après l’installation :</span><span class="sxs-lookup"><span data-stu-id="bddf4-171">The Policies dialog box displays the <a href="system-policy.md">System Policy</a> set after the installation:</span></span>
<ul>
<li><span data-ttu-id="bddf4-172">Une valeur 0 (zéro) définie pour la stratégie signifie que la stratégie n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="bddf4-172">A value of 0 (zero) set for the policy means the policy is not enabled.</span></span></li>
<li><span data-ttu-id="bddf4-173">La valeur 1 (un) signifie que la stratégie est activée.</span><span class="sxs-lookup"><span data-stu-id="bddf4-173">A value of 1 (one) means the policy is enabled.</span></span></li>
<li><span data-ttu-id="bddf4-174">La valeur ?</span><span class="sxs-lookup"><span data-stu-id="bddf4-174">A value of ?</span></span> <span data-ttu-id="bddf4-175">(point d’interrogation) signifie que la valeur de stratégie n’est pas enregistrée dans le journal.</span><span class="sxs-lookup"><span data-stu-id="bddf4-175">(question mark) means the policy value is not recorded in the log.</span></span></li>
</ul>
<span data-ttu-id="bddf4-176">Si vous avez besoin d’une valeur de stratégie qui n’est pas dans le journal, essayez d’utiliser Regedit.exe pour vérifier les clés de Registre sur l’ordinateur qui n’a pas pu être installé.</span><span class="sxs-lookup"><span data-stu-id="bddf4-176">If you need a policy value that is not in the log, try using Regedit.exe to check the registry keys on the computer failing the installation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a><span data-ttu-id="bddf4-177">Fichiers de rapport</span><span class="sxs-lookup"><span data-stu-id="bddf4-177">Report Files</span></span>

<span data-ttu-id="bddf4-178">Lorsque vous effectuez une analyse en mode silencieux ou que vous cliquez sur le bouton **enregistrer les résultats** dans la boîte de dialogue **vue détaillée du fichier journal** , l’outil analyseur d’installation de Windows Installer génère trois fichiers texte et un fichier journal annoté html.</span><span class="sxs-lookup"><span data-stu-id="bddf4-178">When performing a quiet mode analysis or clicking the **Save Results** button on the **Detailed Log File View** dialog, the Windows Installer Setup Analyzer tool generates three text files and an HTML annotated log file.</span></span>

<span data-ttu-id="bddf4-179">Le tableau suivant identifie les noms et le contenu des fichiers de rapport.</span><span class="sxs-lookup"><span data-stu-id="bddf4-179">The following table identifies the names and contents in the report files.</span></span>



| <span data-ttu-id="bddf4-180">Nom</span><span class="sxs-lookup"><span data-stu-id="bddf4-180">Name</span></span>                      | <span data-ttu-id="bddf4-181">Description</span><span class="sxs-lookup"><span data-stu-id="bddf4-181">Description</span></span>                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddf4-182">\_summary.txt LogFileName</span><span class="sxs-lookup"><span data-stu-id="bddf4-182">logfilename\_summary.txt</span></span>  | <span data-ttu-id="bddf4-183">Résume le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bddf4-183">Summarizes the log file.</span></span> <span data-ttu-id="bddf4-184">Répertorie les informations affichées dans la boîte de dialogue Affichage détaillé du fichier journal et la première erreur.</span><span class="sxs-lookup"><span data-stu-id="bddf4-184">Lists the information displayed by the Detailed Log File View dialog box and the first error.</span></span>         |
| <span data-ttu-id="bddf4-185">\_errors.txt LogFileName</span><span class="sxs-lookup"><span data-stu-id="bddf4-185">logfilename\_errors.txt</span></span>   | <span data-ttu-id="bddf4-186">Identifie le nombre d’erreurs, les erreurs et les solutions recommandées.</span><span class="sxs-lookup"><span data-stu-id="bddf4-186">Identifies the number of errors, the errors, and recommended solutions.</span></span> <span data-ttu-id="bddf4-187">Ce fichier répertorie les erreurs critiques et non critiques.</span><span class="sxs-lookup"><span data-stu-id="bddf4-187">This file lists both critical and non-critical errors.</span></span> |
| <span data-ttu-id="bddf4-188">\_policies.txt LogFileName</span><span class="sxs-lookup"><span data-stu-id="bddf4-188">logfilename\_policies.txt</span></span> | <span data-ttu-id="bddf4-189">Identifie les noms et valeurs de stratégie définis à la fin de l’installation comme dans la boîte de dialogue stratégies.</span><span class="sxs-lookup"><span data-stu-id="bddf4-189">Identifies the policy names and values set at the end of the installation as in the Policies dialog box.</span></span>                       |
| <span data-ttu-id="bddf4-190">Détails \_logfilename.htm</span><span class="sxs-lookup"><span data-stu-id="bddf4-190">details\_logfilename.htm</span></span>  | <span data-ttu-id="bddf4-191">Journal annoté HTML avec une légende pour le codage en couleurs.</span><span class="sxs-lookup"><span data-stu-id="bddf4-191">An HTML annotated log with a legend for the color coding.</span></span>                                                                      |



 

## <a name="return-values"></a><span data-ttu-id="bddf4-192">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bddf4-192">Return Values</span></span>

<span data-ttu-id="bddf4-193">Si des arguments de ligne de commande non valides sont passés pour les opérations en mode silencieux, Wilogutl.exe ne fait rien, et le processus retourne l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bddf4-193">If invalid command-line arguments are passed for quiet mode operations, Wilogutl.exe does nothing, and the process returns one of the values in the following table.</span></span>



| <span data-ttu-id="bddf4-194">Valeur</span><span class="sxs-lookup"><span data-stu-id="bddf4-194">Value</span></span> | <span data-ttu-id="bddf4-195">Signification</span><span class="sxs-lookup"><span data-stu-id="bddf4-195">Meaning</span></span>                                                                 |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="bddf4-196">1</span><span class="sxs-lookup"><span data-stu-id="bddf4-196">1</span></span>     | <span data-ttu-id="bddf4-197">Le répertoire de sortie incorrect est spécifié.</span><span class="sxs-lookup"><span data-stu-id="bddf4-197">Bad output directory is specified.</span></span>                                      |
| <span data-ttu-id="bddf4-198">2</span><span class="sxs-lookup"><span data-stu-id="bddf4-198">2</span></span>     | <span data-ttu-id="bddf4-199">Un nom de fichier journal incorrect est spécifié.</span><span class="sxs-lookup"><span data-stu-id="bddf4-199">Bad log file name is specified.</span></span>                                         |
| <span data-ttu-id="bddf4-200">3</span><span class="sxs-lookup"><span data-stu-id="bddf4-200">3</span></span>     | <span data-ttu-id="bddf4-201">A réussi, mais il manque le commutateur obligatoire/l pour le nom du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="bddf4-201">Passed /q, but is missing the required switch /l for the log file name.</span></span> |
| <span data-ttu-id="bddf4-202">4</span><span class="sxs-lookup"><span data-stu-id="bddf4-202">4</span></span>     | <span data-ttu-id="bddf4-203">Réussite de/l, mais absence du commutateur requis/q pour le mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="bddf4-203">Passed /l, but is missing the required switch /q for quiet mode.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bddf4-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bddf4-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bddf4-205">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="bddf4-205">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> <dt>

[<span data-ttu-id="bddf4-206">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="bddf4-206">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> </dl>

 

 




