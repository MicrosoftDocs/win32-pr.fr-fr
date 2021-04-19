---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 6 lorsque les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Type d’action personnalisé 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531720"
---
# <a name="custom-action-type-6"></a><span data-ttu-id="37395-103">Type d’action personnalisé 6</span><span class="sxs-lookup"><span data-stu-id="37395-103">Custom Action Type 6</span></span>

<span data-ttu-id="37395-104">Cette action personnalisée est écrite en VBScript.</span><span class="sxs-lookup"><span data-stu-id="37395-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="37395-105">Pour plus d’informations, consultez [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="37395-105">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="37395-106">Source</span><span class="sxs-lookup"><span data-stu-id="37395-106">Source</span></span>

<span data-ttu-id="37395-107">Le script est généré à partir d’un flux binaire temporaire.</span><span class="sxs-lookup"><span data-stu-id="37395-107">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="37395-108">Le champ source de la [table CustomAction](customaction-table.md) contient une clé pour la [table binaire](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="37395-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="37395-109">La colonne de données de la table binaire contient les données de flux.</span><span class="sxs-lookup"><span data-stu-id="37395-109">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="37395-110">Un flux distinct est alloué pour chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="37395-110">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="37395-111">De nouvelles données binaires peuvent être insérées à partir d’un fichier à l’aide de [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) , puis de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer l’enregistrement dans la table.</span><span class="sxs-lookup"><span data-stu-id="37395-111">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="37395-112">Lorsque l’action personnalisée est appelée, les données de flux sont copiées dans un fichier temporaire, qui est ensuite traité en fonction du type d’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="37395-112">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="37395-113">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="37395-113">Type Value</span></span>

<span data-ttu-id="37395-114">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="37395-114">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="37395-115">Constantes</span><span class="sxs-lookup"><span data-stu-id="37395-115">Constants</span></span>                                                               | <span data-ttu-id="37395-116">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="37395-116">Hexadecimal</span></span> | <span data-ttu-id="37395-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="37395-117">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="37395-118">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="37395-118">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="37395-119">0x006</span><span class="sxs-lookup"><span data-stu-id="37395-119">0x006</span></span>       | <span data-ttu-id="37395-120">6</span><span class="sxs-lookup"><span data-stu-id="37395-120">6</span></span>       |



 

<span data-ttu-id="37395-121">Windows Installer pouvez utiliser des actions personnalisées 64 bits sur les systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37395-121">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="37395-122">Une action personnalisée 64 bits basée sur des scripts doit inclure le bit **msidbCustomActionType64BitScript** dans son type numérique.</span><span class="sxs-lookup"><span data-stu-id="37395-122">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="37395-123">Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="37395-123">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="37395-124">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base d’une action personnalisée 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37395-124">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="37395-125">Constantes</span><span class="sxs-lookup"><span data-stu-id="37395-125">Constants</span></span>                                                                                                      | <span data-ttu-id="37395-126">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="37395-126">Hexadecimal</span></span> | <span data-ttu-id="37395-127">Decimal</span><span class="sxs-lookup"><span data-stu-id="37395-127">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="37395-128">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="37395-128">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="37395-129">0x0001006</span><span class="sxs-lookup"><span data-stu-id="37395-129">0x0001006</span></span>   | <span data-ttu-id="37395-130">4102</span><span class="sxs-lookup"><span data-stu-id="37395-130">4102</span></span>    |



 

## <a name="target"></a><span data-ttu-id="37395-131">Cible</span><span class="sxs-lookup"><span data-stu-id="37395-131">Target</span></span>

<span data-ttu-id="37395-132">Le champ cible de la [table CustomAction](customaction-table.md) contient une fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="37395-132">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="37395-133">Le traitement envoie tout d’abord le script pour l’analyse, puis appelle la fonction de script facultative.</span><span class="sxs-lookup"><span data-stu-id="37395-133">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="37395-134">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="37395-134">Return Processing Options</span></span>

<span data-ttu-id="37395-135">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de traitement des retours.</span><span class="sxs-lookup"><span data-stu-id="37395-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="37395-136">Pour obtenir une description des options et des valeurs, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="37395-136">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="37395-137">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="37395-137">Execution Scheduling Options</span></span>

<span data-ttu-id="37395-138">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="37395-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="37395-139">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="37395-139">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="37395-140">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="37395-140">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="37395-141">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="37395-141">In-Script Execution Options</span></span>

<span data-ttu-id="37395-142">Incluez des bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier une option d’exécution in-script.</span><span class="sxs-lookup"><span data-stu-id="37395-142">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="37395-143">Ces options copient le code d’action dans le script d’exécution, de restauration ou de validation.</span><span class="sxs-lookup"><span data-stu-id="37395-143">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="37395-144">Pour obtenir une description des options, consultez [action personnalisée In-Script options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="37395-144">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="37395-145">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="37395-145">Return Values</span></span>

<span data-ttu-id="37395-146">Les fonctions facultatives écrites dans le script doivent retourner l’une des valeurs décrites dans les [valeurs de retour des actions personnalisées JScript et VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="37395-146">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="37395-147">Notes</span><span class="sxs-lookup"><span data-stu-id="37395-147">Remarks</span></span>

<span data-ttu-id="37395-148">Une action personnalisée écrite en JScript ou VBScript nécessite l’installation de l’objet de [**session**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="37395-148">A custom action that is written in JScript or VBScript requires the installation of the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="37395-149">Le programme d’installation joint l’objet de **session** au script avec la *session* de nom.</span><span class="sxs-lookup"><span data-stu-id="37395-149">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="37395-150">Étant donné que l’objet **session** n’existe peut-être pas lors d’une restauration de l’installation, une action personnalisée différée écrite dans le script doit utiliser l’une des méthodes ou propriétés de l’objet **session** décrit dans la section [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md) afin d’extraire son contexte.</span><span class="sxs-lookup"><span data-stu-id="37395-150">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="37395-151">Lorsqu’une table de base de données est exportée, chaque flux est écrit sous la forme d’un fichier distinct dans le sous-dossier nommé d’après la table, à l’aide de la clé primaire en tant que nom de fichier (colonne de nom pour la table binaire), avec l’extension par défaut « . IBD ».</span><span class="sxs-lookup"><span data-stu-id="37395-151">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="37395-152">Le nom doit utiliser le format de nom de fichier 8,3 Si le système de fichiers ou le système de gestion de version ne prend pas en charge les noms de fichiers longs.</span><span class="sxs-lookup"><span data-stu-id="37395-152">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="37395-153">Le fichier d’archive persistant remplace les données de flux par le nom de fichier utilisé, afin que les données puissent être localisées lors de l’importation de la table.</span><span class="sxs-lookup"><span data-stu-id="37395-153">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37395-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37395-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37395-155">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="37395-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



