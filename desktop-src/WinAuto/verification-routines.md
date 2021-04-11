---
title: Routines de vérification
description: Cette section décrit les routines de vérification que l’outil de vérification de l’accessibilité de l’interface utilisateur peut exécuter pour tester l’implémentation de l’accessibilité d’une application.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310149"
---
# <a name="verification-routines"></a><span data-ttu-id="ced37-103">Routines de vérification</span><span class="sxs-lookup"><span data-stu-id="ced37-103">Verification Routines</span></span>

<span data-ttu-id="ced37-104">Cette section décrit les routines de vérification que l’outil de vérification de l’accessibilité de l’interface utilisateur peut exécuter pour tester l’implémentation de l’accessibilité d’une application.</span><span class="sxs-lookup"><span data-stu-id="ced37-104">This section describes the verification routines that UI Accessibility Checker can run to test an application's accessibility implementation.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ced37-105">Category</span><span class="sxs-lookup"><span data-stu-id="ced37-105">Category</span></span></th>
<th><span data-ttu-id="ced37-106">Routine</span><span class="sxs-lookup"><span data-stu-id="ced37-106">Routine</span></span></th>
<th><span data-ttu-id="ced37-107">Description</span><span class="sxs-lookup"><span data-stu-id="ced37-107">Description</span></span></th>
</tr><span data-ttu-id="ced37-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Cohérence</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ced37-108">
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistency</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ced37-109"><strong>ScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-109"><strong>ScreenReader</strong></span></span></td>
<td><span data-ttu-id="ced37-110">Compile tous les éléments visibles dans la cible de vérification et les affiche dans un contrôle ListView dans l’ordre dans lequel un lecteur d’écran standard les annonce à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ced37-110">Compiles all visible elements in the verification target and displays them in a ListView control in the order that a standard screen reader announces them to a user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ced37-111"><strong>UiaScreenReader</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-111"><strong>UiaScreenReader</strong></span></span></td>
<td><span data-ttu-id="ced37-112">Identique à <strong>Screenreader</strong>, mais pour les implémentations de UIA.</span><span class="sxs-lookup"><span data-stu-id="ced37-112">Same as <strong>ScreenReader</strong>, but for UIA implementations.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="ced37-113"><strong>Navigation</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ced37-113"><strong>Navigation</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ced37-114"><strong>CheckTreeDepth</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-114"><strong>CheckTreeDepth</strong></span></span></td>
<td><span data-ttu-id="ced37-115">Envoie les caractères de tabulation (ou Maj + Tab) comme entrée à la cible de vérification pour confirmer que l’interface utilisateur de la cible n’est pas trop complexe ou inaccessible à l’aide de la navigation au clavier standard.</span><span class="sxs-lookup"><span data-stu-id="ced37-115">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that the target's UI isn't overly complex or inaccessible using standard keyboard navigation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ced37-116"><strong>CheckTabbingUia</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-116"><strong>CheckTabbingUia</strong></span></span></td>
<td><span data-ttu-id="ced37-117">Envoie les caractères de tabulation (ou Maj + Tab) comme entrée à la cible de vérification pour confirmer que tous les éléments pouvant être activés dans l’interface utilisateur sont accessibles de façon ordonnée et logique à l’aide de la navigation au clavier standard.</span><span class="sxs-lookup"><span data-stu-id="ced37-117">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that all focusable elements in the UI are reachable in an orderly, logical fashion using standard keyboard navigation.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="5"><span data-ttu-id="ced37-118"><strong>Propriétés</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ced37-118"><strong>Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ced37-119"><strong>CheckRole</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-119"><strong>CheckRole</strong></span></span></td>
<td><span data-ttu-id="ced37-120">Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un rôle MSAA logique et valide, et que le contrôle a une valeur comme requis par ce rôle.</span><span class="sxs-lookup"><span data-stu-id="ced37-120">Confirms that each focusable element in the UI reports a valid, logical MSAA role, and that the control has a value as required by that role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ced37-121"><strong>CheckState</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-121"><strong>CheckState</strong></span></span></td>
<td><span data-ttu-id="ced37-122">Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un État MSAA logique valide.</span><span class="sxs-lookup"><span data-stu-id="ced37-122">Confirms that each focusable element in the UI reports a valid, logical MSAA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-123"><strong>CheckName</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-123"><strong>CheckName</strong></span></span></td>
<td><span data-ttu-id="ced37-124">Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un nom MSAA logique valide.</span><span class="sxs-lookup"><span data-stu-id="ced37-124">Confirms that each focusable element in the UI reports a valid, logical MSAA name.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ced37-125"><strong>CheckAccessKeys</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-125"><strong>CheckAccessKeys</strong></span></span></td>
<td><span data-ttu-id="ced37-126">Confirme que les clés d’accès qui sont assignées aux éléments de la cible de vérification sont uniques dans la cible de vérification.</span><span class="sxs-lookup"><span data-stu-id="ced37-126">Confirms that access keys that are assigned to elements in the verification target are unique within the verification target.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-127"><strong>CheckBoundingRect</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-127"><strong>CheckBoundingRect</strong></span></span></td>
<td><span data-ttu-id="ced37-128">Confirme que chaque élément pouvant être actif dans l’interface utilisateur possède un rectangle englobant qui peut être utilisé comme cible pour le test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="ced37-128">Confirms that each focusable element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="ced37-129"><strong>Arborescence</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ced37-129"><strong>Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ced37-130"><strong>CheckParentChild</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-130"><strong>CheckParentChild</strong></span></span></td>
<td><span data-ttu-id="ced37-131">Les relations parent et enfant dans l’arborescence d’éléments sont cohérentes et prévisibles.</span><span class="sxs-lookup"><span data-stu-id="ced37-131">Parent and child relationships in the element tree are consistent and predictable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-132"><strong>CheckOrphanChildren</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-132"><strong>CheckOrphanChildren</strong></span></span></td>
<td><span data-ttu-id="ced37-133">Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un parent MSAA valide.</span><span class="sxs-lookup"><span data-stu-id="ced37-133">Confirms that each focusable element in the UI reports a valid MSAA parent.</span></span></td>

