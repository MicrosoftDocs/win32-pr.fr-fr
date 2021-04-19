---
description: ICE23 valide l’ordre de tabulation des contrôles pour chaque boîte de dialogue.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536719"
---
# <a name="ice23"></a><span data-ttu-id="6f501-103">ICE23</span><span class="sxs-lookup"><span data-stu-id="6f501-103">ICE23</span></span>

<span data-ttu-id="6f501-104">ICE23 valide l’ordre de tabulation des contrôles pour chaque boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6f501-104">ICE23 validates the control tab order for each dialog box.</span></span>

<span data-ttu-id="6f501-105">ICE23 valide les éléments suivants dans la [table de boîtes de dialogue](dialog-table.md) et la [table de contrôle](control-table.md):</span><span class="sxs-lookup"><span data-stu-id="6f501-105">ICE23 validates the following in the [Dialog table](dialog-table.md) and [Control table](control-table.md):</span></span>

-   <span data-ttu-id="6f501-106">Que chaque enregistrement dans la table de boîte de dialogue spécifie un contrôle dans la \_ première colonne du contrôle qui existe dans la boîte de dialogue spécifiée par la colonne de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6f501-106">That every record in the Dialog table specifies a control in the Control\_First column that exists in the dialog box specified by the Dialog column.</span></span>
-   <span data-ttu-id="6f501-107">Chaque enregistrement dans la table de contrôle spécifie un contrôle dans la \_ colonne de contrôle suivant qui se trouve dans la même boîte de dialogue que le contrôle figurant dans la colonne de contrôle, ou \_ le contrôle suivant contient la valeur null.</span><span class="sxs-lookup"><span data-stu-id="6f501-107">That every record in the Control table specifies a control in the Control\_Next column that is on the same dialog as the control listed in the Control column, or Control\_Next contains the Null value.</span></span>
-   <span data-ttu-id="6f501-108">Qui suit le contrôle les \_ entrées suivantes du contrôle au contrôle dans la table de contrôle rend une boucle unique et fermée qui revient au contrôle initial.</span><span class="sxs-lookup"><span data-stu-id="6f501-108">That following the Control\_Next entries from control to control in the Control table makes a single, closed, loop that comes back to the initial control.</span></span> <span data-ttu-id="6f501-109">Tous les contrôles ne doivent pas être dans la boucle, mais la boucle doit traverser chaque contrôle qui a une entrée dans la \_ colonne Control Next.</span><span class="sxs-lookup"><span data-stu-id="6f501-109">Not every control needs to be in the loop, but the loop must pass through every control that has an entry in the Control\_Next column.</span></span>

## <a name="result"></a><span data-ttu-id="6f501-110">Résultats</span><span class="sxs-lookup"><span data-stu-id="6f501-110">Result</span></span>

<span data-ttu-id="6f501-111">ICE23 publie un message d’erreur si l’ordre de tabulation des contrôles ne constitue pas une boucle fermée unique dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6f501-111">ICE23 posts an error message if the tab order of controls does not form a single closed loop in the dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="6f501-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="6f501-112">Example</span></span>

<span data-ttu-id="6f501-113">ICE23 publie les messages d’erreur suivants pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="6f501-113">ICE23 would post the following error messages for the example shown.</span></span>

-   <span data-ttu-id="6f501-114">Dialog1 n’a pas d’abord de contrôle \_ .</span><span class="sxs-lookup"><span data-stu-id="6f501-114">Dialog1 has no Control\_First.</span></span>
-   <span data-ttu-id="6f501-115">Le \_ premier contrôle de la boîte de dialogue Dialog2 fait référence à des ControlX de contrôle inexistants.</span><span class="sxs-lookup"><span data-stu-id="6f501-115">Control\_First of dialog Dialog2 refers to nonexistent control ControlX.</span></span>
-   <span data-ttu-id="6f501-116">Dialog3 a un ordre de tabulation de fin mort à l’ControlB de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6f501-116">Dialog3 has dead-end tab order at control ControlB.</span></span>
-   <span data-ttu-id="6f501-117">Dialog4 a un ordre de tabulation incorrect au niveau du contrôle ControlC</span><span class="sxs-lookup"><span data-stu-id="6f501-117">Dialog4 has malformed tab order at control ControlC</span></span>
-   <span data-ttu-id="6f501-118">Dialog5 a un ordre de tabulation incorrect au niveau du contrôle ControlC.</span><span class="sxs-lookup"><span data-stu-id="6f501-118">Dialog5 has malformed tab order at control ControlC.</span></span>
-   <span data-ttu-id="6f501-119">Contrôle \_ en regard du contrôle Dialog6. controlc liens vers un contrôle inconnu.</span><span class="sxs-lookup"><span data-stu-id="6f501-119">Control\_Next of control Dialog6.ControlC links to unknown control.</span></span>

