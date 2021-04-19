---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 34 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Type d’action personnalisé 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536774"
---
# <a name="custom-action-type-34"></a><span data-ttu-id="0027a-103">Type d’action personnalisé 34</span><span class="sxs-lookup"><span data-stu-id="0027a-103">Custom Action Type 34</span></span>

<span data-ttu-id="0027a-104">Cette action personnalisée appelle un exécutable lancé avec une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0027a-104">This custom action calls an executable launched with a command line.</span></span> <span data-ttu-id="0027a-105">Pour plus d’informations, consultez [fichiers exécutables](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="0027a-105">For more information, see [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="0027a-106">Source</span><span class="sxs-lookup"><span data-stu-id="0027a-106">Source</span></span>

<span data-ttu-id="0027a-107">L’exécutable est généré à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="0027a-107">The executable is generated from a file.</span></span> <span data-ttu-id="0027a-108">Le champ source de la table [CustomAction](customaction-table.md) contient une clé dans la table de [répertoires](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0027a-108">The Source field of the [CustomAction](customaction-table.md) table contains a key into the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="0027a-109">L’entrée de table de répertoire référencée est utilisée pour résoudre le chemin d’accès complet à un répertoire de travail.</span><span class="sxs-lookup"><span data-stu-id="0027a-109">The referenced Directory table entry is used to resolve the full path to a working directory.</span></span> <span data-ttu-id="0027a-110">Cela ne doit pas obligatoirement être le chemin d’accès au répertoire contenant le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="0027a-110">This is not required to be the path to the directory containing the executable.</span></span>

## <a name="type-value"></a><span data-ttu-id="0027a-111">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="0027a-111">Type Value</span></span>

<span data-ttu-id="0027a-112">Incluez la valeur suivante dans la colonne type de la table [CustomAction](customaction-table.md) pour spécifier le type numérique de base.</span><span class="sxs-lookup"><span data-stu-id="0027a-112">Include the following value in the Type column of the [CustomAction](customaction-table.md) table to specify the basic numeric type.</span></span>



| <span data-ttu-id="0027a-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="0027a-113">Constants</span></span>                                                         | <span data-ttu-id="0027a-114">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="0027a-114">Hexadecimal</span></span> | <span data-ttu-id="0027a-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="0027a-115">Decimal</span></span> |
|-------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="0027a-116">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="0027a-116">**msidbCustomActionTypeExe** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="0027a-117">0x022</span><span class="sxs-lookup"><span data-stu-id="0027a-117">0x022</span></span>       | <span data-ttu-id="0027a-118">34</span><span class="sxs-lookup"><span data-stu-id="0027a-118">34</span></span>      |



 

## <a name="target"></a><span data-ttu-id="0027a-119">Cible</span><span class="sxs-lookup"><span data-stu-id="0027a-119">Target</span></span>

<span data-ttu-id="0027a-120">La colonne cible de la table [CustomAction](customaction-table.md) contient le chemin d’accès complet et le nom du fichier exécutable suivi d’arguments facultatifs pour l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="0027a-120">The Target column of the [CustomAction](customaction-table.md) table contains the full path and name of the executable file followed by optional arguments to the executable.</span></span> <span data-ttu-id="0027a-121">Le chemin d’accès complet et le nom du fichier exécutable sont requis.</span><span class="sxs-lookup"><span data-stu-id="0027a-121">The full path and name to the executable file is required.</span></span> <span data-ttu-id="0027a-122">Les guillemets doivent être utilisés autour des chemins d’accès ou des noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="0027a-122">Quotation marks must be used around long file names or paths.</span></span> <span data-ttu-id="0027a-123">La valeur est traitée comme du texte [mis en forme](formatted.md) et peut contenir des références à des propriétés, des fichiers, des répertoires ou d’autres attributs de texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="0027a-123">The value is treated as [formatted](formatted.md) text and may contain references to properties, files, directories, or other formatted text attributes.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="0027a-124">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="0027a-124">Return Processing Options</span></span>

<span data-ttu-id="0027a-125">Incluez les bits d’indicateur facultatifs dans la colonne type de la table [CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="0027a-125">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify return processing options.</span></span> <span data-ttu-id="0027a-126">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="0027a-126">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="0027a-127">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="0027a-127">Execution Scheduling Options</span></span>

<span data-ttu-id="0027a-128">Incluez les bits d’indicateur facultatifs dans la colonne type de la table [CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0027a-128">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify execution scheduling options.</span></span> <span data-ttu-id="0027a-129">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0027a-129">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="0027a-130">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="0027a-130">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="0027a-131">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="0027a-131">In-Script Execution Options</span></span>

<span data-ttu-id="0027a-132">Incluez des bits d’indicateur facultatifs dans la colonne type de la table [CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="0027a-132">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify an in-script execution option.</span></span> <span data-ttu-id="0027a-133">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="0027a-133">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="0027a-134">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="0027a-134">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="0027a-135">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0027a-135">Return Values</span></span>

<span data-ttu-id="0027a-136">Les actions personnalisées qui sont des [fichiers exécutables](executable-files.md) doivent retourner la valeur 0 en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0027a-136">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="0027a-137">Le programme d’installation interprète toute autre valeur de retour comme un échec.</span><span class="sxs-lookup"><span data-stu-id="0027a-137">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="0027a-138">Pour ignorer les valeurs de retour, définissez l’indicateur de bit **msidbCustomActionTypeContinue** dans le champ type de la table [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0027a-138">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction](customaction-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="0027a-139">Notes</span><span class="sxs-lookup"><span data-stu-id="0027a-139">Remarks</span></span>

<span data-ttu-id="0027a-140">Une action personnalisée qui lance un exécutable prend une ligne de commande, qui contient généralement des propriétés qui sont désignées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="0027a-140">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="0027a-141">S’il s’agit également d’une [action personnalisée d’exécution différée](deferred-execution-custom-actions.md), le programme d’installation utilise [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) pour créer le processus lorsque l’action personnalisée est appelée à partir du script d’installation.</span><span class="sxs-lookup"><span data-stu-id="0027a-141">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0027a-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0027a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0027a-143">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="0027a-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 
