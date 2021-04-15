---
title: Interface utilisateur graphique AccChecker
description: Cette rubrique décrit les éléments qui composent l’interface graphique utilisateur AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104556648"
---
# <a name="the-accchecker-graphical-user-interface"></a><span data-ttu-id="547f9-103">Interface utilisateur graphique AccChecker</span><span class="sxs-lookup"><span data-stu-id="547f9-103">The AccChecker Graphical User Interface</span></span>

<span data-ttu-id="547f9-104">Cette rubrique décrit les éléments qui composent l’interface graphique utilisateur AccChecker.</span><span class="sxs-lookup"><span data-stu-id="547f9-104">This topic describes the elements that make up the AccChecker GUI.</span></span>

-   [<span data-ttu-id="547f9-105">Onglet vérifications</span><span class="sxs-lookup"><span data-stu-id="547f9-105">Verifications Tab</span></span>](#verifications-tab)
-   [<span data-ttu-id="547f9-106">Onglet résultats</span><span class="sxs-lookup"><span data-stu-id="547f9-106">Results Tab</span></span>](#results-tab)
-   [<span data-ttu-id="547f9-107">Onglets lecteur d’écran MSAA et UIA</span><span class="sxs-lookup"><span data-stu-id="547f9-107">MSAA and UIA Screen Reader Tabs</span></span>](#msaa-and-uia-screen-reader-tabs)
-   [<span data-ttu-id="547f9-108">Onglets d’arborescence MSAA et UIA</span><span class="sxs-lookup"><span data-stu-id="547f9-108">MSAA and UIA Tree Tabs</span></span>](#msaa-and-uia-tree-tabs)
-   [<span data-ttu-id="547f9-109">Menu fichier</span><span class="sxs-lookup"><span data-stu-id="547f9-109">File Menu</span></span>](#file-menu)
-   [<span data-ttu-id="547f9-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="547f9-110">Related topics</span></span>](#related-topics)

## <a name="verifications-tab"></a><span data-ttu-id="547f9-111">Onglet vérifications</span><span class="sxs-lookup"><span data-stu-id="547f9-111">Verifications Tab</span></span>

<span data-ttu-id="547f9-112">AccChecker démarre avec la vue par défaut de l’onglet **vérifications** :</span><span class="sxs-lookup"><span data-stu-id="547f9-112">AccChecker starts with the default view of the **Verifications** tab:</span></span>

![Capture d’écran montrant l’onglet « vérifications » dans l’outil de vérification de l’accessibilité U I.](images/accchecker-verifications-tab.png)

<span data-ttu-id="547f9-114">L’onglet **vérifications** contient les composants suivants.</span><span class="sxs-lookup"><span data-stu-id="547f9-114">The **Verifications** tab contains the following components.</span></span>

-   <span data-ttu-id="547f9-115">**Sélecteur de cible de vérification** Offre les options suivantes pour sélectionner une application ou un contrôle cible.</span><span class="sxs-lookup"><span data-stu-id="547f9-115">**Verification target selector** Offers the following options for selecting a target application or control.</span></span>
    -   <span data-ttu-id="547f9-116">Choisissez une cible dans la liste déroulante préremplie.</span><span class="sxs-lookup"><span data-stu-id="547f9-116">Choose a target from the pre-populated drop-down list.</span></span> <span data-ttu-id="547f9-117">Cette liste contient tous les HWND de niveau supérieur identifiés au démarrage.</span><span class="sxs-lookup"><span data-stu-id="547f9-117">This list contains all top-level HWNDs identified at start-up.</span></span>
    -   <span data-ttu-id="547f9-118">Choisissez un HWND en fonction de l’emplacement du curseur de la souris (les contrôles sélectionnables sont mis en surbrillance avec un rectangle rouge).</span><span class="sxs-lookup"><span data-stu-id="547f9-118">Choose an HWND based on the location of the mouse cursor (selectable controls are highlighted with a red rectangle).</span></span> <span data-ttu-id="547f9-119">Cette option vous permet de sélectionner n’importe quel objet visible ayant un HWND.</span><span class="sxs-lookup"><span data-stu-id="547f9-119">This option lets you select any visible object that has an HWND.</span></span>
    -   <span data-ttu-id="547f9-120">Entrez un HWND particulier.</span><span class="sxs-lookup"><span data-stu-id="547f9-120">Enter a particular HWND.</span></span>
-   <span data-ttu-id="547f9-121">Liste de vérification des **routines de vérification** Permet de sélectionner la routine de vérification souhaitée à exécuter sur une application ou un contrôle.</span><span class="sxs-lookup"><span data-stu-id="547f9-121">**Verification routines checklist** Provides the ability to select the desired verification routine to be performed against an application or control.</span></span> <span data-ttu-id="547f9-122">Pour plus d’informations, consultez routines de vérification.</span><span class="sxs-lookup"><span data-stu-id="547f9-122">See Verification Routines for more information.</span></span>
-   <span data-ttu-id="547f9-123">**Sélecteur de fichier de suppression d’erreur et d’avertissement** Les fichiers de suppression sont générés à partir de l’onglet **résultats** de la vérification. En cliquant avec le bouton droit sur un message d’erreur ou d’avertissement et en sélectionnant **supprimer** dans le menu contextuel, un indicateur est défini pour ce message.</span><span class="sxs-lookup"><span data-stu-id="547f9-123">**Error and warning suppression file selector** Suppression files are generated from the verification **Results** tab. By right-clicking an error or warning message and selecting **Suppress** from the context menu, a flag is set for that message.</span></span> <span data-ttu-id="547f9-124">Si la case à cocher **suppressions** est activée, les entrées supprimées apparaissent dans la liste.</span><span class="sxs-lookup"><span data-stu-id="547f9-124">If the **Suppressions** check box is checked, suppressed entries appear in the list.</span></span> <span data-ttu-id="547f9-125">Une entrée supprimée peut être supprimée en utilisant le même menu contextuel que celui utilisé pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="547f9-125">A suppressed entry can be unsuppressed by using the same context menu used to suppress it.</span></span>

    <span data-ttu-id="547f9-126">Un fichier de suppression est enregistré au format XML en sélectionnant **enregistrer la suppression** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="547f9-126">A suppression file is saved in XML format by selecting **Save Suppression** from the **File** menu.</span></span> <span data-ttu-id="547f9-127">Ce fichier est consommé lors des exécutions de vérification suivantes où les messages sont masqués.</span><span class="sxs-lookup"><span data-stu-id="547f9-127">This file is consumed on subsequent verification runs where the messages will be hidden.</span></span> <span data-ttu-id="547f9-128">Pour supprimer le fichier de suppression, cliquez sur **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="547f9-128">To remove the suppression file, click **Clear**.</span></span> <span data-ttu-id="547f9-129">Pour plus d’informations sur des messages spécifiques, consultez messages du journal de vérification.</span><span class="sxs-lookup"><span data-stu-id="547f9-129">For information on specific messages, see Verification Log Messages.</span></span> <span data-ttu-id="547f9-130">Utilisez l’option **enregistrer le journal** du menu **fichier** pour enregistrer la liste entière sous forme de fichier journal au format XML ou sous forme de fichier texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="547f9-130">Use **Save Log** from the **File** menu to save the entire list as a log file in XML or as a formatted text file.</span></span>

    ![accchecker onglet résultats avec l’élément de contexte de suppression mis en surbrillance](images/accchecker-results-tab-with-suppress.png)

    <span data-ttu-id="547f9-132">L’exemple suivant montre le contenu d’un fichier de suppression généré en exécutant les vérifications des **Propriétés** sur l’application du panneau de configuration du pare-feu Windows.</span><span class="sxs-lookup"><span data-stu-id="547f9-132">The following example shows the content of a suppression file generated by running the **Properties** verifications on the Windows Firewall control panel application.</span></span> <span data-ttu-id="547f9-133">L’erreur avec l’ID « ElementHasNoName » a été choisie pour la suppression dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="547f9-133">The error with an ID of "ElementHasNoName" was chosen for suppression in this example.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   <span data-ttu-id="547f9-134">**Afficher les résultats classés par ordre de priorité** Offre les options suivantes pour filtrer les résultats de la vérification par priorité.</span><span class="sxs-lookup"><span data-stu-id="547f9-134">**Show prioritized results** Offers the following options for filtering the verification results by priority.</span></span>
    -   <span data-ttu-id="547f9-135">**Tout** Inclure tous les résultats, quelle que soit la priorité.</span><span class="sxs-lookup"><span data-stu-id="547f9-135">**All** Include all all results regardless of priority.</span></span>
    -   <span data-ttu-id="547f9-136">**P1 uniquement** Inclure uniquement les résultats de priorité 0 et de priorité 1.</span><span class="sxs-lookup"><span data-stu-id="547f9-136">**P1 only** Include only priority 0 and priority 1 results.</span></span>
    -   <span data-ttu-id="547f9-137">**P1 P2 uniquement** Incluez les résultats de priorité 0 à priorité 2.</span><span class="sxs-lookup"><span data-stu-id="547f9-137">**P1   P2 only** Include priority 0 through priority 2 results.</span></span>
-   <span data-ttu-id="547f9-138">**Exécuter les vérifications sélectionnées** Fournit le bouton **exécuter des vérifications** pour démarrer le processus de vérification.</span><span class="sxs-lookup"><span data-stu-id="547f9-138">**Run selected verifications** Provides the **Run Verifications** button for starting the verification process.</span></span> <span data-ttu-id="547f9-139">Lorsque les vérifications sont en cours d’exécution, le bouton prend la valeur **annuler les vérifications** et peut être utilisé pour arrêter les vérifications une fois l’exécution du en cours terminée.</span><span class="sxs-lookup"><span data-stu-id="547f9-139">While verifications are running, the button changes to **Cancel Verifications** and can be used to stop the verifications after the current one completes.</span></span>

## <a name="results-tab"></a><span data-ttu-id="547f9-140">Onglet Résultats</span><span class="sxs-lookup"><span data-stu-id="547f9-140">Results Tab</span></span>

<span data-ttu-id="547f9-141">L’onglet **résultats** est rempli une fois les tâches de vérification sélectionnées terminées.</span><span class="sxs-lookup"><span data-stu-id="547f9-141">The **Results** tab is populated after the selected verification tasks are complete.</span></span> <span data-ttu-id="547f9-142">Il comprend les composants suivants.</span><span class="sxs-lookup"><span data-stu-id="547f9-142">It consists of the following components.</span></span>

-   <span data-ttu-id="547f9-143">La liste des messages, qui affiche les messages d’erreur, d’avertissement et d’information générés par les tâches de vérification sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="547f9-143">The message list, which displays the error, warning, and informational messages generated by the selected verification tasks.</span></span> <span data-ttu-id="547f9-144">Les messages affichés peuvent être filtrés par type à l’aide des cases à cocher au-dessus de la liste des messages.</span><span class="sxs-lookup"><span data-stu-id="547f9-144">The messages displayed can be filtered by type using the checkboxes above the message list.</span></span>
-   <span data-ttu-id="547f9-145">Détails du message et capture d’écran de la cible de vérification.</span><span class="sxs-lookup"><span data-stu-id="547f9-145">The message details and a screen capture of the verification target.</span></span> <span data-ttu-id="547f9-146">La sélection d’un message dans la liste des messages affiche plus de détails et met en surbrillance l’élément correspondant dans le volet de capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="547f9-146">Selecting a message from the message list displays further details and highlights the corresponding element in the screen capture pane.</span></span> <span data-ttu-id="547f9-147">Le bouton **visualiser** , bascule AccChecker vers l’onglet de l' **arborescence MSAA** . Si une erreur est mise en surbrillance sous l’onglet **résultats** , l’élément correspondant est mis en surbrillance sous l’onglet de l' **arborescence MSAA** .</span><span class="sxs-lookup"><span data-stu-id="547f9-147">The **Visualize** button, switches AccChecker to the **MSAA Tree** tab. If an error is highlighted on the **Results** tab, the corresponding element is highlighted on the **MSAA Tree** tab.</span></span>

<span data-ttu-id="547f9-148">Cliquer avec le bouton droit sur un message expose un menu contextuel avec les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="547f9-148">Right-clicking on a message exposes a context menu with the following items.</span></span>

-   <span data-ttu-id="547f9-149">**Supprimer** Ajoute le message à la liste de suppression.</span><span class="sxs-lookup"><span data-stu-id="547f9-149">**Suppress** Adds the message to the suppression list.</span></span>
-   <span data-ttu-id="547f9-150">**Copier dans le presse-papiers** Copie les détails du message dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="547f9-150">**Copy to clipboard** Copies the message details to the clipboard.</span></span>
-   <span data-ttu-id="547f9-151">**Visualiser** Bascule AccChecker vers l’onglet d' **arborescence MSAA** . L’élément qui correspond à l’erreur sélectionnée est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="547f9-151">**Visualize** Switches AccChecker to the **MSAA Tree** tab. The element that corresponds to the selected error is highlighted.</span></span>
-   <span data-ttu-id="547f9-152">**Aide** Affiche des informations supplémentaires sur le message.</span><span class="sxs-lookup"><span data-stu-id="547f9-152">**Help** Displays additional information about the message.</span></span>

## <a name="msaa-and-uia-screen-reader-tabs"></a><span data-ttu-id="547f9-153">Onglets lecteur d’écran MSAA et UIA</span><span class="sxs-lookup"><span data-stu-id="547f9-153">MSAA and UIA Screen Reader Tabs</span></span>

<span data-ttu-id="547f9-154">Les onglets lecteur d’écran MSAA et lecteur d’écran UIA sont similaires.</span><span class="sxs-lookup"><span data-stu-id="547f9-154">The MSAA Screen reader and the UIA Screen reader tabs are similar.</span></span> <span data-ttu-id="547f9-155">Les deux affichent une transcription des éléments rencontrés dans un parcours simulé de la cible de vérification par un lecteur d’écran, à l’exception de l’implémentation MSAA, tandis que l’autre montre l’implémentation de UIA.</span><span class="sxs-lookup"><span data-stu-id="547f9-155">Both display a transcript of elements encountered in a simulated traversal of the verification target by a screen reader, except that one shows the MSAA implementation, and the other shows the UIA implemention.</span></span>

<span data-ttu-id="547f9-156">Les éléments sont consultés et journalisés comme un lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="547f9-156">Elements are navigated and logged just as a screen reader would read them.</span></span> <span data-ttu-id="547f9-157">Les informations présentées dans cet onglet sont essentielles pour confirmer que seules les informations utiles et pertinentes sont annoncées.</span><span class="sxs-lookup"><span data-stu-id="547f9-157">The information presented on this tab is essential to confirm that only useful and relevant information is being announced.</span></span> <span data-ttu-id="547f9-158">Par exemple, un nom de contrôle de son mode normal, tel que « Edit MenuItem » ou « PushButton Close », est acceptable ; Toutefois, un nom de contrôle qui n’a pas de sens, tel que « CPNavPanel22 » ou « DefaultValue1 », n’est pas acceptable.</span><span class="sxs-lookup"><span data-stu-id="547f9-158">For example, a normal-sounding control name such as "MenuItem Edit" or "PushButton Close" is acceptable; however, a control name that doesn't make sense, such as "CPNavPanel22" or "DefaultValue1", is not acceptable.</span></span> <span data-ttu-id="547f9-159">Le bouton **visualiser** , force AccChecker à basculer vers l' **arborescence MSAA** ou l’onglet d' **arborescence UIA** . Si un élément est mis en surbrillance sous l’onglet **lecteur d’écran** , l’élément correspondant est mis en surbrillance dans l' **arborescence MSAA** ou l’onglet d' **arborescence UIA** .</span><span class="sxs-lookup"><span data-stu-id="547f9-159">The **Visualize** button, causes AccChecker to switch to the **MSAA Tree** or **UIA Tree** tab. If an element is highlighted on the **Screen Reader** tab, the corresponding element is highlighted on the **MSAA Tree** or **UIA Tree** tab.</span></span>

<span data-ttu-id="547f9-160">La routine de vérification **Screenreader** sous **consistance** doit être sélectionnée dans l’onglet **vérifications** de l' **onglet lecteur d’écran MSAA** à afficher.</span><span class="sxs-lookup"><span data-stu-id="547f9-160">The **ScreenReader** verification routine under **Consistence** must be selected in the **Verifications** tab for the **MSAA Screen reader tab** to be displayed.</span></span> <span data-ttu-id="547f9-161">De même, la routine de vérification **UiaScreenReader** doit être sélectionnée pour que l’onglet **lecteur d’écran UIA** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="547f9-161">Similarly, the **UiaScreenReader** verification routine must be selected for the **UIA Screen reader** tab to be displayed.</span></span>

<span data-ttu-id="547f9-162">La capture d’écran suivante montre l’onglet lecteur de l’écran UIA avec un exemple de vérification du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="547f9-162">The following screen shot shows the UIA Screen reader tab with a sample verification of Notepad.</span></span>

![accchecker onglet lecteur d’écran affichant les exemples de résultats de la vérification](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a><span data-ttu-id="547f9-164">Onglets d’arborescence MSAA et UIA</span><span class="sxs-lookup"><span data-stu-id="547f9-164">MSAA and UIA Tree Tabs</span></span>

<span data-ttu-id="547f9-165">Si vous exécutez une routine de vérification, AccChecker compile tous les éléments visibles dans la cible de vérification et les affiche hiérarchiquement sous l’onglet de l' **arborescence MSAA** et l’onglet d' **arborescence UIA** . La capture d’écran suivante montre l’onglet d’arborescence MSAA avec la hiérarchie d’éléments pour le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="547f9-165">Running any verification routine causes AccChecker to compile all visible elements in the verification target and display them hierarchically on the **MSAA Tree** tab and the **UIA Tree** tab. The following screen shot shows the MSAA Tree tab with the hierarchy of elements for Notepad.</span></span>

![onglet d’arborescence accchecker MSAA](images/accchecker-tree-tab.png)

## <a name="file-menu"></a><span data-ttu-id="547f9-167">Menu Fichier</span><span class="sxs-lookup"><span data-stu-id="547f9-167">File Menu</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="547f9-168">Menu</span><span class="sxs-lookup"><span data-stu-id="547f9-168">Menu</span></span></th>
<th><span data-ttu-id="547f9-169">Commande</span><span class="sxs-lookup"><span data-stu-id="547f9-169">Command</span></span></th>
<th><span data-ttu-id="547f9-170">Description</span><span class="sxs-lookup"><span data-stu-id="547f9-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="547f9-171"><strong>Fichier</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="547f9-171"><strong>File</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="547f9-172"><strong>Ouvrir</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-172"><strong>Open</strong></span></span></td>
<td><span data-ttu-id="547f9-173">Fournit les options suivantes.</span><span class="sxs-lookup"><span data-stu-id="547f9-173">Provides the following options.</span></span><br/>
<ul>
<li><span data-ttu-id="547f9-174"><strong>Dll de vérification</strong> Ouvre une DLL de vérification.</span><span class="sxs-lookup"><span data-stu-id="547f9-174"><strong>Verifications DLL</strong> Opens a verification DLL.</span></span> <span data-ttu-id="547f9-175">Les vérifications AccChecker natives sont encapsulées dans une DLL autonome (VerificationRoutines.dll).</span><span class="sxs-lookup"><span data-stu-id="547f9-175">Native AccChecker verifications are encapsulated in a standalone DLL (VerificationRoutines.dll).</span></span> <span data-ttu-id="547f9-176">Cette conception permet aux équipes de test de créer leur propre ensemble de vérifications en fonction de la plateforme d’interface utilisateur en cours de test.</span><span class="sxs-lookup"><span data-stu-id="547f9-176">This design allows test teams to create their own set of verifications based on the UI platform being tested.</span></span></li>
<li><span data-ttu-id="547f9-177"><strong>Fichier journal</strong> Vous permet de choisir un fichier journal de vérification à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="547f9-177"><strong>Log file</strong> Lets you choose a verification log file to open.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="547f9-178"><strong>Charger automatiquement les vérifications disponibles</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-178"><strong>Automatically load available verifications</strong></span></span></td>
<td><span data-ttu-id="547f9-179">Charge automatiquement toutes les vérifications AccChecker disponibles.</span><span class="sxs-lookup"><span data-stu-id="547f9-179">Automatically loads all available AccChecker verifications.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="547f9-180"><strong>Enregistrer le journal</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-180"><strong>Save Log</strong></span></span></td>
<td><span data-ttu-id="547f9-181">Enregistrez le journal de vérification au format XML ou sous forme de texte brut.</span><span class="sxs-lookup"><span data-stu-id="547f9-181">Save the verification log as XML or as plain text.</span></span> <span data-ttu-id="547f9-182">Le texte brut est plus lisible.</span><span class="sxs-lookup"><span data-stu-id="547f9-182">Plain text is more readable.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="547f9-183"><strong>Enregistrement de la suppression</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-183"><strong>Save Suppression</strong></span></span></td>
<td><span data-ttu-id="547f9-184">Enregistrez le journal des suppressions au format XML.</span><span class="sxs-lookup"><span data-stu-id="547f9-184">Save the suppression log as XML.</span></span> <span data-ttu-id="547f9-185">Ce fichier spécifie les messages de vérification à ignorer dans les tests de régression.</span><span class="sxs-lookup"><span data-stu-id="547f9-185">This file specifies the verification messages to ignore in regression testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="547f9-186"><strong>Quitter</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-186"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="547f9-187">Ferme l’outil AccChecker.</span><span class="sxs-lookup"><span data-stu-id="547f9-187">Closes the AccChecker tool.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="547f9-188"><strong>Vérifications</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="547f9-188"><strong>Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="547f9-189"><strong>Exécuter maintenant</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-189"><strong>Run Now</strong></span></span></td>
<td><span data-ttu-id="547f9-190">Exécutez les routines de vérification comme spécifié pour la cible de vérification choisie.</span><span class="sxs-lookup"><span data-stu-id="547f9-190">Run the verification routines as specified for the chosen verification target.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="547f9-191"><strong>Activer tout</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-191"><strong>Enable All</strong></span></span></td>
<td><span data-ttu-id="547f9-192">Activez toutes les cases à cocher de la routine de vérification.</span><span class="sxs-lookup"><span data-stu-id="547f9-192">Check all verification routine check boxes.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="547f9-193"><strong>Désactiver tout</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-193"><strong>Disable All</strong></span></span></td>
<td><span data-ttu-id="547f9-194">Désactivez toutes les cases à cocher de la routine de vérification.</span><span class="sxs-lookup"><span data-stu-id="547f9-194">Uncheck all verification routine check boxes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="547f9-195"><strong>Options</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-195"><strong>Options</strong></span></span></td>
<td><span data-ttu-id="547f9-196"><strong>Always On haut</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-196"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="547f9-197">Faites de AccChecker la fenêtre de niveau supérieur dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="547f9-197">Make AccChecker the topmost window in the z-order.</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="547f9-198"><strong>Aide</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="547f9-198"><strong>Help</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="547f9-199"><strong>Aide</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-199"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="547f9-200">Affichez les informations d’aide.</span><span class="sxs-lookup"><span data-stu-id="547f9-200">Display help information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="547f9-201"><strong>À propos de</strong></span><span class="sxs-lookup"><span data-stu-id="547f9-201"><strong>About</strong></span></span></td>
<td><span data-ttu-id="547f9-202">Affichez la version de AccChecker et une adresse de messagerie pour contacter Microsoft sur AccChecker.</span><span class="sxs-lookup"><span data-stu-id="547f9-202">Display the AccChecker version and an email address for contacting Microsoft about AccChecker.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="547f9-203">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="547f9-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="547f9-204">Vérificateur d’accessibilité de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="547f9-204">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





