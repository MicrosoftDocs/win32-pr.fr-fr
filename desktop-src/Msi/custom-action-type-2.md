---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 2 lorsque les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Type d’action personnalisé 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544996"
---
# <a name="custom-action-type-2"></a><span data-ttu-id="79609-103">Type d’action personnalisé 2</span><span class="sxs-lookup"><span data-stu-id="79609-103">Custom Action Type 2</span></span>

<span data-ttu-id="79609-104">Cette action personnalisée appelle un exécutable lancé avec une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="79609-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="79609-105">Source</span><span class="sxs-lookup"><span data-stu-id="79609-105">Source</span></span>

<span data-ttu-id="79609-106">L’exécutable est généré à partir d’un flux binaire temporaire.</span><span class="sxs-lookup"><span data-stu-id="79609-106">The executable is generated from a temporary binary stream.</span></span> <span data-ttu-id="79609-107">Le champ source de la [table CustomAction](customaction-table.md) contient une clé pour la [table binaire](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="79609-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="79609-108">La colonne de données de la table binaire contient les données de flux.</span><span class="sxs-lookup"><span data-stu-id="79609-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="79609-109">Un flux distinct est alloué pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="79609-109">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="79609-110">De nouvelles données binaires peuvent être insérées à partir d’un fichier à l’aide de [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , puis de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer l’enregistrement dans la table.</span><span class="sxs-lookup"><span data-stu-id="79609-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="79609-111">Lorsque l’action personnalisée est appelée, les données de flux sont copiées dans un fichier temporaire, qui est ensuite traité en fonction du type d’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="79609-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="79609-112">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="79609-112">Type Value</span></span>

<span data-ttu-id="79609-113">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.</span><span class="sxs-lookup"><span data-stu-id="79609-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="79609-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="79609-114">Constants</span></span>                                                          | <span data-ttu-id="79609-115">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="79609-115">Hexadecimal</span></span> | <span data-ttu-id="79609-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="79609-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="79609-117">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="79609-117">**msidbCustomActionTypeExe** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="79609-118">0x002</span><span class="sxs-lookup"><span data-stu-id="79609-118">0x002</span></span>       | <span data-ttu-id="79609-119">2</span><span class="sxs-lookup"><span data-stu-id="79609-119">2</span></span>       |



 

## <a name="target"></a><span data-ttu-id="79609-120">Cible</span><span class="sxs-lookup"><span data-stu-id="79609-120">Target</span></span>

<span data-ttu-id="79609-121">La colonne cible de la [table CustomAction](customaction-table.md) contient la chaîne de ligne de commande pour l’exécutable nommé dans la colonne source.</span><span class="sxs-lookup"><span data-stu-id="79609-121">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable named in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="79609-122">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="79609-122">Return Processing Options</span></span>

<span data-ttu-id="79609-123">Incluez les bits d’indicateur facultatifs dans la colonne type de la table CustomAction pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="79609-123">Include optional flag bits in the Type column of the CustomAction table to specify return processing options.</span></span> <span data-ttu-id="79609-124">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="79609-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="79609-125">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="79609-125">Execution Scheduling Options</span></span>

<span data-ttu-id="79609-126">Incluez les bits d’indicateur facultatifs dans la colonne type de la table CustomAction pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="79609-126">Include optional flag bits in the Type column of the CustomAction table to specify execution scheduling options.</span></span> <span data-ttu-id="79609-127">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="79609-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="79609-128">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="79609-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="79609-129">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="79609-129">In-Script Execution Options</span></span>

<span data-ttu-id="79609-130">Incluez des bits d’indicateur facultatifs dans la colonne type de la table CustomAction pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="79609-130">Include optional flag bits in the Type column of the CustomAction table to specify an in-script execution option.</span></span> <span data-ttu-id="79609-131">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="79609-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="79609-132">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="79609-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="79609-133">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="79609-133">Return Values</span></span>

<span data-ttu-id="79609-134">Les actions personnalisées qui sont des [fichiers exécutables](executable-files.md) doivent retourner la valeur 0 en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="79609-134">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="79609-135">Le programme d’installation interprète toute autre valeur de retour comme un échec.</span><span class="sxs-lookup"><span data-stu-id="79609-135">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="79609-136">Pour ignorer les valeurs de retour, définissez l’indicateur de bit **msidbCustomActionTypeContinue** dans le champ type de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="79609-136">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="79609-137">Notes</span><span class="sxs-lookup"><span data-stu-id="79609-137">Remarks</span></span>

<span data-ttu-id="79609-138">Une action personnalisée qui lance un exécutable prend une ligne de commande, qui contient généralement des propriétés qui sont désignées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="79609-138">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="79609-139">S’il s’agit également d’une [action personnalisée d’exécution différée](deferred-execution-custom-actions.md), le programme d’installation utilise [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) ou [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) pour créer le processus lorsque l’action personnalisée est appelée à partir du script d’installation.</span><span class="sxs-lookup"><span data-stu-id="79609-139">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="79609-140">Lorsqu’une table de base de données est exportée, chaque flux est écrit sous la forme d’un fichier distinct dans le sous-dossier nommé d’après la table, à l’aide de la clé primaire en tant que nom de fichier (colonne de nom pour la table binaire), avec l’extension par défaut « . IBD ».</span><span class="sxs-lookup"><span data-stu-id="79609-140">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="79609-141">Le nom doit utiliser le format 8,3 Si le système de fichiers ou le système de gestion de version ne prend pas en charge les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="79609-141">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="79609-142">Le fichier d’archive persistant remplace les données de flux par le nom de fichier utilisé, afin que les données puissent être localisées lors de l’importation de la table.</span><span class="sxs-lookup"><span data-stu-id="79609-142">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79609-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79609-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79609-144">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="79609-144">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="79609-145">Fichiers exécutables</span><span class="sxs-lookup"><span data-stu-id="79609-145">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