</tr>
<tr class="even">
<td rowspan="6"><span data-ttu-id="ced37-134"><strong>Propriétés de UIA</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ced37-134"><strong>UIA Properties</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ced37-135"><strong>CheckNameUIA</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-135"><strong>CheckNameUIA</strong></span></span></td>
<td><span data-ttu-id="ced37-136">Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un nom UIA logique valide.</span><span class="sxs-lookup"><span data-stu-id="ced37-136">Confirms that each focusable element in the UI reports a valid, logical UIA name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-137"><strong>CheckTreeDepthUIA</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-137"><strong>CheckTreeDepthUIA</strong></span></span></td>
<td><span data-ttu-id="ced37-138">Envoie les caractères de tabulation (ou Maj + Tab) comme entrée à la cible de vérification pour confirmer que les éléments UIA de l’interface utilisateur de la cible ne sont pas trop complexes ou inaccessibles à l’aide de la navigation au clavier standard.</span><span class="sxs-lookup"><span data-stu-id="ced37-138">Sends Tab (or Shift+Tab) characters as input to the verification target to confirm that to UIA elements in the target's UI aren't overly complex or inaccessible using standard keyboard navigation.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ced37-139"><strong>CheckStateUIA</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-139"><strong>CheckStateUIA</strong></span></span></td>
<td><span data-ttu-id="ced37-140">Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un État UIA logique valide.</span><span class="sxs-lookup"><span data-stu-id="ced37-140">Confirms that each focusable element in the UI reports a valid, logical UIA state.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-141"><strong>CheckAccessKeysUIA</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-141"><strong>CheckAccessKeysUIA</strong></span></span></td>
<td><span data-ttu-id="ced37-142">Confirme que les éléments frères n’ont pas les mêmes accès et/ou touche accélérateur.</span><span class="sxs-lookup"><span data-stu-id="ced37-142">Confirms that sibling elements do not have the same access and/or accelerator key.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ced37-143"><strong>CheckBoundingRectUIA</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-143"><strong>CheckBoundingRectUIA</strong></span></span></td>
<td><span data-ttu-id="ced37-144">Confirme que chaque élément UIA pouvant être actif dans l’interface utilisateur possède un rectangle englobant qui peut être utilisé comme cible pour le test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="ced37-144">Confirms that each focusable UIA element in the UI has a bounding rectangle that can be used as a target for hit testing.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-145"><strong>CheckControlTypeUIA</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-145"><strong>CheckControlTypeUIA</strong></span></span></td>
<td><span data-ttu-id="ced37-146">Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un type de contrôle UIA logique valide.</span><span class="sxs-lookup"><span data-stu-id="ced37-146">Confirms that each focusable element in the UI reports a valid, logical UIA control type.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="ced37-147"><strong>Arborescence UIA</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ced37-147"><strong>UIA Tree</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ced37-148"><strong>CheckNavigateUia</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-148"><strong>CheckNavigateUia</strong></span></span></td>
<td><span data-ttu-id="ced37-149">Confirme que le TreeWalker UIA peut naviguer dans les enfants d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ced37-149">Confirms that the UIA TreeWalker can navigate through an element's children.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-150"><strong>CheckOrphanChildrenUia</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-150"><strong>CheckOrphanChildrenUia</strong></span></span></td>
<td><span data-ttu-id="ced37-151">Confirme que chaque élément pouvant être actif dans l’interface utilisateur signale un parent UIA valide.</span><span class="sxs-lookup"><span data-stu-id="ced37-151">Confirms that each focusable element in the UI reports a valid UIA parent.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ced37-152"><strong>CheckSiblingsUia</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-152"><strong>CheckSiblingsUia</strong></span></span></td>
<td><span data-ttu-id="ced37-153">Confirme que les éléments frères n’ont pas le même nom : les paires ControlType, ni les mêmes AutomationId.</span><span class="sxs-lookup"><span data-stu-id="ced37-153">Confirms that sibling elements do not have the same Name:ControlType pairs, nor the same AutomationId's.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-154"><strong>Vérifications Web</strong>de $ {ROWSPAN9} $ Aria $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ced37-154">${ROWSPAN9}$<strong>ARIA Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ced37-155"><strong>CheckARIARole</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-155"><strong>CheckARIARole</strong></span></span></td>
<td><span data-ttu-id="ced37-156">Confirme que tous les éléments ont un rôle ARIA valide.</span><span class="sxs-lookup"><span data-stu-id="ced37-156">Confirms that all elements have a valid ARIA role.</span></span> <span data-ttu-id="ced37-157">La balise HTML et le rôle ARIA associés sont des éléments d’information dont les rôles non valides sont signalés comme des erreurs.</span><span class="sxs-lookup"><span data-stu-id="ced37-157">The associated HTML tag and ARIA role are information elements with invalid roles flagged as errors.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ced37-158"><strong>CheckLabel</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-158"><strong>CheckLabel</strong></span></span></td>
<td><span data-ttu-id="ced37-159">Confirme que chaque élément avec un rôle d’entrée, de bouton, d’image ou de repère a une étiquette.</span><span class="sxs-lookup"><span data-stu-id="ced37-159">Confirms each element with input, button, image-button, or landmark role has a label.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-160"><strong>CheckRangeControls</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-160"><strong>CheckRangeControls</strong></span></span></td>
<td><span data-ttu-id="ced37-161">Confirme que les contrôles de plage avec le curseur ou le rôle de barre de progression ont des attributs ARIA appropriés définis.</span><span class="sxs-lookup"><span data-stu-id="ced37-161">Confirms range controls with slider or progress bar role have proper ARIA attributes defined.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ced37-162"><strong>CheckContainerRole</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-162"><strong>CheckContainerRole</strong></span></span></td>
<td><span data-ttu-id="ced37-163">Confirme qu’un élément, ou au moins un de ses enfants, a l’élément OnKeyDown/OnKeyPress défini.</span><span class="sxs-lookup"><span data-stu-id="ced37-163">Confirms an element, or at least one of its children, has onkeydown/onkeypress defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-164"><strong>CheckLayoutTable</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-164"><strong>CheckLayoutTable</strong></span></span></td>
<td><span data-ttu-id="ced37-165">Confirme qu’une mise en page de table a un résumé/th/Aria-DescribedBy inclus.</span><span class="sxs-lookup"><span data-stu-id="ced37-165">Confirms a table layout has a summary/th/aria-describedby included.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ced37-166"><strong>CheckGridStructure</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-166"><strong>CheckGridStructure</strong></span></span></td>
<td><span data-ttu-id="ced37-167">Confirme qu’un élément qui n’est pas une table avec un rôle de grille a une structure de grille>ligne>GridCell avec des attributs associés.</span><span class="sxs-lookup"><span data-stu-id="ced37-167">Confirms a non-table element with grid role has a structure of grid>row>gridcell with associated attributes.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-168"><strong>CheckDataTable</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-168"><strong>CheckDataTable</strong></span></span></td>
<td><span data-ttu-id="ced37-169">Confirme les propriétés des tables de données.</span><span class="sxs-lookup"><span data-stu-id="ced37-169">Confirms the properties of data tables.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ced37-170"><strong>CheckActiveDescendants</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-170"><strong>CheckActiveDescendants</strong></span></span></td>
<td><span data-ttu-id="ced37-171">Confirme les propriétés des éléments avec un descendant actif défini.</span><span class="sxs-lookup"><span data-stu-id="ced37-171">Confirms the properties of elements with an active descendant defined.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-172"><strong>CheckElementsWithClickHandler</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-172"><strong>CheckElementsWithClickHandler</strong></span></span></td>
<td><span data-ttu-id="ced37-173">Confirme l’index de tabulation des éléments avec des gestionnaires de clic.</span><span class="sxs-lookup"><span data-stu-id="ced37-173">Confirms the tab index of elements with click handlers.</span></span></td>

