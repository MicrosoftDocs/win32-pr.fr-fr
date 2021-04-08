---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 37 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Type d’action personnalisé 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a42d4837af6fe2878f33624251d9c06550855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034958"
---
# <a name="custom-action-type-37"></a><span data-ttu-id="9acab-103">Type d’action personnalisé 37</span><span class="sxs-lookup"><span data-stu-id="9acab-103">Custom Action Type 37</span></span>

<span data-ttu-id="9acab-104">Cette action personnalisée est écrite en JScript, telle que l’ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="9acab-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="9acab-105">Windows Installer ne prend pas en charge JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="9acab-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="9acab-106">Pour plus d’informations, consultez [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9acab-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="9acab-107">Source</span><span class="sxs-lookup"><span data-stu-id="9acab-107">Source</span></span>

<span data-ttu-id="9acab-108">Le champ source de la [table CustomAction](customaction-table.md) contient la valeur null.</span><span class="sxs-lookup"><span data-stu-id="9acab-108">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="9acab-109">Le code de script de l’action personnalisée est stocké sous la forme d’une chaîne de texte de script littéral dans le champ cible.</span><span class="sxs-lookup"><span data-stu-id="9acab-109">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="9acab-110">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="9acab-110">Type Value</span></span>

<span data-ttu-id="9acab-111">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9acab-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="9acab-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="9acab-112">Constants</span></span>                                                             | <span data-ttu-id="9acab-113">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="9acab-113">Hexadecimal</span></span> | <span data-ttu-id="9acab-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="9acab-114">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9acab-115">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="9acab-115">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="9acab-116">0x025</span><span class="sxs-lookup"><span data-stu-id="9acab-116">0x025</span></span>       | <span data-ttu-id="9acab-117">37</span><span class="sxs-lookup"><span data-stu-id="9acab-117">37</span></span>      |



 

<span data-ttu-id="9acab-118">Windows Installer pouvez utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9acab-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="9acab-119">Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique.</span><span class="sxs-lookup"><span data-stu-id="9acab-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="9acab-120">Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9acab-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="9acab-121">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9acab-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="9acab-122">Constantes</span><span class="sxs-lookup"><span data-stu-id="9acab-122">Constants</span></span>                                                                                                    | <span data-ttu-id="9acab-123">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="9acab-123">Hexadecimal</span></span> | <span data-ttu-id="9acab-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="9acab-124">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="9acab-125">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="9acab-125">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="9acab-126">0x0001025</span><span class="sxs-lookup"><span data-stu-id="9acab-126">0x0001025</span></span>   | <span data-ttu-id="9acab-127">4133</span><span class="sxs-lookup"><span data-stu-id="9acab-127">4133</span></span>    |



 

## <a name="target"></a><span data-ttu-id="9acab-128">Cible</span><span class="sxs-lookup"><span data-stu-id="9acab-128">Target</span></span>

<span data-ttu-id="9acab-129">Le champ cible de la [table CustomAction](customaction-table.md) contient le code de script de l’action personnalisée sous la forme d’une chaîne de texte de script littéral.</span><span class="sxs-lookup"><span data-stu-id="9acab-129">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="9acab-130">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="9acab-130">Return Processing Options</span></span>

<span data-ttu-id="9acab-131">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="9acab-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="9acab-132">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="9acab-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="9acab-133">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="9acab-133">Execution Scheduling Options</span></span>

<span data-ttu-id="9acab-134">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9acab-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="9acab-135">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="9acab-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="9acab-136">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="9acab-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="9acab-137">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="9acab-137">In-Script Execution Options</span></span>

<span data-ttu-id="9acab-138">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="9acab-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="9acab-139">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="9acab-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="9acab-140">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="9acab-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="9acab-141">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="9acab-141">Return Values</span></span>

<span data-ttu-id="9acab-142">Ce type d’action personnalisé retourne toujours Success.</span><span class="sxs-lookup"><span data-stu-id="9acab-142">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="9acab-143">Notes</span><span class="sxs-lookup"><span data-stu-id="9acab-143">Remarks</span></span>

<span data-ttu-id="9acab-144">Une action personnalisée écrite en JScript ou VBScript requiert l’objet de [**session**](session-object.md) d’installation.</span><span class="sxs-lookup"><span data-stu-id="9acab-144">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="9acab-145">Le programme d’installation joint l' **objet de session** au script avec le nom « session ».</span><span class="sxs-lookup"><span data-stu-id="9acab-145">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="9acab-146">Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.</span><span class="sxs-lookup"><span data-stu-id="9acab-146">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9acab-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9acab-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9acab-148">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="9acab-148">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



