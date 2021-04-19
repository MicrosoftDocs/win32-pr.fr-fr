---
title: Glossaire (concepts de base de la conception)
description: Glossaire des termes utilisés dans les instructions d’expérience utilisateur pour les applications de bureau Windows.
ms.assetid: 9f35f9be-6165-4d98-a2e6-26fb4fc91eae
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3009940612d0b42ae8ee225e8db59ebabdbf35fa
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106527268"
---
# <a name="glossary-design-basics"></a><span data-ttu-id="e6b1b-103">Glossaire (concepts de base de la conception)</span><span class="sxs-lookup"><span data-stu-id="e6b1b-103">Glossary (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="e6b1b-104">Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="e6b1b-105">La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="e6b1b-106">[A](#alink) \| [B](#b) \| [C](#c) \| [D](#d) \| [e](#e) \| [F](#f) \| [G](#g) \| [H](#h) \| [I](#i) \| [J](#j) \| [K](#k) \| [L](#l) \| [M](#m)\|</span><span class="sxs-lookup"><span data-stu-id="e6b1b-106">[A](#alink) \| [B](#b) \| [C](#c) \| [D](#d) \| [E](#e) \| [F](#f) \| [G](#g) \| [H](#h) \| [I](#i) \| [J](#j) \| [K](#k) \| [L](#l) \| [M](#m) \|</span></span>

