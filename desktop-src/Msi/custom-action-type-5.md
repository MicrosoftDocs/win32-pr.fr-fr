---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 5 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 32b10271-44b1-4c5d-9c8b-eed1b4cd31e2
title: Type d’action personnalisé 5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85460c9a41dca060ca2634c013999c2c340ddfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533932"
---
# <a name="custom-action-type-5"></a><span data-ttu-id="ad101-103">Type d’action personnalisé 5</span><span class="sxs-lookup"><span data-stu-id="ad101-103">Custom Action Type 5</span></span>

<span data-ttu-id="ad101-104">Cette action personnalisée est écrite en JScript, telle que l’ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="ad101-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="ad101-105">Windows Installer ne prend pas en charge JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad101-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="ad101-106">Pour plus d’informations, consultez [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="ad101-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="ad101-107">Source</span><span class="sxs-lookup"><span data-stu-id="ad101-107">Source</span></span>

<span data-ttu-id="ad101-108">Le script est généré à partir d’un flux binaire temporaire.</span><span class="sxs-lookup"><span data-stu-id="ad101-108">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="ad101-109">Le champ source de la [table CustomAction](customaction-table.md) contient une clé pour la [table binaire](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="ad101-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="ad101-110">La colonne de données de la table binaire contient les données de flux.</span><span class="sxs-lookup"><span data-stu-id="ad101-110">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="ad101-111">Un flux distinct est alloué pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="ad101-111">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="ad101-112">De nouvelles données binaires peuvent être insérées à partir d’un fichier à l’aide de [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , puis de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer l’enregistrement dans la table.</span><span class="sxs-lookup"><span data-stu-id="ad101-112">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="ad101-113">Lorsque l’action personnalisée est appelée, les données de flux sont copiées dans un fichier temporaire, qui est ensuite traité selon le type d’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ad101-113">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed according to the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="ad101-114">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="ad101-114">Type Value</span></span>

<span data-ttu-id="ad101-115">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base de l’action personnalisée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ad101-115">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of 32-bit custom action.</span></span>



| <span data-ttu-id="ad101-116">Constantes</span><span class="sxs-lookup"><span data-stu-id="ad101-116">Constants</span></span>                                                              | <span data-ttu-id="ad101-117">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="ad101-117">Hexadecimal</span></span> | <span data-ttu-id="ad101-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="ad101-118">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="ad101-119">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="ad101-119">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="ad101-120">0x05</span><span class="sxs-lookup"><span data-stu-id="ad101-120">0x05</span></span>        | <span data-ttu-id="ad101-121">5</span><span class="sxs-lookup"><span data-stu-id="ad101-121">5</span></span>       |



 

<span data-ttu-id="ad101-122">Windows Installer pouvez utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ad101-122">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="ad101-123">Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique.</span><span class="sxs-lookup"><span data-stu-id="ad101-123">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="ad101-124">Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="ad101-124">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="ad101-125">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ad101-125">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="ad101-126">Constantes</span><span class="sxs-lookup"><span data-stu-id="ad101-126">Constants</span></span>                                                                                                     | <span data-ttu-id="ad101-127">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="ad101-127">Hexadecimal</span></span> | <span data-ttu-id="ad101-128">Decimal</span><span class="sxs-lookup"><span data-stu-id="ad101-128">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="ad101-129">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="ad101-129">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="ad101-130">0x0001005</span><span class="sxs-lookup"><span data-stu-id="ad101-130">0x0001005</span></span>   | <span data-ttu-id="ad101-131">4101</span><span class="sxs-lookup"><span data-stu-id="ad101-131">4101</span></span>    |



 

## <a name="target"></a><span data-ttu-id="ad101-132">Cible</span><span class="sxs-lookup"><span data-stu-id="ad101-132">Target</span></span>

<span data-ttu-id="ad101-133">Le champ cible de la [table CustomAction](customaction-table.md) contient une fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="ad101-133">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="ad101-134">Le traitement envoie tout d’abord le script pour l’analyse, puis appelle la fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="ad101-134">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="ad101-135">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="ad101-135">Return Processing Options</span></span>

<span data-ttu-id="ad101-136">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="ad101-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="ad101-137">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="ad101-137">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="ad101-138">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="ad101-138">Execution Scheduling Options</span></span>

<span data-ttu-id="ad101-139">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad101-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="ad101-140">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="ad101-140">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="ad101-141">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="ad101-141">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="ad101-142">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="ad101-142">In-Script Execution Options</span></span>

<span data-ttu-id="ad101-143">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="ad101-143">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="ad101-144">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="ad101-144">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="ad101-145">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="ad101-145">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="ad101-146">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ad101-146">Return Values</span></span>

<span data-ttu-id="ad101-147">Les fonctions facultatives écrites dans le script doivent retourner l’une des valeurs décrites dans les [valeurs de retour des actions personnalisées JScript et VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="ad101-147">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad101-148">Notes</span><span class="sxs-lookup"><span data-stu-id="ad101-148">Remarks</span></span>

<span data-ttu-id="ad101-149">Une action personnalisée écrite en JScript ou VBScript nécessite l’installation de l' [**objet session**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="ad101-149">A custom action that is written in JScript or VBScript requires the installation of [**Session Object**](session-object.md).</span></span> <span data-ttu-id="ad101-150">Le programme d’installation joint l’objet de **session** au script avec la *session* de nom.</span><span class="sxs-lookup"><span data-stu-id="ad101-150">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="ad101-151">Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.</span><span class="sxs-lookup"><span data-stu-id="ad101-151">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="ad101-152">Lorsqu’une table de base de données est exportée, chaque flux est écrit sous la forme d’un fichier distinct dans le sous-dossier nommé d’après la table, à l’aide de la clé primaire en tant que nom de fichier (colonne de nom pour la table binaire), avec l’extension par défaut « . IBD ».</span><span class="sxs-lookup"><span data-stu-id="ad101-152">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="ad101-153">Le nom doit utiliser le format de nom de fichier 8,3 Si le système de fichiers ou le système de gestion de version ne prend pas en charge les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="ad101-153">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="ad101-154">Le fichier d’archive persistant remplace les données de flux par le nom de fichier utilisé, afin que les données puissent être localisées lors de l’importation de la table.</span><span class="sxs-lookup"><span data-stu-id="ad101-154">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad101-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad101-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad101-156">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="ad101-156">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



