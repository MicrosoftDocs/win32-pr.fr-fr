---
description: ICE34 valide que chaque case d’option sur chaque contrôle RadioButtonGroup a une propriété dans la colonne propriété de la table RadioButton qui spécifie son groupe de cases d’option.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536484"
---
# <a name="ice34"></a><span data-ttu-id="0ace3-103">ICE34</span><span class="sxs-lookup"><span data-stu-id="0ace3-103">ICE34</span></span>

<span data-ttu-id="0ace3-104">ICE34 valide que chaque case d’option sur chaque [contrôle RadioButtonGroup](radiobuttongroup-control.md) a une propriété dans la colonne propriété de la [table RadioButton](radiobutton-table.md) qui spécifie son groupe de cases d’option.</span><span class="sxs-lookup"><span data-stu-id="0ace3-104">ICE34 validates that each radio button on every [RadioButtonGroup Control](radiobuttongroup-control.md) has a property in the Property column of the [RadioButton table](radiobutton-table.md) that specifies its radio button group.</span></span> <span data-ttu-id="0ace3-105">ICE34 valide que cette propriété existe et qu’elle est définie sur une valeur par défaut dans la [table de propriétés](property-table.md) qui est égale à l’une des valeurs de case d’option du groupe dans la colonne valeur de la table RadioButton.</span><span class="sxs-lookup"><span data-stu-id="0ace3-105">ICE34 validates that this property exists and is set to a default value in the [Property table](property-table.md) which is equal to one of the group's radio button values in the Value column of the RadioButton table.</span></span>

<span data-ttu-id="0ace3-106">Un groupe de cases d’option doit avoir une valeur par défaut pour que les utilisateurs puissent sélectionner un choix à l’aide de la touche TAB.</span><span class="sxs-lookup"><span data-stu-id="0ace3-106">A radio button group must have a default for users to be able to select a choice using the TAB key.</span></span> <span data-ttu-id="0ace3-107">Cela est nécessaire pour une accessibilité appropriée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ace3-107">This is required for proper user accessibility.</span></span>

<span data-ttu-id="0ace3-108">ICE34 signale les tables manquantes.</span><span class="sxs-lookup"><span data-stu-id="0ace3-108">ICE34 reports missing tables.</span></span>

## <a name="result"></a><span data-ttu-id="0ace3-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="0ace3-109">Result</span></span>

<span data-ttu-id="0ace3-110">ICE34 publiez un message d’erreur s’il existe une case d’option qui spécifie une propriété non valide.</span><span class="sxs-lookup"><span data-stu-id="0ace3-110">ICE34 post an error message if there is a radio button that specifies an invalid property.</span></span>

## <a name="example"></a><span data-ttu-id="0ace3-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ace3-111">Example</span></span>

