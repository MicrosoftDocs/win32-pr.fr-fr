---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 17 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Type d’action personnalisée 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320577"
---
# <a name="custom-action-type-17"></a><span data-ttu-id="b74dd-103">Type d’action personnalisée 17</span><span class="sxs-lookup"><span data-stu-id="b74dd-103">Custom Action Type 17</span></span>

<span data-ttu-id="b74dd-104">Cette action personnalisée appelle une bibliothèque de liens dynamiques (DLL) écrite en C ou C++.</span><span class="sxs-lookup"><span data-stu-id="b74dd-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="b74dd-105">Source</span><span class="sxs-lookup"><span data-stu-id="b74dd-105">Source</span></span>

<span data-ttu-id="b74dd-106">La DLL est installée avec l’application pendant la session active.</span><span class="sxs-lookup"><span data-stu-id="b74dd-106">The DLL is installed with the application during the current session.</span></span> <span data-ttu-id="b74dd-107">Le champ source de la [table CustomAction](customaction-table.md) contient une clé de la [table de fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="b74dd-108">L’emplacement du code d’action personnalisé est déterminé par la résolution du chemin d’accès cible de ce fichier ; par conséquent, cette action personnalisée doit être appelée une fois que ce fichier a été installé et avant d’être supprimé.</span><span class="sxs-lookup"><span data-stu-id="b74dd-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after that file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="b74dd-109">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="b74dd-109">Type Value</span></span>

<span data-ttu-id="b74dd-110">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.</span><span class="sxs-lookup"><span data-stu-id="b74dd-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="b74dd-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="b74dd-111">Constants</span></span>                                                          | <span data-ttu-id="b74dd-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="b74dd-112">Hexadecimal</span></span> | <span data-ttu-id="b74dd-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="b74dd-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="b74dd-114">**msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="b74dd-114">**msidbCustomActionTypeDll** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="b74dd-115">0x011</span><span class="sxs-lookup"><span data-stu-id="b74dd-115">0x011</span></span>       | <span data-ttu-id="b74dd-116">17</span><span class="sxs-lookup"><span data-stu-id="b74dd-116">17</span></span>      |



 

## <a name="target"></a><span data-ttu-id="b74dd-117">Cible</span><span class="sxs-lookup"><span data-stu-id="b74dd-117">Target</span></span>

<span data-ttu-id="b74dd-118">La DLL est appelée à l’aide du point d’entrée nommé dans le champ cible de la [table CustomAction](customaction-table.md), en passant un argument unique qui est le descripteur à la session d’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="b74dd-118">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="b74dd-119">Le nom du point d’entrée spécifié dans la table doit correspondre à celui exporté à partir de la DLL.</span><span class="sxs-lookup"><span data-stu-id="b74dd-119">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="b74dd-120">Notez que si la fonction d’entrée n’est pas spécifiée par un. Fichier DEF ou d’une spécification/EXPORT : linker, le nom peut avoir un trait de soulignement de début et un @4 suffixe «».</span><span class="sxs-lookup"><span data-stu-id="b74dd-120">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="b74dd-121">La fonction appelée doit spécifier la \_ \_ Convention d’appel StdCall.</span><span class="sxs-lookup"><span data-stu-id="b74dd-121">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="b74dd-122">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="b74dd-122">Return Processing Options</span></span>

<span data-ttu-id="b74dd-123">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="b74dd-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="b74dd-124">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="b74dd-125">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="b74dd-125">Execution Scheduling Options</span></span>

<span data-ttu-id="b74dd-126">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b74dd-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="b74dd-127">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b74dd-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="b74dd-128">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="b74dd-129">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="b74dd-129">In-Script Execution Options</span></span>

<span data-ttu-id="b74dd-130">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="b74dd-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="b74dd-131">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="b74dd-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="b74dd-132">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="b74dd-133">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="b74dd-133">Return Values</span></span>

<span data-ttu-id="b74dd-134">Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-134">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b74dd-135">Notes</span><span class="sxs-lookup"><span data-stu-id="b74dd-135">Remarks</span></span>

<span data-ttu-id="b74dd-136">Une action personnalisée qui appelle une bibliothèque de liens dynamiques (DLL) requiert un handle pour la session d’installation.</span><span class="sxs-lookup"><span data-stu-id="b74dd-136">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="b74dd-137">S’il s’agit également d’une action personnalisée d’exécution différée, la session n’existe peut-être plus pendant l’exécution du script d’installation.</span><span class="sxs-lookup"><span data-stu-id="b74dd-137">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="b74dd-138">Pour plus d’informations sur la façon dont une action personnalisée de ce type peut obtenir des informations de contexte, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-138">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="b74dd-139">Les actions personnalisées s’exécutent dans un thread distinct et peuvent avoir un accès limité au système.</span><span class="sxs-lookup"><span data-stu-id="b74dd-139">Custom actions execute in a separate thread, and may have limited access to the system.</span></span> <span data-ttu-id="b74dd-140">Les actions personnalisées qui s’exécutent de façon asynchrone bloquent le thread principal à l’arrêt de la séquence actuelle ou de la session d’installation jusqu’à ce qu’elles retournent.</span><span class="sxs-lookup"><span data-stu-id="b74dd-140">Custom actions that run asynchronously block the main thread at the termination of either the current sequence or the install session until they return.</span></span>

<span data-ttu-id="b74dd-141">Les actions personnalisées qui font référence à un fichier installé comme source, telles que le type d’action personnalisé 17 (DLL), doivent respecter les restrictions de séquencement suivantes :</span><span class="sxs-lookup"><span data-stu-id="b74dd-141">Custom actions that reference an installed file as their source, such as Custom Action Type 17 (DLL), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="b74dd-142">L’action personnalisée doit être séquencée après l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-142">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="b74dd-143">Cela permet à l’action personnalisée de résoudre le chemin d’accès nécessaire pour localiser la DLL.</span><span class="sxs-lookup"><span data-stu-id="b74dd-143">This is so that the custom action can resolve the path needed to locate the DLL.</span></span>
-   <span data-ttu-id="b74dd-144">Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées différées (dans le script) de ce type doivent être séquencées après l' [action InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-144">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="b74dd-145">Si le fichier source n’est pas déjà installé sur l’ordinateur, les actions personnalisées non différées de ce type doivent être séquencées après l' [action InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="b74dd-145">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b74dd-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b74dd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b74dd-147">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="b74dd-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="b74dd-148">Actions personnalisées d’exécution différée</span><span class="sxs-lookup"><span data-stu-id="b74dd-148">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="b74dd-149">Bibliothèques de liens dynamiques</span><span class="sxs-lookup"><span data-stu-id="b74dd-149">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> </dl>

 

 



