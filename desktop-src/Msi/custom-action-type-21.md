---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser une action personnalisée de type 21 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Type d’action personnalisée 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5bb7482c2f7c7b6cbd85af7a6f01cc83edbb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320574"
---
# <a name="custom-action-type-21"></a><span data-ttu-id="d4c64-103">Type d’action personnalisée 21</span><span class="sxs-lookup"><span data-stu-id="d4c64-103">Custom Action Type 21</span></span>

<span data-ttu-id="d4c64-104">Cette action personnalisée est écrite en JScript, telle que l’ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="d4c64-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="d4c64-105">Windows Installer ne prend pas en charge JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="d4c64-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="d4c64-106">Pour plus d’informations, consultez [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="d4c64-107">Source</span><span class="sxs-lookup"><span data-stu-id="d4c64-107">Source</span></span>

<span data-ttu-id="d4c64-108">Le script est installé avec l’application pendant la session active.</span><span class="sxs-lookup"><span data-stu-id="d4c64-108">The script is installed with the application during the current session.</span></span> <span data-ttu-id="d4c64-109">Le champ source de la [table CustomAction](customaction-table.md) contient une clé de la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="d4c64-110">L’emplacement du code d’action personnalisé est déterminé par la résolution du chemin d’accès cible de ce fichier ; par conséquent, cette action personnalisée doit être appelée une fois que le fichier a été installé et avant d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="d4c64-110">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="d4c64-111">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="d4c64-111">Type Value</span></span>

<span data-ttu-id="d4c64-112">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d4c64-112">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="d4c64-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="d4c64-113">Constants</span></span>                                                              | <span data-ttu-id="d4c64-114">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="d4c64-114">Hexadecimal</span></span> | <span data-ttu-id="d4c64-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="d4c64-115">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="d4c64-116">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="d4c64-116">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="d4c64-117">0x015</span><span class="sxs-lookup"><span data-stu-id="d4c64-117">0x015</span></span>       | <span data-ttu-id="d4c64-118">21</span><span class="sxs-lookup"><span data-stu-id="d4c64-118">21</span></span>      |



 

<span data-ttu-id="d4c64-119">Windows Installer pouvez utiliser des [actions personnalisées 64 bits](64-bit-custom-actions.md) sur les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d4c64-119">Windows Installer may use [64-bit Custom Actions](64-bit-custom-actions.md) on 64-bit operating systems.</span></span> <span data-ttu-id="d4c64-120">Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique.</span><span class="sxs-lookup"><span data-stu-id="d4c64-120">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="d4c64-121">Pour plus d’informations, consultez actions personnalisées 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d4c64-121">For information see 64-bit Custom Actions.</span></span> <span data-ttu-id="d4c64-122">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d4c64-122">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="d4c64-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="d4c64-123">Constants</span></span>                                                                                                     | <span data-ttu-id="d4c64-124">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="d4c64-124">Hexadecimal</span></span> | <span data-ttu-id="d4c64-125">Decimal</span><span class="sxs-lookup"><span data-stu-id="d4c64-125">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="d4c64-126">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="d4c64-126">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="d4c64-127">0x0001015</span><span class="sxs-lookup"><span data-stu-id="d4c64-127">0x0001015</span></span>   | <span data-ttu-id="d4c64-128">4117</span><span class="sxs-lookup"><span data-stu-id="d4c64-128">4117</span></span>    |



 

## <a name="target"></a><span data-ttu-id="d4c64-129">Cible</span><span class="sxs-lookup"><span data-stu-id="d4c64-129">Target</span></span>

<span data-ttu-id="d4c64-130">Le champ cible de la [table CustomAction](customaction-table.md) contient une fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="d4c64-130">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="d4c64-131">Le traitement envoie tout d’abord le script pour l’analyse, puis appelle la fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="d4c64-131">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="d4c64-132">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="d4c64-132">Return Processing Options</span></span>

<span data-ttu-id="d4c64-133">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="d4c64-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="d4c64-134">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-134">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="d4c64-135">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="d4c64-135">Execution Scheduling Options</span></span>

<span data-ttu-id="d4c64-136">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d4c64-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="d4c64-137">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="d4c64-137">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="d4c64-138">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-138">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="d4c64-139">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="d4c64-139">In-Script Execution Options</span></span>

<span data-ttu-id="d4c64-140">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="d4c64-140">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="d4c64-141">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="d4c64-141">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="d4c64-142">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-142">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="d4c64-143">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="d4c64-143">Return Values</span></span>

<span data-ttu-id="d4c64-144">Les fonctions facultatives écrites dans le script doivent retourner l’une des valeurs décrites dans les [valeurs de retour des actions personnalisées JScript et VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-144">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c64-145">Notes</span><span class="sxs-lookup"><span data-stu-id="d4c64-145">Remarks</span></span>

<span data-ttu-id="d4c64-146">Une action personnalisée écrite en JScript ou VBScript requiert l’objet de [**session**](session-object.md) d’installation.</span><span class="sxs-lookup"><span data-stu-id="d4c64-146">A custom action that is written in JScript or VBScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="d4c64-147">Le programme d’installation joint l' **objet de session** au script avec le nom « session ».</span><span class="sxs-lookup"><span data-stu-id="d4c64-147">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="d4c64-148">Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.</span><span class="sxs-lookup"><span data-stu-id="d4c64-148">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="d4c64-149">Les actions personnalisées qui font référence à un fichier installé comme source, telles que le type d’action personnalisé 21 (JScript), doivent respecter les restrictions de séquencement suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4c64-149">Custom actions that reference an installed file as their source, such as Custom Action Type 21 (JScript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="d4c64-150">L’action personnalisée doit être séquencée après l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-150">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="d4c64-151">Cela permet à l’action personnalisée de résoudre le chemin d’accès nécessaire pour localiser le fichier source contenant JScript.</span><span class="sxs-lookup"><span data-stu-id="d4c64-151">This is so that the custom action can resolve the path needed to locate the source file containing the JScript.</span></span>
-   <span data-ttu-id="d4c64-152">Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées différées (dans le script) de ce type doivent être séquencées après l' [action InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-152">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="d4c64-153">Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées non différées de ce type doivent être séquencées après l' [action InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d4c64-153">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4c64-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4c64-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4c64-155">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="d4c64-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