<span data-ttu-id="e6b1b-107">[N](#n) \| [O](#o) \| [P](#p) \| [Q](#q) \| [R](#r) \| [](#s) \| [T](#t) \| [U](#u) \| [V](#v) \| [W](#w) \| [X](#x) \| [Y](#y) \| [Z](#z)</span><span class="sxs-lookup"><span data-stu-id="e6b1b-107">[N](#n) \| [O](#o) \| [P](#p) \| [Q](#q) \| [R](#r) \| [S](#s) \| [T](#t) \| [U](#u) \| [V](#v) \| [W](#w) \| [X](#x) \| [Y](#y) \| [Z](#z)</span></span>

## <a name=""></a><span data-ttu-id="e6b1b-108"><a name="alink">A</a></span><span class="sxs-lookup"><span data-stu-id="e6b1b-108"><a name="alink">A</a></span></span>

<span data-ttu-id="e6b1b-109">**Boîte à propos**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-109">**About box**</span></span>

<span data-ttu-id="e6b1b-110">Boîte de dialogue fournissant des informations générales sur le programme, telles que l’identification de la version, le Copyright, les contrats de licence et les moyens d’accéder au support technique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-110">A dialog box providing general program information, such as version identification, copyright, licensing agreements, and ways to access technical support.</span></span>

<span data-ttu-id="e6b1b-111">**au-dessus du pli**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-111">**above the fold**</span></span>

<span data-ttu-id="e6b1b-112">Métaphore de la disposition d’écran tirée du journal journalisme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-112">A screen layout metaphor taken from newspaper journalism.</span></span> <span data-ttu-id="e6b1b-113">Le contenu au-dessus de la pliure du journal doit être particulièrement attrayant pour les ventes.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-113">The content above the fold of the newspaper must be particularly engaging to spur sales.</span></span> <span data-ttu-id="e6b1b-114">De même, dans la disposition de l’écran, le contenu le plus important doit être visible sans défilement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-114">Similarly, in screen layout, the most important content must be visible without scrolling.</span></span> <span data-ttu-id="e6b1b-115">Les utilisateurs doivent être motivés à prendre le temps de faire défiler le contenu qu’ils rencontrent initialement « au-dessus du pli ».</span><span class="sxs-lookup"><span data-stu-id="e6b1b-115">Users must be motivated to take the time to scroll past the content they encounter initially "above the fold."</span></span>

<span data-ttu-id="e6b1b-116">**clé d’accès**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-116">**access key**</span></span>

<span data-ttu-id="e6b1b-117">Touche alphanumérique qui, lorsqu’elle est combinée avec la touche Alt, active un contrôle.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-117">An alphanumeric key that, when combined with the Alt key, activates a control.</span></span> <span data-ttu-id="e6b1b-118">Les touches d’accès sont indiquées par un soulignement de l’un des caractères de l’étiquette du contrôle.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-118">Access keys are indicated by underlining one of the characters in the control's label.</span></span> <span data-ttu-id="e6b1b-119">Par exemple, en appuyant sur Alt + O, vous activez un contrôle dont l’étiquette est « Open » et dont la clé d’accès est « O ».</span><span class="sxs-lookup"><span data-stu-id="e6b1b-119">For example, pressing Alt+O activates a control whose label is "Open" and whose assigned access key is "O".</span></span> <span data-ttu-id="e6b1b-120">Les clés d’accès ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-120">Access keys aren't case sensitive.</span></span> <span data-ttu-id="e6b1b-121">L’effet de l’activation d’un contrôle dépend du type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-121">The effect of activating a control depends on the type of control.</span></span>

<span data-ttu-id="e6b1b-122">Contrairement aux touches de raccourci, qui sont principalement destinées aux utilisateurs expérimentés, les clés d’accès sont conçues pour améliorer l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-122">In contrast to shortcut keys, which are intended mostly for advanced users, access keys are designed to improve accessibility.</span></span> <span data-ttu-id="e6b1b-123">Étant donné qu’elles sont documentées directement dans l’interface utilisateur proprement dite, elles ne peuvent pas toujours être affectées de manière cohérente et ne sont pas destinées à être mémorisées.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-123">Because they are documented directly within the user interface (UI) itself, they can't always be assigned consistently and they aren't intended to be memorized.</span></span>

<span data-ttu-id="e6b1b-124">**moniteur actif**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-124">**active monitor**</span></span>

<span data-ttu-id="e6b1b-125">Analyse où le programme actif est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-125">The monitor where the active program is running.</span></span>

<span data-ttu-id="e6b1b-126">**barre d’adresses**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-126">**address bar**</span></span>

<span data-ttu-id="e6b1b-127">Élément de navigation, généralement apparaissant en haut d’une fenêtre, qui affiche et permet aux utilisateurs de modifier leur emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-127">A navigational element, usually appearing at the top of a window, that displays, and allows users to change, their current location.</span></span> <span data-ttu-id="e6b1b-128">Voir aussi : [barre de navigation](#b).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-128">See also: [breadcrumb bar](#b).</span></span>

<span data-ttu-id="e6b1b-129">**offre**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-129">**affordance**</span></span>

<span data-ttu-id="e6b1b-130">Propriétés visuelles d’un objet qui indiquent comment il peut être utilisé ou traité.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-130">Visual properties of an object that indicate how it can be used or acted on.</span></span> <span data-ttu-id="e6b1b-131">Par exemple, les boutons de commande ont l’apparence visuelle des boutons réels, suggérant un push ou un clic.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-131">For example, command buttons have the visual appearance of real-world buttons, suggesting pushing or clicking.</span></span>

<span data-ttu-id="e6b1b-132">**application**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-132">**application**</span></span>

<span data-ttu-id="e6b1b-133">Programme utilisé pour effectuer un ensemble connexe de tâches utilisateur ; souvent relativement complexes et sophistiqués.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-133">A program used to perform a related set of user tasks; often relatively complex and sophisticated.</span></span> <span data-ttu-id="e6b1b-134">Voir aussi : [programme](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-134">See also: [program](#p).</span></span>

<span data-ttu-id="e6b1b-135">**clé d’application**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-135">**application key**</span></span>

<span data-ttu-id="e6b1b-136">Touche du clavier avec un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-136">A keyboard key with a context menu graphic on it.</span></span> <span data-ttu-id="e6b1b-137">Cette clé est utilisée pour afficher le menu contextuel de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-137">This key is used to display the context menu for the selected item.</span></span>

<span data-ttu-id="e6b1b-138">**menu de l’application**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-138">**application menu**</span></span>

<span data-ttu-id="e6b1b-139">Contrôle qui présente un menu de commandes qui impliquent d’effectuer des opérations dans ou avec un document ou un espace de travail, tel que des commandes associées aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-139">A control that presents a menu of commands that involve doing something to or with a document or workspace, such as file-related commands.</span></span>

<span data-ttu-id="e6b1b-140">Affiche le menu contextuel de la sélection actuelle (identique à la combinaison de touches MAJ + F10).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-140">Displays the context menu for the current selection (the same as pressing Shift+F10).</span></span>

<span data-ttu-id="e6b1b-141">**application de thèmes**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-141">**application theming**</span></span>

<span data-ttu-id="e6b1b-142">À l’aide de techniques visuelles associées, telles que des contrôles personnalisés, pour créer une apparence ou une personnalisation unique pour une application.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-142">Using related visual techniques, such as customized controls, to create a unique look or branding for an application.</span></span>

<span data-ttu-id="e6b1b-143">**proportions**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-143">**aspect ratio**</span></span>

<span data-ttu-id="e6b1b-144">Expression de la relation entre la largeur d’un objet et sa hauteur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-144">An expression of the relation between the width of an object and its height.</span></span> <span data-ttu-id="e6b1b-145">Par exemple, la télévision haute définition utilise un proportions de 16:9.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-145">For example, high definition television uses a 16:9 aspect ratio.</span></span>

<span data-ttu-id="e6b1b-146">**saisie semi-automatique**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-146">**auto-complete**</span></span>

<span data-ttu-id="e6b1b-147">Type de liste utilisé dans les zones de texte et liste déroulante modifiable dans laquelle l’entrée probable peut être extrapolée et remplie automatiquement à partir de l’entrée précédente.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-147">A type of list used in text boxes and editable drop-down lists in which the likely input can be extrapolated and populated automatically from having been entered previously.</span></span> <span data-ttu-id="e6b1b-148">Les utilisateurs tapent une quantité minimale de texte pour remplir la liste de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-148">Users type a minimal amount of text to populate the auto-complete list.</span></span>

<span data-ttu-id="e6b1b-149">**fermeture automatique**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-149">**auto-exit**</span></span>

<span data-ttu-id="e6b1b-150">Zone de texte dans laquelle le focus d’entrée passe automatiquement à la zone de texte associée suivante dès qu’un utilisateur tape le dernier caractère.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-150">A text box in which the input focus automatically moves to the next related text box as soon as a user types the last character.</span></span>

## <a name="b"></a><span data-ttu-id="e6b1b-151">B</span><span class="sxs-lookup"><span data-stu-id="e6b1b-151">B</span></span>

<span data-ttu-id="e6b1b-152">**forfaitaire**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-152">**balloon**</span></span>

<span data-ttu-id="e6b1b-153">Contrôle Windows commun qui informe les utilisateurs d’un problème non critique ou d’une condition spéciale.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-153">A common Windows control that informs users of a non-critical problem or special condition.</span></span>

<span data-ttu-id="e6b1b-154">**barre de navigation**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-154">**breadcrumb bar**</span></span>

<span data-ttu-id="e6b1b-155">Élément de navigation, généralement apparaissant en haut d’une fenêtre, qui affiche et permet aux utilisateurs de modifier leur emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-155">A navigational element, usually appearing at the top of a window, that displays, and allows users to change, their current location.</span></span> <span data-ttu-id="e6b1b-156">« Breadcrumb » fait référence à la Division de l’emplacement actuel en une série de liens séparés par des flèches que les utilisateurs peuvent manipuler directement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-156">"Breadcrumb" refers to breaking the current location into a series of links separated by arrows that users can interact with directly.</span></span> <span data-ttu-id="e6b1b-157">Utilisez la barre d’adresses à la place.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-157">Use address bar instead.</span></span> <span data-ttu-id="e6b1b-158">Voir aussi : [barre d’adresses](#alink).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-158">See also: [address bar](#alink).</span></span>

## <a name="c"></a><span data-ttu-id="e6b1b-159">C</span><span class="sxs-lookup"><span data-stu-id="e6b1b-159">C</span></span>

<span data-ttu-id="e6b1b-160">**case à cocher**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-160">**check box**</span></span>

<span data-ttu-id="e6b1b-161">Contrôle Windows commun qui permet aux utilisateurs de choisir entre différents choix, tels que l’activation ou la désactivation d’une option.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-161">A common Windows control that allows users to decide between clearly differing choices, such as toggling an option on or off.</span></span>

<span data-ttu-id="e6b1b-162">**ouvrant**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-162">**chevron**</span></span>

<span data-ttu-id="e6b1b-163">Un petit contrôle ou bouton qui indique qu’il y a plus d’éléments qu’il n’est possible d’afficher dans l’espace alloué.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-163">A small control or button that indicates there are more items than can be displayed in the allotted space.</span></span> <span data-ttu-id="e6b1b-164">Les utilisateurs cliquent sur le Chevron pour afficher les éléments supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-164">Users click the chevron to see the additional items.</span></span>

<span data-ttu-id="e6b1b-165">**fenêtre enfant**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-165">**child window**</span></span>

<span data-ttu-id="e6b1b-166">Une fenêtre, telle qu’un contrôle ou un volet, contenue entièrement dans une autre fenêtre, appelée fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-166">A window, such as a control or pane, that is contained completely within another window, referred to as the parent window.</span></span> <span data-ttu-id="e6b1b-167">Voir aussi : [fenêtre parente](#p), [fenêtre propriétaire](#o).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-167">See also: [parent window](#p), [owned window](#o).</span></span>

<span data-ttu-id="e6b1b-168">**désactivé**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-168">**cleared**</span></span>

<span data-ttu-id="e6b1b-169">Dans une case à cocher, indique que l’option n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-169">In a check box, indicates that the option is not set.</span></span> <span data-ttu-id="e6b1b-170">Voir aussi : [État mixte](#m) [sélectionné](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-170">See also: [selected](#s), [mixed state](#m).</span></span>

<span data-ttu-id="e6b1b-171">**zone de liste déroulante**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-171">**combo box**</span></span>

<span data-ttu-id="e6b1b-172">Contrôle Windows commun qui combine les caractéristiques d’une liste déroulante ou d’une zone de liste standard, et une zone de texte modifiable.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-172">A common Windows control that combines the characteristics of a drop-down list or standard list box, and an editable text box.</span></span> <span data-ttu-id="e6b1b-173">Voir aussi : [zone de liste](#l), [liste déroulante](#d).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-173">See also: [list box](#l), [drop-down list](#d).</span></span>

<span data-ttu-id="e6b1b-174">**zone de commande**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-174">**command area**</span></span>

<span data-ttu-id="e6b1b-175">Zone dans une fenêtre où se trouvent les boutons de validation.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-175">The area in a window where the commit buttons are located.</span></span> <span data-ttu-id="e6b1b-176">En règle générale, les boîtes de dialogue et les assistants ont une zone de commande.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-176">Typically, dialog boxes and wizards have a command area.</span></span> <span data-ttu-id="e6b1b-177">Voir aussi : bouton valider.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-177">See also: commit button.</span></span>

<span data-ttu-id="e6b1b-178">**bouton de commande**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-178">**command button**</span></span>

<span data-ttu-id="e6b1b-179">Contrôle Windows commun qui permet aux utilisateurs de lancer immédiatement une action.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-179">A common Windows control that allows users to initiate an action immediately.</span></span>

<span data-ttu-id="e6b1b-180">**lien de commande**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-180">**command link**</span></span>

<span data-ttu-id="e6b1b-181">Contrôle utilisé pour faire un choix parmi un ensemble de choix associés s’excluant mutuellement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-181">A control used to make a choice among a set of mutually exclusive, related choices.</span></span> <span data-ttu-id="e6b1b-182">Dans leur état normal, les liens de commande ont une apparence légère similaire à celle des liens hypertexte, mais leur comportement est plus semblable aux boutons de commande.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-182">In their normal state, command links have a lightweight appearance similar to hyperlinks, but their behavior is more similar to command buttons.</span></span>

<span data-ttu-id="e6b1b-183">**bouton valider**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-183">**commit button**</span></span>

<span data-ttu-id="e6b1b-184">Bouton de commande utilisé pour valider une tâche, passer à l’étape suivante d’une tâche à plusieurs étapes ou annuler une tâche.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-184">A command button used to commit to a task, proceed to the next step in a multi-step task, or cancel a task.</span></span> <span data-ttu-id="e6b1b-185">Voir aussi : zone de commande.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-185">See also: command area.</span></span>

<span data-ttu-id="e6b1b-186">**page de validation**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-186">**commit page**</span></span>

<span data-ttu-id="e6b1b-187">Type de page d’assistant dans laquelle les utilisateurs s’engagent à effectuer la tâche.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-187">A type of wizard page in which users commit to performing the task.</span></span> <span data-ttu-id="e6b1b-188">Après cela, la tâche ne peut pas être annulée en cliquant sur les boutons précédent ou annuler.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-188">After doing so, the task cannot be undone by clicking Back or Cancel buttons.</span></span>

<span data-ttu-id="e6b1b-189">**page dernière étape**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-189">**completion page**</span></span>

<span data-ttu-id="e6b1b-190">Page d’Assistant utilisée pour indiquer la fin d’un Assistant.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-190">A wizard page used to indicate the end of a wizard.</span></span> <span data-ttu-id="e6b1b-191">Parfois utilisé à la place des pages de félicitations.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-191">Sometimes used instead of Congratulations pages.</span></span> <span data-ttu-id="e6b1b-192">Voir aussi : page félicitations.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-192">See also: congratulations page.</span></span>

<span data-ttu-id="e6b1b-193">**page félicitations**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-193">**congratulations page**</span></span>

<span data-ttu-id="e6b1b-194">Page d’Assistant utilisée pour indiquer la fin d’un Assistant.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-194">A wizard page used to indicate the end of a wizard.</span></span> <span data-ttu-id="e6b1b-195">Ces pages ne sont plus recommandées.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-195">These pages are no longer recommended.</span></span> <span data-ttu-id="e6b1b-196">Les assistants se terminent plus efficacement avec une page de validation ou, si nécessaire, une page de suivi ou de fin.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-196">Wizards conclude more efficiently with a commit page or, if necessary, a follow-up or completion page.</span></span> <span data-ttu-id="e6b1b-197">Voir aussi : page validation, page dernière étape, [page de suivi](#f).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-197">See also: commit page, completion page, [follow-up page](#f).</span></span>

<span data-ttu-id="e6b1b-198">**Interface utilisateur de consentement**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-198">**Consent UI**</span></span>

<span data-ttu-id="e6b1b-199">Boîte de dialogue utilisée par le contrôle de compte d’utilisateur (UAC) qui permet aux administrateurs protégés d’élever temporairement leurs privilèges.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-199">A dialog box used by User Account Control (UAC) that allows protected administrators to elevate their privileges temporarily.</span></span>

<span data-ttu-id="e6b1b-200">**contrainte**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-200">**constraint**</span></span>

<span data-ttu-id="e6b1b-201">Dans les contrôles qui impliquent une entrée d’utilisateur, tels que des zones de texte, les contraintes d’entrée sont un moyen utile d’éviter les erreurs.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-201">In controls that involve user input, such as text boxes, input constraints are a valuable way to prevent errors.</span></span> <span data-ttu-id="e6b1b-202">Par exemple, si la seule entrée valide pour un contrôle particulier est numérique, le contrôle peut utiliser les contraintes de valeur appropriées pour appliquer cette exigence.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-202">For example, if the only valid input for a particular control is numeric, the control can use appropriate value constraints to enforce this requirement.</span></span>

<span data-ttu-id="e6b1b-203">**zone de contenu**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-203">**content area**</span></span>

<span data-ttu-id="e6b1b-204">La partie des surfaces de l’interface utilisateur, telles que les boîtes de dialogue, les éléments du panneau de configuration et les assistants, consacrée à la présentation des options, à la fourniture d’informations et à la description des contrôles.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-204">The portion of UI surfaces, such as dialog boxes, control panel items, and wizards, devoted to presenting options, providing information, and describing controls.</span></span> <span data-ttu-id="e6b1b-205">Distingué de la zone de commande, du volet de tâches et de la zone de navigation.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-205">Distinguished from the command area, task pane, and navigation area.</span></span>

<span data-ttu-id="e6b1b-206">**onglet contextuel**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-206">**contextual tab**</span></span>

<span data-ttu-id="e6b1b-207">Onglet contenant une collection de commandes qui sont pertinentes uniquement lorsque l’utilisateur a sélectionné un type d’objet particulier.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-207">A tab containing a collection of commands that are relevant only when the user has selected a particular object type.</span></span> <span data-ttu-id="e6b1b-208">Voir aussi : [ruban](#r).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-208">See also: [Ribbon](#r).</span></span>

<span data-ttu-id="e6b1b-209">**Panneau de configuration**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-209">**Control Panel**</span></span>

<span data-ttu-id="e6b1b-210">Programme Windows qui recueille et affiche pour les utilisateurs les fonctionnalités au niveau du système de l’ordinateur, y compris l’installation et la configuration du matériel et des logiciels.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-210">A Windows program that collects and displays for users the system-level features of the computer, including hardware and software setup and configuration.</span></span> <span data-ttu-id="e6b1b-211">Dans le panneau de configuration, les utilisateurs peuvent cliquer sur des éléments individuels pour configurer des fonctionnalités au niveau du système et effectuer des tâches associées.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-211">From Control Panel, users can click individual items to configure system-level features and perform related tasks.</span></span> <span data-ttu-id="e6b1b-212">Voir aussi : élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-212">See also: control panel item.</span></span>

<span data-ttu-id="e6b1b-213">**élément du panneau de configuration**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-213">**control panel item**</span></span>

<span data-ttu-id="e6b1b-214">Une fonctionnalité individuelle disponible dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-214">An individual feature available from Control Panel.</span></span> <span data-ttu-id="e6b1b-215">Par exemple, les programmes et la facilité d’accès sont deux éléments du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-215">For example, Programs and Ease of Access are two control panel items.</span></span>

<span data-ttu-id="e6b1b-216">**Interface utilisateur des informations d’identification**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-216">**Credential UI**</span></span>

<span data-ttu-id="e6b1b-217">Boîte de dialogue utilisée par le contrôle de compte d’utilisateur (UAC) qui permet aux utilisateurs standard de demander une élévation temporaire de leurs privilèges.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-217">A dialog box used by User Account Control (UAC) that allows standard users to request temporary elevation of their privileges.</span></span>

<span data-ttu-id="e6b1b-218">**critique**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-218">**critical**</span></span>

<span data-ttu-id="e6b1b-219">Degré de gravité le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-219">The highest degree of severity.</span></span> <span data-ttu-id="e6b1b-220">Par exemple, dans les messages d’erreur et d’avertissement, les circonstances critiques peuvent impliquer la perte de données, la perte de confidentialité ou la perte de l’intégrité du système.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-220">For example, in error and warning messages, critical circumstances might involve data loss, loss of privacy, or loss of system integrity.</span></span>

<span data-ttu-id="e6b1b-221">**icône personnalisée**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-221">**custom icon**</span></span>

<span data-ttu-id="e6b1b-222">Représentation graphique propre à un programme (par opposition à une icône système Windows).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-222">A pictorial representation unique to a program (as opposed to a Windows system icon).</span></span>

<span data-ttu-id="e6b1b-223">**visuels personnalisés**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-223">**custom visuals**</span></span>

<span data-ttu-id="e6b1b-224">Les graphiques, les animations, les icônes et d’autres éléments visuels spécialement développés pour un programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-224">Graphics, animations, icons, and other visual elements specially developed for a program.</span></span>

## <a name="d"></a><span data-ttu-id="e6b1b-225">D</span><span class="sxs-lookup"><span data-stu-id="e6b1b-225">D</span></span>

<span data-ttu-id="e6b1b-226">**lien ou bouton de commande par défaut**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-226">**default command button or link**</span></span>

<span data-ttu-id="e6b1b-227">Le bouton de commande ou le lien qui est appelé quand les utilisateurs appuient sur la touche entrée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-227">The command button or link that is invoked when users press the Enter key.</span></span> <span data-ttu-id="e6b1b-228">Le bouton ou le lien de commande par défaut est assigné par le développeur, mais un bouton de commande ou un lien devient la valeur par défaut lorsque l’utilisateur clique sur l’onglet utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-228">The default command button or link is assigned by the developer, but any command button or link becomes the default when users tab to it.</span></span>

<span data-ttu-id="e6b1b-229">**moniteur par défaut**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-229">**default monitor**</span></span>

<span data-ttu-id="e6b1b-230">Analyse avec le menu Démarrer, la barre des tâches et la zone de notification.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-230">The monitor with the Start menu, taskbar, and notification area.</span></span>

<span data-ttu-id="e6b1b-231">**modèle de validation différée**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-231">**delayed commit model**</span></span>

<span data-ttu-id="e6b1b-232">Modèle de validation utilisé par les pages spoke de l’élément du panneau de configuration, où les modifications ne sont pas apportées jusqu’à ce que les utilisateurs cliquent explicitement sur un bouton de validation.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-232">The commit model used by control panel item spoke pages where changes aren't made until explicitly committed by users clicking a commit button.</span></span> <span data-ttu-id="e6b1b-233">Ainsi, les utilisateurs peuvent abandonner une tâche, naviguer à l’aide du bouton précédent, fermer ou la barre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-233">Thus, users can abandon a task, navigating away using the Back button, Close, or the Address bar.</span></span> <span data-ttu-id="e6b1b-234">Voir aussi : [modèle de validation immédiate](#i).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-234">See also: [immediate commit model](#i).</span></span>

<span data-ttu-id="e6b1b-235">**écran**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-235">**desktop**</span></span>

<span data-ttu-id="e6b1b-236">Zone de travail à l’écran fournie par Windows, analogue à un bureau physique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-236">The onscreen work area provided by Windows, analogous to a physical desktop.</span></span> <span data-ttu-id="e6b1b-237">Voir aussi : [zone de travail](#w).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-237">See also: [work area](#w).</span></span>

<span data-ttu-id="e6b1b-238">**commande destructrice**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-238">**destructive command**</span></span>

<span data-ttu-id="e6b1b-239">Action qui a un effet étendu et qui ne peut pas être annulée facilement, ou qui n’est pas immédiatement perceptible.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-239">An action that has a widespread effect and cannot be undone easily, or is not immediately noticeable.</span></span>

<span data-ttu-id="e6b1b-240">**volet d’informations**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-240">**details pane**</span></span>

<span data-ttu-id="e6b1b-241">Volet en bas d’une fenêtre de l’Explorateur Windows qui affiche des détails (le cas échéant) sur les éléments sélectionnés ; dans le cas contraire, il affiche des détails sur le dossier.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-241">The pane at the bottom of a Windows Explorer window that displays details (if any) about the selected items; otherwise, it displays details about the folder.</span></span> <span data-ttu-id="e6b1b-242">Par exemple, la Galerie de photos Windows affiche le nom de l’image, le type de fichier, la date de prise, les balises, l’évaluation, les dimensions et la taille de fichier.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-242">For example, Windows Photo Gallery displays the picture name, file type, date taken, tags, rating, dimensions, and file size.</span></span> <span data-ttu-id="e6b1b-243">Voir aussi : [volet de visualisation](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-243">See also: [preview pane](#p).</span></span>

<span data-ttu-id="e6b1b-244">**boîte de dialogue**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-244">**dialog box**</span></span>

<span data-ttu-id="e6b1b-245">Une fenêtre secondaire qui permet aux utilisateurs d’exécuter une commande, demande aux utilisateurs une question ou fournit aux utilisateurs des informations ou des commentaires sur la progression.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-245">A secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span>

<span data-ttu-id="e6b1b-246">**lanceur de boîte de dialogue**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-246">**dialog box launcher**</span></span>

<span data-ttu-id="e6b1b-247">Dans un ruban, bouton en bas de certains groupes qui ouvre une boîte de dialogue avec les fonctionnalités associées au groupe.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-247">In a ribbon, a button at the bottom of some groups that opens a dialog box with features related to the group.</span></span> <span data-ttu-id="e6b1b-248">Voir aussi : [ruban](#r).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-248">See also: [Ribbon](#r).</span></span>

<span data-ttu-id="e6b1b-249">**unité de boîte de dialogue**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-249">**dialog unit**</span></span>

<span data-ttu-id="e6b1b-250">Une unité de boîte de dialogue (DLU) est la mesure indépendante du périphérique à utiliser pour la disposition basée sur la police système actuelle.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-250">A dialog unit (DLU) is the device-independent measure to use for layout based on the current system font.</span></span>

<span data-ttu-id="e6b1b-251">**manipulation directe**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-251">**direct manipulation**</span></span>

<span data-ttu-id="e6b1b-252">Interaction directe entre l’utilisateur et les objets de l’interface utilisateur (tels que les icônes, les contrôles et les éléments de navigation).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-252">Direct interaction between the user and the objects in the UI (such as icons, controls, and navigational elements).</span></span> <span data-ttu-id="e6b1b-253">La souris et l’effleurement sont des méthodes courantes de manipulation directe.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-253">The mouse and touch are common methods of direct manipulation.</span></span>

<span data-ttu-id="e6b1b-254">**fenêtre ancrée**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-254">**docked window**</span></span>

<span data-ttu-id="e6b1b-255">Fenêtre qui apparaît à un emplacement fixe sur le bord de sa fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-255">A window that appears at a fixed location on the edge of its owner window.</span></span> <span data-ttu-id="e6b1b-256">Voir aussi : [fenêtre flottante](#f).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-256">See also: [floating window](#f).</span></span>

<span data-ttu-id="e6b1b-257">**flèche déroulante**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-257">**drop-down arrow**</span></span>

<span data-ttu-id="e6b1b-258">Flèche associée à des listes déroulantes, des zones de liste modifiable, des boutons partagés et des boutons de menu, indiquant que les utilisateurs peuvent afficher la liste associée en cliquant sur la flèche.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-258">The arrow associated with drop-down lists, combo boxes, split buttons, and menu buttons, indicating that users can view the associated list by clicking the arrow.</span></span>

<span data-ttu-id="e6b1b-259">**liste déroulante**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-259">**drop-down list**</span></span>

<span data-ttu-id="e6b1b-260">Contrôle Windows commun qui permet aux utilisateurs de sélectionner parmi une liste de valeurs s’excluant mutuellement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-260">A common Windows control that allows users to select among a list of mutually exclusive values.</span></span> <span data-ttu-id="e6b1b-261">Contrairement à une zone de liste, cette liste de choix disponibles est normalement masquée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-261">Unlike a list box, this list of available choices is normally hidden.</span></span>

## <a name="e"></a><span data-ttu-id="e6b1b-262">E</span><span class="sxs-lookup"><span data-stu-id="e6b1b-262">E</span></span>

<span data-ttu-id="e6b1b-263">**résolution efficace**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-263">**effective resolution**</span></span>

<span data-ttu-id="e6b1b-264">Résolution physique d’une analyse normalisée par le paramètre ppp (points par pouce) actuel.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-264">The physical resolution of a monitor normalized by the current dpi (dots per inch) setting.</span></span> <span data-ttu-id="e6b1b-265">À 96 ppp, la résolution effective est la même que la résolution physique, mais dans d’autres DPI, la résolution effective doit être mise à l’échelle proportionnellement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-265">At 96 dpi, the effective resolution is the same as the physical resolution, but in other dpis, the effective resolution must be scaled proportionately.</span></span> <span data-ttu-id="e6b1b-266">En règle générale, la résolution effective peut être calculée à l’aide de l’équation suivante :</span><span class="sxs-lookup"><span data-stu-id="e6b1b-266">Generally, the effective resolution can be calculated using the following equation:</span></span>

<span data-ttu-id="e6b1b-267">Résolution effective = résolution physique x (96/paramètre PPP actuel)</span><span class="sxs-lookup"><span data-stu-id="e6b1b-267">Effective resolution = Physical resolution x (96 / current dpi setting)</span></span>

<span data-ttu-id="e6b1b-268">Voir aussi : [pixels relatifs](#r), [résolution physique](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-268">See also: [relative pixels](#r), [physical resolution](#p).</span></span>

<span data-ttu-id="e6b1b-269">**administrateur avec élévation de privilèges**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-269">**elevated administrator**</span></span>

<span data-ttu-id="e6b1b-270">Dans le contrôle de compte d’utilisateur, les administrateurs élevés disposent de leurs privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-270">In User Account Control, elevated administrators have their administrator privileges.</span></span> <span data-ttu-id="e6b1b-271">Sans élévation, les administrateurs s’exécutent dans leur état le moins privilégié.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-271">Without elevating, administrators run in their least-privileged state.</span></span> <span data-ttu-id="e6b1b-272">La boîte de dialogue de consentement de l’interface utilisateur est utilisée pour élever l’état des administrateurs uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-272">The Consent UI dialog is used to elevate administrators to elevated status only when necessary.</span></span> <span data-ttu-id="e6b1b-273">Voir aussi : [administrateur protégé](#p), [utilisateur standard](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-273">See also: [protected administrator](#p), [standard user](#s).</span></span>

<span data-ttu-id="e6b1b-274">**info-bulle améliorée**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-274">**enhanced tooltip**</span></span>

<span data-ttu-id="e6b1b-275">Fenêtre contextuelle qui décrit de façon concise la commande désignée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-275">A pop-up window that concisely explains the command being pointed to.</span></span> <span data-ttu-id="e6b1b-276">Comme les info-bulles classiques, les info-bulles améliorées peuvent fournir la touche de raccourci de la commande.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-276">Like regular tooltips, enhanced tooltips may provide the shortcut key for the command.</span></span> <span data-ttu-id="e6b1b-277">Mais contrairement aux info-bulles classiques, elles peuvent également fournir des informations supplémentaires, des graphiques et un indicateur permettant d’obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-277">But unlike regular tooltips, they may also provide supplemental information, graphics, and an indicator that Help is available.</span></span> <span data-ttu-id="e6b1b-278">Ils peuvent également utiliser du texte enrichi et des séparateurs.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-278">They may also use rich text and separators.</span></span> <span data-ttu-id="e6b1b-279">Voir aussi : [info-bulle](#t).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-279">See also: [tooltip](#t).</span></span>

<span data-ttu-id="e6b1b-280">**error**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-280">**error**</span></span>

<span data-ttu-id="e6b1b-281">État dans lequel un problème s’est produit.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-281">A state in which a problem has occurred.</span></span> <span data-ttu-id="e6b1b-282">Voir aussi : [Avertissement](#w).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-282">See also: [warning](#w).</span></span>

<span data-ttu-id="e6b1b-283">**en-têtes extensibles**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-283">**expandable headings**</span></span>

<span data-ttu-id="e6b1b-284">Modèle de Chevron de divulgation progressive dans lequel un en-tête peut être développé ou réduit pour afficher ou masquer un groupe d’éléments.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-284">A progressive disclosure chevron pattern where a heading can be expanded or collapsed to reveal or hide a group of items.</span></span> <span data-ttu-id="e6b1b-285">Voir aussi : [Divulgation progressive](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-285">See also: [progressive disclosure](#p).</span></span>

<span data-ttu-id="e6b1b-286">**sélection étendue**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-286">**extended selection**</span></span>

<span data-ttu-id="e6b1b-287">Dans les affichages de liste et les zones de liste, un mode de sélection multiple dans lequel vous pouvez étendre la sélection d’un seul élément en faisant glisser ou en appuyant sur Maj + clic ou Ctrl + clic pour sélectionner respectivement des groupes de valeurs contiguës ou non adjacentes.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-287">In list views and list boxes, a multiple selection mode where selection of a single item can be extended by dragging or with Shift+click or Ctrl+click to select groups of contiguous or non-adjacent values, respectively.</span></span> <span data-ttu-id="e6b1b-288">Voir aussi : [sélection multiple](#m).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-288">See also: [multiple selection](#m).</span></span>

## <a name="f"></a><span data-ttu-id="e6b1b-289">F</span><span class="sxs-lookup"><span data-stu-id="e6b1b-289">F</span></span>

<span data-ttu-id="e6b1b-290">**raccourci**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-290">**flick**</span></span>

<span data-ttu-id="e6b1b-291">Trait rapide et droit d’un doigt ou d’un stylet sur un écran.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-291">A quick, straight stroke of a finger or pen on a screen.</span></span> <span data-ttu-id="e6b1b-292">Un raccourci est reconnu comme un geste et interprété comme une navigation ou une commande de modification.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-292">A flick is recognized as a gesture, and interpreted as a navigation or an editing command.</span></span>

<span data-ttu-id="e6b1b-293">**fenêtre flottante**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-293">**floating window**</span></span>

<span data-ttu-id="e6b1b-294">Fenêtre qui peut apparaître n’importe où sur l’écran souhaité par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-294">A window that can appear anywhere on the screen the user wants.</span></span> <span data-ttu-id="e6b1b-295">Voir aussi : [fenêtre ancrée](#d).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-295">See also: [docked window](#d).</span></span>

<span data-ttu-id="e6b1b-296">**volant**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-296">**flyout**</span></span>

<span data-ttu-id="e6b1b-297">Fenêtre contextuelle qui affiche temporairement plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-297">A popup window that temporarily shows more information.</span></span> <span data-ttu-id="e6b1b-298">Sur le bureau Windows, les lanceurs s’affichent en cliquant sur un gadget et sont ignorés en cliquant n’importe où en dehors du lanceur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-298">On the Windows desktop, flyouts are displayed by clicking on a gadget, and dismissed by clicking anywhere outside the flyout.</span></span> <span data-ttu-id="e6b1b-299">Vous pouvez utiliser des lanceurs à la fois dans les États ancré et flottant.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-299">You can use flyouts in both the docked and floating states.</span></span>

<span data-ttu-id="e6b1b-300">**page de suivi**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-300">**follow-up page**</span></span>

<span data-ttu-id="e6b1b-301">Page de l’Assistant utilisée pour présenter les tâches associées que les utilisateurs sont susceptibles de faire comme suivi.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-301">A wizard page used to present related tasks that users are likely to do as follow-up.</span></span> <span data-ttu-id="e6b1b-302">Parfois utilisé à la place des pages de félicitations.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-302">Sometimes used instead of congratulations pages.</span></span>

<span data-ttu-id="e6b1b-303">**son**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-303">**font**</span></span>

<span data-ttu-id="e6b1b-304">Ensemble d’attributs pour les caractères de texte.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-304">A set of attributes for text characters.</span></span>

<span data-ttu-id="e6b1b-305">**plein écran**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-305">**full screen**</span></span>

<span data-ttu-id="e6b1b-306">Fenêtre agrandie qui n’a pas de cadre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-306">A maximized window that does not have a frame.</span></span>

## <a name="g"></a><span data-ttu-id="e6b1b-307">G</span><span class="sxs-lookup"><span data-stu-id="e6b1b-307">G</span></span>

<span data-ttu-id="e6b1b-308">**Gadget**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-308">**gadget**</span></span>

<span data-ttu-id="e6b1b-309">Mini-application simple hébergée sur le Bureau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-309">A simple mini-application hosted on the user's desktop.</span></span> <span data-ttu-id="e6b1b-310">Voir aussi : [encadré](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-310">See also: [Sidebar](#s).</span></span>

<span data-ttu-id="e6b1b-311">**Office**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-311">**gallery**</span></span>

<span data-ttu-id="e6b1b-312">Liste des commandes ou options présentées graphiquement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-312">A list of commands or options presented graphically.</span></span> <span data-ttu-id="e6b1b-313">Une galerie basée sur les résultats illustre l’effet des commandes ou des options à la place des commandes elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-313">A results-based gallery illustrates the effect of the commands or options instead of the commands themselves.</span></span> <span data-ttu-id="e6b1b-314">Peut être étiqueté ou groupé.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-314">May be labeled or grouped.</span></span> <span data-ttu-id="e6b1b-315">Par exemple, les options de mise en forme peuvent être présentées dans une galerie de miniatures.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-315">For example, formatting options can be presented in a thumbnail gallery.</span></span>

<span data-ttu-id="e6b1b-316">**mouvement**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-316">**gesture**</span></span>

<span data-ttu-id="e6b1b-317">Mouvement rapide d’un doigt ou d’un stylet sur un écran que l’ordinateur interprète comme une commande, plutôt qu’en tant que déplacement de la souris, écriture ou dessin.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-317">A quick movement of a finger or pen on a screen that the computer interprets as a command, rather than as a mouse movement, writing, or drawing.</span></span>

<span data-ttu-id="e6b1b-318">**page mise en route**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-318">**getting started page**</span></span>

<span data-ttu-id="e6b1b-319">Une page d’Assistant facultative qui décrit la configuration requise pour l’exécution de l’Assistant ou explique l’objectif de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-319">An optional wizard page that outlines prerequisites for running the wizard successfully or explains the purpose of the wizard.</span></span>

<span data-ttu-id="e6b1b-320">**reflet**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-320">**glass**</span></span>

<span data-ttu-id="e6b1b-321">Option de cadre de fenêtre caractérisée par translucence, qui aide les utilisateurs à se concentrer sur le contenu et les fonctionnalités plutôt que sur l’interface qui les entoure.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-321">A window frame option characterized by translucence, helping users focus on content and functionality rather than the interface surrounding it.</span></span>

<span data-ttu-id="e6b1b-322">**variante**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-322">**glyph**</span></span>

<span data-ttu-id="e6b1b-323">Terme générique utilisé pour faire référence à n’importe quel graphique ou image symbolique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-323">A generic term used to refer to any graph or symbolic image.</span></span> <span data-ttu-id="e6b1b-324">Les flèches, les chevrons et les puces sont des glyphes couramment utilisés dans Windows.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-324">Arrows, chevrons, and bullets are glyphs commonly used in Windows.</span></span>

<span data-ttu-id="e6b1b-325">**zone de groupe**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-325">**group box**</span></span>

<span data-ttu-id="e6b1b-326">Contrôle Windows commun qui affiche des relations entre un ensemble de contrôles connexes.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-326">A common Windows control that shows relationships among a set of related controls.</span></span>

## <a name="h"></a><span data-ttu-id="e6b1b-327">H</span><span class="sxs-lookup"><span data-stu-id="e6b1b-327">H</span></span>

<span data-ttu-id="e6b1b-328">**reconnaissance de l’écriture manuscrite**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-328">**handwriting recognition**</span></span>

<span data-ttu-id="e6b1b-329">Logiciel qui convertit l’entrée manuscrite en texte.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-329">Software that converts ink to text.</span></span>

<span data-ttu-id="e6b1b-330">**Aide**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-330">**Help**</span></span>

<span data-ttu-id="e6b1b-331">Assistance utilisateur d’une nature plus détaillée que celle disponible dans l’interface utilisateur principale.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-331">User assistance of a more detailed nature than is available in the primary UI.</span></span> <span data-ttu-id="e6b1b-332">Généralement accessible à partir d’un menu ou en cliquant sur un lien ou une icône d’aide, ce contenu peut prendre plusieurs formes, y compris des procédures pas à pas, du texte conceptuel ou d’autres didacticiels guidés basés sur visuel.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-332">Typically accessed from a menu or by clicking a Help link or icon, this content may take a variety of forms, including step-by-step procedures, conceptual text, or more visually-based, guided tutorials.</span></span>

<span data-ttu-id="e6b1b-333">**mode de contraste élevé**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-333">**high-contrast mode**</span></span>

<span data-ttu-id="e6b1b-334">Paramètre d’affichage spécial qui fournit un contraste extrême pour les éléments visuels de premier plan et d’arrière-plan (noir blanc ou blanc sur noir).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-334">A special display setting that provides extreme contrast for foreground and background visual elements (either black on white or white on black).</span></span> <span data-ttu-id="e6b1b-335">Particulièrement utile pour l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-335">Particularly helpful for accessibility.</span></span>

<span data-ttu-id="e6b1b-336">**page Hub**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-336">**hub page**</span></span>

<span data-ttu-id="e6b1b-337">Dans les éléments du panneau de configuration, une page de concentrateur présente des choix de haut niveau, tels que les tâches les plus couramment utilisées (comme les pages de concentrateur basées sur les tâches) ou les objets disponibles (comme avec les pages de concentrateur basés sur des objets).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-337">In control panel items, a hub page presents high-level choices, such as the most commonly used tasks (as with task-based hub pages) or the available objects (as with object-based hub pages).</span></span> <span data-ttu-id="e6b1b-338">Les utilisateurs peuvent accéder aux pages spoke pour effectuer des tâches spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-338">Users can navigate to spoke pages to perform specific tasks.</span></span> <span data-ttu-id="e6b1b-339">Voir aussi : [page spoke](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-339">See also: [spoke page](#s).</span></span>

<span data-ttu-id="e6b1b-340">**page concentrateur hybride**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-340">**hybrid hub page**</span></span>

<span data-ttu-id="e6b1b-341">Dans les éléments du panneau de configuration, une page de concentrateur hybride est une page Hub qui contient également des propriétés ou des commandes directement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-341">In control panel items, a hybrid hub page is a hub page that also has some properties or commands directly on it.</span></span> <span data-ttu-id="e6b1b-342">Les pages de concentrateur hybride sont vivement recommandées lorsque les utilisateurs sont plus susceptibles d’utiliser l’élément du panneau de configuration pour accéder à ces propriétés et commandes.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-342">Hybrid hub pages are strongly recommended when users are most likely to use the control panel item to access those properties and commands.</span></span>

## <a name="i"></a><span data-ttu-id="e6b1b-343">I</span><span class="sxs-lookup"><span data-stu-id="e6b1b-343">I</span></span>

<span data-ttu-id="e6b1b-344">**modèle de validation immédiate**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-344">**immediate commit model**</span></span>

<span data-ttu-id="e6b1b-345">Modèle de validation utilisé par les pages de concentrateur hybride où les modifications prennent effet dès que les utilisateurs les effectuent.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-345">The commit model used by hybrid hub pages where changes take effect as soon as users make them.</span></span> <span data-ttu-id="e6b1b-346">Les boutons de validation ne sont pas utilisés dans ce modèle.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-346">Commit buttons aren't used in this model.</span></span> <span data-ttu-id="e6b1b-347">Voir aussi : [modèle de validation retardé](#d).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-347">See also: [delayed commit model](#d).</span></span>

<span data-ttu-id="e6b1b-348">**message sur place**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-348">**in-place message**</span></span>

<span data-ttu-id="e6b1b-349">Message qui s’affiche dans le contexte de la surface de l’interface utilisateur actuelle, au lieu d’une fenêtre distincte.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-349">A message that appears in the context of the current UI surface, instead of a separate window.</span></span> <span data-ttu-id="e6b1b-350">Contrairement aux fenêtres distinctes, les messages sur place nécessitent un espace d’écran disponible ou une disposition dynamique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-350">Unlike separate windows, in-place messages require either available screen space or dynamic layout.</span></span>

<span data-ttu-id="e6b1b-351">**boîte de dialogue indirecte**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-351">**indirect dialog box**</span></span>

<span data-ttu-id="e6b1b-352">Une boîte de dialogue s’affiche en dehors du contexte, soit en tant que résultat indirect d’une tâche, soit en raison d’un problème avec un processus système ou d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-352">A dialog box displayed out of context, either as an indirect result of a task or as the result of a problem with a system or background process.</span></span>

<span data-ttu-id="e6b1b-353">**interface utilisateur inductive**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-353">**inductive user interface**</span></span>

<span data-ttu-id="e6b1b-354">Une interface utilisateur qui divise une tâche complexe en une tâche simple et facile à décrire, avec un objectif clair.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-354">A UI that breaks a complex task down into simple, easily explained, clearly stated steps with a clear purpose.</span></span>

<span data-ttu-id="e6b1b-355">**info-bulle**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-355">**infotip**</span></span>

<span data-ttu-id="e6b1b-356">Petite fenêtre contextuelle qui décrit de façon concise l’objet désigné, par exemple les descriptions des contrôles ToolBar, les icônes, les graphiques, les liens, les objets de l’Explorateur Windows, les éléments du menu Démarrer et les boutons de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-356">A small pop-up window that concisely describes the object being pointed to, such as descriptions of toolbar controls, icons, graphics, links, Windows Explorer objects, Start menu items, and taskbar buttons.</span></span> <span data-ttu-id="e6b1b-357">Les info-bulles sont une forme de divulgation progressive, ce qui évite d’avoir à utiliser du texte descriptif à l’écran à tout moment.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-357">Infotips are a form of progressive disclosure, eliminating the need to have descriptive text on screen at all times.</span></span>

<span data-ttu-id="e6b1b-358">**trait**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-358">**ink**</span></span>

<span data-ttu-id="e6b1b-359">Sortie brute d’un stylet.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-359">The raw output for a pen.</span></span> <span data-ttu-id="e6b1b-360">Cette encre numérique peut être conservée comme écrite, ou elle peut être convertie en texte à l’aide du logiciel de reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-360">This digital ink can be kept just as written, or it can be converted to text using handwriting recognition software.</span></span>

<span data-ttu-id="e6b1b-361">**Inline**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-361">**inline**</span></span>

<span data-ttu-id="e6b1b-362">Emplacement des liens ou des messages directement dans le contexte de l’interface utilisateur associée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-362">Placement of links or messages directly in the context of its related UI.</span></span> <span data-ttu-id="e6b1b-363">Par exemple, un lien Inline apparaît dans un autre texte et non séparément.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-363">For example, an inline link occurs within other text instead of separately.</span></span>

<span data-ttu-id="e6b1b-364">**Focus d’entrée**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-364">**input focus**</span></span>

<span data-ttu-id="e6b1b-365">Emplacement dans lequel l’utilisateur dirige actuellement l’entrée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-365">The location where the user is currently directing input.</span></span> <span data-ttu-id="e6b1b-366">Notez que, juste parce qu’un emplacement de l’interface utilisateur est mis en surbrillance, cela ne signifie pas nécessairement que cet emplacement a le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-366">Note that just because a location in the UI is highlighted does not necessarily mean this location has input focus.</span></span>

<span data-ttu-id="e6b1b-367">**instancié**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-367">**instance**</span></span>

<span data-ttu-id="e6b1b-368">Session de programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-368">A program session.</span></span> <span data-ttu-id="e6b1b-369">Par exemple, Windows Internet Explorer permet aux utilisateurs d’exécuter plusieurs instances du programme, car plusieurs sessions indépendantes peuvent s’exécuter à la fois.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-369">For example, Windows Internet Explorer allows users to run multiple instances of the program because users can have several independent sessions running at a time.</span></span> <span data-ttu-id="e6b1b-370">Les paramètres peuvent être enregistrés entre les sessions de programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-370">Settings can be saved across program sessions.</span></span> <span data-ttu-id="e6b1b-371">Voir aussi : [persistance](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-371">See also: [persistence](#p).</span></span>

## <a name="j"></a><span data-ttu-id="e6b1b-372">J</span><span class="sxs-lookup"><span data-stu-id="e6b1b-372">J</span></span>

## <a name="k"></a><span data-ttu-id="e6b1b-373">K</span><span class="sxs-lookup"><span data-stu-id="e6b1b-373">K</span></span>

<span data-ttu-id="e6b1b-374">**KeyTip**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-374">**keytip**</span></span>

<span data-ttu-id="e6b1b-375">Dans un ruban, mécanisme utilisé pour afficher les clés d’accès.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-375">In a ribbon, the mechanism used to display access keys.</span></span> <span data-ttu-id="e6b1b-376">Les touches d’accès s’affichent sous la forme d’un petit Conseil sur chaque commande ou groupe, par opposition aux lettres soulignées généralement utilisées pour afficher les clés d’accès.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-376">The access keys appear in the form of a small tip over each command or group, as opposed to the underlined letters typically used to display access keys.</span></span> <span data-ttu-id="e6b1b-377">Voir aussi : [clé d’accès](#alink).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-377">See also: [access key](#alink).</span></span>

## <a name="l"></a><span data-ttu-id="e6b1b-378">L</span><span class="sxs-lookup"><span data-stu-id="e6b1b-378">L</span></span>

<span data-ttu-id="e6b1b-379">**mode paysage**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-379">**landscape mode**</span></span>

<span data-ttu-id="e6b1b-380">Option de présentation qui oriente un objet pour qu’il soit plus grand que haut.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-380">A presentation option that orients an object to be wider than it is tall.</span></span> <span data-ttu-id="e6b1b-381">Voir aussi : [mode portrait](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-381">See also: [portrait mode](#p).</span></span>

<span data-ttu-id="e6b1b-382">**compte d’utilisateur doté de privilèges minimum**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-382">**least-privilege user account**</span></span>

<span data-ttu-id="e6b1b-383">Un compte d’utilisateur qui s’exécute normalement avec des privilèges minimaux.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-383">A user account that normally runs with minimal privileges.</span></span> <span data-ttu-id="e6b1b-384">Voir aussi : [contrôle de compte d’utilisateur](#u).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-384">See also: [User Account Control](#u).</span></span>

<span data-ttu-id="e6b1b-385">**zone de liste**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-385">**list box**</span></span>

<span data-ttu-id="e6b1b-386">Contrôle Windows commun qui permet aux utilisateurs de sélectionner un ensemble de valeurs présentées dans une liste, qui, à la différence d’une liste déroulante, est toujours visible.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-386">A common Windows control that allows users to select from a set of values presented in a list, which, unlike a drop-down list, is always visible.</span></span> <span data-ttu-id="e6b1b-387">Prend en charge les sélections uniques ou multiples.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-387">Supports single or multiple selections.</span></span>

<span data-ttu-id="e6b1b-388">**mode liste**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-388">**list view**</span></span>

<span data-ttu-id="e6b1b-389">Contrôle Windows commun qui permet aux utilisateurs d’afficher et d’interagir avec une collection d’objets de données, à l’aide d’une sélection unique ou d’une sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-389">A common Windows control that allows users to view and interact with a collection of data objects, using either single selection or multiple selection.</span></span>

<span data-ttu-id="e6b1b-390">**aperçu instantané**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-390">**live preview**</span></span>

<span data-ttu-id="e6b1b-391">Technique de préversion qui affiche l’effet d’une commande immédiatement sur la sélection ou le pointage sans que l’utilisateur n’ait à valider l’action.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-391">A preview technique that shows the effect of a command immediately on selection or hover without the user commiting the action.</span></span> <span data-ttu-id="e6b1b-392">Par exemple, les options de mise en forme, telles que les thèmes, les polices et les couleurs, tirent parti des aperçus instantanés en indiquant aux utilisateurs l’effet avec un minimum d’effort.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-392">For example, formatting options such as themes, fonts, and colors benefit from live previews by showing users the effect with minimal effort.</span></span>

<span data-ttu-id="e6b1b-393">**localisation**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-393">**localization**</span></span>

<span data-ttu-id="e6b1b-394">Processus d’adaptation des logiciels pour différents pays, langues, cultures ou marchés.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-394">The process of adapting software for different countries, languages, cultures, or markets.</span></span>

<span data-ttu-id="e6b1b-395">**fichier journal**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-395">**log file**</span></span>

<span data-ttu-id="e6b1b-396">Référentiel basé sur des fichiers pour obtenir des informations sur les différents types d’activité sur un système informatique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-396">A file-based repository for information of various kinds about activity on a computer system.</span></span> <span data-ttu-id="e6b1b-397">Les administrateurs consultent souvent les fichiers journaux. en général, les utilisateurs ordinaires ne le font pas.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-397">Administrators often consult log files; ordinary users generally do not.</span></span>

## <a name="m"></a><span data-ttu-id="e6b1b-398">M</span><span class="sxs-lookup"><span data-stu-id="e6b1b-398">M</span></span>

<span data-ttu-id="e6b1b-399">**instruction principale**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-399">**main instruction**</span></span>

<span data-ttu-id="e6b1b-400">Texte affiché en évidence qui explique comment faire dans la fenêtre ou la page.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-400">Prominently displayed text that concisely explains what to do in the window or page.</span></span> <span data-ttu-id="e6b1b-401">L’instruction doit être une instruction spécifique, une direction impérative ou une question.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-401">The instruction should be a specific statement, imperative direction, or question.</span></span> <span data-ttu-id="e6b1b-402">Les bonnes instructions principales communiquent l’objectif de l’utilisateur au lieu de se concentrer uniquement sur la manipulation de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-402">Good main instructions communicate the user's objective rather than focusing just on manipulating the UI.</span></span>

<span data-ttu-id="e6b1b-403">**environnement géré**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-403">**managed environment**</span></span>

<span data-ttu-id="e6b1b-404">Un environnement informatique en réseau géré par un service informatique ou un fournisseur tiers, plutôt que par des utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-404">A networked computer environment managed by an IT department or third-party provider, instead of by individual users.</span></span> <span data-ttu-id="e6b1b-405">Les administrateurs peuvent optimiser les performances et appliquer les mises à jour du système d’exploitation et des applications, entre autres tâches.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-405">Administrators may optimize performance and apply operating system and application updates, among other tasks.</span></span>

<span data-ttu-id="e6b1b-406">**manoeuvr**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-406">**manipulation**</span></span>

<span data-ttu-id="e6b1b-407">Type d’interaction tactile dans laquelle l’entrée correspond directement à la façon dont l’objet touchées réagira naturellement à l’action dans le monde réel.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-407">A type of touch interaction in which input corresponds directly to how the object being touched would react naturally to the action in the real world.</span></span>

<span data-ttu-id="e6b1b-408">**valoris**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-408">**maximize**</span></span>

<span data-ttu-id="e6b1b-409">Pour afficher une fenêtre à sa plus grande taille.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-409">To display a window at its largest size.</span></span> <span data-ttu-id="e6b1b-410">Voir aussi : réduire, [fenêtre restaurée](#r).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-410">See also: minimize, [restored window](#r).</span></span>

<span data-ttu-id="e6b1b-411">**menus**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-411">**menu**</span></span>

<span data-ttu-id="e6b1b-412">Liste des commandes ou options disponibles pour les utilisateurs dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-412">A list of commands or options available to users in the current context.</span></span>

<span data-ttu-id="e6b1b-413">**boîte de message**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-413">**message box**</span></span>

<span data-ttu-id="e6b1b-414">Fenêtre secondaire qui s’affiche pour informer l’utilisateur d’une condition particulière.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-414">A secondary window that is displayed to inform a user about a particular condition.</span></span>

<span data-ttu-id="e6b1b-415">**Mini-barre d’outils**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-415">**mini-toolbar**</span></span>

<span data-ttu-id="e6b1b-416">Barre d’outils contextuelle affichée au pointage.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-416">A contextual toolbar displayed on hover.</span></span>

<span data-ttu-id="e6b1b-417">**icône**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-417">**minimize**</span></span>

<span data-ttu-id="e6b1b-418">Pour masquer une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-418">To hide a window.</span></span> <span data-ttu-id="e6b1b-419">Voir aussi : agrandir, [fenêtre restaurée](#r).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-419">See also: maximize, [restored window](#r).</span></span>

<span data-ttu-id="e6b1b-420">**État mixte**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-420">**mixed state**</span></span>

<span data-ttu-id="e6b1b-421">Pour les cases à cocher qui s’appliquent à un groupe d’éléments, un État mixte indique que certains éléments sont sélectionnés et que d’autres sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-421">For check boxes that apply to a group of items, a mixed state indicates that some of the items are selected and others are cleared.</span></span>

<span data-ttu-id="e6b1b-422">**exigeant**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-422">**modal**</span></span>

<span data-ttu-id="e6b1b-423">Interaction restrictive ou limitée en raison de l’utilisation d’un mode.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-423">Restrictive or limited interaction due to operating in a mode.</span></span> <span data-ttu-id="e6b1b-424">Modale décrit souvent une fenêtre secondaire qui restreint l’interaction d’un utilisateur avec la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-424">Modal often describes a secondary window that restricts a user's interaction with the owner window.</span></span> <span data-ttu-id="e6b1b-425">Voir aussi : non modal.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-425">See also: modeless.</span></span>

<span data-ttu-id="e6b1b-426">**non modales**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-426">**modeless**</span></span>

<span data-ttu-id="e6b1b-427">Interaction non restrictive ou non limitée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-427">Non-restrictive or non-limited interaction.</span></span> <span data-ttu-id="e6b1b-428">Non modal décrit souvent une fenêtre secondaire qui ne restreint pas l’interaction d’un utilisateur avec la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-428">Modeless often describes a secondary window that does not restrict a user's interaction with the owner window.</span></span> <span data-ttu-id="e6b1b-429">Voir aussi : modal.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-429">See also: modal.</span></span>

<span data-ttu-id="e6b1b-430">**sélection multiple**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-430">**multiple selection**</span></span>

<span data-ttu-id="e6b1b-431">Possibilité pour les utilisateurs de choisir plusieurs objets dans une liste ou une arborescence.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-431">The ability for users to choose more than one object in a list or tree.</span></span>

## <a name="n"></a><span data-ttu-id="e6b1b-432">N</span><span class="sxs-lookup"><span data-stu-id="e6b1b-432">N</span></span>

<span data-ttu-id="e6b1b-433">**événement système non critique**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-433">**non-critical system event**</span></span>

<span data-ttu-id="e6b1b-434">Type d’événement système qui ne nécessite pas une attention immédiate, souvent lié à l’état du système.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-434">A type of system event that does not require immediate attention, often pertaining to system status.</span></span> <span data-ttu-id="e6b1b-435">Voir aussi : [critique](#c).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-435">See also: [critical](#c).</span></span>

<span data-ttu-id="e6b1b-436">**notification**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-436">**notification**</span></span>

<span data-ttu-id="e6b1b-437">Informations sur une nature non critique qui s’affiche brièvement pour l’utilisateur ; une notification prend la forme d’une info-bulle à partir d’une icône dans la zone de notification de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-437">Information of a non-critical nature that is displayed briefly to the user; a notification takes the form of a balloon from an icon in the notification area of the taskbar.</span></span>

## <a name="o"></a><span data-ttu-id="e6b1b-438">O</span><span class="sxs-lookup"><span data-stu-id="e6b1b-438">O</span></span>

<span data-ttu-id="e6b1b-439">**accepter**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-439">**opt in**</span></span>

<span data-ttu-id="e6b1b-440">La possibilité pour les utilisateurs de sélectionner explicitement des fonctionnalités facultatives.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-440">The ability for users to select optional features explicitly.</span></span> <span data-ttu-id="e6b1b-441">Moins intrusif pour les utilisateurs que pour la désactivation, en particulier pour les fonctionnalités liées à la confidentialité et au marketing, en raison de l’absence de présomption des souhaits des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-441">Less intrusive to users than opt-out, especially for privacy and marketing related features, because there is no presumption of users' wishes.</span></span> <span data-ttu-id="e6b1b-442">Voir aussi : refuser, options.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-442">See also: opt out, options.</span></span>

<span data-ttu-id="e6b1b-443">**refuser**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-443">**opt out**</span></span>

<span data-ttu-id="e6b1b-444">La possibilité pour les utilisateurs de supprimer les fonctionnalités qu’ils ne souhaitent pas en effaçant leur sélection.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-444">The ability for users to remove features they don't want by clearing their selection.</span></span> <span data-ttu-id="e6b1b-445">Plus intrusive pour les utilisateurs que pour les abonnements, en particulier pour les fonctionnalités liées à la confidentialité et au marketing, en raison des souhaits des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-445">More intrusive to users than opt-in, especially for privacy and marketing related features, because there is an assumption of users' wishes.</span></span> <span data-ttu-id="e6b1b-446">Voir aussi : opt in, options.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-446">See also: opt in, options.</span></span>

<span data-ttu-id="e6b1b-447">**options**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-447">**options**</span></span>

<span data-ttu-id="e6b1b-448">Choix à la disposition des utilisateurs pour la personnalisation d’un programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-448">Choices available to users for customizing a program.</span></span> <span data-ttu-id="e6b1b-449">Par exemple, une boîte de dialogue Options permet aux utilisateurs d’afficher et de modifier les options du programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-449">For example, an Options dialog box allows users to view and change program options.</span></span> <span data-ttu-id="e6b1b-450">Voir aussi : [Propriétés](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-450">See also: [properties](#p).</span></span>

<span data-ttu-id="e6b1b-451">**interface utilisateur hors contexte**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-451">**out-of-context UI**</span></span>

<span data-ttu-id="e6b1b-452">Toute interface utilisateur affichée dans une fenêtre indépendante qui n’est pas directement liée à l’activité actuelle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-452">Any UI displayed in a pop-up window that isn't directly related to the user's current activity.</span></span> <span data-ttu-id="e6b1b-453">Par exemple, les notifications et l’interface utilisateur de consentement pour l’utilisateur Access Control sont des interfaces utilisateur hors contexte.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-453">For example, notifications and the Consent UI for User Access Control are out-of-context UI.</span></span>

<span data-ttu-id="e6b1b-454">**fenêtre propriétaire**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-454">**owned window**</span></span>

<span data-ttu-id="e6b1b-455">Fenêtre secondaire utilisée pour effectuer une tâche auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-455">A secondary window used to perform an auxiliary task.</span></span> <span data-ttu-id="e6b1b-456">Il ne s’agit pas d’une fenêtre de niveau supérieur (elle n’est donc pas affichée sur la barre des tâches). au lieu de cela, il est « détenu » par sa fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-456">It is not a top-level window (so it isn't displayed on the taskbar); rather, it is "owned" by its owner window.</span></span> <span data-ttu-id="e6b1b-457">Par exemple, la plupart des boîtes de dialogue sont des fenêtres détenues.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-457">For example, most dialog boxes are owned windows.</span></span> <span data-ttu-id="e6b1b-458">Voir aussi : [fenêtre enfant](#c), fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-458">See also: [child window](#c), owner window.</span></span>

<span data-ttu-id="e6b1b-459">**contrôle propriétaire**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-459">**owner control**</span></span>

<span data-ttu-id="e6b1b-460">Source d’une info-bulle, d’une bulle ou d’un menu volant.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-460">The source of a tip, balloon, or flyout.</span></span> <span data-ttu-id="e6b1b-461">Par exemple, une zone de texte qui a des contraintes d’entrée peut afficher une bulle pour informer l’utilisateur de ces limitations.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-461">For example, a text box that has input constraints might display a balloon to let the user know of these limitations.</span></span> <span data-ttu-id="e6b1b-462">Dans ce cas, la zone de texte est considérée comme le contrôle propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-462">In this case, the text box is considered the owner control.</span></span>

<span data-ttu-id="e6b1b-463">**fenêtre propriétaire**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-463">**owner window**</span></span>

<span data-ttu-id="e6b1b-464">Fenêtre à partir de laquelle provient une fenêtre détenue.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-464">A window from which an owned window originates.</span></span> <span data-ttu-id="e6b1b-465">S’affiche sous la fenêtre appartenant dans l’ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-465">Appears beneath the owned window in Z order.</span></span> <span data-ttu-id="e6b1b-466">Voir aussi : fenêtre propriétaire, [fenêtre parente](#p), [ordre de plan](#z).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-466">See also: owned window, [parent window](#p), [Z order](#z).</span></span>

## <a name="p"></a><span data-ttu-id="e6b1b-467">P</span><span class="sxs-lookup"><span data-stu-id="e6b1b-467">P</span></span>

<span data-ttu-id="e6b1b-468">**page**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-468">**page**</span></span>

<span data-ttu-id="e6b1b-469">Unité de navigation de base pour l’interface utilisateur basée sur les tâches, comme les assistants, les feuilles de propriétés, les éléments du panneau de configuration et les sites Web.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-469">A basic unit of navigation for task-based UI, such as wizards, property sheets, control panel items, and Web sites.</span></span> <span data-ttu-id="e6b1b-470">Les utilisateurs effectuent des tâches en naviguant d’une page à l’autres au sein d’une même fenêtre hôte.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-470">Users perform tasks by navigating from page to page within a single host window.</span></span> <span data-ttu-id="e6b1b-471">Voir aussi : Flow page, [Window](#w).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-471">See also: page flow, [window](#w).</span></span>

<span data-ttu-id="e6b1b-472">**Flow page**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-472">**page flow**</span></span>

<span data-ttu-id="e6b1b-473">Collection de pages dans laquelle les utilisateurs effectuent une tâche.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-473">A collection of pages in which users perform a task.</span></span> <span data-ttu-id="e6b1b-474">Voir aussi : page, [tâche](#t), [Assistant](#w), [panneau de configuration](#c).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-474">See also: page, [task](#t), [wizard](#w), [Control Panel](#c).</span></span>

<span data-ttu-id="e6b1b-475">**contrôle de l’espace de page**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-475">**page space control**</span></span>

<span data-ttu-id="e6b1b-476">Permet aux utilisateurs d’afficher et d’interagir avec une collection hiérarchique d’objets organisée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-476">Allows users to view and interact with a hierarchically arranged collection of objects.</span></span> <span data-ttu-id="e6b1b-477">Les contrôles d’espace de page sont semblables aux contrôles d’arborescence, mais ils ont une apparence visuelle légèrement différente.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-477">Page space controls are like tree controls, but they have a slightly different visual appearance.</span></span> <span data-ttu-id="e6b1b-478">Ils sont principalement utilisés par l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-478">They are used primarily by Windows Explorer.</span></span>

<span data-ttu-id="e6b1b-479">**fenêtre de palette**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-479">**palette window**</span></span>

<span data-ttu-id="e6b1b-480">Fenêtre secondaire non modale qui affiche une barre d’outils ou d’autres choix, tels que des couleurs, des modèles, des polices ou des attributs de police.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-480">A modeless secondary window that displays a toolbar or other choices, such as colors, patterns, fonts, or font attributes.</span></span>

<span data-ttu-id="e6b1b-481">**fonctions**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-481">**pan**</span></span>

<span data-ttu-id="e6b1b-482">Pour déplacer une scène, telle qu’une carte ou une photo, dans deux dimensions, faites-la glisser directement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-482">To move a scene, such as a map or photo, in two dimensions by dragging it directly.</span></span> <span data-ttu-id="e6b1b-483">Cela diffère de la défiler de deux manières : le contenu défilé a généralement une dimension dominante et fait souvent défiler uniquement le long de cette dimension ; et le contenu de défilement apparaît conventionnellement avec des barres de défilement que l’utilisateur fait glisser dans la direction opposée du mouvement de défilement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-483">This differs from scrolling in two ways: scrolled content usually has one predominant dimension and often scrolls only along that dimension; and scrolling content conventionally appears with scroll bars that the user drags in the opposite direction of the scrolling motion.</span></span>

<span data-ttu-id="e6b1b-484">**propane**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-484">**pane**</span></span>

<span data-ttu-id="e6b1b-485">Zone rectangulaire dans une fenêtre que les utilisateurs peuvent être en mesure de déplacer, redimensionner, masquer ou fermer.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-485">A rectangular area within a window that users may be able to move, resize, hide, or close.</span></span> <span data-ttu-id="e6b1b-486">Les volets sont toujours ancrés sur le côté de leur fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-486">Panes are always docked to the side of their parent window.</span></span> <span data-ttu-id="e6b1b-487">Ils peuvent être adjacents à d’autres volets, mais ils ne se chevauchent jamais.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-487">They can be adjacent to other panes, but they never overlap.</span></span> <span data-ttu-id="e6b1b-488">La désancrage d’un volet le convertit en fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-488">Undocking a pane converts it to a child window.</span></span> <span data-ttu-id="e6b1b-489">Voir aussi : [fenêtre](#w).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-489">See also: [window](#w).</span></span>

<span data-ttu-id="e6b1b-490">**fenêtre parente**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-490">**parent window**</span></span>

<span data-ttu-id="e6b1b-491">Conteneur de fenêtres enfants (tels que les contrôles ou les volets).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-491">The container of child windows (such as controls or panes).</span></span> <span data-ttu-id="e6b1b-492">Voir aussi : [fenêtre propriétaire](#o).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-492">See also: [owner window](#o).</span></span>

<span data-ttu-id="e6b1b-493">**pénétration**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-493">**pen**</span></span>

<span data-ttu-id="e6b1b-494">Stylet utilisé pour le pointage, les gestes, l’entrée de texte simple et l’écriture manuscrite de forme libre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-494">A stylus used for pointing, gestures, simple text entry, and free-form handwriting.</span></span> <span data-ttu-id="e6b1b-495">Les plumes ont une astuce fine qui prend en charge le pointage, l’écriture ou le dessin précis de l’encre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-495">Pens have a fine, smooth tip that supports precise pointing, writing, or drawing in ink.</span></span> <span data-ttu-id="e6b1b-496">Ils peuvent également avoir un bouton de stylet facultatif (utilisé pour effectuer un clic droit) et un gomme (utilisé pour effacer l’encre).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-496">They may also have an optional pen button (used to perform right-clicks) and eraser (used to erase ink).</span></span>

<span data-ttu-id="e6b1b-497">**persistance**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-497">**persistence**</span></span>

<span data-ttu-id="e6b1b-498">Principe selon lequel l’État ou les propriétés d’un objet sont conservés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-498">The principle that the state or properties of an object is automatically preserved.</span></span>

<span data-ttu-id="e6b1b-499">**réalisée**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-499">**personalization**</span></span>

<span data-ttu-id="e6b1b-500">Personnalisation d’une expérience de base cruciale pour l’identification personnelle de l’utilisateur avec un programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-500">Customizing a core experience that is crucial to the user's personal identification with a program.</span></span> <span data-ttu-id="e6b1b-501">En revanche, les options et les propriétés ordinaires ne sont pas essentielles à l’identification personnelle de l’utilisateur avec un programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-501">By contrast, ordinary options and properties aren't crucial to the user's personal identification with a program.</span></span>

<span data-ttu-id="e6b1b-502">**personnes**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-502">**personas**</span></span>

<span data-ttu-id="e6b1b-503">Description détaillée des personnes imaginaires.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-503">Detailed descriptions of imaginary people.</span></span> <span data-ttu-id="e6b1b-504">Les personnages sont construits à partir de données bien comprises et fortement spécifiées sur les véritables gens.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-504">Personas are constructed out of well-understood, highly specified data about real people.</span></span>

<span data-ttu-id="e6b1b-505">**résolution physique**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-505">**physical resolution**</span></span>

<span data-ttu-id="e6b1b-506">Pixels horizontaux et verticaux qui peuvent être affichés par le matériel d’un moniteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-506">The horizontal and vertical pixels that can be displayed by a computer monitor's hardware.</span></span>

<span data-ttu-id="e6b1b-507">**bouton de groupe contextuel**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-507">**pop-up group button**</span></span>

<span data-ttu-id="e6b1b-508">Dans un ruban, bouton de menu qui consolide toutes les commandes et options au sein d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-508">In a ribbon, a menu button that consolidates all the commands and options within a group.</span></span> <span data-ttu-id="e6b1b-509">Utilisé pour afficher des rubans dans de petits espaces.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-509">Used to display ribbons in small spaces.</span></span>

<span data-ttu-id="e6b1b-510">**mode portrait**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-510">**portrait mode**</span></span>

<span data-ttu-id="e6b1b-511">Option de présentation qui oriente un objet pour qu’il soit plus haut que grand.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-511">A presentation option that orients an object to be taller than it is wide.</span></span> <span data-ttu-id="e6b1b-512">Voir aussi : [mode paysage](#l).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-512">See also: [landscape mode](#l).</span></span>

<span data-ttu-id="e6b1b-513">**préférences**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-513">**preferences**</span></span>

<span data-ttu-id="e6b1b-514">N’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-514">Don't use.</span></span> <span data-ttu-id="e6b1b-515">Utilisez des [options](#o) ou des propriétés à la place.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-515">Use [options](#o) or properties instead.</span></span>

<span data-ttu-id="e6b1b-516">**préversion**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-516">**preview**</span></span>

<span data-ttu-id="e6b1b-517">Représentation de ce que les utilisateurs verront lorsqu’ils sélectionneront une option.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-517">A representation of what users will see when they select an option.</span></span> <span data-ttu-id="e6b1b-518">Les aperçus peuvent être affichés de manière statique dans le cadre de l’option, ou à la demande avec un bouton d’aperçu ou d’application.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-518">Previews can be displayed statically as part of the option, or upon request with a Preview or Apply button.</span></span>

<span data-ttu-id="e6b1b-519">**volet de visualisation**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-519">**preview pane**</span></span>

<span data-ttu-id="e6b1b-520">Volet de fenêtre utilisé pour afficher des aperçus et d’autres données sur les objets sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-520">A window pane used to show previews and other data about selected objects.</span></span>

<span data-ttu-id="e6b1b-521">**commande principale**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-521">**primary command**</span></span>

<span data-ttu-id="e6b1b-522">Action centrale qui respecte l’objectif principal d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-522">A central action that fulfills the primary purpose of a window.</span></span> <span data-ttu-id="e6b1b-523">Par exemple, l’option imprimer est une commande principale pour une boîte de dialogue Imprimer.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-523">For example, Print is a primary command for a Print dialog box.</span></span> <span data-ttu-id="e6b1b-524">Voir aussi : [commande secondaire](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-524">See also: [secondary command](#s).</span></span>

<span data-ttu-id="e6b1b-525">**barre d’outils principale**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-525">**primary toolbar**</span></span>

<span data-ttu-id="e6b1b-526">Collection de commandes conçues pour être suffisamment complètes pour empêcher l’utilisation d’une barre de menus.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-526">A collection of commands designed to be comprehensive enough to preclude the use of a menu bar.</span></span> <span data-ttu-id="e6b1b-527">Voir aussi : [barre d’outils supplémentaires](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-527">See also: [supplemental toolbar](#s).</span></span>

<span data-ttu-id="e6b1b-528">**fenêtre principale**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-528">**primary window**</span></span>

<span data-ttu-id="e6b1b-529">Une fenêtre principale n’a pas de fenêtre propriétaire et est affichée dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-529">A primary window has no owner window and is displayed on the taskbar.</span></span> <span data-ttu-id="e6b1b-530">Les fenêtres principales du programme sont toujours les fenêtres principales.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-530">Main program windows are always primary windows.</span></span> <span data-ttu-id="e6b1b-531">Voir aussi : [fenêtre secondaire](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-531">See also: [secondary window](#s).</span></span>

<span data-ttu-id="e6b1b-532">**table**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-532">**program**</span></span>

<span data-ttu-id="e6b1b-533">Séquence d’instructions qui peuvent être exécutées par un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-533">A sequence of instructions that can be executed by a computer.</span></span> <span data-ttu-id="e6b1b-534">Les types de programmes courants sont les applications de productivité, les applications grand public, les jeux, les bornes et les utilitaires.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-534">Common types of programs include productivity applications, consumer applications, games, kiosks, and utilities.</span></span>

<span data-ttu-id="e6b1b-535">**barre de progression**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-535">**progress bar**</span></span>

<span data-ttu-id="e6b1b-536">Contrôle Windows commun qui affiche la progression d’une opération particulière sous la forme d’une barre graphique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-536">A common Windows control that displays the progress of a particular operation as a graphical bar.</span></span>

<span data-ttu-id="e6b1b-537">**Divulgation progressive**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-537">**progressive disclosure**</span></span>

<span data-ttu-id="e6b1b-538">Technique permettant aux utilisateurs d’afficher des informations moins couramment utilisées (en général, des données, des options ou des commandes) en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-538">A technique of allowing users to display less commonly used information (typically, data, options, or commands) as needed.</span></span> <span data-ttu-id="e6b1b-539">Par exemple, si d’autres options sont parfois nécessaires, les utilisateurs peuvent les exposer en contexte en cliquant sur un bouton de Chevron.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-539">For example, if more options are sometimes needed, users can expose them in context by clicking a chevron button.</span></span>

<span data-ttu-id="e6b1b-540">**escalade progressive**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-540">**progressive escalation**</span></span>

<span data-ttu-id="e6b1b-541">Séquence dans laquelle l’interface utilisateur utilisée pour informer les utilisateurs devient progressivement plus discrète lorsque l’événement devient plus critique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-541">A sequence in which the UI used to inform users becomes progressively more obtrusive as the event becomes more critical.</span></span> <span data-ttu-id="e6b1b-542">Par exemple, une notification peut être utilisée pour un événement que les utilisateurs peuvent ignorer au préalable en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-542">For example, a notification can be used for an event that users can safely ignore at first.</span></span> <span data-ttu-id="e6b1b-543">À mesure que la situation devient critique, une interface utilisateur plus discrète comme une boîte de dialogue modale doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-543">As the situation becomes critical, a more obtrusive UI such as a modal dialog should be used.</span></span>

<span data-ttu-id="e6b1b-544">**prompt**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-544">**prompt**</span></span>

<span data-ttu-id="e6b1b-545">Étiquette ou brève instruction placée à l’intérieur d’une zone de texte ou d’une liste déroulante modifiable comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-545">A label or short instruction placed inside a text box or editable drop-down list as its default value.</span></span> <span data-ttu-id="e6b1b-546">Contrairement au texte statique, les invites disparaissent une fois que les utilisateurs ont tapé un texte dans le contrôle ou qu’il obtient le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-546">Unlike static text, prompts disappear once users type something into the control or it gets input focus.</span></span>

<span data-ttu-id="e6b1b-547">**properties**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-547">**properties**</span></span>

<span data-ttu-id="e6b1b-548">Paramètres d’un objet que les utilisateurs peuvent modifier, tels que le nom d’un fichier et l’État en lecture seule, ainsi que les attributs d’un objet que les utilisateurs ne peuvent pas modifier directement, tels que la date de création et la taille d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-548">Settings of an object that users can change, such as a file's name and read-only status, as well as attributes of an object that users can't directly change, such as a file's size and creation date.</span></span> <span data-ttu-id="e6b1b-549">En général, les propriétés définissent l’État, la valeur ou l’apparence d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-549">Typically properties define the state, value, or appearance of an object.</span></span>

<span data-ttu-id="e6b1b-550">**administrateur protégé**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-550">**protected administrator**</span></span>

<span data-ttu-id="e6b1b-551">Dans le contrôle de compte d’utilisateur, administrateur s’exécutant dans l’état le moins privilégié.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-551">In User Account Control, an administrator running in their least-privileged state.</span></span> <span data-ttu-id="e6b1b-552">Voir aussi : [administrateur avec élévation de privilèges](#e), [utilisateur standard](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-552">See also: [elevated administrator](#e), [standard user](#s).</span></span>

## <a name="q"></a><span data-ttu-id="e6b1b-553">Q</span><span class="sxs-lookup"><span data-stu-id="e6b1b-553">Q</span></span>

<span data-ttu-id="e6b1b-554">**Barre d’outils accès rapide**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-554">**Quick Access Toolbar**</span></span>

<span data-ttu-id="e6b1b-555">Une petite barre d’outils personnalisable qui affiche les commandes fréquemment utilisées.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-555">A small, customizable toolbar that displays frequently used commands.</span></span>

<span data-ttu-id="e6b1b-556">**Barre lancement rapide**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-556">**Quick Launch bar**</span></span>

<span data-ttu-id="e6b1b-557">Point d’accès direct sur le bureau Windows, situé en regard du bouton Démarrer, renseigné avec des icônes pour les programmes choisis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-557">A direct access point on the Windows desktop, located next to the Start button, populated with icons for programs of the user's choosing.</span></span> <span data-ttu-id="e6b1b-558">Supprimé dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-558">Removed in Windows 7.</span></span>

## <a name="r"></a><span data-ttu-id="e6b1b-559">R</span><span class="sxs-lookup"><span data-stu-id="e6b1b-559">R</span></span>

<span data-ttu-id="e6b1b-560">**case d’option**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-560">**radio button**</span></span>

<span data-ttu-id="e6b1b-561">Contrôle Windows commun qui permet aux utilisateurs de choisir parmi un ensemble de choix s’excluant mutuellement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-561">A common Windows control that allow users to select from among a set of mutually exclusive, related choices.</span></span>

<span data-ttu-id="e6b1b-562">**pixels relatifs**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-562">**relative pixels**</span></span>

<span data-ttu-id="e6b1b-563">Métrique indépendante du périphérique qui est identique à un pixel physique à 96 ppp (points par pouce), mais mis à l’échelle proportionnellement dans d’autres DPI.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-563">A device-independent metric that is the same as a physical pixel at 96 dpi (dots per inch), but proportionately scaled in other dpis.</span></span> <span data-ttu-id="e6b1b-564">Voir aussi : [résolution efficace](#e).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-564">See also: [effective resolution](#e).</span></span>

<span data-ttu-id="e6b1b-565">**fenêtre restaurée**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-565">**restored window**</span></span>

<span data-ttu-id="e6b1b-566">Fenêtre d’écran partielle visible, ni agrandie, ni réduite.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-566">A visible, partial-screen window, neither maximized nor minimized.</span></span> <span data-ttu-id="e6b1b-567">Voir aussi : [agrandir](#m), réduire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-567">See also: [maximize](#m), minimize.</span></span>

<span data-ttu-id="e6b1b-568">**dernier**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-568">**ribbon**</span></span>

<span data-ttu-id="e6b1b-569">Conteneur avec onglets de commandes et d’options, situé en haut d’une fenêtre ou d’une zone de travail et ayant un emplacement fixe et une hauteur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-569">A tabbed container of commands and options, located at the top of a window or work area and having a fixed location and height.</span></span> <span data-ttu-id="e6b1b-570">Les rubans comportent généralement un menu d’application et une barre d’outils accès rapide.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-570">Ribbons usually have an Application menu and Quick Access Toolbar.</span></span> <span data-ttu-id="e6b1b-571">Voir aussi : [menu](#m), [barre d’outils](#t).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-571">See also: [menu](#m), [toolbar](#t).</span></span>

<span data-ttu-id="e6b1b-572">**action risquée**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-572">**risky action**</span></span>

<span data-ttu-id="e6b1b-573">Une qualité d’action de l’utilisateur qui peut avoir des conséquences négatives et ne peut pas être facilement annulée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-573">A quality of user action that can have negative consequences and can't be easily undone.</span></span> <span data-ttu-id="e6b1b-574">Les actions risquées incluent des actions qui peuvent nuire à la sécurité d’un ordinateur, affecter l’accès à un ordinateur ou entraîner une perte de données involontaire.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-574">Risky actions include actions that can harm the security of a computer, affect access to a computer, or result in unintended loss of data.</span></span>

## <a name="s"></a><span data-ttu-id="e6b1b-575">S</span><span class="sxs-lookup"><span data-stu-id="e6b1b-575">S</span></span>

<span data-ttu-id="e6b1b-576">**chemin d’analyse**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-576">**scan path**</span></span>

<span data-ttu-id="e6b1b-577">Les utilisateurs de la route sont susceptibles d’effectuer une analyse pour localiser des éléments dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-577">The route users are likely to take as they scan to locate things in a window.</span></span> <span data-ttu-id="e6b1b-578">Particulièrement important si les utilisateurs ne sont pas engagés dans la lecture immersive du texte.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-578">Particularly important if users are not engaged in immersive reading of text.</span></span>

<span data-ttu-id="e6b1b-579">**lecteur d’écran**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-579">**screen reader**</span></span>

<span data-ttu-id="e6b1b-580">Une technologie d’assistance qui permet aux utilisateurs ayant des handicaps d’interpréter et de naviguer dans une interface utilisateur en transformant les éléments visuels en données audio.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-580">An assistive technology that enables users with visual impairments to interpret and navigate a user interface by transforming visuals to audio.</span></span> <span data-ttu-id="e6b1b-581">Ainsi, le texte, les contrôles, les menus, les barres d’outils, les graphiques et les autres éléments d’écran sont parlés par la voix informatisée du lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-581">Thus, text, controls, menus, toolbars, graphics, and other screen elements are spoken by the computerized voice of the screen reader.</span></span>

<span data-ttu-id="e6b1b-582">**barre de défilement**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-582">**scroll bar**</span></span>

<span data-ttu-id="e6b1b-583">Contrôle qui permet aux utilisateurs de faire défiler le contenu d’une fenêtre, verticalement ou horizontalement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-583">A control that allows users to scroll the content of a window, either vertically or horizontally.</span></span>

<span data-ttu-id="e6b1b-584">**commande secondaire**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-584">**secondary command**</span></span>

<span data-ttu-id="e6b1b-585">Une action périphérique qui, bien qu’utile, n’est pas essentielle à l’objectif de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-585">A peripheral action that, while helpful, isn't essential to the purpose of the window.</span></span> <span data-ttu-id="e6b1b-586">Par exemple, Rechercher l’imprimante ou installer l’imprimante sont des commandes secondaires pour une boîte de dialogue Imprimer.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-586">For example, Find Printer or Install Printer are secondary commands for a Print dialog box.</span></span> <span data-ttu-id="e6b1b-587">Voir aussi : [commande principale](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-587">See also: [primary command](#p).</span></span>

<span data-ttu-id="e6b1b-588">**fenêtre secondaire**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-588">**secondary window**</span></span>

<span data-ttu-id="e6b1b-589">Fenêtre qui a une fenêtre propriétaire et qui, par conséquent, n’est pas affichée dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-589">A window that has an owner window and consequently is not displayed on the taskbar.</span></span> <span data-ttu-id="e6b1b-590">Voir aussi : [fenêtre principale](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-590">See also: [primary window](#p).</span></span>

<span data-ttu-id="e6b1b-591">**Bureau sécurisé**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-591">**secure desktop**</span></span>

<span data-ttu-id="e6b1b-592">Environnement protégé qui est isolé des programmes en cours d’exécution sur le système, utilisé pour augmenter la sécurité des tâches hautement sécurisées telles que l’ouverture de session, les modifications de mot de passe et l’interface utilisateur d’élévation UAC.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-592">A protected environment that is isolated from programs running on the system, used to increase the security of highly secure tasks such as log on, password changes, and UAC Elevation UI.</span></span> <span data-ttu-id="e6b1b-593">Voir aussi : [contrôle de compte d’utilisateur](#u).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-593">See also: [User Account Control](#u).</span></span>

<span data-ttu-id="e6b1b-594">**Bouclier de sécurité**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-594">**security shield**</span></span>

<span data-ttu-id="e6b1b-595">Icône de blindage utilisée pour la personnalisation de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-595">A shield icon used for security branding.</span></span>

<span data-ttu-id="e6b1b-596">**sélectionné**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-596">**selected**</span></span>

<span data-ttu-id="e6b1b-597">Choisi par l’utilisateur pour effectuer une opération ; mise.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-597">Chosen by the user in order to perform an operation; highlighted.</span></span>

<span data-ttu-id="e6b1b-598">**majuscules de style de phrase**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-598">**sentence-style capitalization**</span></span>

<span data-ttu-id="e6b1b-599">Pour les majuscules de style phrase :</span><span class="sxs-lookup"><span data-stu-id="e6b1b-599">For sentence-style capitalization:</span></span>

-   <span data-ttu-id="e6b1b-600">Mettez toujours en majuscule le premier mot d’une nouvelle phrase.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-600">Always capitalize the first word of a new sentence.</span></span>
-   <span data-ttu-id="e6b1b-601">Ne mettez pas en majuscule le mot qui suit un signe deux-points, sauf si le mot est un nom propre ou si le texte qui suit le signe deux-points est une phrase complète.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-601">Don't capitalize the word following a colon unless the word is a proper noun, or the text following the colon is a complete sentence.</span></span>
-   <span data-ttu-id="e6b1b-602">N’mettez pas en majuscule le mot suivant un tiret cadratin, sauf s’il s’agit d’un nom propre, même si le texte qui suit le tiret est une phrase complète.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-602">Don't capitalize the word following an em-dash unless it is a proper noun, even if the text following the dash is a complete sentence.</span></span>
-   <span data-ttu-id="e6b1b-603">Mettez toujours en majuscule le premier mot d’une nouvelle phrase à la suite de la ponctuation finale.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-603">Always capitalize the first word of a new sentence following any end punctuation.</span></span> <span data-ttu-id="e6b1b-604">Réécrivez les phrases qui commencent par un mot en minuscules respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-604">Rewrite sentences that start with a case-sensitive lowercase word.</span></span>

<span data-ttu-id="e6b1b-605">**settings**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-605">**settings**</span></span>

<span data-ttu-id="e6b1b-606">Valeurs spécifiques qui ont été choisies (par l’utilisateur ou par défaut) pour configurer un programme ou un objet.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-606">Specific values that have been chosen (either by the user or by default) to configure a program or object.</span></span>

<span data-ttu-id="e6b1b-607">**touche de raccourci**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-607">**shortcut key**</span></span>

<span data-ttu-id="e6b1b-608">Clés ou combinaisons de touches que les utilisateurs peuvent appuyer pour accéder rapidement aux actions qu’ils effectuent fréquemment.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-608">Keys or key combinations that users can press for quick access to actions they perform frequently.</span></span> <span data-ttu-id="e6b1b-609">Les combinaisons CTRL + lettre et touches (F1 à F12) sont généralement les meilleures options pour les touches de raccourci.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-609">Ctrl+letter combinations and function keys (F1 through F12) are usually the best choices for shortcut keys.</span></span> <span data-ttu-id="e6b1b-610">Par définition, une touche de raccourci est l’équivalent du clavier des fonctionnalités prises en charge de manière adéquate ailleurs dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-610">By definition, a shortcut key is the keyboard equivalent of functionality that is supported adequately elsewhere in the interface.</span></span> <span data-ttu-id="e6b1b-611">Par conséquent, évitez d’utiliser une touche de raccourci comme seule façon d’accéder à une opération particulière.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-611">Therefore, avoid using a shortcut key as the only way to access a particular operation.</span></span>

<span data-ttu-id="e6b1b-612">Contrairement aux clés d’accès, qui sont conçues pour améliorer l’accessibilité, les touches de raccourci sont conçues principalement pour les utilisateurs expérimentés.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-612">In contrast to access keys, which are designed to improve accessibility, shortcut keys are designed primarily for advanced users.</span></span> <span data-ttu-id="e6b1b-613">Étant donné qu’ils ne sont pas documentés directement dans l’interface utilisateur proprement dite (même s’ils peuvent être documentés dans les menus et les info-bulles de barre d’outils), ils sont destinés à être mémorisés et doivent donc être attribués de manière cohérente dans les applications et dans les différentes applications.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-613">Because they aren't documented directly within the UI itself (although they might be documented in menus and toolbar tooltips), they are intended to be memorized and therefore they must be assigned consistently within applications and across different applications.</span></span>

<span data-ttu-id="e6b1b-614">**Encadré**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-614">**Sidebar**</span></span>

<span data-ttu-id="e6b1b-615">Une région sur le côté du Bureau de l’utilisateur, utilisée pour afficher les gadgets dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-615">A region on the side of the user's desktop used to display gadgets in Windows Vista.</span></span> <span data-ttu-id="e6b1b-616">Voir aussi : [gadget](#g).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-616">See also: [gadget](#g).</span></span>

<span data-ttu-id="e6b1b-617">**erreur de point unique**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-617">**single-point error**</span></span>

<span data-ttu-id="e6b1b-618">Erreur d’entrée utilisateur liée à un contrôle unique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-618">A user input error relating to a single control.</span></span> <span data-ttu-id="e6b1b-619">Par exemple, l’entrée d’un numéro de carte de crédit incorrect est une erreur à point unique, alors qu’une ouverture de session incorrecte est une erreur de double point, car le nom d’utilisateur ou le mot de passe peut être le problème.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-619">For example, entering an incorrect credit card number is a single-point error, whereas an incorrect logon is a double-point error, because either the user name or password could be the problem.</span></span>

<span data-ttu-id="e6b1b-620">**curseur**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-620">**slider**</span></span>

<span data-ttu-id="e6b1b-621">Contrôle Windows commun qui affiche et définit une valeur à partir d’une plage continue de valeurs possibles, telles que la luminosité ou le volume.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-621">A common Windows control that displays and sets a value from a continuous range of possible values, such as brightness or volume.</span></span>

<span data-ttu-id="e6b1b-622">**expérience spéciale**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-622">**special experience**</span></span>

<span data-ttu-id="e6b1b-623">Dans les programmes, les expériences spéciales sont liées à la fonction principale du programme, à un point unique sur le programme, ou à une connexion émotionnelle aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-623">In programs, special experiences relate to the primary function of the program, something unique about the program, or otherwise make an emotional connection to users.</span></span> <span data-ttu-id="e6b1b-624">Par exemple, la lecture d’un fichier audio ou vidéo est une expérience spéciale pour un lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-624">For example, playing an audio or video is a special experience for a media player.</span></span>

<span data-ttu-id="e6b1b-625">**zone de sélection numérique**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-625">**spin box**</span></span>

<span data-ttu-id="e6b1b-626">Combinaison d’une zone de texte et de son contrôle spin associé.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-626">The combination of a text box and its associated spin control.</span></span> <span data-ttu-id="e6b1b-627">Les utilisateurs cliquent sur la flèche vers le haut ou vers le bas d’une zone de sélection numérique pour augmenter ou diminuer une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-627">Users click the up or down arrow of a spin box to increase or decrease a numeric value.</span></span> <span data-ttu-id="e6b1b-628">Contrairement aux contrôles Slider, qui sont utilisés pour les quantités relatives, les zones de sélection numérique sont utilisées uniquement pour les valeurs numériques exactes et connues.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-628">Unlike slider controls, which are used for relative quantities, spin boxes are used only for exact, known numeric values.</span></span>

<span data-ttu-id="e6b1b-629">**contrôle spin**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-629">**spin control**</span></span>

<span data-ttu-id="e6b1b-630">Contrôle sur lequel les utilisateurs cliquent pour modifier les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-630">A control that users click to change values.</span></span> <span data-ttu-id="e6b1b-631">Les contrôles spin utilisent des flèches vers le haut et vers le bas pour augmenter ou diminuer la valeur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-631">Spin controls use up and down arrows to increase or decrease the value.</span></span>

<span data-ttu-id="e6b1b-632">**écran de démarrage**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-632">**splash screen**</span></span>

<span data-ttu-id="e6b1b-633">L’image de transition d’écran qui apparaît en tant que programme est en cours de lancement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-633">Transitional screen image that appears as a program is in the process of launching.</span></span>

<span data-ttu-id="e6b1b-634">**bouton partagé**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-634">**split button**</span></span>

<span data-ttu-id="e6b1b-635">Un bouton de commande bipartite qui comprend un petit bouton avec un triangle pointant vers le bas sur la partie la plus à droite du bouton principal.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-635">A bipartite command button that includes a small button with a downward pointing triangle on the rightmost portion of the main button.</span></span> <span data-ttu-id="e6b1b-636">Les utilisateurs cliquent sur le triangle pour afficher les variations d’une commande dans un menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-636">Users click the triangle to display variations of a command in a drop-down menu.</span></span> <span data-ttu-id="e6b1b-637">Voir aussi : [bouton de commande](#c).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-637">See also: [command button](#c).</span></span>

<span data-ttu-id="e6b1b-638">**page spoke**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-638">**spoke page**</span></span>

<span data-ttu-id="e6b1b-639">Dans les éléments du panneau de configuration, les pages spoke sont l’endroit où les utilisateurs effectuent des tâches.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-639">In control panel items, spoke pages are the place in which users perform tasks.</span></span> <span data-ttu-id="e6b1b-640">Deux types de pages spoke sont des pages de tâches et des pages de formulaire : les pages de tâches présentent une tâche ou une étape dans une tâche avec une instruction principale spécifique basée sur des tâches. les pages de formulaire présentent une collection de propriétés et de tâches associées basées sur une instruction principale générale.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-640">Two types of spoke pages are task pages and form pages: task pages present a task or a step in a task with a specific, task-based main instruction; form pages present a collection of related properties and tasks based on a general main instruction.</span></span> <span data-ttu-id="e6b1b-641">Voir aussi : [page Hub](#h).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-641">See also: [hub page](#h).</span></span>

<span data-ttu-id="e6b1b-642">**utilisateur standard**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-642">**standard user**</span></span>

<span data-ttu-id="e6b1b-643">Dans le contrôle de compte d’utilisateur, les utilisateurs standard disposent des privilèges minimum sur l’ordinateur et doivent demander l’autorisation à un administrateur sur l’ordinateur pour effectuer des tâches d’administration.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-643">In User Account Control, standard users have the least privileges on the computer, and must request permission from an administrator on the computer in order to perform administrative tasks.</span></span> <span data-ttu-id="e6b1b-644">Contrairement aux administrateurs protégés, les utilisateurs standard ne peuvent pas s’élever eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-644">In contrast with protected administrators, standard users can't elevate themselves.</span></span> <span data-ttu-id="e6b1b-645">Voir aussi : [administrateur avec élévation de privilèges](#e), [administrateur protégé](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-645">See also: [elevated administrator](#e), [protected administrator](#p).</span></span>

<span data-ttu-id="e6b1b-646">**texte statique**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-646">**static text**</span></span>

<span data-ttu-id="e6b1b-647">Texte de l’interface utilisateur qui ne fait pas partie d’un contrôle interactif.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-647">User interface text that is not part of an interactive control.</span></span> <span data-ttu-id="e6b1b-648">Comprend des étiquettes, des instructions principales, des instructions supplémentaires et des explications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-648">Includes labels, main instructions, supplemental instructions, and supplemental explanations.</span></span>

<span data-ttu-id="e6b1b-649">**instructions supplémentaires**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-649">**supplemental instructions**</span></span>

<span data-ttu-id="e6b1b-650">Forme facultative de texte d’interface utilisateur qui ajoute des informations, des détails ou un contexte à l’instruction principale.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-650">An optional form of user interface text that adds information, detail, or context to the main instruction.</span></span> <span data-ttu-id="e6b1b-651">Voir aussi : [instruction principale](#m).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-651">See also: [main instruction](#m).</span></span>

<span data-ttu-id="e6b1b-652">**barre d’outils supplémentaire**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-652">**supplemental toolbar**</span></span>

<span data-ttu-id="e6b1b-653">Collection de commandes conçue pour fonctionner conjointement avec une barre de menus.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-653">A collection of commands designed to work in conjunction with a menu bar.</span></span> <span data-ttu-id="e6b1b-654">Voir aussi : [barre d’outils principale](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-654">See also: [primary toolbar](#p).</span></span>

<span data-ttu-id="e6b1b-655">**couleur système**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-655">**system color**</span></span>

<span data-ttu-id="e6b1b-656">Couleur définie par Windows dans un but spécifique, accessible à l’aide de l’interface de programmation d’applications (API) GetSysColor.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-656">A color defined by Windows for a specific purpose, accessed using the GetSysColor application programming interface (API).</span></span> <span data-ttu-id="e6b1b-657">Par exemple, \_ la fenêtre couleur définit la couleur et la couleur d’arrière-plan de la fenêtre \_ WINDOWTEXT définit la couleur du texte de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-657">For example, COLOR\_WINDOW defines the window background color and COLOR\_WINDOWTEXT defines the window text color.</span></span> <span data-ttu-id="e6b1b-658">Les couleurs système ne sont pas aussi riches que les couleurs de thème.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-658">System colors are not as rich as theme colors.</span></span> <span data-ttu-id="e6b1b-659">Voir aussi : [couleur de thème](#t).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-659">See also: [theme color](#t).</span></span>

<span data-ttu-id="e6b1b-660">**menu système**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-660">**system menu**</span></span>

<span data-ttu-id="e6b1b-661">Collection de commandes de fenêtre de base, telles que déplacer, dimensionner, agrandir, réduire et fermer, disponibles à partir de l’icône de programme dans la barre de titre, ou en cliquant avec le bouton droit sur un bouton de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-661">A collection of basic window commands, such as move, size, maximize, minimize, and close, available from the program icon on the title bar, or by right-clicking a taskbar button.</span></span>

## <a name="t"></a><span data-ttu-id="e6b1b-662">T</span><span class="sxs-lookup"><span data-stu-id="e6b1b-662">T</span></span>

<span data-ttu-id="e6b1b-663">**boîte de dialogue à onglets**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-663">**tabbed dialog**</span></span>

<span data-ttu-id="e6b1b-664">Boîte de dialogue qui contient des informations connexes sur des pages étiquetées distinctes (onglets).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-664">A dialog box that contains related information on separate labeled pages (tabs).</span></span> <span data-ttu-id="e6b1b-665">Contrairement aux feuilles de propriétés, qui contiennent également souvent des tabulations, les boîtes de dialogue à onglets ne sont pas utilisées pour afficher les propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-665">Unlike property sheets, which also often contain tabs, tabbed dialog boxes are not used to display an object's properties.</span></span> <span data-ttu-id="e6b1b-666">Voir aussi : [Propriétés](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-666">See also: [properties](#p).</span></span>

<span data-ttu-id="e6b1b-667">**tâche**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-667">**task**</span></span>

<span data-ttu-id="e6b1b-668">Unité d’activité utilisateur, souvent représentée par une seule surface d’interface utilisateur (par exemple, une boîte de dialogue) ou une séquence de pages (par exemple, un Assistant).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-668">A unit of user activity, often represented by a single UI surface (such as a dialog box), or a sequence of pages (such as a wizard).</span></span>

<span data-ttu-id="e6b1b-669">**boîte de dialogue de tâches**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-669">**task dialog**</span></span>

<span data-ttu-id="e6b1b-670">Boîte de dialogue implémentée à l’aide de l’API de la boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-670">A dialog box implemented using the task dialog API.</span></span> <span data-ttu-id="e6b1b-671">Nécessite Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-671">Requires Windows Vista or later.</span></span>

<span data-ttu-id="e6b1b-672">**déroulement des tâches**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-672">**task flow**</span></span>

<span data-ttu-id="e6b1b-673">Séquence de pages qui aide les utilisateurs à effectuer une tâche, qu’il s’agisse d’un Assistant, d’un explorateur ou d’un navigateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-673">A sequence of pages that helps users perform a task, either in a wizard, explorer, or browser.</span></span>

<span data-ttu-id="e6b1b-674">**lien de tâche**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-674">**task link**</span></span>

<span data-ttu-id="e6b1b-675">Un lien utilisé pour lancer une tâche, contrairement aux liens qui naviguent vers d’autres pages ou fenêtres, choisissez Options ou affichez l’aide.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-675">A link used to initiate a task, in contrast to links that navigate to other pages or windows, choose options, or display Help.</span></span>

<span data-ttu-id="e6b1b-676">**volet des tâches**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-676">**task pane**</span></span>

<span data-ttu-id="e6b1b-677">Type d’interface utilisateur semblable à une boîte de dialogue, à la différence qu’elle est présentée dans un volet de fenêtre plutôt que dans une fenêtre distincte.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-677">A type of UI similar to a dialog box, except that it is presented within a window pane instead of a separate window.</span></span> <span data-ttu-id="e6b1b-678">Par conséquent, les volets des tâches ont une apparence plus directe et contextuelle que les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-678">As a result, task panes have a more direct, contextual feel than dialog boxes.</span></span> <span data-ttu-id="e6b1b-679">Un volet de tâches peut contenir un menu pour fournir à l’utilisateur un petit ensemble de commandes liées à l’objet sélectionné ou au mode de programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-679">A task pane can contain a menu to provide the user with a small set of commands related to the selected object or program mode.</span></span>

<span data-ttu-id="e6b1b-680">**tâches**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-680">**taskbar**</span></span>

<span data-ttu-id="e6b1b-681">Point d’accès pour exécuter des programmes qui ont une présence sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-681">The access point for running programs that have a desktop presence.</span></span> <span data-ttu-id="e6b1b-682">Les utilisateurs interagissent avec les contrôles appelés boutons de la barre des tâches pour afficher, masquer et réduire les fenêtres de programme.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-682">Users interact with controls called taskbar buttons to show, hide, and minimize program windows.</span></span>

<span data-ttu-id="e6b1b-683">**zone de texte**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-683">**text box**</span></span>

<span data-ttu-id="e6b1b-684">Contrôle spécifiquement conçu pour l’entrée textuelle ; permet aux utilisateurs d’afficher, d’entrer ou de modifier du texte ou des nombres.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-684">A control specifically designed for textual input; allows users to view, enter, or edit text or numbers.</span></span>

<span data-ttu-id="e6b1b-685">**couleur du thème**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-685">**theme color**</span></span>

<span data-ttu-id="e6b1b-686">Couleur définie par Windows pour un usage spécifique, accessible à l’aide de l’API GetThemeColor avec des parties, des États et des couleurs.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-686">A color defined by Windows for a specific purpose, accessed using the GetThemeColor API along with parts, states, and colors.</span></span> <span data-ttu-id="e6b1b-687">Par exemple, la partie Windows définit un FillColor et un TextColor.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-687">For example, the windows part defines a FillColor and a TextColor.</span></span> <span data-ttu-id="e6b1b-688">Les couleurs de thème sont plus riches que les couleurs système, mais nécessitent l’exécution du service de thème.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-688">Theme colors are richer than system colors, but require the theme service to be running.</span></span> <span data-ttu-id="e6b1b-689">Voir aussi : [couleur système](#s).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-689">See also: [system color](#s).</span></span>

<span data-ttu-id="e6b1b-690">**titre-style de casse**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-690">**title-style capitalization**</span></span>

<span data-ttu-id="e6b1b-691">Pour la mise en majuscules du titre :</span><span class="sxs-lookup"><span data-stu-id="e6b1b-691">For title-style capitalization:</span></span>

-   <span data-ttu-id="e6b1b-692">Mettre en majuscules tous les noms, verbes (y compris les autres formes de), les adverbes (y compris et le cas), les adjectifs (y compris celui-ci) et les pronoms (y compris son).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-692">Capitalize all nouns, verbs (including is and other forms of to be), adverbs (including than and when), adjectives (including this and that), and pronouns (including its).</span></span>
-   <span data-ttu-id="e6b1b-693">Mettez en majuscule le premier et le dernier mot, indépendamment de leurs parties vocales (par exemple, le texte à rechercher).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-693">Capitalize the first and last words, regardless of their parts of speech (for example, The Text to Look For).</span></span>
-   <span data-ttu-id="e6b1b-694">Mettre en majuscule les prépositions qui font partie d’une expression verbale (par exemple, la sauvegarde de votre disque).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-694">Capitalize prepositions that are part of a verb phrase (for example, Backing Up Your Disk).</span></span>
-   <span data-ttu-id="e6b1b-695">Ne mettez pas en majuscule les articles (a, a, le), sauf si l’article est le premier mot du titre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-695">Don't capitalize articles (a, an, the), unless the article is the first word in the title.</span></span>
-   <span data-ttu-id="e6b1b-696">Ne pas mettre en majuscules les conjonctions de coordonnées (et, mais, pour, ou), sauf si la conjonction est le premier mot du titre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-696">Don't capitalize coordinate conjunctions (and, but, for, nor, or), unless the conjunction is the first word in the title.</span></span>
-   <span data-ttu-id="e6b1b-697">Ne pas mettre en majuscules les prépositions de quatre lettres ou moins, sauf si la préposition est le premier mot du titre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-697">Don't capitalize prepositions of four or fewer letters, unless the preposition is the first word in the title.</span></span>
-   <span data-ttu-id="e6b1b-698">Ne vous contentez pas d’une expression infinitive (par exemple, le formatage de votre disque dur), à moins que l’expression ne soit le premier mot du titre.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-698">Don't capitalize to in an infinitive phrase (for example, How to Format Your Hard Disk), unless the phrase is the first word in the title.</span></span>
-   <span data-ttu-id="e6b1b-699">Mettez en majuscule le deuxième mot dans les mots composés s’il s’agit d’un nom ou d’un adjectif approprié, un « e-Word » ou les mots ont le même poids (par exemple, le commerce électronique, les références croisées, les logiciels antérieurs à Microsoft, l’accès en lecture/écriture, l’exécution).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-699">Capitalize the second word in compound words if it is a noun or proper adjective, an "e-word," or the words have equal weight (for example, E-Commerce, Cross-Reference, Pre-Microsoft Software, Read/Write Access, Run-Time).</span></span> <span data-ttu-id="e6b1b-700">Ne mettez pas en majuscule le deuxième mot s’il s’agit d’une autre partie de la parole, telle qu’une préposition ou un autre mot secondaire (par exemple, complément, procédure, prise de vue).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-700">Do not capitalize the second word if it is another part of speech, such as a preposition or other minor word (for example, Add-in, How-to, Take-off).</span></span>
-   <span data-ttu-id="e6b1b-701">Mettez en majuscule l’interface utilisateur et les termes de l’interface de programmation d’applications que vous ne devriez généralement pas mettre en majuscules, à moins qu’ils respectent la casse (par exemple, la commande FDISK).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-701">Capitalize user interface and application programming interface terms that you would not ordinarily capitalize, unless they are case-sensitive (for example, The fdisk Command).</span></span> <span data-ttu-id="e6b1b-702">Suivez la casse traditionnelle des mots clés et d’autres termes spéciaux dans les langages de programmation (par exemple, la fonction printf, à l’aide des directives pair et ALIGN).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-702">Follow the traditional capitalization of keywords and other special terms in programming languages (for example, The printf Function, Using the EVEN and ALIGN Directives).</span></span>
-   <span data-ttu-id="e6b1b-703">Mettre en majuscules uniquement le premier mot de chaque en-tête de colonne.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-703">Capitalize only the first word of each column heading.</span></span>

<span data-ttu-id="e6b1b-704">**barre**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-704">**toolbar**</span></span>

<span data-ttu-id="e6b1b-705">Présentation graphique des commandes optimisées pour un accès efficace.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-705">A graphical presentation of commands optimized for efficient access.</span></span>

<span data-ttu-id="e6b1b-706">**bulle**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-706">**tooltip**</span></span>

<span data-ttu-id="e6b1b-707">Petite fenêtre contextuelle qui étiquette le contrôle sans étiquette désigné, par exemple les contrôles de barre d’outils sans étiquette ou les boutons de commande.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-707">A small pop-up window that labels the unlabeled control being pointed to, such as unlabeled toolbar controls or command buttons.</span></span>

<span data-ttu-id="e6b1b-708">**interface**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-708">**touch**</span></span>

<span data-ttu-id="e6b1b-709">Interaction directe avec un écran d’ordinateur à l’aide d’un doigt.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-709">Direct interaction with a computer display using a finger.</span></span>

## <a name="u"></a><span data-ttu-id="e6b1b-710">U</span><span class="sxs-lookup"><span data-stu-id="e6b1b-710">U</span></span>

<span data-ttu-id="e6b1b-711">**étude de la convivialité**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-711">**usability study**</span></span>

<span data-ttu-id="e6b1b-712">Technique de recherche qui vous aide à améliorer votre expérience utilisateur en testant la conception de votre interface utilisateur et en recueillant des commentaires à partir d’utilisateurs cibles réels.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-712">A research technique that helps you improve your user experience by testing your UI design and gathering feedback from real target users.</span></span> <span data-ttu-id="e6b1b-713">Les études de convivialité peuvent aller des techniques formelles dans des paramètres tels que les laboratoires de convivialité aux techniques informelles dans des paramètres tels que le Bureau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-713">Usability studies can range from formal techniques in settings such as usability labs, to informal techniques in settings such as the user's own office.</span></span> <span data-ttu-id="e6b1b-714">Toutefois, les constantes de ces études sont les suivantes : capture d’informations auprès des participants ; l’évaluation de ces informations pour des tendances et des modèles significatifs ; Enfin, implémenter des modifications logiques qui résolvent les problèmes identifiés dans l’étude.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-714">But the constants of such studies are: capturing information from the participants; evaluating that information for meaningful trends and patterns; and finally implementing logical changes that address the problems identified in the study.</span></span>

<span data-ttu-id="e6b1b-715">**Contrôle de compte d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-715">**User Account Control**</span></span>

<span data-ttu-id="e6b1b-716">Avec le contrôle de compte d’utilisateur (ou le contrôle de compte d’utilisateur, anciennement « compte d’utilisateur avec privilèges minimum » ou LUA) activé, les administrateurs interactifs s’exécutent normalement avec le moins de privilèges utilisateur, mais ils peuvent s’élever automatiquement pour effectuer des tâches d’administration en donnant un consentement explicite avec l’interface utilisateur de consentement.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-716">With User Account Control (or UAC, formerly known as "Least-privilege User Account," or LUA) enabled, interactive administrators normally run with least user privileges, but they can self-elevate to perform administrative tasks by giving explicit consent with the Consent UI.</span></span> <span data-ttu-id="e6b1b-717">Ces tâches d’administration incluent l’installation de logiciels et de pilotes, la modification des paramètres au niveau du système, l’affichage ou la modification d’autres comptes d’utilisateur et l’exécution d’outils d’administration.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-717">Such administrative tasks include installing software and drivers, changing system-wide settings, viewing or changing other user accounts, and running administrative tools.</span></span>

<span data-ttu-id="e6b1b-718">**Blindage du contrôle de compte d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-718">**User Account Control shield**</span></span>

<span data-ttu-id="e6b1b-719">Icône de bouclier utilisée pour indiquer qu’une commande ou une option requiert une élévation pour le contrôle de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-719">A shield icon used to indicate that a command or option needs elevation for User Account Control.</span></span>

<span data-ttu-id="e6b1b-720">**problème d’entrée d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-720">**user input problem**</span></span>

<span data-ttu-id="e6b1b-721">Erreur résultant d’une entrée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-721">An error resulting from user input.</span></span> <span data-ttu-id="e6b1b-722">Les problèmes d’entrée d’utilisateur ne sont généralement pas critiques, car ils doivent être corrigés avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-722">User input problems are usually non-critical because they must be corrected before proceeding.</span></span>

<span data-ttu-id="e6b1b-723">**scénario utilisateur**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-723">**user scenario**</span></span>

<span data-ttu-id="e6b1b-724">Description d’un objectif d’utilisateur, d’un problème ou d’une tâche dans un ensemble spécifique de circonstances.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-724">A description of a user goal, problem, or task in a specific set of circumstances.</span></span>

## <a name="v"></a><span data-ttu-id="e6b1b-725">V</span><span class="sxs-lookup"><span data-stu-id="e6b1b-725">V</span></span>

## <a name="w"></a><span data-ttu-id="e6b1b-726">W</span><span class="sxs-lookup"><span data-stu-id="e6b1b-726">W</span></span>

<span data-ttu-id="e6b1b-727">**warning**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-727">**warning**</span></span>

<span data-ttu-id="e6b1b-728">Message qui décrit une condition susceptible de provoquer un problème à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-728">A message that describes a condition that might cause a problem in the future.</span></span> <span data-ttu-id="e6b1b-729">Les avertissements ne sont pas des erreurs ou des questions.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-729">Warnings aren't errors or questions.</span></span> <span data-ttu-id="e6b1b-730">Dans Windows Vista et versions ultérieures, les messages d’avertissement s’affichent généralement dans les boîtes de dialogue de tâches, incluent une instruction principale claire et concise, et incluent généralement une icône d’avertissement standard pour le renforcement visuel du texte.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-730">In Windows Vista and later, warning messages are typically displayed in task dialogs, include a clear, concise main instruction, and usually include a standard warning icon for visual reinforcement of the text.</span></span>

<span data-ttu-id="e6b1b-731">**Page d’accueil**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-731">**welcome page**</span></span>

<span data-ttu-id="e6b1b-732">Première page d’un Assistant, utilisée pour expliquer l’objectif de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-732">The first page of a wizard, used to explain the purpose of the wizard.</span></span> <span data-ttu-id="e6b1b-733">Les pages d’accueil ne sont plus recommandées.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-733">Welcome pages are no longer recommended.</span></span> <span data-ttu-id="e6b1b-734">Les utilisateurs bénéficient d’une expérience plus efficace sans ces pages.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-734">Users have a more efficient experience without such pages.</span></span>

<span data-ttu-id="e6b1b-735">**fenetre**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-735">**window**</span></span>

<span data-ttu-id="e6b1b-736">Zone rectangulaire sur un écran d’ordinateur dans laquelle les programmes et le contenu s’affichent.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-736">A rectangular area on a computer screen in which programs and content appear.</span></span> <span data-ttu-id="e6b1b-737">Une fenêtre peut être déplacée, redimensionnée, réduite ou fermée ; Il peut chevaucher d’autres fenêtres.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-737">A window can be moved, resized, minimized, or closed; it can overlap other windows.</span></span> <span data-ttu-id="e6b1b-738">L’ancrage d’une fenêtre enfant la convertit en un volet.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-738">Docking a child window converts it to a pane.</span></span> <span data-ttu-id="e6b1b-739">Voir aussi : [volet](#p).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-739">See also: [pane](#p).</span></span>

<span data-ttu-id="e6b1b-740">**Touche Windows**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-740">**Windows logo key**</span></span>

<span data-ttu-id="e6b1b-741">Touche de modification avec le logo Windows.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-741">A modifier key with the Windows logo on it.</span></span> <span data-ttu-id="e6b1b-742">Cette clé est utilisée pour un certain nombre de raccourcis Windows et est réservée à l’utilisation de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-742">This key is used for a number of Windows shortcuts, and is reserved for Windows use.</span></span> <span data-ttu-id="e6b1b-743">Par exemple, si vous appuyez sur la touche Windows, vous affichez ou masquez le menu Démarrer de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-743">For example, pressing the Windows logo key displays or hides the Windows Start menu.</span></span>

<span data-ttu-id="e6b1b-744">**des maquettes**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-744">**wireframes**</span></span>

<span data-ttu-id="e6b1b-745">Maquette d’interface utilisateur qui affiche les fonctionnalités et la mise en page d’une fenêtre, mais pas son apparence terminée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-745">A UI mockup that shows a window's functionality and layout, but not its finished appearance.</span></span> <span data-ttu-id="e6b1b-746">Un filaire utilise uniquement des segments de ligne, des contrôles et du texte, sans couleurs, graphiques complexes, ou l’utilisation de thèmes.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-746">A wireframe uses only line segments, controls, and text, without color, complex graphics, or the use of themes.</span></span>

<span data-ttu-id="e6b1b-747">**création**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-747">**wizard**</span></span>

<span data-ttu-id="e6b1b-748">Séquence de pages qui guide les utilisateurs dans une tâche à plusieurs étapes, rarement exécutée.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-748">A sequence of pages that guides users through a multi-step, infrequently performed task.</span></span> <span data-ttu-id="e6b1b-749">Les assistants efficaces réduisent les connaissances requises pour effectuer la tâche par rapport aux autres interfaces utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-749">Effective wizards reduce the knowledge required to perform the task compared to alternative UIs.</span></span>

<span data-ttu-id="e6b1b-750">**Zone de travail**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-750">**work area**</span></span>

<span data-ttu-id="e6b1b-751">Zone à l’écran où les utilisateurs peuvent effectuer leur travail, ainsi que pour stocker des programmes, des documents et leurs raccourcis.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-751">The onscreen area where users can perform their work, as well as store programs, documents, and their shortcuts.</span></span> <span data-ttu-id="e6b1b-752">Voir aussi : [Bureau](#d).</span><span class="sxs-lookup"><span data-stu-id="e6b1b-752">See also: [desktop](#d).</span></span>

## <a name="x"></a><span data-ttu-id="e6b1b-753">X</span><span class="sxs-lookup"><span data-stu-id="e6b1b-753">X</span></span>

## <a name="y"></a><span data-ttu-id="e6b1b-754">O</span><span class="sxs-lookup"><span data-stu-id="e6b1b-754">Y</span></span>

## <a name="z"></a><span data-ttu-id="e6b1b-755">Z</span><span class="sxs-lookup"><span data-stu-id="e6b1b-755">Z</span></span>

<span data-ttu-id="e6b1b-756">**Ordre de plan**</span><span class="sxs-lookup"><span data-stu-id="e6b1b-756">**Z order**</span></span>

<span data-ttu-id="e6b1b-757">Relation en couches des fenêtres sur l’affichage.</span><span class="sxs-lookup"><span data-stu-id="e6b1b-757">The layered relationship of windows on the display.</span></span>

 

 
