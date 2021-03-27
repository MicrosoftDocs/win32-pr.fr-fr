---
description: Représente les objets dans l’interpréteur de commandes. Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell. Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.
title: Objet Shell (shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 3e891278d98ca2eb51fca11054cba01947e03c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867745"
---
# <a name="shell-object"></a><span data-ttu-id="1a5c6-105">Objet Shell</span><span class="sxs-lookup"><span data-stu-id="1a5c6-105">Shell object</span></span>

<span data-ttu-id="1a5c6-106">Représente les objets dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-106">Represents the objects in the Shell.</span></span> <span data-ttu-id="1a5c6-107">Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-107">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="1a5c6-108">Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-108">There are also methods to obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="1a5c6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="1a5c6-109">Members</span></span>

<span data-ttu-id="1a5c6-110">L’objet **Shell** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1a5c6-110">The **Shell** object has these types of members:</span></span>

-   [<span data-ttu-id="1a5c6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1a5c6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1a5c6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1a5c6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1a5c6-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1a5c6-113">Methods</span></span>

<span data-ttu-id="1a5c6-114">L’objet **Shell** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-114">The **Shell** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1a5c6-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="1a5c6-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1a5c6-116">Description</span><span class="sxs-lookup"><span data-stu-id="1a5c6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-117"><a href="/windows/desktop/shell/shell-addtorecent"><strong>AddToRecent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-118">Ajoute un fichier à la liste des derniers fichiers utilisés (MRU).</span><span class="sxs-lookup"><span data-stu-id="1a5c6-118">Adds a file to the most recently used (MRU) list.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-119"><a href="shell-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-120">Crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de retourner l’objet <a href="folder.md"><strong>dossier</strong></a> du dossier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-120">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-121"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>CanStartStopService</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-122">Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-122">Determines if the current user can start and stop the named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-123"><a href="shell-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-124">Cascade toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-124">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="1a5c6-125">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner des <strong>fenêtres en cascade</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-125">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade Windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-126"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-127">Exécute l’application spécifiée du panneau de configuration (\*. cpl).</span><span class="sxs-lookup"><span data-stu-id="1a5c6-127">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="1a5c6-128">Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-128">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="1a5c6-129">À compter de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-129">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="1a5c6-130">Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-130">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="1a5c6-131">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="1a5c6-131">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-132"><a href="shell-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-133">Éjecte l’ordinateur de sa station d’accueil.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-133">Ejects the computer from its docking station.</span></span> <span data-ttu-id="1a5c6-134">Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>éjecter le PC</strong>, si votre ordinateur prend en charge cette commande.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-134">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-135"><a href="shell-explore.md"><strong>Explorer</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-135"><a href="shell-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-136">Ouvre un dossier spécifié dans une fenêtre de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-136">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-137"><a href="shell-explorerpolicy.md"><strong>ExplorerPolicy</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-138">Obtient la valeur d’une stratégie Internet Explorer spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-138">Gets the value for a specified Internet Explorer policy.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-139"><a href="shell-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-140">Affiche la boîte de dialogue <strong>exécuter</strong> à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-140">Displays the <strong>Run</strong> dialog to the user.</span></span> <span data-ttu-id="1a5c6-141">Cette méthode a le même effet que lorsque vous cliquez sur le menu <strong>Démarrer</strong> et sélectionnez <strong>exécuter</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-141">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Run</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-142"><a href="shell-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-143">Affiche la boîte de dialogue résultats de la <strong>recherche : ordinateurs</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-143">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="1a5c6-144">La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-144">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-145"><a href="shell-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-146">Affiche la boîte de dialogue <strong>Rechercher : tous les fichiers</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-146">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="1a5c6-147">Cela revient à cliquer sur le menu <strong>Démarrer</strong> , puis à sélectionner <strong>Rechercher</strong> (ou son équivalent sous systèmes ANTÉRIEURs à Windows XP).</span><span class="sxs-lookup"><span data-stu-id="1a5c6-147">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong> (or its equivalent under systems earlier than Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-148"><a href="/windows/desktop/shell/shell-findprinter"><strong>FindPrinter</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-149">Affiche la boîte de dialogue <strong>Rechercher l’imprimante</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-149">Displays the <strong>Find Printer</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-150"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-151">Récupère un paramètre d’interpréteur de commandes global.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-151">Retrieves a global Shell setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-152"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>GetSystemInformation</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-153">Récupère des informations système.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-153">Retrieves system information.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-154"><a href="shell-help.md"><strong>Aide</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-154"><a href="shell-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-155">Affiche le centre d’aide et de support Windows.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-155">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="1a5c6-156">Cette méthode a le même effet que le fait de cliquer sur le menu <strong>Démarrer</strong> et de sélectionner <strong>aide et support</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-156">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-157"><a href="/windows/desktop/shell/shell-isrestricted"><strong>IsRestricted</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-158">Récupère le paramètre de restriction d’un groupe à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-158">Retrieves a group's restriction setting from the registry.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-159"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>IsServiceRunning</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-160">Retourne une valeur qui indique si un service particulier est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-160">Returns a value that indicates whether a particular service is running.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-161"><a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-162">Réduit toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-162">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="1a5c6-163">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner <strong>réduire toutes les fenêtres</strong> sur les systèmes plus anciens ou de cliquer sur l’icône <strong>afficher le bureau</strong> dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-163">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-164"><a href="shell-namespace.md"><strong>Joint</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-164"><a href="shell-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-165">Crée et retourne un objet <a href="folder.md"><strong>Folder</strong></a> pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-165">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-166"><a href="shell-open.md"><strong>Ouvrir</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-166"><a href="shell-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-167">Ouvre le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-167">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-168"><a href="shell-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-169">Actualise le contenu du menu <strong>Démarrer</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-169">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="1a5c6-170">Utilisé uniquement avec les systèmes antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-170">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-171"><a href="shell-searchcommand.md"><strong>SearchCommand</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-172">Affiche le volet de recherche applications.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-172">Displays the Apps Search pane.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-173"><a href="/windows/desktop/shell/shell-servicestart"><strong>ServiceStart</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-174">Démarre un service nommé.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-174">Starts a named service.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-175"><a href="/windows/desktop/shell/shell-servicestop"><strong>ServiceStop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-176">Arrête un service nommé.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-176">Stops a named service.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-177"><a href="shell-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-178">Affiche la boîte de dialogue <strong>Propriétés de date et heure</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-178">Displays the <strong>Date and Time Properties</strong> dialog box.</span></span> <span data-ttu-id="1a5c6-179">Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner <strong>ajuster la date/l’heure</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-179">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust Date/Time</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-180"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-181">Exécute une opération spécifiée sur un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-181">Performs a specified operation on a specified file.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-182"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>ShowBrowserBar</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-183">Affiche une barre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-183">Displays a browser bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-184"><a href="shell-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-185">Affiche la boîte de dialogue <strong>arrêter Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-185">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="1a5c6-186">Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>arrêter</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-186">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-187"><a href="shell-suspend.md"><strong>Interrompre</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-187"><a href="shell-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-188"><a href="shell-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-189">Mosaïques horizontalement toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-189">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="1a5c6-190">Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection <strong>horizontale des fenêtres de mosaïque</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-190">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Horizontally</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-191"><a href="shell-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-192">Mosaïque verticalement toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-192">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="1a5c6-193">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner les <strong>fenêtres de mosaïque verticalement</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-193">This method has the same effect as right-clicking the taskbar and selecting <strong>Tile Windows Vertically</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-194"><a href="shell-toggledesktop.md"><strong>ToggleDesktop</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-195">Affiche ou masque le bureau.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-195">Displays or hides the desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-196"><a href="shell-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-197">Affiche la boîte de dialogue <strong>Propriétés de la barre des tâches et du menu Démarrer</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-197">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="1a5c6-198">Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez <strong>Propriétés</strong>.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-198">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-199"><a href="shell-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-200">Restaure toutes les fenêtres de bureau dans le même État que celui dans lequel elles se trouvaient avant la dernière commande <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-200">Restores all desktop windows to the same state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="1a5c6-201">Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et que vous sélectionnez <strong>Annuler réduire toutes les fenêtres</strong> sur les systèmes plus anciens ou un second clic sur l’icône <strong>afficher le bureau</strong> dans la zone lancement rapide de la barre des tâches de Windows 2000 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-201">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> on older systems or a second clicking of the <strong>Show Desktop</strong> icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-202"><a href="shell-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-202"><a href="shell-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-203">Crée et retourne un objet <a href="shellwindows.md"><strong>ShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-203">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="1a5c6-204">Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-204">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1a5c6-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-205"><a href="shell-windowssecurity.md"><strong>WindowsSecurity</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-206">Affiche la boîte de dialogue <strong>sécurité Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a5c6-206">Displays the <strong>Windows Security</strong> dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a5c6-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a5c6-207"><a href="shell-windowswitcher.md"><strong>WindowSwitcher</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="1a5c6-208">Affiche vos fenêtres ouvertes dans une pile 3D que vous pouvez parcourir.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-208">Displays your open windows in a 3D stack that you can flip through.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="1a5c6-209">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1a5c6-209">Properties</span></span>

<span data-ttu-id="1a5c6-210">L’objet **Shell** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-210">The **Shell** object has these properties.</span></span>



| <span data-ttu-id="1a5c6-211">Propriété</span><span class="sxs-lookup"><span data-stu-id="1a5c6-211">Property</span></span>                                            | <span data-ttu-id="1a5c6-212">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="1a5c6-212">Access type</span></span>          | <span data-ttu-id="1a5c6-213">Description</span><span class="sxs-lookup"><span data-stu-id="1a5c6-213">Description</span></span>                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="1a5c6-214">**Application**</span><span class="sxs-lookup"><span data-stu-id="1a5c6-214">**Application**</span></span>](shell-application.md)<br/> | <span data-ttu-id="1a5c6-215">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1a5c6-215">Read-only</span></span><br/> | <span data-ttu-id="1a5c6-216">Contient l’objet d’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-216">Contains the object's Application object.</span></span><br/>                        |
| [<span data-ttu-id="1a5c6-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="1a5c6-217">**Parent**</span></span>](shell-parent.md)<br/>           | <span data-ttu-id="1a5c6-218">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1a5c6-218">Read-only</span></span><br/> | <span data-ttu-id="1a5c6-219">Obtient un objet qui représente le parent de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="1a5c6-219">Gets an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a5c6-220">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1a5c6-220">Requirements</span></span>



| <span data-ttu-id="1a5c6-221">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a5c6-221">Requirement</span></span> | <span data-ttu-id="1a5c6-222">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a5c6-222">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a5c6-223">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a5c6-223">Minimum supported client</span></span><br/> | <span data-ttu-id="1a5c6-224">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a5c6-224">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1a5c6-225">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a5c6-225">Minimum supported server</span></span><br/> | <span data-ttu-id="1a5c6-226">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a5c6-226">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a5c6-227">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a5c6-227">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a5c6-228"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a5c6-228"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1a5c6-229">MIDL</span><span class="sxs-lookup"><span data-stu-id="1a5c6-229">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a5c6-230"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a5c6-230"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1a5c6-231">DLL</span><span class="sxs-lookup"><span data-stu-id="1a5c6-231">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a5c6-232"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1a5c6-232"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
