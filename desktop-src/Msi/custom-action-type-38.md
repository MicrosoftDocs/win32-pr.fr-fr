---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 38 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Type d’action personnalisé 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952514"
---
# <a name="custom-action-type-38"></a><span data-ttu-id="7a296-103">Type d’action personnalisé 38</span><span class="sxs-lookup"><span data-stu-id="7a296-103">Custom Action Type 38</span></span>

<span data-ttu-id="7a296-104">Cette action personnalisée est écrite en VBScript.</span><span class="sxs-lookup"><span data-stu-id="7a296-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="7a296-105">Voir aussi [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="7a296-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="7a296-106">Source</span><span class="sxs-lookup"><span data-stu-id="7a296-106">Source</span></span>

<span data-ttu-id="7a296-107">Le champ source de la [table CustomAction](customaction-table.md) contient la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7a296-107">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="7a296-108">Le code de script de l’action personnalisée est stocké sous la forme d’une chaîne de texte de script littéral dans le champ cible.</span><span class="sxs-lookup"><span data-stu-id="7a296-108">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="7a296-109">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="7a296-109">Type Value</span></span>

<span data-ttu-id="7a296-110">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7a296-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="7a296-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="7a296-111">Constants</span></span>                                                              | <span data-ttu-id="7a296-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="7a296-112">Hexadecimal</span></span> | <span data-ttu-id="7a296-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="7a296-113">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="7a296-114">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="7a296-114">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="7a296-115">0x026</span><span class="sxs-lookup"><span data-stu-id="7a296-115">0x026</span></span>       | <span data-ttu-id="7a296-116">38</span><span class="sxs-lookup"><span data-stu-id="7a296-116">38</span></span>      |



 

<span data-ttu-id="7a296-117">Windows Installer pouvez utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a296-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="7a296-118">Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique.</span><span class="sxs-lookup"><span data-stu-id="7a296-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="7a296-119">Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="7a296-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="7a296-120">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a296-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="7a296-121">Constantes</span><span class="sxs-lookup"><span data-stu-id="7a296-121">Constants</span></span>                                                                                                     | <span data-ttu-id="7a296-122">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="7a296-122">Hexadecimal</span></span> | <span data-ttu-id="7a296-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="7a296-123">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="7a296-124">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="7a296-124">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="7a296-125">0x0001026</span><span class="sxs-lookup"><span data-stu-id="7a296-125">0x0001026</span></span>   | <span data-ttu-id="7a296-126">4134</span><span class="sxs-lookup"><span data-stu-id="7a296-126">4134</span></span>    |



 

## <a name="target"></a><span data-ttu-id="7a296-127">Cible</span><span class="sxs-lookup"><span data-stu-id="7a296-127">Target</span></span>

<span data-ttu-id="7a296-128">Le champ cible de la [table CustomAction](customaction-table.md) contient le code de script de l’action personnalisée sous la forme d’une chaîne de texte de script littéral.</span><span class="sxs-lookup"><span data-stu-id="7a296-128">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="7a296-129">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="7a296-129">Return Processing Options</span></span>

<span data-ttu-id="7a296-130">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="7a296-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="7a296-131">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="7a296-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="7a296-132">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="7a296-132">Execution Scheduling Options</span></span>

<span data-ttu-id="7a296-133">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7a296-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="7a296-134">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7a296-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="7a296-135">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="7a296-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="7a296-136">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="7a296-136">In-Script Execution Options</span></span>

<span data-ttu-id="7a296-137">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="7a296-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="7a296-138">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="7a296-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="7a296-139">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="7a296-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="7a296-140">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7a296-140">Return Values</span></span>

<span data-ttu-id="7a296-141">Ce type d’action personnalisé retourne toujours Success.</span><span class="sxs-lookup"><span data-stu-id="7a296-141">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a296-142">Notes</span><span class="sxs-lookup"><span data-stu-id="7a296-142">Remarks</span></span>

<span data-ttu-id="7a296-143">Une action personnalisée écrite en JScript ou VBScript requiert l’objet de [**session**](session-object.md) d’installation.</span><span class="sxs-lookup"><span data-stu-id="7a296-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="7a296-144">Le programme d’installation joint l' **objet de session** au script avec le nom « session ».</span><span class="sxs-lookup"><span data-stu-id="7a296-144">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="7a296-145">Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.</span><span class="sxs-lookup"><span data-stu-id="7a296-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a296-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a296-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a296-147">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="7a296-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