<span data-ttu-id="6f501-120">[Table de boîtes de dialogue](dialog-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="6f501-120">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="6f501-121">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="6f501-121">Dialog</span></span>  | <span data-ttu-id="6f501-122">\_Premier contrôle</span><span class="sxs-lookup"><span data-stu-id="6f501-122">Control\_First</span></span> |
|---------|----------------|
| <span data-ttu-id="6f501-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="6f501-123">Dialog1</span></span> |                |
| <span data-ttu-id="6f501-124">Dialog2</span><span class="sxs-lookup"><span data-stu-id="6f501-124">Dialog2</span></span> | <span data-ttu-id="6f501-125">ControlX</span><span class="sxs-lookup"><span data-stu-id="6f501-125">ControlX</span></span>       |
| <span data-ttu-id="6f501-126">Dialog3</span><span class="sxs-lookup"><span data-stu-id="6f501-126">Dialog3</span></span> | <span data-ttu-id="6f501-127">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-127">ControlA</span></span>       |
| <span data-ttu-id="6f501-128">Dialog4</span><span class="sxs-lookup"><span data-stu-id="6f501-128">Dialog4</span></span> | <span data-ttu-id="6f501-129">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-129">ControlA</span></span>       |
| <span data-ttu-id="6f501-130">Dialog5</span><span class="sxs-lookup"><span data-stu-id="6f501-130">Dialog5</span></span> | <span data-ttu-id="6f501-131">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-131">ControlA</span></span>       |



 

<span data-ttu-id="6f501-132">[Table de contrôle](control-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="6f501-132">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="6f501-133">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="6f501-133">Dialog</span></span>  | <span data-ttu-id="6f501-134">Contrôler</span><span class="sxs-lookup"><span data-stu-id="6f501-134">Control</span></span>  | <span data-ttu-id="6f501-135">Contrôle \_ suivant</span><span class="sxs-lookup"><span data-stu-id="6f501-135">Control\_Next</span></span> |
|---------|----------|---------------|
| <span data-ttu-id="6f501-136">Dialog1</span><span class="sxs-lookup"><span data-stu-id="6f501-136">Dialog1</span></span> | <span data-ttu-id="6f501-137">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-137">ControlA</span></span> |               |
| <span data-ttu-id="6f501-138">Dialog1</span><span class="sxs-lookup"><span data-stu-id="6f501-138">Dialog1</span></span> | <span data-ttu-id="6f501-139">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-139">ControlB</span></span> | <span data-ttu-id="6f501-140">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-140">ControlA</span></span>      |
| <span data-ttu-id="6f501-141">Dialog2</span><span class="sxs-lookup"><span data-stu-id="6f501-141">Dialog2</span></span> | <span data-ttu-id="6f501-142">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-142">ControlA</span></span> | <span data-ttu-id="6f501-143">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-143">ControlB</span></span>      |
| <span data-ttu-id="6f501-144">Dialog2</span><span class="sxs-lookup"><span data-stu-id="6f501-144">Dialog2</span></span> | <span data-ttu-id="6f501-145">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-145">ControlB</span></span> | <span data-ttu-id="6f501-146">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-146">ControlA</span></span>      |
| <span data-ttu-id="6f501-147">Dialog3</span><span class="sxs-lookup"><span data-stu-id="6f501-147">Dialog3</span></span> | <span data-ttu-id="6f501-148">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-148">ControlA</span></span> | <span data-ttu-id="6f501-149">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-149">ControlB</span></span>      |
| <span data-ttu-id="6f501-150">Dialog3</span><span class="sxs-lookup"><span data-stu-id="6f501-150">Dialog3</span></span> | <span data-ttu-id="6f501-151">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-151">ControlB</span></span> |               |
| <span data-ttu-id="6f501-152">Dialog4</span><span class="sxs-lookup"><span data-stu-id="6f501-152">Dialog4</span></span> | <span data-ttu-id="6f501-153">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-153">ControlA</span></span> | <span data-ttu-id="6f501-154">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-154">ControlB</span></span>      |
| <span data-ttu-id="6f501-155">Dialog4</span><span class="sxs-lookup"><span data-stu-id="6f501-155">Dialog4</span></span> | <span data-ttu-id="6f501-156">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-156">ControlB</span></span> | <span data-ttu-id="6f501-157">ControlC</span><span class="sxs-lookup"><span data-stu-id="6f501-157">ControlC</span></span>      |
| <span data-ttu-id="6f501-158">Dialog4</span><span class="sxs-lookup"><span data-stu-id="6f501-158">Dialog4</span></span> | <span data-ttu-id="6f501-159">ControlC</span><span class="sxs-lookup"><span data-stu-id="6f501-159">ControlC</span></span> | <span data-ttu-id="6f501-160">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-160">ControlB</span></span>      |
| <span data-ttu-id="6f501-161">Dialog5</span><span class="sxs-lookup"><span data-stu-id="6f501-161">Dialog5</span></span> | <span data-ttu-id="6f501-162">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-162">ControlA</span></span> | <span data-ttu-id="6f501-163">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-163">ControlB</span></span>      |
| <span data-ttu-id="6f501-164">Dialog5</span><span class="sxs-lookup"><span data-stu-id="6f501-164">Dialog5</span></span> | <span data-ttu-id="6f501-165">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-165">ControlB</span></span> | <span data-ttu-id="6f501-166">ControlC</span><span class="sxs-lookup"><span data-stu-id="6f501-166">ControlC</span></span>      |
| <span data-ttu-id="6f501-167">Dialog5</span><span class="sxs-lookup"><span data-stu-id="6f501-167">Dialog5</span></span> | <span data-ttu-id="6f501-168">ControlC</span><span class="sxs-lookup"><span data-stu-id="6f501-168">ControlC</span></span> | <span data-ttu-id="6f501-169">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-169">ControlA</span></span>      |
| <span data-ttu-id="6f501-170">Dialog5</span><span class="sxs-lookup"><span data-stu-id="6f501-170">Dialog5</span></span> | <span data-ttu-id="6f501-171">En contrôle</span><span class="sxs-lookup"><span data-stu-id="6f501-171">ControlD</span></span> | <span data-ttu-id="6f501-172">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-172">ControlA</span></span>      |
| <span data-ttu-id="6f501-173">Dialog6</span><span class="sxs-lookup"><span data-stu-id="6f501-173">Dialog6</span></span> | <span data-ttu-id="6f501-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-174">ControlA</span></span> | <span data-ttu-id="6f501-175">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-175">ControlB</span></span>      |
| <span data-ttu-id="6f501-176">Dialog6</span><span class="sxs-lookup"><span data-stu-id="6f501-176">Dialog6</span></span> | <span data-ttu-id="6f501-177">ControlB</span><span class="sxs-lookup"><span data-stu-id="6f501-177">ControlB</span></span> | <span data-ttu-id="6f501-178">ControlC</span><span class="sxs-lookup"><span data-stu-id="6f501-178">ControlC</span></span>      |
| <span data-ttu-id="6f501-179">Dialog6</span><span class="sxs-lookup"><span data-stu-id="6f501-179">Dialog6</span></span> | <span data-ttu-id="6f501-180">ControlC</span><span class="sxs-lookup"><span data-stu-id="6f501-180">ControlC</span></span> | <span data-ttu-id="6f501-181">ControlX</span><span class="sxs-lookup"><span data-stu-id="6f501-181">ControlX</span></span>      |
| <span data-ttu-id="6f501-182">Dialog6</span><span class="sxs-lookup"><span data-stu-id="6f501-182">Dialog6</span></span> | <span data-ttu-id="6f501-183">En contrôle</span><span class="sxs-lookup"><span data-stu-id="6f501-183">ControlD</span></span> | <span data-ttu-id="6f501-184">ControlA</span><span class="sxs-lookup"><span data-stu-id="6f501-184">ControlA</span></span>      |



 

<span data-ttu-id="6f501-185">Pour corriger ces erreurs, notez les points suivants dans les tableaux ci-dessus et apportez les modifications indiquées.</span><span class="sxs-lookup"><span data-stu-id="6f501-185">To fix these errors note the following in the above tables and make the indicated changes.</span></span>

<span data-ttu-id="6f501-186">Aucune ligne de la table de boîte de dialogue n’a de contrôle spécifié dans la \_ première colonne du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6f501-186">Not every row in the Dialog table has a control specified in the Control\_First column.</span></span> <span data-ttu-id="6f501-187">Remplacez la \_ première colonne du contrôle de l’enregistrement dialog1 dans la table de boîte de dialogue par un contrôle qui existe dans dialog1.</span><span class="sxs-lookup"><span data-stu-id="6f501-187">Change the Control\_First column of the Dialog1 record in the Dialog table to a control that exists in Dialog1.</span></span>

<span data-ttu-id="6f501-188">Les lignes de la table de boîtes de dialogue n’ont pas toutes un contrôle spécifié dans la \_ première colonne du contrôle qui existe dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6f501-188">Not every row in the Dialog table has a control specified in the Control\_First column that exists on the dialog box.</span></span> <span data-ttu-id="6f501-189">Remplacez la \_ première colonne Control de Dialog2 par un contrôle qui existe dans Dialog2.</span><span class="sxs-lookup"><span data-stu-id="6f501-189">Change the Control\_First column of the Dialog2 to a control that exists in Dialog2.</span></span>

<span data-ttu-id="6f501-190">Après le contrôle, les \_ entrées suivantes dans la table de contrôle du contrôle au contrôle ne font pas de boucle fermée dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="6f501-190">Following the Control\_Next entries in the Control table from control to control does not make a closed loop in every case.</span></span> <span data-ttu-id="6f501-191">Modifiez la \_ colonne Control Next de ControlB dans Dialog3 en ControlA.</span><span class="sxs-lookup"><span data-stu-id="6f501-191">Change the Control\_Next column for ControlB in Dialog3 to ControlA.</span></span>

<span data-ttu-id="6f501-192">Après le contrôle, les \_ entrées suivantes dans la table de contrôle du contrôle au contrôle ne renvoient pas au contrôle initial dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="6f501-192">Following the Control\_Next entries in the Control table from control to control does not lead back to the initial control in every case.</span></span> <span data-ttu-id="6f501-193">Modifiez la \_ colonne Control Next de controlc dans Dialog4 pour faire référence à ControlA.</span><span class="sxs-lookup"><span data-stu-id="6f501-193">Change the Control\_Next column for ControlC in Dialog4 to refer to ControlA.</span></span>

<span data-ttu-id="6f501-194">Après le contrôle, les \_ entrées suivantes dans la table de contrôle du contrôle au contrôle ne passent pas par chaque contrôle de la boîte de dialogue avec une entrée dans la \_ colonne contrôle suivant.</span><span class="sxs-lookup"><span data-stu-id="6f501-194">Following the Control\_Next entries in the Control table from control to control does not pass through every control in the dialog box having an entry in the Control\_Next column.</span></span> <span data-ttu-id="6f501-195">Modifiez la \_ colonne Control Next pour controlc dans Dialog5 en controled.</span><span class="sxs-lookup"><span data-stu-id="6f501-195">Change the Control\_Next column for ControlC in Dialog5 to ControlD.</span></span>

<span data-ttu-id="6f501-196">Control \_ Next ne fait pas référence à un contrôle valide qui se trouve dans la même boîte de dialogue que le contrôle figurant dans la colonne Control.</span><span class="sxs-lookup"><span data-stu-id="6f501-196">Control\_Next does not refer to a valid control that is in the same dialog as the control listed in the Control column.</span></span> <span data-ttu-id="6f501-197">Modifiez la \_ colonne Control Next de controlc dans Dialog6 pour faire référence à controled.</span><span class="sxs-lookup"><span data-stu-id="6f501-197">Change the Control\_Next column for ControlC in Dialog6 to refer to ControlD.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f501-198">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f501-198">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f501-199">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="6f501-199">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