<span data-ttu-id="0ace3-112">ICE34 signale les erreurs suivantes pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="0ace3-112">ICE34 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="0ace3-113">Erreur ICE34</span><span class="sxs-lookup"><span data-stu-id="0ace3-113">ICE34 error</span></span>                                                                                                                                                                | <span data-ttu-id="0ace3-114">Description</span><span class="sxs-lookup"><span data-stu-id="0ace3-114">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ace3-115">La boîte de dialogue de contrôlea. Control2 doit avoir une propriété, car elle est de type RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="0ace3-115">Control DialogA.Control2 must have a property because it is of type RadioButtonGroup.</span></span>                                                                                      | <span data-ttu-id="0ace3-116">Il existe un [contrôle RadioButtonGroup](radiobuttongroup-control.md), sans le bit de [contrôle indirect](indirect-control-attribute.md) défini dans la colonne attributs de la [table de contrôle](control-table.md), pour laquelle aucune propriété n’est indiquée dans la colonne propriété.</span><span class="sxs-lookup"><span data-stu-id="0ace3-116">There is a [RadioButtonGroup control](radiobuttongroup-control.md), without the [Indirect control](indirect-control-attribute.md) bit set in the Attributes column of the [Control table](control-table.md), that does not have a property listed in the Property column.</span></span> |
| <span data-ttu-id="0ace3-117">Peut-être n’est pas une valeur par défaut valide pour RadioButtonGroup à l’aide de la propriété Property3.</span><span class="sxs-lookup"><span data-stu-id="0ace3-117">Maybe is not a valid default value for the RadioButtonGroup using property Property3.</span></span> <span data-ttu-id="0ace3-118">La valeur doit être indiquée en tant qu’option dans la table RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="0ace3-118">The value must be listed as an option in the RadioButtonGroup table.</span></span>                 | <span data-ttu-id="0ace3-119">Il existe une valeur par défaut pour une propriété spécifiée dans la colonne valeur de la [table de propriétés](property-table.md) qui ne fait pas partie des valeurs du groupe de cases d’option spécifié dans la colonne valeur de la [table RadioButton](radiobutton-table.md).</span><span class="sxs-lookup"><span data-stu-id="0ace3-119">There is a default value for a property specified in the Value column of the [Property table](property-table.md) that is not one of the values for the radio button group specified in the Value column of the [RadioButton table](radiobutton-table.md).</span></span>                  |
| <span data-ttu-id="0ace3-120">La propriété PropertyB doit être définie, car il s’agit d’une propriété indirecte d’une boîte de dialogue de contrôle RadioButtonGroupa. Control4</span><span class="sxs-lookup"><span data-stu-id="0ace3-120">Property PropertyB must be defined because it is an indirect property of a RadioButtonGroup control DialogA.Control4</span></span>                                                       | <span data-ttu-id="0ace3-121">La propriété référencée par ce groupe RadioButton est une propriété indirecte et la valeur de la propriété indirect n’est pas l’un des choix du groupe RadioButton.</span><span class="sxs-lookup"><span data-stu-id="0ace3-121">The property referenced by this RadioButton group is an indirect property, and the value of the indirect property is not one of the choices for the RadioButton group.</span></span>                                                                                                       |
| <span data-ttu-id="0ace3-122">Peut-être n’est pas une valeur par défaut valide pour la propriété PropertyA.</span><span class="sxs-lookup"><span data-stu-id="0ace3-122">Maybe is not a valid default value for the property PropertyA.</span></span> <span data-ttu-id="0ace3-123">La propriété est une propriété RadioButtonGroup indirecte de Control DIALOGA. Control5 (via la propriété Property5).</span><span class="sxs-lookup"><span data-stu-id="0ace3-123">The property is an indirect RadioButtonGroup property of control DialogA.Control5 (via property Property5).</span></span> | <span data-ttu-id="0ace3-124">La valeur de la propriété indirecte référencée via le contrôle n’est pas l’une des valeurs par défaut pour ce RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="0ace3-124">The value of the indirect property referenced via the control is not one of the default values for that RadioButtonGroup.</span></span>                                                                                                                                                    |



 

