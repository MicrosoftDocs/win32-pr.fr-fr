---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 53 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Type d’action personnalisé 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a016d3b3f5a282567b909215d6ab7b32759417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952314"
---
# <a name="custom-action-type-53"></a><span data-ttu-id="edd8c-103">Type d’action personnalisé 53</span><span class="sxs-lookup"><span data-stu-id="edd8c-103">Custom Action Type 53</span></span>

<span data-ttu-id="edd8c-104">Cette action personnalisée est écrite en JScript, telle que l’ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="edd8c-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="edd8c-105">Windows Installer ne prend pas en charge JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="edd8c-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="edd8c-106">Pour plus d’informations, consultez [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="edd8c-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="edd8c-107">Source</span><span class="sxs-lookup"><span data-stu-id="edd8c-107">Source</span></span>

<span data-ttu-id="edd8c-108">Le champ source de la [table CustomAction](customaction-table.md) contient un nom de propriété ou une clé de la [table de propriétés](property-table.md) pour une propriété contenant le texte du script.</span><span class="sxs-lookup"><span data-stu-id="edd8c-108">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="edd8c-109">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="edd8c-109">Type Value</span></span>

<span data-ttu-id="edd8c-110">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="edd8c-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="edd8c-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="edd8c-111">Constants</span></span>                                                            | <span data-ttu-id="edd8c-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="edd8c-112">Hexadecimal</span></span> | <span data-ttu-id="edd8c-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="edd8c-113">Decimal</span></span> |
|----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="edd8c-114">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="edd8c-114">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="edd8c-115">0x035</span><span class="sxs-lookup"><span data-stu-id="edd8c-115">0x035</span></span>       | <span data-ttu-id="edd8c-116">53</span><span class="sxs-lookup"><span data-stu-id="edd8c-116">53</span></span>      |



 

<span data-ttu-id="edd8c-117">Windows Installer pouvez utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="edd8c-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="edd8c-118">Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique.</span><span class="sxs-lookup"><span data-stu-id="edd8c-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="edd8c-119">Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="edd8c-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="edd8c-120">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.</span><span class="sxs-lookup"><span data-stu-id="edd8c-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="edd8c-121">Constantes</span><span class="sxs-lookup"><span data-stu-id="edd8c-121">Constants</span></span>                                                                                                   | <span data-ttu-id="edd8c-122">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="edd8c-122">Hexadecimal</span></span> | <span data-ttu-id="edd8c-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="edd8c-123">Decimal</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="edd8c-124">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="edd8c-124">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="edd8c-125">0x0001035</span><span class="sxs-lookup"><span data-stu-id="edd8c-125">0x0001035</span></span>   | <span data-ttu-id="edd8c-126">4149</span><span class="sxs-lookup"><span data-stu-id="edd8c-126">4149</span></span>    |



 

## <a name="target"></a><span data-ttu-id="edd8c-127">Cible</span><span class="sxs-lookup"><span data-stu-id="edd8c-127">Target</span></span>

<span data-ttu-id="edd8c-128">Le champ cible de la [table CustomAction](customaction-table.md) contient une fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="edd8c-128">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="edd8c-129">Le traitement envoie tout d’abord le script pour l’analyse, puis appelle la fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="edd8c-129">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="edd8c-130">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="edd8c-130">Return Processing Options</span></span>

<span data-ttu-id="edd8c-131">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="edd8c-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="edd8c-132">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="edd8c-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="edd8c-133">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="edd8c-133">Execution Scheduling Options</span></span>

<span data-ttu-id="edd8c-134">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="edd8c-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="edd8c-135">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="edd8c-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="edd8c-136">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="edd8c-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="edd8c-137">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="edd8c-137">In-Script Execution Options</span></span>

<span data-ttu-id="edd8c-138">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="edd8c-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="edd8c-139">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="edd8c-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="edd8c-140">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="edd8c-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="edd8c-141">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="edd8c-141">Return Values</span></span>

<span data-ttu-id="edd8c-142">Les fonctions facultatives écrites dans le script doivent retourner l’une des valeurs décrites dans les [valeurs de retour des actions personnalisées JScript et VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="edd8c-142">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="edd8c-143">Notes</span><span class="sxs-lookup"><span data-stu-id="edd8c-143">Remarks</span></span>

<span data-ttu-id="edd8c-144">Une action personnalisée écrite en JScript requiert l’objet de [**session**](session-object.md) d’installation.</span><span class="sxs-lookup"><span data-stu-id="edd8c-144">A custom action that is written in JScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="edd8c-145">Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration d’installation, une action personnalisée différée écrite dans un script utilise l’une des méthodes décrites dans [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="edd8c-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script uses one of the methods described in [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="edd8c-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="edd8c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edd8c-147">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="edd8c-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



