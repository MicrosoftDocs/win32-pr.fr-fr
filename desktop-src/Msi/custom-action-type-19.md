---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser une action personnalisée de type 19 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Type d’action personnalisée 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531432"
---
# <a name="custom-action-type-19"></a><span data-ttu-id="3e75e-103">Type d’action personnalisée 19</span><span class="sxs-lookup"><span data-stu-id="3e75e-103">Custom Action Type 19</span></span>

<span data-ttu-id="3e75e-104">Cette action personnalisée affiche un message d’erreur spécifié, retourne un échec, puis termine l’installation.</span><span class="sxs-lookup"><span data-stu-id="3e75e-104">This custom action displays a specified error message, returns failure, and then terminates the installation.</span></span> <span data-ttu-id="3e75e-105">Le message d’erreur affiché peut être fourni sous la forme d’une chaîne ou d’un index dans la [table d’erreurs](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="3e75e-105">The error message displayed can be supplied as a string or as an index into the [Error table](error-table.md).</span></span>

## <a name="source"></a><span data-ttu-id="3e75e-106">Source</span><span class="sxs-lookup"><span data-stu-id="3e75e-106">Source</span></span>

<span data-ttu-id="3e75e-107">Laissez la colonne source de la [table CustomAction](customaction-table.md) vide.</span><span class="sxs-lookup"><span data-stu-id="3e75e-107">Leave the Source column of the [CustomAction table](customaction-table.md) blank.</span></span>

## <a name="type-value"></a><span data-ttu-id="3e75e-108">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="3e75e-108">Type Value</span></span>

<span data-ttu-id="3e75e-109">Incluez la valeur suivante dans la colonne type de la table CustomAction pour spécifier le type numérique de base.</span><span class="sxs-lookup"><span data-stu-id="3e75e-109">Include the following value in the Type column of the CustomAction table to specify the basic numeric type.</span></span>



| <span data-ttu-id="3e75e-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="3e75e-110">Constants</span></span>                                                               | <span data-ttu-id="3e75e-111">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="3e75e-111">Hexadecimal</span></span> | <span data-ttu-id="3e75e-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="3e75e-112">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3e75e-113">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="3e75e-113">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="3e75e-114">0x013</span><span class="sxs-lookup"><span data-stu-id="3e75e-114">0x013</span></span>       | <span data-ttu-id="3e75e-115">19</span><span class="sxs-lookup"><span data-stu-id="3e75e-115">19</span></span>      |



 

## <a name="target"></a><span data-ttu-id="3e75e-116">Cible</span><span class="sxs-lookup"><span data-stu-id="3e75e-116">Target</span></span>

<span data-ttu-id="3e75e-117">La colonne cible de la [table CustomAction](customaction-table.md) contient une chaîne de texte mise en forme à l’aide de la fonctionnalité spécifiée dans [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sans les spécificateurs de champ numérique).</span><span class="sxs-lookup"><span data-stu-id="3e75e-117">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="3e75e-118">Les paramètres à remplacer sont placés entre crochets, \[ ... \] et peuvent être des propriétés, des variables d’environnement (% prefix), des chemins d’accès de fichier (préfixe \# ) ou des chemins d’accès de répertoire de composant ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="3e75e-118">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="3e75e-119">Si, après la mise en forme de la chaîne, la valeur est un entier, cet entier est utilisé comme index dans la [table d’erreurs](error-table.md) pour récupérer le message à afficher.</span><span class="sxs-lookup"><span data-stu-id="3e75e-119">If after formatting the string evaluates to an integer, that integer is used as an index into the [Error table](error-table.md) to retrieve the message to display.</span></span> <span data-ttu-id="3e75e-120">Si, après la mise en forme, la chaîne contient des caractères non numériques, la chaîne est affichée en tant que message.</span><span class="sxs-lookup"><span data-stu-id="3e75e-120">If after formatting the string contains non-numeric characters, the string itself is displayed as the message.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="3e75e-121">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="3e75e-121">Return Processing Options</span></span>

<span data-ttu-id="3e75e-122">L’action personnalisée n’utilise pas d’options.</span><span class="sxs-lookup"><span data-stu-id="3e75e-122">The custom action does not use any options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="3e75e-123">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="3e75e-123">Execution Scheduling Options</span></span>

<span data-ttu-id="3e75e-124">L’action personnalisée n’utilise pas d’options.</span><span class="sxs-lookup"><span data-stu-id="3e75e-124">The custom action does not use any options.</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="3e75e-125">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="3e75e-125">In-Script Execution Options</span></span>

<span data-ttu-id="3e75e-126">L’action personnalisée n’utilise pas d’options.</span><span class="sxs-lookup"><span data-stu-id="3e75e-126">The custom action does not use any options.</span></span>

## <a name="return-values"></a><span data-ttu-id="3e75e-127">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3e75e-127">Return Values</span></span>

<span data-ttu-id="3e75e-128">Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3e75e-128">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e75e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="3e75e-129">Remarks</span></span>

<span data-ttu-id="3e75e-130">Par exemple, les actions personnalisées CAError1, CAError2, CAError3 et CAError4 retournent ces messages.</span><span class="sxs-lookup"><span data-stu-id="3e75e-130">For example, the custom actions CAError1, CAError2, CAError3, and CAError4 return these messages.</span></span>

[<span data-ttu-id="3e75e-131">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="3e75e-131">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="3e75e-132">Action</span><span class="sxs-lookup"><span data-stu-id="3e75e-132">Action</span></span>   | <span data-ttu-id="3e75e-133">Type</span><span class="sxs-lookup"><span data-stu-id="3e75e-133">Type</span></span> | <span data-ttu-id="3e75e-134">Source</span><span class="sxs-lookup"><span data-stu-id="3e75e-134">Source</span></span> | <span data-ttu-id="3e75e-135">Cible</span><span class="sxs-lookup"><span data-stu-id="3e75e-135">Target</span></span>                              |
|----------|------|--------|-------------------------------------|
| <span data-ttu-id="3e75e-136">CAError1</span><span class="sxs-lookup"><span data-stu-id="3e75e-136">CAError1</span></span> | <span data-ttu-id="3e75e-137">19</span><span class="sxs-lookup"><span data-stu-id="3e75e-137">19</span></span>   |        | <span data-ttu-id="3e75e-138">\[Prop1\]</span><span class="sxs-lookup"><span data-stu-id="3e75e-138">\[Prop1\]</span></span>                           |
| <span data-ttu-id="3e75e-139">CAError2</span><span class="sxs-lookup"><span data-stu-id="3e75e-139">CAError2</span></span> | <span data-ttu-id="3e75e-140">19</span><span class="sxs-lookup"><span data-stu-id="3e75e-140">19</span></span>   |        | <span data-ttu-id="3e75e-141">Échec de l’installation en raison de Error2.</span><span class="sxs-lookup"><span data-stu-id="3e75e-141">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="3e75e-142">CAError3</span><span class="sxs-lookup"><span data-stu-id="3e75e-142">CAError3</span></span> | <span data-ttu-id="3e75e-143">19</span><span class="sxs-lookup"><span data-stu-id="3e75e-143">19</span></span>   |        | <span data-ttu-id="3e75e-144">25000</span><span class="sxs-lookup"><span data-stu-id="3e75e-144">25000</span></span>                               |
| <span data-ttu-id="3e75e-145">CAError4</span><span class="sxs-lookup"><span data-stu-id="3e75e-145">CAError4</span></span> | <span data-ttu-id="3e75e-146">19</span><span class="sxs-lookup"><span data-stu-id="3e75e-146">19</span></span>   |        | <span data-ttu-id="3e75e-147">\[Prop2\]</span><span class="sxs-lookup"><span data-stu-id="3e75e-147">\[Prop2\]</span></span>                           |



 

[<span data-ttu-id="3e75e-148">Table de propriétés</span><span class="sxs-lookup"><span data-stu-id="3e75e-148">Property Table</span></span>](property-table.md)



| <span data-ttu-id="3e75e-149">Propriété</span><span class="sxs-lookup"><span data-stu-id="3e75e-149">Property</span></span> | <span data-ttu-id="3e75e-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e75e-150">Value</span></span>                                 |
|----------|---------------------------------------|
| <span data-ttu-id="3e75e-151">Prop1</span><span class="sxs-lookup"><span data-stu-id="3e75e-151">Prop1</span></span>    | <span data-ttu-id="3e75e-152">« Échec de l’installation en raison de Error1 ».</span><span class="sxs-lookup"><span data-stu-id="3e75e-152">"Installation failure due to Error1."</span></span> |
| <span data-ttu-id="3e75e-153">Prop2</span><span class="sxs-lookup"><span data-stu-id="3e75e-153">Prop2</span></span>    | <span data-ttu-id="3e75e-154">« 25100 »</span><span class="sxs-lookup"><span data-stu-id="3e75e-154">"25100"</span></span>                               |



 

[<span data-ttu-id="3e75e-155">Table des erreurs</span><span class="sxs-lookup"><span data-stu-id="3e75e-155">Error Table</span></span>](error-table.md)



| <span data-ttu-id="3e75e-156">Code</span><span class="sxs-lookup"><span data-stu-id="3e75e-156">Code</span></span>  | <span data-ttu-id="3e75e-157">Message</span><span class="sxs-lookup"><span data-stu-id="3e75e-157">Message</span></span>                             |
|-------|-------------------------------------|
| <span data-ttu-id="3e75e-158">25000</span><span class="sxs-lookup"><span data-stu-id="3e75e-158">25000</span></span> | <span data-ttu-id="3e75e-159">Échec de l’installation en raison de Error3.</span><span class="sxs-lookup"><span data-stu-id="3e75e-159">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="3e75e-160">25100</span><span class="sxs-lookup"><span data-stu-id="3e75e-160">25100</span></span> | <span data-ttu-id="3e75e-161">Échec de l’installation en raison de Error4.</span><span class="sxs-lookup"><span data-stu-id="3e75e-161">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="3e75e-162">Ces actions personnalisées retournent les messages d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="3e75e-162">These custom actions return the following error messages:</span></span>



| <span data-ttu-id="3e75e-163">Action personnalisée</span><span class="sxs-lookup"><span data-stu-id="3e75e-163">Custom action</span></span> | <span data-ttu-id="3e75e-164">Chaîne de message retournée</span><span class="sxs-lookup"><span data-stu-id="3e75e-164">Returned message string</span></span>             |
|---------------|-------------------------------------|
| <span data-ttu-id="3e75e-165">CAError1</span><span class="sxs-lookup"><span data-stu-id="3e75e-165">CAError1</span></span>      | <span data-ttu-id="3e75e-166">Échec de l’installation en raison de Error1.</span><span class="sxs-lookup"><span data-stu-id="3e75e-166">Installation failure due to Error1.</span></span> |
| <span data-ttu-id="3e75e-167">CAError2</span><span class="sxs-lookup"><span data-stu-id="3e75e-167">CAError2</span></span>      | <span data-ttu-id="3e75e-168">Échec de l’installation en raison de Error2.</span><span class="sxs-lookup"><span data-stu-id="3e75e-168">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="3e75e-169">CAError3</span><span class="sxs-lookup"><span data-stu-id="3e75e-169">CAError3</span></span>      | <span data-ttu-id="3e75e-170">Échec de l’installation en raison de Error3.</span><span class="sxs-lookup"><span data-stu-id="3e75e-170">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="3e75e-171">CAError4</span><span class="sxs-lookup"><span data-stu-id="3e75e-171">CAError4</span></span>      | <span data-ttu-id="3e75e-172">Échec de l’installation en raison de Error4.</span><span class="sxs-lookup"><span data-stu-id="3e75e-172">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="3e75e-173">Notez que, étant donné que l’ordre d’évaluation des conditions de lancement ne peut pas être garanti en créant la [table LaunchCondition](launchcondition-table.md), vous devez utiliser une action personnalisée type 19 actions personnalisées dans votre installation pour évaluer des conditions dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="3e75e-173">Note that because the order of evaluation of launch conditions cannot be guaranteed by authoring the [LaunchCondition table](launchcondition-table.md), you should use Custom Action Type 19 custom actions in your installation to evaluate conditions in a specific order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e75e-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e75e-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e75e-175">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="3e75e-175">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



