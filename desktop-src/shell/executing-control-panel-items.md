---
description: Décrit les méthodes d’ouverture d’un élément du panneau de configuration pour les systèmes Windows Vista et versions ultérieures, ainsi que la couverture des commandes du panneau de configuration héritées.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Exécution des éléments du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991689"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="307dc-103">Exécution des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="307dc-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="307dc-104">Si vous recherchez la liste des noms canoniques et des noms de module pour les éléments du panneau de configuration, consultez [noms canoniques des éléments du panneau de configuration](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="307dc-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="307dc-105">Il existe deux façons d’ouvrir un élément du panneau de configuration :</span><span class="sxs-lookup"><span data-stu-id="307dc-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="307dc-106">L’utilisateur peut ouvrir le panneau de configuration, puis ouvrir un élément en cliquant ou en double-cliquant sur l’icône de l’élément.</span><span class="sxs-lookup"><span data-stu-id="307dc-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="307dc-107">L’utilisateur ou une application peut démarrer un élément du panneau de configuration en l’exécutant directement à partir de l’invite de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="307dc-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="307dc-108">Une application peut ouvrir le panneau de configuration par programmation à l’aide de la fonction [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="307dc-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="307dc-109">L’exemple suivant montre comment une application peut démarrer l’élément du panneau de configuration nommé **MyCpl.cpl** à l’aide de la fonction [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="307dc-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="307dc-110">Lorsqu’un élément du panneau de configuration est ouvert par le biais d’une ligne de commande, vous pouvez l’indiquer pour qu’il s’ouvre à un onglet particulier dans l’élément.</span><span class="sxs-lookup"><span data-stu-id="307dc-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="307dc-111">En raison de l’ajout et de la suppression de certains onglets dans certains éléments du panneau de configuration de Windows Vista, la numérotation des onglets peut avoir changé par rapport à celui de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="307dc-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="307dc-112">Par exemple, l’exemple suivant lance le quatrième onglet de l’élément système sous Windows XP et le troisième onglet sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="307dc-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="307dc-113">Cette rubrique traite des sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="307dc-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="307dc-114">Noms canoniques Windows Vista</span><span class="sxs-lookup"><span data-stu-id="307dc-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="307dc-115">Nouvelles commandes pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="307dc-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="307dc-116">Commandes du panneau de configuration héritées</span><span class="sxs-lookup"><span data-stu-id="307dc-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="307dc-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="307dc-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="307dc-118">Noms canoniques Windows Vista</span><span class="sxs-lookup"><span data-stu-id="307dc-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="307dc-119">Dans Windows Vista et versions ultérieures, la méthode recommandée pour lancer un élément du panneau de configuration à partir d’une ligne de commande consiste à utiliser le nom canonique de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="307dc-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="307dc-120">Un nom canonique est une chaîne non localisée que l’élément du panneau de configuration déclare dans le registre.</span><span class="sxs-lookup"><span data-stu-id="307dc-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="307dc-121">La valeur de l’utilisation d’un nom canonique est qu’elle résume le nom de module de l’élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="307dc-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="307dc-122">Il est possible d’implémenter un élément dans un fichier. dll et de le réimplémenter ultérieurement en tant que. exe ou de modifier son nom de module.</span><span class="sxs-lookup"><span data-stu-id="307dc-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="307dc-123">Tant que le nom canonique reste le même, tout programme qui l’ouvre à l’aide de ce nom canonique n’a pas besoin d’être mis à jour.</span><span class="sxs-lookup"><span data-stu-id="307dc-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="307dc-124">Par Convention, le nom canonique est formé en tant que « CorporationName. ControlPanelItemName ».</span><span class="sxs-lookup"><span data-stu-id="307dc-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="307dc-125">L’exemple suivant montre comment une application peut démarrer l’élément du panneau de configuration **Windows Update** avec [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span><span class="sxs-lookup"><span data-stu-id="307dc-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="307dc-126">Pour démarrer un élément du panneau de configuration avec son nom canonique, utilisez : "% systemroot% \\ system32 \\control.exe/name *canonicalName*"</span><span class="sxs-lookup"><span data-stu-id="307dc-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="307dc-127">Pour ouvrir une sous-page spécifique dans un élément ou pour l’ouvrir avec des paramètres supplémentaires, utilisez : « % systemroot% \\ system32 \\control.exe/name **canonicalName** des pages **pagename**»</span><span class="sxs-lookup"><span data-stu-id="307dc-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="307dc-128">Une application peut également implémenter la méthode [**IOpenControlPanel :: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) pour lancer des éléments du panneau de configuration, y compris la possibilité d’ouvrir une sous-page spécifique.</span><span class="sxs-lookup"><span data-stu-id="307dc-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="307dc-129">Pour obtenir la liste complète des noms canoniques des éléments du panneau de configuration, consultez [noms canoniques des éléments du panneau de configuration](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="307dc-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="307dc-130">Nouvelles commandes pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="307dc-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="307dc-131">Sur Windows Vista, certaines options qui étaient accessibles par un module. cpl sur Windows XP sont désormais implémentées en tant que fichiers. exe.</span><span class="sxs-lookup"><span data-stu-id="307dc-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="307dc-132">Cela permet de renforcer la sécurité en permettant aux utilisateurs standard d’être invités à fournir des informations d’identification d’administrateur lors de la tentative de lancement des fichiers.</span><span class="sxs-lookup"><span data-stu-id="307dc-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="307dc-133">Les options qui ne nécessitent pas de sécurité supplémentaire sont accessibles par les lignes de commande qui ont été utilisées dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="307dc-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="307dc-134">La liste suivante répertorie les commandes utilisées dans Windows Vista pour accéder à des onglets spécifiques des éléments du panneau de configuration :</span><span class="sxs-lookup"><span data-stu-id="307dc-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="307dc-135">Personnalisation</span><span class="sxs-lookup"><span data-stu-id="307dc-135">Personalization</span></span>

-   <span data-ttu-id="307dc-136">Taille de police et PPP :% windir% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="307dc-137">Résolution d’écran :% windir% \\ system32 \\control.exe desk.cpl, paramètres,@Settings</span><span class="sxs-lookup"><span data-stu-id="307dc-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="307dc-138">Paramètres d’affichage :% windir% \\ system32 \\control.exe desk.cpl, paramètres,@Settings</span><span class="sxs-lookup"><span data-stu-id="307dc-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="307dc-139">Thèmes :% windir% \\ system32 \\control.exe desk.cpl, thèmes,@Themes</span><span class="sxs-lookup"><span data-stu-id="307dc-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="307dc-140">Économiseur d’écran :% windir% \\ system32 \\control.exe desk.cpl, écran de veille,@screensaver</span><span class="sxs-lookup"><span data-stu-id="307dc-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="307dc-141">Multi-Monitor :% windir% \\ system32 \\control.exe desk.cpl, surveiller@Monitor</span><span class="sxs-lookup"><span data-stu-id="307dc-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="307dc-142">Modèle de couleurs :% windir% \\ system32 \\control.exe/name Microsoft. Personalization des pages pageColorization</span><span class="sxs-lookup"><span data-stu-id="307dc-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="307dc-143">Arrière-plan du Bureau :% windir% \\ system32 \\control.exe/name Microsoft. Personalization des pages pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="307dc-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="307dc-144">Les éditions Starter et Basic ne prennent pas en charge la commande control.exe/name Microsoft. Personalization.</span><span class="sxs-lookup"><span data-stu-id="307dc-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="307dc-145">Système</span><span class="sxs-lookup"><span data-stu-id="307dc-145">System</span></span>

-   <span data-ttu-id="307dc-146">Performances :% windir% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="307dc-147">Accès à distance :% windir% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="307dc-148">Nom de l’ordinateur :% windir% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="307dc-149">Protection du système :% windir% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="307dc-150">Propriétés système avancées :% windir% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="307dc-151">Programmes et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="307dc-151">Programs and Features</span></span>

-   <span data-ttu-id="307dc-152">Ajout/suppression de programmes :% windir% \\ system32 \\control.exe/name Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="307dc-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="307dc-153">Fonctionnalités Windows :% windir% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="307dc-154">Options régionales et linguistiques</span><span class="sxs-lookup"><span data-stu-id="307dc-154">Regional and Language Options</span></span>

-   <span data-ttu-id="307dc-155">Clavier :% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions des pages/p : "Keyboard"</span><span class="sxs-lookup"><span data-stu-id="307dc-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="307dc-156">Emplacement :% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions des pages/p : "location"</span><span class="sxs-lookup"><span data-stu-id="307dc-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="307dc-157">Administration :% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions des pages/p : "administrative"</span><span class="sxs-lookup"><span data-stu-id="307dc-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="307dc-158">Options des dossiers</span><span class="sxs-lookup"><span data-stu-id="307dc-158">Folder Options</span></span>

-   <span data-ttu-id="307dc-159">Recherche de dossier :% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundll 2</span><span class="sxs-lookup"><span data-stu-id="307dc-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="307dc-160">Associations de fichiers :% windir% \\ system32 \\control.exe/name Microsoft. DefaultPrograms des pages pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="307dc-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="307dc-161">Affichage :% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundll 7</span><span class="sxs-lookup"><span data-stu-id="307dc-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="307dc-162">Général :% windir% \\ system32 \\rundll32.exe shell32.dll, options \_ Rundll 0</span><span class="sxs-lookup"><span data-stu-id="307dc-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="307dc-163">Options d’alimentation</span><span class="sxs-lookup"><span data-stu-id="307dc-163">Power Options</span></span>

-   <span data-ttu-id="307dc-164">Modifier les paramètres actuels du plan :% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions des pages pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="307dc-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="307dc-165">Paramètres système :% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions des pages pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="307dc-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="307dc-166">Créer un mode de gestion de l’alimentation :% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions des pages pageCreateNewPlan</span><span class="sxs-lookup"><span data-stu-id="307dc-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="307dc-167">Il n’existe aucune commande canonique pour la page Paramètres avancés, elle est accessible de la manière précédente :% windir% \\ system32 \\control.exe powercfg.cpl,, 3</span><span class="sxs-lookup"><span data-stu-id="307dc-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="307dc-168">Commandes du panneau de configuration héritées</span><span class="sxs-lookup"><span data-stu-id="307dc-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="307dc-169">Lorsque vous utilisez la fonction [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) , le système peut reconnaître des commandes spéciales du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="307dc-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="307dc-170">Ces commandes prédatent Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="307dc-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="307dc-171">control.exe Desktop</span><span class="sxs-lookup"><span data-stu-id="307dc-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="307dc-172">Lance la fenêtre <strong>propriétés d’affichage</strong> .</span><span class="sxs-lookup"><span data-stu-id="307dc-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="307dc-173">Les éditions Starter et Basic ne prennent pas en charge cette commande.</span><span class="sxs-lookup"><span data-stu-id="307dc-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="307dc-174">Couleur de control.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-174">control.exe color</span></span></td>
<td><span data-ttu-id="307dc-175">Ouvre la fenêtre <strong>propriétés d’affichage</strong> avec l’onglet <strong>apparence</strong> présélectionné.</span><span class="sxs-lookup"><span data-stu-id="307dc-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="307dc-176">Date/heure de control.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="307dc-177">Lance la fenêtre des <strong>Propriétés de date et d’heure</strong> .</span><span class="sxs-lookup"><span data-stu-id="307dc-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="307dc-178">control.exe international</span><span class="sxs-lookup"><span data-stu-id="307dc-178">control.exe international</span></span></td>
<td><span data-ttu-id="307dc-179">Lance la fenêtre <strong>Options régionales et linguistiques</strong> .</span><span class="sxs-lookup"><span data-stu-id="307dc-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="307dc-180">control.exe souris</span><span class="sxs-lookup"><span data-stu-id="307dc-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="307dc-181">Lance la fenêtre Propriétés de la <strong>souris</strong> .</span><span class="sxs-lookup"><span data-stu-id="307dc-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="307dc-182">Clavier control.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="307dc-183">Lance la fenêtre <strong>Propriétés du clavier</strong> .</span><span class="sxs-lookup"><span data-stu-id="307dc-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="307dc-184">Imprimantes control.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-184">control.exe printers</span></span></td>
<td><span data-ttu-id="307dc-185">Affiche le dossier <strong>imprimantes et télécopieurs</strong> .</span><span class="sxs-lookup"><span data-stu-id="307dc-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="307dc-186">Polices de control.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="307dc-187">Affiche le dossier <strong>polices</strong> .</span><span class="sxs-lookup"><span data-stu-id="307dc-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="307dc-188">Pour les systèmes Windows 2000 et versions ultérieures :</span><span class="sxs-lookup"><span data-stu-id="307dc-188">For Windows 2000 and later systems:</span></span>



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="307dc-189">Dossiers de control.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-189">control.exe folders</span></span>        | <span data-ttu-id="307dc-190">Lance la fenêtre **Options des dossiers** .</span><span class="sxs-lookup"><span data-stu-id="307dc-190">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="307dc-191">control.exe NetWare</span><span class="sxs-lookup"><span data-stu-id="307dc-191">control.exe netware</span></span>        | <span data-ttu-id="307dc-192">Lance la fenêtre **Novell NetWare** (si installée).</span><span class="sxs-lookup"><span data-stu-id="307dc-192">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="307dc-193">Téléphonie control.exe</span><span class="sxs-lookup"><span data-stu-id="307dc-193">control.exe telephony</span></span>      | <span data-ttu-id="307dc-194">Ouvre la fenêtre **options de téléphone et de modem** .</span><span class="sxs-lookup"><span data-stu-id="307dc-194">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="307dc-195">control.exe AdminTools</span><span class="sxs-lookup"><span data-stu-id="307dc-195">control.exe admintools</span></span>     | <span data-ttu-id="307dc-196">Affiche le dossier **Outils d’administration** .</span><span class="sxs-lookup"><span data-stu-id="307dc-196">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="307dc-197">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="307dc-197">control.exe schedtasks</span></span>     | <span data-ttu-id="307dc-198">Affiche le dossier **tâches planifiées** .</span><span class="sxs-lookup"><span data-stu-id="307dc-198">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="307dc-199">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="307dc-199">control.exe netconnections</span></span> | <span data-ttu-id="307dc-200">Affiche le dossier **connexions réseau** .</span><span class="sxs-lookup"><span data-stu-id="307dc-200">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="307dc-201">control.exe infrarouge</span><span class="sxs-lookup"><span data-stu-id="307dc-201">control.exe infrared</span></span>       | <span data-ttu-id="307dc-202">Lance la fenêtre **Moniteur infrarouge** (si installée).</span><span class="sxs-lookup"><span data-stu-id="307dc-202">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="307dc-203">control.exe userpasswords</span><span class="sxs-lookup"><span data-stu-id="307dc-203">control.exe userpasswords</span></span>  | <span data-ttu-id="307dc-204">Lance la fenêtre **comptes d’utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="307dc-204">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="307dc-205">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="307dc-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="307dc-206">Éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="307dc-206">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="307dc-207">Conseils sur l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="307dc-207">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="307dc-208">Inscription des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="307dc-208">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="307dc-209">Utilisation de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="307dc-209">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="307dc-210">Traitement des messages du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="307dc-210">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="307dc-211">Extension des éléments du panneau de configuration système</span><span class="sxs-lookup"><span data-stu-id="307dc-211">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="307dc-212">Affectation des catégories du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="307dc-212">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="307dc-213">Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="307dc-213">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="307dc-214">Accès au panneau de configuration en mode sans échec sous Windows Vista</span><span class="sxs-lookup"><span data-stu-id="307dc-214">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
