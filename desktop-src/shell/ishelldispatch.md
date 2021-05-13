---
description: Représente un objet dans l’interpréteur de commandes.
title: Objet IShellDispatch (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840890"
---
# <a name="ishelldispatch-object"></a><span data-ttu-id="ea4a3-103">Objet IShellDispatch</span><span class="sxs-lookup"><span data-stu-id="ea4a3-103">IShellDispatch object</span></span>

<span data-ttu-id="ea4a3-104">Représente un objet dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-104">Represents an object in the Shell.</span></span> <span data-ttu-id="ea4a3-105">Des méthodes sont fournies pour contrôler l’interpréteur de commandes et exécuter des commandes dans le shell.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-105">Methods are provided to control the Shell and to execute commands within the Shell.</span></span> <span data-ttu-id="ea4a3-106">Il existe également des méthodes pour obtenir d’autres objets liés à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-106">There are also methods to obtain other Shell-related objects.</span></span>

> [!Note]  
> <span data-ttu-id="ea4a3-107">**IShellDispatch** est implémenté et accessible via l’objet [**Shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-107">**IShellDispatch** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="ea4a3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ea4a3-108">Members</span></span>

<span data-ttu-id="ea4a3-109">L’objet **IShellDispatch** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea4a3-109">The **IShellDispatch** object has these types of members:</span></span>

-   [<span data-ttu-id="ea4a3-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ea4a3-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea4a3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea4a3-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea4a3-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ea4a3-112">Methods</span></span>

<span data-ttu-id="ea4a3-113">L’objet **IShellDispatch** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-113">The **IShellDispatch** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="ea4a3-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea4a3-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="ea4a3-115">Description</span><span class="sxs-lookup"><span data-stu-id="ea4a3-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-116"><a href="ishelldispatch-browseforfolder.md"><strong>BrowseForFolder</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-117">Crée une boîte de dialogue qui permet à l’utilisateur de sélectionner un dossier, puis de retourner l’objet <a href="folder.md"><strong>dossier</strong></a> du dossier sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-117">Creates a dialog box that enables the user to select a folder and then returns the selected folder's <a href="folder.md"><strong>Folder</strong></a> object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-118"><a href="ishelldispatch-cascadewindows.md"><strong>CascadeWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-119">Cascade toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-119">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="ea4a3-120">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner des <strong>fenêtres en cascade</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-120">This method has the same effect as right-clicking the taskbar and selecting <strong>Cascade windows</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-121"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-122">Exécute l’application du panneau de configuration spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-122">Runs the specified Control Panel application.</span></span> <span data-ttu-id="ea4a3-123">Si l’application est déjà ouverte, elle activera l’instance en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-123">If the application is already open, it will activate the running instance.</span></span> <br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="ea4a3-124">À compter de Windows Vista, la plupart des applications du panneau de configuration sont des éléments de Shell et ne peuvent pas être ouvertes avec cette fonction.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-124">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="ea4a3-125">Pour ouvrir ces applications du panneau de configuration, transmettez le nom canonique à control.exe.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-125">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="ea4a3-126">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ea4a3-126">For example:</span></span></p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-127"><a href="ishelldispatch-ejectpc.md"><strong>EjectPC</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-128">Éjecte l’ordinateur de sa station d’accueil.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-128">Ejects the computer from its docking station.</span></span> <span data-ttu-id="ea4a3-129">Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>éjecter le PC</strong>, si votre ordinateur prend en charge cette commande.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-129">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Eject PC</strong>, if your computer supports this command.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-130"><a href="ishelldispatch-explore.md"><strong>Explorer</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-130"><a href="ishelldispatch-explore.md"><strong>Explore</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-131">Ouvre un dossier spécifié dans une fenêtre de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-131">Opens a specified folder in a Windows Explorer window.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-132"><a href="ishelldispatch-filerun.md"><strong>FileRun</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-133">Affiche la boîte de dialogue <strong>exécuter</strong> à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-133">Displays the <strong>Run</strong> dialog to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-134"><a href="ishelldispatch-findcomputer.md"><strong>FindComputer</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-135">Affiche la boîte de dialogue résultats de la <strong>recherche : ordinateurs</strong> .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-135">Displays the <strong>Search Results: Computers</strong> dialog box.</span></span> <span data-ttu-id="ea4a3-136">La boîte de dialogue affiche le résultat de la recherche d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-136">The dialog box shows the result of the search for a specified computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-137"><a href="ishelldispatch-findfiles.md"><strong>FindFiles</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-138">Affiche la boîte de dialogue <strong>Rechercher : tous les fichiers</strong> .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-138">Displays the <strong>Find: All Files</strong> dialog box.</span></span> <span data-ttu-id="ea4a3-139">Cela revient à cliquer sur le menu <strong>Démarrer</strong> , puis à sélectionner <strong>Rechercher</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-139">This is the same as clicking the <strong>Start</strong> menu and then selecting <strong>Search</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-140"><a href="ishelldispatch-help.md"><strong>Aide</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-140"><a href="ishelldispatch-help.md"><strong>Help</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-141">Affiche la fenêtre aide et support Windows.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-141">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="ea4a3-142">Cette méthode a le même effet que le fait de cliquer sur le menu <strong>Démarrer</strong> et de sélectionner <strong>aide et support</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-142">This method has the same effect as clicking the <strong>Start</strong> menu and selecting <strong>Help and Support</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-143"><a href="ishelldispatch-minimizeall.md"><strong>MinimizeAll</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-144">Réduit toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-144">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="ea4a3-145">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner <strong>réduire toutes les fenêtres</strong> sur les anciens systèmes ou cliquer sur l’icône <strong>afficher le bureau</strong> dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-145">This method has the same effect as right-clicking the taskbar and selecting <strong>Minimize All Windows</strong> on older systems or clicking the <strong>Show Desktop</strong> icon on the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-146"><a href="ishelldispatch-namespace.md"><strong>Joint</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-146"><a href="ishelldispatch-namespace.md"><strong>NameSpace</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-147">Crée et retourne un objet <a href="folder.md"><strong>Folder</strong></a> pour le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-147">Creates and returns a <a href="folder.md"><strong>Folder</strong></a> object for the specified folder.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-148"><a href="ishelldispatch-open.md"><strong>Afficher</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-148"><a href="ishelldispatch-open.md"><strong>Open</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-149">Ouvre le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-149">Opens the specified folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-150"><a href="ishelldispatch-refreshmenu.md"><strong>RefreshMenu</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-151">Actualise le contenu du menu <strong>Démarrer</strong> .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-151">Refreshes the contents of the <strong>Start</strong> menu.</span></span> <span data-ttu-id="ea4a3-152">Utilisé uniquement avec les systèmes antérieurs à Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-152">Used only with systems preceding Windows XP.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-153"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-154">Affiche la boîte de dialogue <strong>date et heure</strong> .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-154">Displays the <strong>Date and Time</strong> dialog box.</span></span> <span data-ttu-id="ea4a3-155">Cette méthode a le même effet que de cliquer avec le bouton droit sur l’horloge dans la zone d’état de la barre des tâches et de sélectionner <strong>ajuster la date/l’heure</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-155">This method has the same effect as right-clicking the clock in the taskbar status area and selecting <strong>Adjust date/time</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-156"><a href="ishelldispatch-shutdownwindows.md"><strong>ShutdownWindows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-157">Affiche la boîte de dialogue <strong>arrêter Windows</strong> .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-157">Displays the <strong>Shut Down Windows</strong> dialog box.</span></span> <span data-ttu-id="ea4a3-158">Cela revient à cliquer sur le menu <strong>Démarrer</strong> et à sélectionner <strong>arrêter</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-158">This is the same as clicking the <strong>Start</strong> menu and selecting <strong>Shut Down</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-159"><a href="ishelldispatch-suspend.md"><strong>Momentané</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-159"><a href="ishelldispatch-suspend.md"><strong>Suspend</strong></a></span></span></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-160"><a href="ishelldispatch-tilehorizontally.md"><strong>TileHorizontally</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-161">Mosaïques horizontalement toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-161">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="ea4a3-162">Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection de l’option <strong>afficher les fenêtres empilées</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-162">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows stacked</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-163"><a href="ishelldispatch-tilevertically.md"><strong>TileVertically</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-164">Mosaïque verticalement toutes les fenêtres sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-164">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="ea4a3-165">Cette méthode a le même effet que le clic droit sur la barre des tâches et la sélection de l’option <strong>afficher les fenêtres côte à côte</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-165">This method has the same effect as right-clicking the taskbar and selecting <strong>Show windows side by side</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-166"><a href="ishelldispatch-trayproperties.md"><strong>TrayProperties</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-167">Affiche la boîte de dialogue <strong>Propriétés de la barre des tâches et du menu Démarrer</strong> .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-167">Displays the <strong>Taskbar and Start Menu Properties</strong> dialog box.</span></span> <span data-ttu-id="ea4a3-168">Cette méthode a le même effet que lorsque vous cliquez avec le bouton droit sur la barre des tâches et sélectionnez <strong>Propriétés</strong>.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-168">This method has the same effect as right-clicking the taskbar and selecting <strong>Properties</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="ea4a3-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-169"><a href="ishelldispatch-undominimizeall.md"><strong>UndoMinimizeALL</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-170">Restaure toutes les fenêtres de bureau à l’État où elles se trouvaient avant la dernière commande <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-170">Restores all desktop windows to the state they were in before the last <a href="shell-minimizeall.md"><strong>MinimizeAll</strong></a> command.</span></span> <span data-ttu-id="ea4a3-171">Cette méthode a le même effet que de cliquer avec le bouton droit sur la barre des tâches et de sélectionner <strong>Annuler réduire toutes les fenêtres</strong> (sur les systèmes plus anciens) ou un second clic sur l’icône <strong>afficher le bureau</strong> dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-171">This method has the same effect as right-clicking the taskbar and selecting <strong>Undo Minimize All Windows</strong> (on older systems) or a second clicking of the <strong>Show Desktop</strong> icon in the taskbar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="ea4a3-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4a3-172"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="ea4a3-173">Crée et retourne un objet <a href="shellwindows.md"><strong>ShellWindows</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ea4a3-173">Creates and returns a <a href="shellwindows.md"><strong>ShellWindows</strong></a> object.</span></span> <span data-ttu-id="ea4a3-174">Cet objet représente une collection de toutes les fenêtres ouvertes qui appartiennent au shell.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-174">This object represents a collection of all of the open windows that belong to the Shell.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="ea4a3-175">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea4a3-175">Properties</span></span>

<span data-ttu-id="ea4a3-176">L’objet **IShellDispatch** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-176">The **IShellDispatch** object has these properties.</span></span>



| <span data-ttu-id="ea4a3-177">Propriété</span><span class="sxs-lookup"><span data-stu-id="ea4a3-177">Property</span></span>                                                     | <span data-ttu-id="ea4a3-178">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="ea4a3-178">Access type</span></span>          | <span data-ttu-id="ea4a3-179">Description</span><span class="sxs-lookup"><span data-stu-id="ea4a3-179">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="ea4a3-180">**Application**</span><span class="sxs-lookup"><span data-stu-id="ea4a3-180">**Application**</span></span>](ishelldispatch-application.md)<br/> | <span data-ttu-id="ea4a3-181">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea4a3-181">Read-only</span></span><br/> | <span data-ttu-id="ea4a3-182">Contient un objet qui représente une application.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-182">Contains an object that represents an application.</span></span><br/>                    |
| [<span data-ttu-id="ea4a3-183">**Parent**</span><span class="sxs-lookup"><span data-stu-id="ea4a3-183">**Parent**</span></span>](ishelldispatch-parent.md)<br/>           | <span data-ttu-id="ea4a3-184">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea4a3-184">Read-only</span></span><br/> | <span data-ttu-id="ea4a3-185">Récupère un objet qui représente le parent de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="ea4a3-185">Retrieves an object that represents the parent of the current object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ea4a3-186">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ea4a3-186">Requirements</span></span>



| <span data-ttu-id="ea4a3-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea4a3-187">Requirement</span></span> | <span data-ttu-id="ea4a3-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea4a3-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4a3-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea4a3-189">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4a3-190">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea4a3-190">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ea4a3-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea4a3-191">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4a3-192">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea4a3-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ea4a3-193">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea4a3-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea4a3-194"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea4a3-194"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ea4a3-195">MIDL</span><span class="sxs-lookup"><span data-stu-id="ea4a3-195">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea4a3-196"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea4a3-196"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ea4a3-197">DLL</span><span class="sxs-lookup"><span data-stu-id="ea4a3-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea4a3-198"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ea4a3-198"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4a3-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea4a3-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4a3-200">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ea4a3-200">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="ea4a3-201">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="ea4a3-201">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 
