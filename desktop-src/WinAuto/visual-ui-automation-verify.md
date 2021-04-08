---
title: Vérification de l’interface utilisateur Visual Automation
description: Vérification de l’interface utilisateur de Visual Automation (Visual UIA Verify) est un Windows \ 32 ; Pilote d’interface graphique utilisateur pour la bibliothèque de test UIA conçue pour le test manuel de l’Automation d’interface utilisateur.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e224a52d243427af86c6cd27a3add3be03d9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675381"
---
# <a name="visual-ui-automation-verify"></a><span data-ttu-id="dce86-103">Vérification de l’interface utilisateur Visual Automation</span><span class="sxs-lookup"><span data-stu-id="dce86-103">Visual UI Automation Verify</span></span>

<span data-ttu-id="dce86-104">Vérification de l’interface utilisateur de Visual Automation (Visual UIA Verify) est un pilote GUI Windows pour la bibliothèque de test UIA qui est conçu pour les tests manuels d’UI Automation.</span><span class="sxs-lookup"><span data-stu-id="dce86-104">Visual UI Automation Verify (Visual UIA Verify) is a Windows GUI driver for the UIA Test Library that is designed for manual testing of UI automation.</span></span> <span data-ttu-id="dce86-105">Il fournit une interface à la fonctionnalité de bibliothèque de tests UIA qui élimine la surcharge de codage d’un outil en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="dce86-105">It provides an interface to UIA Test Library functionality that eliminates the coding overhead of a command-line tool.</span></span>