<span data-ttu-id="0ace3-125">[Table de contrôle](control-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="0ace3-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="0ace3-126">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0ace3-126">Dialog</span></span>  | <span data-ttu-id="0ace3-127">Contrôler</span><span class="sxs-lookup"><span data-stu-id="0ace3-127">Control</span></span>  | <span data-ttu-id="0ace3-128">Type</span><span class="sxs-lookup"><span data-stu-id="0ace3-128">Type</span></span>             | <span data-ttu-id="0ace3-129">Attributs</span><span class="sxs-lookup"><span data-stu-id="0ace3-129">Attributes</span></span> | <span data-ttu-id="0ace3-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ace3-130">Property</span></span>  |
|---------|----------|------------------|------------|-----------|
| <span data-ttu-id="0ace3-131">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0ace3-131">DialogA</span></span> | <span data-ttu-id="0ace3-132">Control1</span><span class="sxs-lookup"><span data-stu-id="0ace3-132">Control1</span></span> | <span data-ttu-id="0ace3-133">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0ace3-133">RadioButtonGroup</span></span> | <span data-ttu-id="0ace3-134">0</span><span class="sxs-lookup"><span data-stu-id="0ace3-134">0</span></span>          | <span data-ttu-id="0ace3-135">Property1</span><span class="sxs-lookup"><span data-stu-id="0ace3-135">Property1</span></span> |
| <span data-ttu-id="0ace3-136">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0ace3-136">DialogA</span></span> | <span data-ttu-id="0ace3-137">Control2</span><span class="sxs-lookup"><span data-stu-id="0ace3-137">Control2</span></span> | <span data-ttu-id="0ace3-138">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0ace3-138">RadioButtonGroup</span></span> | <span data-ttu-id="0ace3-139">0</span><span class="sxs-lookup"><span data-stu-id="0ace3-139">0</span></span>          |           |
| <span data-ttu-id="0ace3-140">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0ace3-140">DialogA</span></span> | <span data-ttu-id="0ace3-141">Control3</span><span class="sxs-lookup"><span data-stu-id="0ace3-141">Control3</span></span> | <span data-ttu-id="0ace3-142">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0ace3-142">RadioButtonGroup</span></span> | <span data-ttu-id="0ace3-143">0</span><span class="sxs-lookup"><span data-stu-id="0ace3-143">0</span></span>          | <span data-ttu-id="0ace3-144">Property3</span><span class="sxs-lookup"><span data-stu-id="0ace3-144">Property3</span></span> |
| <span data-ttu-id="0ace3-145">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0ace3-145">DialogA</span></span> | <span data-ttu-id="0ace3-146">Control4</span><span class="sxs-lookup"><span data-stu-id="0ace3-146">Control4</span></span> | <span data-ttu-id="0ace3-147">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0ace3-147">RadioButtonGroup</span></span> | <span data-ttu-id="0ace3-148">8</span><span class="sxs-lookup"><span data-stu-id="0ace3-148">8</span></span>          | <span data-ttu-id="0ace3-149">Property4</span><span class="sxs-lookup"><span data-stu-id="0ace3-149">Property4</span></span> |
| <span data-ttu-id="0ace3-150">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="0ace3-150">DialogA</span></span> | <span data-ttu-id="0ace3-151">Control5</span><span class="sxs-lookup"><span data-stu-id="0ace3-151">Control5</span></span> | <span data-ttu-id="0ace3-152">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0ace3-152">RadioButtonGroup</span></span> | <span data-ttu-id="0ace3-153">8</span><span class="sxs-lookup"><span data-stu-id="0ace3-153">8</span></span>          | <span data-ttu-id="0ace3-154">Property5</span><span class="sxs-lookup"><span data-stu-id="0ace3-154">Property5</span></span> |



 

<span data-ttu-id="0ace3-155">[Table de propriétés](property-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="0ace3-155">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="0ace3-156">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ace3-156">Property</span></span>  | <span data-ttu-id="0ace3-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ace3-157">Value</span></span>     |
|-----------|-----------|
| <span data-ttu-id="0ace3-158">Property1</span><span class="sxs-lookup"><span data-stu-id="0ace3-158">Property1</span></span> | <span data-ttu-id="0ace3-159">Oui</span><span class="sxs-lookup"><span data-stu-id="0ace3-159">Yes</span></span>       |
| <span data-ttu-id="0ace3-160">Property3</span><span class="sxs-lookup"><span data-stu-id="0ace3-160">Property3</span></span> | <span data-ttu-id="0ace3-161">Peut-être</span><span class="sxs-lookup"><span data-stu-id="0ace3-161">Maybe</span></span>     |
| <span data-ttu-id="0ace3-162">Property4</span><span class="sxs-lookup"><span data-stu-id="0ace3-162">Property4</span></span> | <span data-ttu-id="0ace3-163">PropertyB</span><span class="sxs-lookup"><span data-stu-id="0ace3-163">PropertyB</span></span> |
| <span data-ttu-id="0ace3-164">Property5</span><span class="sxs-lookup"><span data-stu-id="0ace3-164">Property5</span></span> | <span data-ttu-id="0ace3-165">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ace3-165">PropertyA</span></span> |
| <span data-ttu-id="0ace3-166">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ace3-166">PropertyA</span></span> | <span data-ttu-id="0ace3-167">Peut-être</span><span class="sxs-lookup"><span data-stu-id="0ace3-167">Maybe</span></span>     |



 

<span data-ttu-id="0ace3-168">[Table RadioButton](radiobutton-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="0ace3-168">[RadioButton Table](radiobutton-table.md) (partial)</span></span>



| <span data-ttu-id="0ace3-169">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ace3-169">Property</span></span>  | <span data-ttu-id="0ace3-170">Commande</span><span class="sxs-lookup"><span data-stu-id="0ace3-170">Order</span></span> | <span data-ttu-id="0ace3-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ace3-171">Value</span></span> |
|-----------|-------|-------|
| <span data-ttu-id="0ace3-172">Property1</span><span class="sxs-lookup"><span data-stu-id="0ace3-172">Property1</span></span> | <span data-ttu-id="0ace3-173">1</span><span class="sxs-lookup"><span data-stu-id="0ace3-173">1</span></span>     | <span data-ttu-id="0ace3-174">Oui</span><span class="sxs-lookup"><span data-stu-id="0ace3-174">Yes</span></span>   |
| <span data-ttu-id="0ace3-175">Property1</span><span class="sxs-lookup"><span data-stu-id="0ace3-175">Property1</span></span> | <span data-ttu-id="0ace3-176">2</span><span class="sxs-lookup"><span data-stu-id="0ace3-176">2</span></span>     | <span data-ttu-id="0ace3-177">maintenant</span><span class="sxs-lookup"><span data-stu-id="0ace3-177">Now</span></span>   |
| <span data-ttu-id="0ace3-178">Property2</span><span class="sxs-lookup"><span data-stu-id="0ace3-178">Property2</span></span> | <span data-ttu-id="0ace3-179">1</span><span class="sxs-lookup"><span data-stu-id="0ace3-179">1</span></span>     | <span data-ttu-id="0ace3-180">Oui</span><span class="sxs-lookup"><span data-stu-id="0ace3-180">Yes</span></span>   |
| <span data-ttu-id="0ace3-181">Property2</span><span class="sxs-lookup"><span data-stu-id="0ace3-181">Property2</span></span> | <span data-ttu-id="0ace3-182">2</span><span class="sxs-lookup"><span data-stu-id="0ace3-182">2</span></span>     | <span data-ttu-id="0ace3-183">Non</span><span class="sxs-lookup"><span data-stu-id="0ace3-183">No</span></span>    |
| <span data-ttu-id="0ace3-184">Property3</span><span class="sxs-lookup"><span data-stu-id="0ace3-184">Property3</span></span> | <span data-ttu-id="0ace3-185">1</span><span class="sxs-lookup"><span data-stu-id="0ace3-185">1</span></span>     | <span data-ttu-id="0ace3-186">Oui</span><span class="sxs-lookup"><span data-stu-id="0ace3-186">Yes</span></span>   |
| <span data-ttu-id="0ace3-187">Property3</span><span class="sxs-lookup"><span data-stu-id="0ace3-187">Property3</span></span> | <span data-ttu-id="0ace3-188">2</span><span class="sxs-lookup"><span data-stu-id="0ace3-188">2</span></span>     | <span data-ttu-id="0ace3-189">Non</span><span class="sxs-lookup"><span data-stu-id="0ace3-189">No</span></span>    |
| <span data-ttu-id="0ace3-190">Property4</span><span class="sxs-lookup"><span data-stu-id="0ace3-190">Property4</span></span> | <span data-ttu-id="0ace3-191">1</span><span class="sxs-lookup"><span data-stu-id="0ace3-191">1</span></span>     | <span data-ttu-id="0ace3-192">Oui</span><span class="sxs-lookup"><span data-stu-id="0ace3-192">Yes</span></span>   |
| <span data-ttu-id="0ace3-193">Property4</span><span class="sxs-lookup"><span data-stu-id="0ace3-193">Property4</span></span> | <span data-ttu-id="0ace3-194">2</span><span class="sxs-lookup"><span data-stu-id="0ace3-194">2</span></span>     | <span data-ttu-id="0ace3-195">Non</span><span class="sxs-lookup"><span data-stu-id="0ace3-195">No</span></span>    |
| <span data-ttu-id="0ace3-196">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ace3-196">PropertyA</span></span> | <span data-ttu-id="0ace3-197">1</span><span class="sxs-lookup"><span data-stu-id="0ace3-197">1</span></span>     | <span data-ttu-id="0ace3-198">Oui</span><span class="sxs-lookup"><span data-stu-id="0ace3-198">Yes</span></span>   |
| <span data-ttu-id="0ace3-199">Propriété</span><span class="sxs-lookup"><span data-stu-id="0ace3-199">PropertyA</span></span> | <span data-ttu-id="0ace3-200">2</span><span class="sxs-lookup"><span data-stu-id="0ace3-200">2</span></span>     | <span data-ttu-id="0ace3-201">Non</span><span class="sxs-lookup"><span data-stu-id="0ace3-201">No</span></span>    |
| <span data-ttu-id="0ace3-202">PropertyB</span><span class="sxs-lookup"><span data-stu-id="0ace3-202">PropertyB</span></span> | <span data-ttu-id="0ace3-203">1</span><span class="sxs-lookup"><span data-stu-id="0ace3-203">1</span></span>     | <span data-ttu-id="0ace3-204">Oui</span><span class="sxs-lookup"><span data-stu-id="0ace3-204">Yes</span></span>   |
| <span data-ttu-id="0ace3-205">PropertyB</span><span class="sxs-lookup"><span data-stu-id="0ace3-205">PropertyB</span></span> | <span data-ttu-id="0ace3-206">2</span><span class="sxs-lookup"><span data-stu-id="0ace3-206">2</span></span>     | <span data-ttu-id="0ace3-207">Non</span><span class="sxs-lookup"><span data-stu-id="0ace3-207">No</span></span>    |



 

<span data-ttu-id="0ace3-208">Pour corriger les erreurs signalées par cette glace, vérifiez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="0ace3-208">To fix the errors reported by this ICE, check the following:</span></span>

-   <span data-ttu-id="0ace3-209">Que chaque entrée de contrôle RadioButton sans l’ensemble d’attributs indirect a une propriété listée dans la colonne de propriété :</span><span class="sxs-lookup"><span data-stu-id="0ace3-209">That every RadioButton control entry without the indirect attribute set has a property listed in the Property column:</span></span>
-   <span data-ttu-id="0ace3-210">Que chaque propriété de ce type possède au moins une entrée correspondante dans la table de RadioButton.</span><span class="sxs-lookup"><span data-stu-id="0ace3-210">That every such property has at least one corresponding entry in the RadioButton table.</span></span>
-   <span data-ttu-id="0ace3-211">Que chaque propriété de ce type est définie dans la table de propriétés, avec une valeur qui est l’un des choix de la table de RadioButton.</span><span class="sxs-lookup"><span data-stu-id="0ace3-211">That every such property is defined in the Property table, with a value that is one of the choices from the RadioButton table.</span></span>
-   <span data-ttu-id="0ace3-212">Chaque propriété référencée dans la colonne de propriété d’un contrôle RadioButton avec l’ensemble d’attributs indirect est définie dans la table de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0ace3-212">That every property referenced in the Property column of a RadioButton control with the indirect attribute set is defined in the Property table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ace3-213">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ace3-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ace3-214">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="0ace3-214">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



