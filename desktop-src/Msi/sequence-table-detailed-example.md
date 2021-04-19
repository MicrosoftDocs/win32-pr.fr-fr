---
description: Voici un exemple de table de séquences.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Exemple de table de séquence détaillé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518937"
---
# <a name="sequence-table-detailed-example"></a><span data-ttu-id="88c5e-103">Exemple de table de séquence détaillé</span><span class="sxs-lookup"><span data-stu-id="88c5e-103">Sequence Table Detailed Example</span></span>

<span data-ttu-id="88c5e-104">Voici un exemple de table de séquences.</span><span class="sxs-lookup"><span data-stu-id="88c5e-104">Here is an example of a sequence table.</span></span>



| <span data-ttu-id="88c5e-105">Action</span><span class="sxs-lookup"><span data-stu-id="88c5e-105">Action</span></span>                                          | <span data-ttu-id="88c5e-106">Condition</span><span class="sxs-lookup"><span data-stu-id="88c5e-106">Condition</span></span>                                                       | <span data-ttu-id="88c5e-107">Séquence</span><span class="sxs-lookup"><span data-stu-id="88c5e-107">Sequence</span></span> |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [<span data-ttu-id="88c5e-108">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="88c5e-108">LaunchConditions</span></span>](launchconditions-action.md) |                                                                 |          |
| [<span data-ttu-id="88c5e-109">AppSearch</span><span class="sxs-lookup"><span data-stu-id="88c5e-109">AppSearch</span></span>](appsearch-action.md)               |                                                                 | <span data-ttu-id="88c5e-110">200</span><span class="sxs-lookup"><span data-stu-id="88c5e-110">200</span></span>      |
| [<span data-ttu-id="88c5e-111">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="88c5e-111">CCPSearch</span></span>](ccpsearch-action.md)               | <span data-ttu-id="88c5e-112">\_test CCP</span><span class="sxs-lookup"><span data-stu-id="88c5e-112">CCP\_TEST</span></span>                                                       | <span data-ttu-id="88c5e-113">300</span><span class="sxs-lookup"><span data-stu-id="88c5e-113">300</span></span>      |
| <span data-ttu-id="88c5e-114">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="88c5e-114">CCPDialog</span></span>                                       | <span data-ttu-id="88c5e-115">PAS \_ de \_ réussite CCP</span><span class="sxs-lookup"><span data-stu-id="88c5e-115">NOT\_CCP\_SUCCESS</span></span>                                               | <span data-ttu-id="88c5e-116">400</span><span class="sxs-lookup"><span data-stu-id="88c5e-116">400</span></span>      |
| <span data-ttu-id="88c5e-117">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="88c5e-117">MyCustomConfig</span></span>                                  | <span data-ttu-id="88c5e-118">NON [ **installé**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="88c5e-118">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="88c5e-119">500</span><span class="sxs-lookup"><span data-stu-id="88c5e-119">500</span></span>      |
| [<span data-ttu-id="88c5e-120">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="88c5e-120">CostInitialize</span></span>](costinitialize-action.md)     |                                                                 | <span data-ttu-id="88c5e-121">600</span><span class="sxs-lookup"><span data-stu-id="88c5e-121">600</span></span>      |
| [<span data-ttu-id="88c5e-122">FileCost</span><span class="sxs-lookup"><span data-stu-id="88c5e-122">FileCost</span></span>](filecost-action.md)                 |                                                                 | <span data-ttu-id="88c5e-123">700</span><span class="sxs-lookup"><span data-stu-id="88c5e-123">700</span></span>      |
| [<span data-ttu-id="88c5e-124">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="88c5e-124">CostFinalize</span></span>](costfinalize-action.md)         |                                                                 | <span data-ttu-id="88c5e-125">800</span><span class="sxs-lookup"><span data-stu-id="88c5e-125">800</span></span>      |
| <span data-ttu-id="88c5e-126">InstallDialog</span><span class="sxs-lookup"><span data-stu-id="88c5e-126">InstallDialog</span></span>                                   | <span data-ttu-id="88c5e-127">NON [ **installé**](installed.md)</span><span class="sxs-lookup"><span data-stu-id="88c5e-127">NOT [**Installed**](installed.md)</span></span>                              | <span data-ttu-id="88c5e-128">900</span><span class="sxs-lookup"><span data-stu-id="88c5e-128">900</span></span>      |
| <span data-ttu-id="88c5e-129">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="88c5e-129">MaintenanceDialog</span></span>                               | <span data-ttu-id="88c5e-130">[**Installé**](installed.md) ET ne pas [ **reprendre**](resume.md)</span><span class="sxs-lookup"><span data-stu-id="88c5e-130">[**Installed**](installed.md) AND NOT [**Resume**](resume.md)</span></span> | <span data-ttu-id="88c5e-131">1 000</span><span class="sxs-lookup"><span data-stu-id="88c5e-131">1000</span></span>     |
| <span data-ttu-id="88c5e-132">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="88c5e-132">ActionDialog</span></span>                                    |                                                                 | <span data-ttu-id="88c5e-133">1100</span><span class="sxs-lookup"><span data-stu-id="88c5e-133">1100</span></span>     |
| [<span data-ttu-id="88c5e-134">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="88c5e-134">RegisterProduct</span></span>](registerproduct-action.md)   |                                                                 | <span data-ttu-id="88c5e-135">1200</span><span class="sxs-lookup"><span data-stu-id="88c5e-135">1200</span></span>     |
| [<span data-ttu-id="88c5e-136">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="88c5e-136">InstallValidate</span></span>](installvalidate-action.md)   |                                                                 | <span data-ttu-id="88c5e-137">1 300</span><span class="sxs-lookup"><span data-stu-id="88c5e-137">1300</span></span>     |
| [<span data-ttu-id="88c5e-138">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="88c5e-138">InstallFiles</span></span>](installfiles-action.md)         |                                                                 | <span data-ttu-id="88c5e-139">1400</span><span class="sxs-lookup"><span data-stu-id="88c5e-139">1400</span></span>     |
| <span data-ttu-id="88c5e-140">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="88c5e-140">MyCustomAction</span></span>                                  | <span data-ttu-id="88c5e-141">$MyComponent > 2</span><span class="sxs-lookup"><span data-stu-id="88c5e-141">$MyComponent > 2</span></span>                                             | <span data-ttu-id="88c5e-142">1500</span><span class="sxs-lookup"><span data-stu-id="88c5e-142">1500</span></span>     |
| [<span data-ttu-id="88c5e-143">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="88c5e-143">InstallFinalize</span></span>](installfinalize-action.md)   |                                                                 | <span data-ttu-id="88c5e-144">1 600</span><span class="sxs-lookup"><span data-stu-id="88c5e-144">1600</span></span>     |



 

<span data-ttu-id="88c5e-145">Les actions suivantes dans cette table de séquences sont définies par le programme d’installation et sont des exemples d’actions standard :</span><span class="sxs-lookup"><span data-stu-id="88c5e-145">The following actions in this sequence table are defined by the installer and are examples of standard actions:</span></span>

[<span data-ttu-id="88c5e-146">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="88c5e-146">LaunchConditions</span></span>](launchconditions-action.md)

 

[<span data-ttu-id="88c5e-147">AppSearch</span><span class="sxs-lookup"><span data-stu-id="88c5e-147">AppSearch</span></span>](appsearch-action.md)

 

[<span data-ttu-id="88c5e-148">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="88c5e-148">CCPSearch</span></span>](ccpsearch-action.md)

 

[<span data-ttu-id="88c5e-149">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="88c5e-149">CostInitialize</span></span>](costinitialize-action.md)

 

[<span data-ttu-id="88c5e-150">FileCost</span><span class="sxs-lookup"><span data-stu-id="88c5e-150">FileCost</span></span>](filecost-action.md)

 

[<span data-ttu-id="88c5e-151">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="88c5e-151">CostFinalize</span></span>](costfinalize-action.md)

 

[<span data-ttu-id="88c5e-152">RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="88c5e-152">RegisterProduct</span></span>](registerproduct-action.md)

 

[<span data-ttu-id="88c5e-153">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="88c5e-153">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="88c5e-154">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="88c5e-154">InstallFiles</span></span>](installfiles-action.md)

 

[<span data-ttu-id="88c5e-155">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="88c5e-155">InstallValidate</span></span>](installvalidate-action.md)

<span data-ttu-id="88c5e-156">Les actions suivantes ont été définies par l’auteur de la table et sont des exemples d' [actions personnalisées](custom-actions.md) et doivent être répertoriées dans la [table CustomAction](customaction-table.md):</span><span class="sxs-lookup"><span data-stu-id="88c5e-156">The following actions were defined by the table's author and are examples of [custom actions](custom-actions.md) and must be listed in the [CustomAction table](customaction-table.md):</span></span>

<span data-ttu-id="88c5e-157">MyCustomConfig</span><span class="sxs-lookup"><span data-stu-id="88c5e-157">MyCustomConfig</span></span>

 

<span data-ttu-id="88c5e-158">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="88c5e-158">MyCustomAction</span></span>

<span data-ttu-id="88c5e-159">Les entrées restantes du champ action sont des clés étrangères dans la [table Dialog](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="88c5e-159">The remaining entries in the Action field are foreign keys into the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="88c5e-160">Ils spécifient les noms des boîtes de dialogue qui s’affichent si le champ condition prend la valeur true.</span><span class="sxs-lookup"><span data-stu-id="88c5e-160">They specify the names of dialog boxes that will displayed if the condition field evaluates to True.</span></span>

<span data-ttu-id="88c5e-161">CCPDialog</span><span class="sxs-lookup"><span data-stu-id="88c5e-161">CCPDialog</span></span>

 

<span data-ttu-id="88c5e-162">InstallDialog</span><span class="sxs-lookup"><span data-stu-id="88c5e-162">InstallDialog</span></span>

 

<span data-ttu-id="88c5e-163">MaintenanceDialog</span><span class="sxs-lookup"><span data-stu-id="88c5e-163">MaintenanceDialog</span></span>

 

<span data-ttu-id="88c5e-164">ActionDialog</span><span class="sxs-lookup"><span data-stu-id="88c5e-164">ActionDialog</span></span>

<span data-ttu-id="88c5e-165">Dans la colonne condition, le programme d’installation ignore l’action si la propriété ou l’expression dans ce champ a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="88c5e-165">The Condition column causes the installer to skip the action if the property or expression in this field is False.</span></span> <span data-ttu-id="88c5e-166">La propriété [**installed**](installed.md) et la propriété [**Resume**](resume.md) sont des exemples de propriétés définies par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="88c5e-166">The [**Installed**](installed.md) property and the [**RESUME**](resume.md) property are example of properties that are set by the installer.</span></span> <span data-ttu-id="88c5e-167">La propriété [**installed**](installed.md) a la valeur true si le produit est déjà installé et que la propriété [**Resume**](resume.md) est définie si la reprise d’une installation a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="88c5e-167">The [**Installed**](installed.md) property is set to true if the product is already installed and the [**RESUME**](resume.md) property is set if resuming a suspended installation.</span></span> <span data-ttu-id="88c5e-168">Le \_ test CCP et les \_ Propriétés de réussite non CCP \_ sont des exemples de propriétés qui peuvent être définies sur la ligne de commande par l’utilisateur qui installe l’application.</span><span class="sxs-lookup"><span data-stu-id="88c5e-168">The CCP\_TEST and the NOT\_CCP\_SUCCESS properties are examples of properties that can be set at the command line by the user installing the application.</span></span>

<span data-ttu-id="88c5e-169">Toutes les actions s’exécutent en séquence avec les étapes conditionnelles suivantes :</span><span class="sxs-lookup"><span data-stu-id="88c5e-169">All actions run in sequence with the following conditional steps:</span></span>

-   <span data-ttu-id="88c5e-170">Le CPPSearch est exécuté uniquement si le \_ test CCP est défini.</span><span class="sxs-lookup"><span data-stu-id="88c5e-170">The CPPSearch is run only if CCP\_TEST is set.</span></span>
-   <span data-ttu-id="88c5e-171">CCPDialog est exécuté uniquement si la \_ réussite du CCP n' \_ est pas définie.</span><span class="sxs-lookup"><span data-stu-id="88c5e-171">CCPDialog is run only if NOT\_CCP\_SUCCESS is set.</span></span>
-   <span data-ttu-id="88c5e-172">MaintenanceDialog est exécuté uniquement si ce produit est déjà installé et s’il ne s’agit pas d’une installation qui est reprise après avoir été suspendue.</span><span class="sxs-lookup"><span data-stu-id="88c5e-172">MaintenanceDialog is run only if this product is already installed and if this is not an installation that is being resume after being suspended.</span></span>
-   <span data-ttu-id="88c5e-173">MyCustomAction est exécuté uniquement si l’expression dans la colonne condition a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="88c5e-173">MyCustomAction is run only if the expression in the Condition column is True.</span></span> <span data-ttu-id="88c5e-174">L’expression $MyComponent > 2 fait référence à l’état d’action du composant appelé MyComponent.</span><span class="sxs-lookup"><span data-stu-id="88c5e-174">The expression $MyComponent > 2 refers to the action state of the component called MyComponent.</span></span> <span data-ttu-id="88c5e-175">Cette condition indique que MyCustomAction doit être exécuté uniquement si MonComposant est configuré pour être installé.</span><span class="sxs-lookup"><span data-stu-id="88c5e-175">This condition indicates that MyCustomAction should only be run if MyComponent is set to be installed.</span></span> <span data-ttu-id="88c5e-176">Pour plus d’informations sur les États d’action et les États de sélection, consultez la propriété [**FeatureRequestState**](session-featurerequeststate.md) , la [table de fonctionnalités](feature-table.md)et l' [action InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="88c5e-176">For more information on Action states and Selection states, see the [**FeatureRequestState**](session-featurerequeststate.md) property, the [Feature table](feature-table.md), and the [InstallFiles action](installfiles-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88c5e-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88c5e-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c5e-178">Utilisation de propriétés</span><span class="sxs-lookup"><span data-stu-id="88c5e-178">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="88c5e-179">Syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="88c5e-179">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 



