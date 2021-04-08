---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser une action personnalisée type 1 lorsque les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Type d’action personnalisé 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035217"
---
# <a name="custom-action-type-1"></a><span data-ttu-id="a071b-103">Type d’action personnalisé 1</span><span class="sxs-lookup"><span data-stu-id="a071b-103">Custom Action Type 1</span></span>

<span data-ttu-id="a071b-104">Cette action personnalisée appelle une bibliothèque de liens dynamiques (DLL) écrite en C ou C++.</span><span class="sxs-lookup"><span data-stu-id="a071b-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="a071b-105">Source</span><span class="sxs-lookup"><span data-stu-id="a071b-105">Source</span></span>

<span data-ttu-id="a071b-106">La DLL est générée à partir d’un flux binaire temporaire.</span><span class="sxs-lookup"><span data-stu-id="a071b-106">The DLL is generated from a temporary binary stream.</span></span> <span data-ttu-id="a071b-107">Le champ source de la [table CustomAction](customaction-table.md) contient une clé pour la [table binaire](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="a071b-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="a071b-108">La colonne de données de la table binaire contient les données de flux.</span><span class="sxs-lookup"><span data-stu-id="a071b-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="a071b-109">Un flux distinct est alloué pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="a071b-109">A separate stream is allocated for each row.</span></span> <span data-ttu-id="a071b-110">De nouvelles données binaires peuvent être insérées à partir d’un fichier à l’aide de [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , puis de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer l’enregistrement dans la table.</span><span class="sxs-lookup"><span data-stu-id="a071b-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="a071b-111">Lorsque l’action personnalisée est appelée, les données de flux sont copiées dans un fichier temporaire, qui est ensuite traité en fonction du type d’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a071b-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="a071b-112">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="a071b-112">Type Value</span></span>

<span data-ttu-id="a071b-113">Incluez les bits d’indicateur suivants dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.</span><span class="sxs-lookup"><span data-stu-id="a071b-113">Include the following flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="a071b-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="a071b-114">Constants</span></span>                                                          | <span data-ttu-id="a071b-115">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="a071b-115">Hexadecimal</span></span> | <span data-ttu-id="a071b-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="a071b-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="a071b-117">**msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="a071b-117">**msidbCustomActionTypeDll** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="a071b-118">0x001</span><span class="sxs-lookup"><span data-stu-id="a071b-118">0x001</span></span>       | <span data-ttu-id="a071b-119">1</span><span class="sxs-lookup"><span data-stu-id="a071b-119">1</span></span>       |



 

## <a name="target"></a><span data-ttu-id="a071b-120">Cible</span><span class="sxs-lookup"><span data-stu-id="a071b-120">Target</span></span>

<span data-ttu-id="a071b-121">La DLL est appelée à l’aide du point d’entrée nommé dans le champ cible de la [table CustomAction](customaction-table.md), en passant un argument unique qui est le descripteur à la session d’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="a071b-121">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="a071b-122">Le nom du point d’entrée spécifié dans la table doit correspondre à celui exporté à partir de la DLL.</span><span class="sxs-lookup"><span data-stu-id="a071b-122">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="a071b-123">Notez que si la fonction d’entrée n’est pas spécifiée par un. Fichier DEF ou d’une spécification/EXPORT : linker, le nom peut avoir un trait de soulignement de début et un @4 suffixe «».</span><span class="sxs-lookup"><span data-stu-id="a071b-123">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="a071b-124">La fonction appelée doit spécifier la \_ \_ Convention d’appel StdCall.</span><span class="sxs-lookup"><span data-stu-id="a071b-124">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="a071b-125">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="a071b-125">Return Processing Options</span></span>

<span data-ttu-id="a071b-126">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="a071b-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="a071b-127">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="a071b-127">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="a071b-128">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="a071b-128">Execution Scheduling Options</span></span>

<span data-ttu-id="a071b-129">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a071b-129">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="a071b-130">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a071b-130">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="a071b-131">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="a071b-131">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="a071b-132">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="a071b-132">In-Script Execution Options</span></span>

<span data-ttu-id="a071b-133">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="a071b-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="a071b-134">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="a071b-134">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="a071b-135">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="a071b-135">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="a071b-136">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a071b-136">Return Values</span></span>

<span data-ttu-id="a071b-137">Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a071b-137">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a071b-138">Notes</span><span class="sxs-lookup"><span data-stu-id="a071b-138">Remarks</span></span>

<span data-ttu-id="a071b-139">Une action personnalisée qui appelle une bibliothèque de liens dynamiques (DLL) requiert un handle pour la session d’installation.</span><span class="sxs-lookup"><span data-stu-id="a071b-139">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="a071b-140">S’il s’agit également d’une action personnalisée d’exécution différée, la session n’existe peut-être plus pendant l’exécution du script d’installation.</span><span class="sxs-lookup"><span data-stu-id="a071b-140">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="a071b-141">Pour plus d’informations sur la façon dont une action personnalisée de ce type peut obtenir des informations de contexte, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a071b-141">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="a071b-142">Lorsqu’une table de base de données est exportée, chaque flux est écrit sous la forme d’un fichier distinct dans le sous-dossier nommé d’après la table, à l’aide de la clé primaire en tant que nom de fichier (colonne de nom pour la table binaire), avec l’extension par défaut « . IBD ».</span><span class="sxs-lookup"><span data-stu-id="a071b-142">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="a071b-143">Le nom doit utiliser le format 8,3 Si le système de fichiers ou le système de gestion de version ne prend pas en charge les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="a071b-143">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="a071b-144">Le fichier d’archive persistant remplace les données de flux par le nom de fichier utilisé, afin que les données puissent être localisées lors de l’importation de la table.</span><span class="sxs-lookup"><span data-stu-id="a071b-144">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a071b-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a071b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a071b-146">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="a071b-146">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="a071b-147">Bibliothèques de liens dynamiques</span><span class="sxs-lookup"><span data-stu-id="a071b-147">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> <dt>

[<span data-ttu-id="a071b-148">Obtention d’informations de contexte pour les actions personnalisées d’exécution différée</span><span class="sxs-lookup"><span data-stu-id="a071b-148">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



