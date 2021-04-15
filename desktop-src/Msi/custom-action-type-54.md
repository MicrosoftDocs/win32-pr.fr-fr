---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 54 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Type d’action personnalisé 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485489"
---
# <a name="custom-action-type-54"></a><span data-ttu-id="3de81-103">Type d’action personnalisé 54</span><span class="sxs-lookup"><span data-stu-id="3de81-103">Custom Action Type 54</span></span>

<span data-ttu-id="3de81-104">Cette action personnalisée est écrite en VBScript.</span><span class="sxs-lookup"><span data-stu-id="3de81-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="3de81-105">Voir aussi [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="3de81-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="3de81-106">Source</span><span class="sxs-lookup"><span data-stu-id="3de81-106">Source</span></span>

<span data-ttu-id="3de81-107">Le champ source de la [table CustomAction](customaction-table.md) contient un nom de propriété ou une clé de la [table de propriétés](property-table.md) pour une propriété contenant le texte du script.</span><span class="sxs-lookup"><span data-stu-id="3de81-107">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="3de81-108">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="3de81-108">Type Value</span></span>

<span data-ttu-id="3de81-109">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3de81-109">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="3de81-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="3de81-110">Constants</span></span>                                                             | <span data-ttu-id="3de81-111">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="3de81-111">Hexadecimal</span></span> | <span data-ttu-id="3de81-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="3de81-112">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3de81-113">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="3de81-113">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="3de81-114">0x036</span><span class="sxs-lookup"><span data-stu-id="3de81-114">0x036</span></span>       | <span data-ttu-id="3de81-115">54</span><span class="sxs-lookup"><span data-stu-id="3de81-115">54</span></span>      |



 

<span data-ttu-id="3de81-116">Windows Installer pouvez utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3de81-116">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="3de81-117">Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique.</span><span class="sxs-lookup"><span data-stu-id="3de81-117">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="3de81-118">Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3de81-118">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="3de81-119">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3de81-119">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="3de81-120">Constantes</span><span class="sxs-lookup"><span data-stu-id="3de81-120">Constants</span></span>                                                                                                    | <span data-ttu-id="3de81-121">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="3de81-121">Hexadecimal</span></span> | <span data-ttu-id="3de81-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="3de81-122">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="3de81-123">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="3de81-123">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="3de81-124">0x0001036</span><span class="sxs-lookup"><span data-stu-id="3de81-124">0x0001036</span></span>   | <span data-ttu-id="3de81-125">4150</span><span class="sxs-lookup"><span data-stu-id="3de81-125">4150</span></span>    |



 

## <a name="target"></a><span data-ttu-id="3de81-126">Cible</span><span class="sxs-lookup"><span data-stu-id="3de81-126">Target</span></span>

<span data-ttu-id="3de81-127">Le champ cible de la [table CustomAction](customaction-table.md) contient une fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="3de81-127">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="3de81-128">Le traitement envoie tout d’abord le script pour l’analyse, puis appelle la fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="3de81-128">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="3de81-129">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="3de81-129">Return Processing Options</span></span>

<span data-ttu-id="3de81-130">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="3de81-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="3de81-131">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="3de81-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="3de81-132">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="3de81-132">Execution Scheduling Options</span></span>

<span data-ttu-id="3de81-133">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3de81-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="3de81-134">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="3de81-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="3de81-135">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="3de81-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="3de81-136">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="3de81-136">In-Script Execution Options</span></span>

<span data-ttu-id="3de81-137">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="3de81-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="3de81-138">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="3de81-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="3de81-139">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="3de81-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="3de81-140">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3de81-140">Return Values</span></span>

<span data-ttu-id="3de81-141">Les fonctions facultatives écrites dans le script doivent retourner l’une des valeurs décrites dans les [valeurs de retour des actions personnalisées JScript et VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3de81-141">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3de81-142">Notes</span><span class="sxs-lookup"><span data-stu-id="3de81-142">Remarks</span></span>

<span data-ttu-id="3de81-143">Une action personnalisée écrite en JScript ou VBScript requiert l’objet de [**session**](session-object.md) d’installation.</span><span class="sxs-lookup"><span data-stu-id="3de81-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="3de81-144">Le programme d’installation joint l' **objet de session** au script avec la *session* de nom.</span><span class="sxs-lookup"><span data-stu-id="3de81-144">The installer attaches the **Session Object** to the script with the name *Session*.</span></span> <span data-ttu-id="3de81-145">Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.</span><span class="sxs-lookup"><span data-stu-id="3de81-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3de81-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3de81-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3de81-147">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="3de81-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



