---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 50 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Type d’action personnalisé 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544297"
---
# <a name="custom-action-type-50"></a><span data-ttu-id="0b86d-103">Type d’action personnalisé 50</span><span class="sxs-lookup"><span data-stu-id="0b86d-103">Custom Action Type 50</span></span>

<span data-ttu-id="0b86d-104">Cette action personnalisée appelle un exécutable lancé avec une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0b86d-104">This custom action calls an executable launched with a command line.</span></span>

<span data-ttu-id="0b86d-105">Voir aussi [fichiers exécutables](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="0b86d-105">See also [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="0b86d-106">Source</span><span class="sxs-lookup"><span data-stu-id="0b86d-106">Source</span></span>

<span data-ttu-id="0b86d-107">L’exécutable est généré à partir d’un fichier existant.</span><span class="sxs-lookup"><span data-stu-id="0b86d-107">The executable is generated from an existing file.</span></span> <span data-ttu-id="0b86d-108">Le champ source de la [table CustomAction](customaction-table.md) contient une clé de la [table de propriétés](property-table.md) pour une propriété qui contient le chemin d’accès complet au fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="0b86d-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Property table](property-table.md) for a property that contains the full path to the executable file.</span></span>

## <a name="type-value"></a><span data-ttu-id="0b86d-109">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="0b86d-109">Type Value</span></span>

<span data-ttu-id="0b86d-110">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.</span><span class="sxs-lookup"><span data-stu-id="0b86d-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="0b86d-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="0b86d-111">Constants</span></span>                                                        | <span data-ttu-id="0b86d-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="0b86d-112">Hexadecimal</span></span> | <span data-ttu-id="0b86d-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="0b86d-113">Decimal</span></span> |
|------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="0b86d-114">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="0b86d-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="0b86d-115">0x032</span><span class="sxs-lookup"><span data-stu-id="0b86d-115">0x032</span></span>       | <span data-ttu-id="0b86d-116">50</span><span class="sxs-lookup"><span data-stu-id="0b86d-116">50</span></span>      |



 

## <a name="target"></a><span data-ttu-id="0b86d-117">Cible</span><span class="sxs-lookup"><span data-stu-id="0b86d-117">Target</span></span>

<span data-ttu-id="0b86d-118">La colonne cible de la [table CustomAction](customaction-table.md) contient la chaîne de ligne de commande pour l’exécutable identifié dans la colonne source.</span><span class="sxs-lookup"><span data-stu-id="0b86d-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="0b86d-119">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="0b86d-119">Return Processing Options</span></span>

<span data-ttu-id="0b86d-120">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="0b86d-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="0b86d-121">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="0b86d-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="0b86d-122">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="0b86d-122">Execution Scheduling Options</span></span>

<span data-ttu-id="0b86d-123">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0b86d-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="0b86d-124">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0b86d-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="0b86d-125">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="0b86d-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="0b86d-126">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="0b86d-126">In-Script Execution Options</span></span>

<span data-ttu-id="0b86d-127">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="0b86d-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="0b86d-128">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="0b86d-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="0b86d-129">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="0b86d-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="0b86d-130">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0b86d-130">Return Values</span></span>

<span data-ttu-id="0b86d-131">Les actions personnalisées qui sont des [fichiers exécutables](executable-files.md) doivent retourner la valeur 0 en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0b86d-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="0b86d-132">Le programme d’installation interprète toute autre valeur de retour comme un échec.</span><span class="sxs-lookup"><span data-stu-id="0b86d-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="0b86d-133">Pour ignorer les valeurs de retour, définissez l’indicateur de bit **msidbCustomActionTypeContinue** dans le champ type de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="0b86d-133">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b86d-134">Notes</span><span class="sxs-lookup"><span data-stu-id="0b86d-134">Remarks</span></span>

<span data-ttu-id="0b86d-135">Une action personnalisée qui lance un exécutable prend une ligne de commande, qui contient généralement des propriétés qui sont désignées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="0b86d-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="0b86d-136">S’il s’agit également d’une [action personnalisée d’exécution différée](deferred-execution-custom-actions.md), le programme d’installation utilise CreateProcessAsUser ou CreateProcess pour créer le processus lorsque l’action personnalisée est appelée à partir du script d’installation.</span><span class="sxs-lookup"><span data-stu-id="0b86d-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses CreateProcessAsUser or CreateProcess to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b86d-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b86d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b86d-138">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="0b86d-138">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