</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="ced37-174"><strong>Vérifications Web</strong>$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="ced37-174"><strong>Web Verifications</strong>${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="ced37-175"><strong>CheckHtml (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-175"><strong>CheckHtml (Web)</strong></span></span></td>
<td><span data-ttu-id="ced37-176">Confirme différentes caractéristiques HTML, telles que les en-têtes, le nom, les cadres et les titres.</span><span class="sxs-lookup"><span data-stu-id="ced37-176">Confirms various HTML characteristics such as headers, name, frames, and titles.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ced37-177"><strong>CheckName (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-177"><strong>CheckName (Web)</strong></span></span></td>
<td><span data-ttu-id="ced37-178">Confirme les caractéristiques de nom, telles que la longueur, les caractères non valides et l’inclusion de rôle.</span><span class="sxs-lookup"><span data-stu-id="ced37-178">Confirms name characteristics such as length, invalid characters, and role inclusion.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="ced37-179"><strong>CheckRole (Web)</strong></span><span class="sxs-lookup"><span data-stu-id="ced37-179"><strong>CheckRole (Web)</strong></span></span></td>
<td><span data-ttu-id="ced37-180">Confirme les rôles non valides, les rôles qui doivent avoir des valeurs, et/ou les rôles qui ne sont pas implémentés.</span><span class="sxs-lookup"><span data-stu-id="ced37-180">Confirms invalid roles, roles that should have values, and/or roles not implemented.</span></span></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ced37-181">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ced37-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ced37-182">Vérificateur d’accessibilité de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="ced37-182">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




