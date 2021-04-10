---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 51 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Type d’action personnalisé 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952599"
---
# <a name="custom-action-type-51"></a><span data-ttu-id="1b4a1-103">Type d’action personnalisé 51</span><span class="sxs-lookup"><span data-stu-id="1b4a1-103">Custom Action Type 51</span></span>

<span data-ttu-id="1b4a1-104">Cette action personnalisée définit une propriété à partir d’une chaîne de texte mise en forme.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-104">This custom action sets a property from a formatted text string.</span></span>

<span data-ttu-id="1b4a1-105">Pour affecter une propriété utilisée dans une condition sur un composant ou une fonctionnalité, l’action personnalisée doit précéder l' [action CostFinalize](costfinalize-action.md) dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-105">To affect a property used in a condition on a component or feature, the custom action must come before the [CostFinalize action](costfinalize-action.md) in the action sequence.</span></span>

## <a name="source"></a><span data-ttu-id="1b4a1-106">Source</span><span class="sxs-lookup"><span data-stu-id="1b4a1-106">Source</span></span>

<span data-ttu-id="1b4a1-107">Le champ source de la [table CustomAction](customaction-table.md) peut contenir soit le nom d’une propriété, soit une clé de la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="1b4a1-107">The Source field of the [CustomAction table](customaction-table.md) can contain either the name of a property or a key to the [Property table](property-table.md).</span></span> <span data-ttu-id="1b4a1-108">Cette propriété est définie par la chaîne mise en forme dans le champ cible à l’aide de [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span><span class="sxs-lookup"><span data-stu-id="1b4a1-108">This property is set by the formatted string in the Target field using [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span></span>

## <a name="type-value"></a><span data-ttu-id="1b4a1-109">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="1b4a1-109">Type Value</span></span>

<span data-ttu-id="1b4a1-110">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="1b4a1-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="1b4a1-111">Constants</span></span>                                                             | <span data-ttu-id="1b4a1-112">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="1b4a1-112">Hexadecimal</span></span> | <span data-ttu-id="1b4a1-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="1b4a1-113">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="1b4a1-114">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="1b4a1-114">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="1b4a1-115">0x033</span><span class="sxs-lookup"><span data-stu-id="1b4a1-115">0x033</span></span>       | <span data-ttu-id="1b4a1-116">51</span><span class="sxs-lookup"><span data-stu-id="1b4a1-116">51</span></span>      |



 

## <a name="target"></a><span data-ttu-id="1b4a1-117">Cible</span><span class="sxs-lookup"><span data-stu-id="1b4a1-117">Target</span></span>

<span data-ttu-id="1b4a1-118">La colonne cible de la [table CustomAction](customaction-table.md) contient une chaîne de texte mise en forme à l’aide de la fonctionnalité spécifiée dans [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sans les spécificateurs de champ numérique).</span><span class="sxs-lookup"><span data-stu-id="1b4a1-118">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="1b4a1-119">Les paramètres à remplacer sont placés entre crochets, \[ ... \] et peuvent être des propriétés, des variables d’environnement (% prefix), des chemins d’accès de fichier (préfixe \# ) ou des chemins d’accès de répertoire de composant ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="1b4a1-119">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="1b4a1-120">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="1b4a1-120">Return Processing Options</span></span>

<span data-ttu-id="1b4a1-121">L’action personnalisée n’utilise pas ces options.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-121">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="1b4a1-122">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="1b4a1-122">Execution Scheduling Options</span></span>

<span data-ttu-id="1b4a1-123">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="1b4a1-124">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="1b4a1-125">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="1b4a1-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="1b4a1-126">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="1b4a1-126">In-Script Execution Options</span></span>

<span data-ttu-id="1b4a1-127">L’action personnalisée n’utilise pas ces options.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-127">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="1b4a1-128">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1b4a1-128">Return Values</span></span>

<span data-ttu-id="1b4a1-129">Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1b4a1-129">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1b4a1-130">Notes</span><span class="sxs-lookup"><span data-stu-id="1b4a1-130">Remarks</span></span>

<span data-ttu-id="1b4a1-131">Si vous définissez une [propriété privée](private-properties.md) dans la séquence d’interface utilisateur en créant une action personnalisée dans l’une des tables de séquence de l’interface utilisateur, cette propriété n’est pas définie dans la séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-131">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="1b4a1-132">Pour définir la propriété dans la séquence d’exécution, vous devez également placer une action personnalisée dans une table de séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-132">To set the property in the execution sequence, you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="1b4a1-133">Vous pouvez également faire de la propriété une [propriété publique](public-properties.md) et l’inclure dans la [**propriété SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="1b4a1-133">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b4a1-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b4a1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b4a1-135">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="1b4a1-135">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="1b4a1-136">Actions personnalisées du texte mis en forme</span><span class="sxs-lookup"><span data-stu-id="1b4a1-136">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