-   [<span data-ttu-id="dce86-106">Commandes de menu</span><span class="sxs-lookup"><span data-stu-id="dce86-106">Menu Commands</span></span>](#menu-commands)
-   [<span data-ttu-id="dce86-107">Volets fonctionnels</span><span class="sxs-lookup"><span data-stu-id="dce86-107">Functional Panes</span></span>](#functional-panes)
    -   [<span data-ttu-id="dce86-108">Volet de l’arborescence des éléments Automation</span><span class="sxs-lookup"><span data-stu-id="dce86-108">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
    -   [<span data-ttu-id="dce86-109">Volet tests</span><span class="sxs-lookup"><span data-stu-id="dce86-109">Tests Pane</span></span>](#tests-pane)
    -   [<span data-ttu-id="dce86-110">Volet Résultats des tests</span><span class="sxs-lookup"><span data-stu-id="dce86-110">Test Results Pane</span></span>](#test-results-pane)
    -   [<span data-ttu-id="dce86-111">Volet Propriétés</span><span class="sxs-lookup"><span data-stu-id="dce86-111">Properties Pane</span></span>](#properties-pane)

<span data-ttu-id="dce86-112">Visual UIA Verify ne prend en charge que le journal XML de vérification UIA (WUIALoggerXml.dll) en mode natif.</span><span class="sxs-lookup"><span data-stu-id="dce86-112">Visual UIA Verify supports only the UIA Verify XML logger (WUIALoggerXml.dll) natively.</span></span> <span data-ttu-id="dce86-113">Les transformations XML sélectionnables par l’utilisateur sont incorporées dans Visual UIA Verify pour présenter diverses vues du rapport d’enregistreur XML dans le volet **résultats des tests** .</span><span class="sxs-lookup"><span data-stu-id="dce86-113">User-selectable XML transformations are incorporated into Visual UIA Verify to present various views of the XML logger report in the **Test Results** pane.</span></span>

<span data-ttu-id="dce86-114">Par défaut, Visual UIA Verify charge le fournisseur UI Automation côté client fourni avec la version d’origine d’UI Automation.</span><span class="sxs-lookup"><span data-stu-id="dce86-114">By default, Visual UIA Verify loads the UI Automation client-side provider that shipped with the original release of UI Automation.</span></span> <span data-ttu-id="dce86-115">Vous pouvez choisir de ne pas charger ce fournisseur en ajoutant **/NOCLIENTSIDEPROVIDER** dans l’option de ligne de commande de VisualUIVerifyNative.exe.</span><span class="sxs-lookup"><span data-stu-id="dce86-115">You can choose not to load this provider by adding **/NOCLIENTSIDEPROVIDER** in the command-line option of VisualUIVerifyNative.exe.</span></span>

<span data-ttu-id="dce86-116">La capture d’écran suivante montre les principales zones fonctionnelles de l’interface utilisateur vérification de Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="dce86-116">The following screen shot shows the main functional areas of the Visual UIA Verify user interface.</span></span>

![principales zones fonctionnelles de l’interface utilisateur vérification de Visual UIA](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a><span data-ttu-id="dce86-118">Commandes de menu</span><span class="sxs-lookup"><span data-stu-id="dce86-118">Menu Commands</span></span>

<span data-ttu-id="dce86-119">Le tableau suivant décrit les commandes du menu vérification de Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="dce86-119">The following table describes the commands in the Visual UIA Verify menu.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dce86-120">Menu</span><span class="sxs-lookup"><span data-stu-id="dce86-120">Menu</span></span></th>
<th><span data-ttu-id="dce86-121">Commande</span><span class="sxs-lookup"><span data-stu-id="dce86-121">Command</span></span></th>
<th><span data-ttu-id="dce86-122">Description</span><span class="sxs-lookup"><span data-stu-id="dce86-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dce86-123"><strong>File</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-123"><strong>File</strong></span></span></td>
<td><span data-ttu-id="dce86-124"><strong>Quitter</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-124"><strong>Exit</strong></span></span></td>
<td><span data-ttu-id="dce86-125">Quittez la vérification de Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="dce86-125">Exit Visual UIA Verify.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dce86-126"><strong>Afficher</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-126"><strong>View</strong></span></span></td>
<td><span data-ttu-id="dce86-127"><strong>Mettre en surbrillance</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-127"><strong>Highlighting</strong></span></span></td>
<td><span data-ttu-id="dce86-128">Mettez en surbrillance le rectangle englobant de l’élément sélectionné dans le volet de l' <strong>arborescence éléments Automation</strong> .</span><span class="sxs-lookup"><span data-stu-id="dce86-128">Highlight the bounding rectangle of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="dce86-129">Les options suivantes sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="dce86-129">The following options are available.</span></span>
<ul>
<li><span data-ttu-id="dce86-130"><strong>Rectangle</strong>: ligne rouge pleine.</span><span class="sxs-lookup"><span data-stu-id="dce86-130"><strong>Rectangle</strong>—A solid red line.</span></span></li>
<li><span data-ttu-id="dce86-131"><strong>Rectangle de fondu</strong>: ligne rouge pleine qui disparaît après quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="dce86-131"><strong>Fading Rectangle</strong>—A solid red line that disappears after a few seconds.</span></span></li>
<li><span data-ttu-id="dce86-132"><strong>Rayons et rectangle</strong>: trait rouge plein avec des lignes de surbrillance bleue supplémentaires qui rayonnent à partir de chaque angle du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="dce86-132"><strong>Rays and Rectangle</strong>—A solid red line with additional blue highlight lines that radiate from each corner of the bounding rectangle.</span></span></li>
<li><span data-ttu-id="dce86-133"><strong>None</strong>: aucune mise en surbrillance visible.</span><span class="sxs-lookup"><span data-stu-id="dce86-133"><strong>None</strong>—No visible highlight.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="dce86-134"><strong>Arborescence des éléments d’automatisation</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dce86-134"><strong>Automation Elements Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="dce86-135"><strong>Actualiser l’élément sélectionné</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-135"><strong>Refresh Selected Element</strong></span></span></td>
<td><span data-ttu-id="dce86-136">Actualise les enfants de l’élément sélectionné dans le volet d' <strong>arborescence éléments Automation</strong> .</span><span class="sxs-lookup"><span data-stu-id="dce86-136">Refresh the children of the selected element in the <strong>Automation Elements Tree</strong> pane.</span></span> <span data-ttu-id="dce86-137">La liste d’éléments est statique et n’est pas actualisée dynamiquement (automatiquement) si l’arborescence d’éléments change.</span><span class="sxs-lookup"><span data-stu-id="dce86-137">The list of elements is static and does not refresh dynamically (automatically) if the element tree changes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dce86-138"><strong>Navigation</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-138"><strong>Navigation</strong></span></span></td>
<td><span data-ttu-id="dce86-139">Naviguez dans la hiérarchie de l’arborescence d’éléments jusqu’à l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="dce86-139">Navigate through the element tree hierarchy to one of the following elements.</span></span>
<ul>
<li><span data-ttu-id="dce86-140"><strong>Parent</strong>: accéder à l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="dce86-140"><strong>Parent</strong>—Go to parent element.</span></span></li>
<li><span data-ttu-id="dce86-141"><strong>Premier enfant</strong>: accéder au premier élément enfant.</span><span class="sxs-lookup"><span data-stu-id="dce86-141"><strong>First Child</strong>—Go to first child element.</span></span></li>
<li><span data-ttu-id="dce86-142"><strong>Frère suivant</strong>: accédez au premier élément frère.</span><span class="sxs-lookup"><span data-stu-id="dce86-142"><strong>Next Sibling</strong>—Go to first sibling element.</span></span></li>
<li><span data-ttu-id="dce86-143"><strong>Frère précédent</strong>: accède à l’élément frère précédent.</span><span class="sxs-lookup"><span data-stu-id="dce86-143"><strong>Previous Sibling</strong>—Go to previous sibling element.</span></span></li>
<li><span data-ttu-id="dce86-144"><strong>Dernier enfant</strong>: accéder au dernier élément enfant.</span><span class="sxs-lookup"><span data-stu-id="dce86-144"><strong>Last Child</strong>—Go to last child element.</span></span></li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="dce86-145"><strong>Mode</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dce86-145"><strong>Mode</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="dce86-146"><strong>Always On haut</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-146"><strong>Always On Top</strong></span></span></td>
<td><span data-ttu-id="dce86-147">La fenêtre de vérification du décodeur Visual UIA reste en haut de l’ordre de plan du bureau.</span><span class="sxs-lookup"><span data-stu-id="dce86-147">The Visual UIA Verify window remains at the top of the desktop z-order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dce86-148"><strong>Mode sensitif (utilisez Ctrl)</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-148"><strong>Hover Mode (Use Ctrl)</strong></span></span></td>
<td><span data-ttu-id="dce86-149">Quand la touche CTRL est enfoncée, l’élément sous le curseur de la souris est identifié comme étant l’élément concerné.</span><span class="sxs-lookup"><span data-stu-id="dce86-149">When the Ctrl key is pressed, the element under the mouse cursor is identified as the element of interest.</span></span> <span data-ttu-id="dce86-150">Le volet d' <strong>arborescence éléments Automation</strong> est actualisé et l’élément correspondant dans la liste d’éléments est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="dce86-150">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dce86-151"><strong>Focus, suivi</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-151"><strong>Focus Tracking</strong></span></span></td>
<td><span data-ttu-id="dce86-152">Au fur et à mesure que le focus change, l’élément ayant le focus est identifié comme l’élément d’intérêt.</span><span class="sxs-lookup"><span data-stu-id="dce86-152">As the focus changes, the element with the focus is identified as the element of interest.</span></span> <span data-ttu-id="dce86-153">Le volet d' <strong>arborescence éléments Automation</strong> est actualisé et l’élément correspondant dans la liste d’éléments est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="dce86-153">The <strong>Automation Elements Tree</strong> pane is refreshed and the corresponding item in the element list is highlighted.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="dce86-154"><strong>Tests</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="dce86-154"><strong>Tests</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="dce86-155"><strong>Aller à gauche</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-155"><strong>Go Left</strong></span></span></td>
<td><span data-ttu-id="dce86-156">Déplacer un nœud vers la gauche dans l’arborescence des <strong>tests</strong> .</span><span class="sxs-lookup"><span data-stu-id="dce86-156">Move one node left in the <strong>Tests</strong> tree.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dce86-157"><strong>Monter</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-157"><strong>Go Up</strong></span></span></td>
<td><span data-ttu-id="dce86-158">Déplacer un nœud vers le haut dans l’arborescence des <strong>tests</strong> .</span><span class="sxs-lookup"><span data-stu-id="dce86-158">Move one node up in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="dce86-159"><strong>Descendre</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-159"><strong>Go Down</strong></span></span></td>
<td><span data-ttu-id="dce86-160">Déplacer un nœud vers le dessous dans l’arborescence des <strong>tests</strong> .</span><span class="sxs-lookup"><span data-stu-id="dce86-160">Move one node down in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dce86-161"><strong>Aller à droite</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-161"><strong>Go Right</strong></span></span></td>
<td><span data-ttu-id="dce86-162">Déplacer un nœud vers la droite dans l’arborescence <strong>tests</strong> .</span><span class="sxs-lookup"><span data-stu-id="dce86-162">Move one node right in the <strong>Tests</strong> tree.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="dce86-163"><strong>Exécuter le ou les tests sélectionnés sur l’élément sélectionné</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-163"><strong>Run Selected Test(s) On Selected Element</strong></span></span></td>
<td><span data-ttu-id="dce86-164">Exécuter les tests sélectionnés à partir de l’arborescence <strong>tests</strong> sur l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dce86-164">Run the selected tests from the <strong>Tests</strong> tree on the selected element.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="dce86-165"><strong>Filtrer les problèmes connus</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-165"><strong>Filter Known Problems</strong></span></span></td>
<td><span data-ttu-id="dce86-166">Filtrez les bogues UI Automation connus des résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="dce86-166">Filter known UI Automation bugs from the test results.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="dce86-167"><strong>Aide</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-167"><strong>Help</strong></span></span></td>
<td><span data-ttu-id="dce86-168"><strong>À propos de la vérification de l’interface utilisateur Visual Automation</strong></span><span class="sxs-lookup"><span data-stu-id="dce86-168"><strong>About Visual UI Automation Verify</strong></span></span></td>
<td><span data-ttu-id="dce86-169">Affichez la version du logiciel et les informations de copyright pour Visual UIA Verify.</span><span class="sxs-lookup"><span data-stu-id="dce86-169">Display the software version and copyright information for Visual UIA Verify.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a><span data-ttu-id="dce86-170">Volets fonctionnels</span><span class="sxs-lookup"><span data-stu-id="dce86-170">Functional Panes</span></span>

<span data-ttu-id="dce86-171">Cette section décrit les volets fonctionnels de l’interface utilisateur vérification de Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="dce86-171">This section describes the functional panes in the Visual UIA Verify user interface.</span></span>

-   [<span data-ttu-id="dce86-172">Volet de l’arborescence des éléments Automation</span><span class="sxs-lookup"><span data-stu-id="dce86-172">Automation Elements Tree Pane</span></span>](#automation-elements-tree-pane)
-   [<span data-ttu-id="dce86-173">Volet tests</span><span class="sxs-lookup"><span data-stu-id="dce86-173">Tests Pane</span></span>](#tests-pane)
-   [<span data-ttu-id="dce86-174">Volet Résultats des tests</span><span class="sxs-lookup"><span data-stu-id="dce86-174">Test Results Pane</span></span>](#test-results-pane)
-   [<span data-ttu-id="dce86-175">Volet Propriétés</span><span class="sxs-lookup"><span data-stu-id="dce86-175">Properties Pane</span></span>](#properties-pane)

### <a name="automation-elements-tree-pane"></a><span data-ttu-id="dce86-176">Volet de l’arborescence des éléments Automation</span><span class="sxs-lookup"><span data-stu-id="dce86-176">Automation Elements Tree Pane</span></span>

<span data-ttu-id="dce86-177">Le volet d' **arborescence éléments Automation** contient un instantané hiérarchique des objets d’élément Automation qui sont disponibles pour le test.</span><span class="sxs-lookup"><span data-stu-id="dce86-177">The **Automation Elements Tree** pane contains a hierarchical snapshot of automation element objects that are available for testing.</span></span> <span data-ttu-id="dce86-178">L’élément supérieur dans l’arborescence représente le bureau.</span><span class="sxs-lookup"><span data-stu-id="dce86-178">The top element in the tree represents the desktop.</span></span>

<span data-ttu-id="dce86-179">Cette vue est une collection statique qui est compilée lors du démarrage de la vérification de Visual UIA.</span><span class="sxs-lookup"><span data-stu-id="dce86-179">This view is a static collection that is compiled when Visual UIA Verify starts.</span></span> <span data-ttu-id="dce86-180">Pour actualiser la vue sur le nœud sélectionné, utilisez la commande de menu **Actualiser l’élément sélectionné** ou le bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="dce86-180">To refresh the view at the selected node, use the **Refresh Selected Element** menu command or toolbar button.</span></span>

<span data-ttu-id="dce86-181">La capture d’écran suivante montre le volet d' **arborescence éléments Automation** .</span><span class="sxs-lookup"><span data-stu-id="dce86-181">The following screen shot shows the **Automation Elements Tree** pane.</span></span>

![volet de l’arborescence des éléments Automation de la vérification de Visual UIA](images/automation-elements-tree-pane.png)

<span data-ttu-id="dce86-183">Un nœud grisé (non disponible) dans l' **arborescence des éléments d’automatisation** indique que l’élément est membre de la vue brute UI Automation, mais ne remplit pas les conditions nécessaires pour être considéré comme un membre de l’affichage de contenu ou de l’affichage de contrôle.</span><span class="sxs-lookup"><span data-stu-id="dce86-183">A dimmed (unavailable) node in the **Automation Elements Tree** indicates that the element is a member of the UI Automation raw view, but does not meet the conditions necessary to be considered a member of the content view or control view.</span></span> <span data-ttu-id="dce86-184">Toutefois, l’élément peut toujours être testé à partir de vérification de l’interface utilisateur de Visual Automation.</span><span class="sxs-lookup"><span data-stu-id="dce86-184">However, the element can still be tested from Visual UI Automation Verify.</span></span> <span data-ttu-id="dce86-185">Pour plus d’informations, consultez la [vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dce86-185">For more information, see the [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="dce86-186">Les commandes disponibles à partir de la barre d’outils de l' **arborescence des éléments Automation** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dce86-186">Commands available from the **Automation Elements Tree** toolbar include:</span></span>

-   <span data-ttu-id="dce86-187">**Actualiser**: actualise le nœud sélectionné et ses enfants.</span><span class="sxs-lookup"><span data-stu-id="dce86-187">**Refresh**—Refresh the selected node and its children.</span></span> <span data-ttu-id="dce86-188">Cette commande n’actualise pas l’intégralité de l’arborescence des éléments, sauf si le nœud racine est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dce86-188">This command does not refresh the entire element tree unless the root node is selected.</span></span>
-   <span data-ttu-id="dce86-189">**Parent (CTRL + MAJ + F6)**: accéder au parent du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-189">**Parent (Ctrl+Shift+F6)**—Go to parent of the current node.</span></span>
-   <span data-ttu-id="dce86-190">**Premier enfant (Ctrl + Maj + F7)**: accéder au premier enfant du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-190">**First Child (Ctrl+Shift+F7)**—Go to first child of the current node..</span></span>
-   <span data-ttu-id="dce86-191">**Frère suivant (Ctrl + Maj + F8)**: accéder à l’enfant frère suivant du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-191">**Next Sibling (Ctrl+Shift+F8)**—Go to next sibling child of the current node.</span></span>
-   <span data-ttu-id="dce86-192">**Frère précédent (Ctrl + Maj + F9)**: accéder au frère précédent du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-192">**Previous Sibling (Ctrl+Shift+F9)**—Go to previous sibling of the current node.</span></span>
-   <span data-ttu-id="dce86-193">**Dernier enfant (CTRL + MAJ + F10)**: accéder au dernier enfant du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-193">**Last Child (Ctrl+Shift+F10)**—Go to last child of the current node.</span></span>
-   <span data-ttu-id="dce86-194">**Focus Tracking**: active ou désactive la sélection de nœud en fonction du suivi du focus.</span><span class="sxs-lookup"><span data-stu-id="dce86-194">**Focus Tracking**—Toggle node selection on or off based on focus tracking.</span></span>

### <a name="tests-pane"></a><span data-ttu-id="dce86-195">Volet tests</span><span class="sxs-lookup"><span data-stu-id="dce86-195">Tests Pane</span></span>

<span data-ttu-id="dce86-196">Le **volet tests** contient une liste de tests UI Automation organisés par type de test (**élément Automation**, **contrôle** et **modèle**) et priorité (**vérification de build**, **priorité 0**, **priorité 1**, **priorité 2** et **priorité 3**).</span><span class="sxs-lookup"><span data-stu-id="dce86-196">The **Tests** pane contains a list of UI Automation tests organized by test type (**Automation Element**, **Control**, and **Pattern**) and priority (**Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, and **Priority 3**).</span></span> <span data-ttu-id="dce86-197">Cette liste est générée en fonction du type de contrôle de l’élément sélectionné dans le volet d' **arborescence éléments Automation** .</span><span class="sxs-lookup"><span data-stu-id="dce86-197">This list is generated based on the control type of the selected element in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="dce86-198">Pour plus d'informations, consultez [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dce86-198">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

<span data-ttu-id="dce86-199">La capture d’écran suivante montre le volet **tests** .</span><span class="sxs-lookup"><span data-stu-id="dce86-199">The following screen shot shows the **Tests** pane.</span></span>

![volet de test](images/test-pane.png)

<span data-ttu-id="dce86-201">Les commandes disponibles à partir de la barre d’outils **tests** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dce86-201">Commands available from the **Tests** toolbar include:</span></span>

-   <span data-ttu-id="dce86-202">**Afficher**: spécifie les tests UI Automation à afficher. autrement dit, affichez tous les tests ou uniquement les tests adaptés au type de contrôle de l’élément sélectionné dans l' **arborescence des éléments Automation** (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="dce86-202">**Show**—Specifies the UI Automation tests to display; that is, display all tests or only tests suited to the control type of the selected element in the **Automation Elements Tree** (default).</span></span>
-   <span data-ttu-id="dce86-203">**Type**: spécifie les types de test à afficher : **élément Automation**, **modèle** ou **contrôle**.</span><span class="sxs-lookup"><span data-stu-id="dce86-203">**Type**—Specifies the test types to display: **Automation Element**, **Pattern**, or **Control**.</span></span>
-   <span data-ttu-id="dce86-204">**Priorités**: spécifie les priorités de test à afficher : **vérification de build**, **priorité 0**, **priorité 1**, **priorité 2** ou **priorité 3**.</span><span class="sxs-lookup"><span data-stu-id="dce86-204">**Priorities**—Specifies the test priorities to display: **Build Verification**, **Priority 0**, **Priority 1**, **Priority 2**, or **Priority 3**.</span></span>
-   <span data-ttu-id="dce86-205">**Aller à gauche**: accéder au parent du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-205">**Go Left**—Go to the parent of the current node.</span></span>
-   <span data-ttu-id="dce86-206">**Monter**: accédez au frère précédent du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-206">**Go Up**—Go to the previous sibling of the current node.</span></span>
-   <span data-ttu-id="dce86-207">**Descendre**: accédez au frère suivant du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-207">**Go Down**—Go to the next sibling of the current node.</span></span>
-   <span data-ttu-id="dce86-208">**Aller à droite**: accède au premier enfant du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="dce86-208">**Go Right**—Go to the first child of the current node.</span></span>
-   <span data-ttu-id="dce86-209">**Exécuter le (s) test (s) sélectionné (s)**: exécute les tests sur l’élément sélectionné dans l' **arborescence des éléments Automation**.</span><span class="sxs-lookup"><span data-stu-id="dce86-209">**Run Selected Test(s)**—Runs the tests on the element selected in the **Automation Elements Tree**.</span></span>

### <a name="test-results-pane"></a><span data-ttu-id="dce86-210">Volet Résultats des tests</span><span class="sxs-lookup"><span data-stu-id="dce86-210">Test Results Pane</span></span>

<span data-ttu-id="dce86-211">Le volet **résultats des tests** contient la fonctionnalité de vérification de la journalisation de vérification de visualable.</span><span class="sxs-lookup"><span data-stu-id="dce86-211">The **Test Results** pane contains the Visual UIA Verify logging functionality.</span></span> <span data-ttu-id="dce86-212">La capture d’écran suivante montre le volet **résultats des tests** .</span><span class="sxs-lookup"><span data-stu-id="dce86-212">The following screen shot shows the **Test Results** pane.</span></span>

![volet résultats des tests](images/test-results-pane.png)

<span data-ttu-id="dce86-214">Les commandes disponibles dans la barre d’outils **résultats des tests** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dce86-214">Commands available from the **Tests Results** toolbar include:</span></span>

-   <span data-ttu-id="dce86-215">**Précédent**: page précédente dans l’historique d’affichage du rapport.</span><span class="sxs-lookup"><span data-stu-id="dce86-215">**Back**—Page backward in report viewing history.</span></span>
-   <span data-ttu-id="dce86-216">**Transférer**: page suivante dans l’historique d’affichage du rapport.</span><span class="sxs-lookup"><span data-stu-id="dce86-216">**Forward**—Page forward in report viewing history.</span></span>
-   <span data-ttu-id="dce86-217">**Global**: affiche un résumé des résultats des tests (**réussite**, **échec** et **erreur inattendue**).</span><span class="sxs-lookup"><span data-stu-id="dce86-217">**Overall**—Displays a summary of the test results (**Passed**, **Failed**, and **Unexpected Error**).</span></span> <span data-ttu-id="dce86-218">Le résultat du test est lié à l’affichage **tous les résultats** .</span><span class="sxs-lookup"><span data-stu-id="dce86-218">The test result is linked to the **All Results** view.</span></span> <span data-ttu-id="dce86-219">La commande **globale** affiche un tableau comme celui qui suit.</span><span class="sxs-lookup"><span data-stu-id="dce86-219">The **Overall** command displays a table like the following one.</span></span>

    ![Tableau des résultats des tests globaux](images/overall-test-results.png)

-   <span data-ttu-id="dce86-221">**Tous les résultats**: affiche un journal détaillé pour chaque résultat de test, comme indiqué dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="dce86-221">**All Results**— Displays a detailed log for each test result, as shown in the following tables.</span></span>

    ![exemple de journaliser les détails des résultats de l’affichage tous les résultats](images/all-results-log.png)

    <span data-ttu-id="dce86-223">Le nom du test dans le tableau **tous les résultats** est lié à une description de cas de test pour l’élément, comme dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dce86-223">The test name in the **All Results** table is linked to a test case description for the element, as in the following table.</span></span>

    ![Détails du cas de test](images/test-case-detail.png)

-   <span data-ttu-id="dce86-225">**Full log (journal complet**) : affiche une autre vue du journal détaillé pour chaque résultat de test, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="dce86-225">**Full Log**—Displays an alternate view of the detailed log for each test result, as shown in the following screen shot.</span></span>

    ![autre vue d’un cas de test, détails](images/alt-view-of-test-case-detail.png)

-   <span data-ttu-id="dce86-227">**XML**— affiche le code XML brut généré par l’enregistreur d’événements XML.</span><span class="sxs-lookup"><span data-stu-id="dce86-227">**XML**—Displays the raw XML generated by the XML logger.</span></span>
-   <span data-ttu-id="dce86-228">Recherche **rapide**: recherche en texte simple de la vue actuelle dans le volet **résultats des tests** .</span><span class="sxs-lookup"><span data-stu-id="dce86-228">**Quick Find**—Simple text search of the current view in the **Test Results** pane.</span></span>
-   <span data-ttu-id="dce86-229">**Ouvrir dans une nouvelle fenêtre**: ouvre la vue actuelle dans une nouvelle instance d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="dce86-229">**Open in New Window**—Opens the current view in a new instance of Internet Explorer.</span></span>

### <a name="properties-pane"></a><span data-ttu-id="dce86-230">Volet Propriétés</span><span class="sxs-lookup"><span data-stu-id="dce86-230">Properties Pane</span></span>

<span data-ttu-id="dce86-231">Le volet **Propriétés** contient une liste de propriétés UI Automation et de valeurs de propriété organisées par type de propriété : **accessibilité générale**, **identification**, **modèles** (modèles de contrôle), **État** et **visibilité**.</span><span class="sxs-lookup"><span data-stu-id="dce86-231">The **Properties** pane contains a list of UI Automation properties and property values organized by property type: **General Accessibility**, **Identification**, **Patterns** (control patterns), **State**, and **Visibility**.</span></span> <span data-ttu-id="dce86-232">Les valeurs de propriété sont renseignées dynamiquement en fonction du type de contrôle de l’objet sélectionné dans le volet d' **arborescence éléments Automation** .</span><span class="sxs-lookup"><span data-stu-id="dce86-232">The property values are dynamically populated based on the control type of the object selected in the **Automation Elements Tree** pane.</span></span> <span data-ttu-id="dce86-233">La capture d’écran suivante montre le volet **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="dce86-233">The following screen shot shows the **Properties** pane.</span></span>

![volet Propriétés](images/properties-pane.png)

<span data-ttu-id="dce86-235">Si le contrôle sélectionné prend en charge un modèle de contrôle spécifique, Visual UIA Verify offre la possibilité d’appeler des méthodes prises en charge par ce modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="dce86-235">If the selected control supports a specific control pattern, Visual UIA Verify provides the ability to call methods that are supported by that control pattern.</span></span> <span data-ttu-id="dce86-236">Par exemple, le [type de contrôle Window](uiauto-supportwindowcontroltype.md) prend en charge le [modèle de contrôle Window](uiauto-implementingwindow.md), qui a une méthode [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) qui peut être appelée à partir du volet **Propriétés** , comme indiqué dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="dce86-236">For example, the [Window control type](uiauto-supportwindowcontroltype.md) supports the [Window control pattern](uiauto-implementingwindow.md), which has a [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) method that can be invoked from the **Properties** pane, as shown in the following screen shot.</span></span> <span data-ttu-id="dce86-237">Pour plus d'informations, consultez [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span><span class="sxs-lookup"><span data-stu-id="dce86-237">For more information, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

![méthode Close du modèle de contrôle Window appelée à partir du volet Propriétés](images/close-invoked-from-properties-pane.png)

<span data-ttu-id="dce86-239">Les commandes disponibles à partir de la barre d’outils **Propriétés** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dce86-239">Commands available from the **Properties** toolbar include:</span></span>

-   <span data-ttu-id="dce86-240">**Actualiser**: actualise l’arborescence des **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="dce86-240">**Refresh**—Refresh the **Properties** tree.</span></span>
-   <span data-ttu-id="dce86-241">**Développer tout**: développe tous les nœuds dans l’arborescence des **Propriétés** .</span><span class="sxs-lookup"><span data-stu-id="dce86-241">**Expand All**—Expands all nodes in the **Properties** tree.</span></span>

 

 




