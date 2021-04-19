---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 35 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Type d’action personnalisé 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520767"
---
# <a name="custom-action-type-35"></a><span data-ttu-id="05a3e-103">Type d’action personnalisé 35</span><span class="sxs-lookup"><span data-stu-id="05a3e-103">Custom Action Type 35</span></span>

<span data-ttu-id="05a3e-104">Cette action personnalisée définit le répertoire d’installation à partir d’une chaîne de texte mise en forme.</span><span class="sxs-lookup"><span data-stu-id="05a3e-104">This custom action sets the install directory from a formatted text string.</span></span> <span data-ttu-id="05a3e-105">Pour plus d’informations, consultez [modification de l’emplacement cible d’un répertoire](changing-the-target-location-for-a-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="05a3e-105">For more information, see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="source"></a><span data-ttu-id="05a3e-106">Source</span><span class="sxs-lookup"><span data-stu-id="05a3e-106">Source</span></span>

<span data-ttu-id="05a3e-107">Le champ source de la [table CustomAction](customaction-table.md) contient une clé dans la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="05a3e-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Directory table](directory-table.md).</span></span> <span data-ttu-id="05a3e-108">Le répertoire désigné est défini par la chaîne mise en forme dans le champ cible à l’aide de [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span><span class="sxs-lookup"><span data-stu-id="05a3e-108">The designated directory is set by the formatted string in the Target field using [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span></span> <span data-ttu-id="05a3e-109">Cela affecte au chemin d’accès cible et à la propriété associée la valeur développée de la chaîne de texte mise en forme dans le champ cible.</span><span class="sxs-lookup"><span data-stu-id="05a3e-109">This sets the target path and associated property to the expanded value of the formatted text string in the Target field.</span></span> <span data-ttu-id="05a3e-110">N’essayez pas de modifier l’emplacement d’un répertoire cible lors de [l’installation](maintenance-installation.md)d’une maintenance.</span><span class="sxs-lookup"><span data-stu-id="05a3e-110">Do not attempt to change the location of a target directory during a [maintenance installation](maintenance-installation.md).</span></span> <span data-ttu-id="05a3e-111">N’essayez pas de modifier le chemin d’accès au répertoire cible si certains composants qui utilisent ce chemin d’accès sont déjà installés pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="05a3e-111">Do not attempt to change the target directory path if some components using that path are already installed for any user.</span></span>

## <a name="type-value"></a><span data-ttu-id="05a3e-112">Valeur de type</span><span class="sxs-lookup"><span data-stu-id="05a3e-112">Type Value</span></span>

<span data-ttu-id="05a3e-113">Incluez la valeur suivante dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier le type numérique de base.</span><span class="sxs-lookup"><span data-stu-id="05a3e-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="05a3e-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="05a3e-114">Constants</span></span>                                                              | <span data-ttu-id="05a3e-115">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="05a3e-115">Hexadecimal</span></span> | <span data-ttu-id="05a3e-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="05a3e-116">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="05a3e-117">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="05a3e-117">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="05a3e-118">0x023</span><span class="sxs-lookup"><span data-stu-id="05a3e-118">0x023</span></span>       | <span data-ttu-id="05a3e-119">35</span><span class="sxs-lookup"><span data-stu-id="05a3e-119">35</span></span>      |



 

## <a name="target"></a><span data-ttu-id="05a3e-120">Cible</span><span class="sxs-lookup"><span data-stu-id="05a3e-120">Target</span></span>

<span data-ttu-id="05a3e-121">La colonne cible de la [table CustomAction](customaction-table.md) contient une chaîne de texte mise en forme à l’aide de la fonctionnalité spécifiée dans [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sans les spécificateurs de champ numérique).</span><span class="sxs-lookup"><span data-stu-id="05a3e-121">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="05a3e-122">Les paramètres à remplacer sont placés entre crochets \[ ... \] et peuvent être des propriétés, des variables d’environnement (% prefix), des chemins d’accès de fichier (préfixe \# ) ou des chemins d’accès de répertoire de composant ($ prefix).</span><span class="sxs-lookup"><span data-stu-id="05a3e-122">Parameters to be replaced are enclosed in square brackets \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="05a3e-123">Notez que les chemins d’accès aux répertoires se terminent toujours par un séparateur de répertoire.</span><span class="sxs-lookup"><span data-stu-id="05a3e-123">Note that directory paths always end with a directory separator.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="05a3e-124">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="05a3e-124">Return Processing Options</span></span>

<span data-ttu-id="05a3e-125">L’action personnalisée n’utilise pas ces options.</span><span class="sxs-lookup"><span data-stu-id="05a3e-125">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="05a3e-126">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="05a3e-126">Execution Scheduling Options</span></span>

<span data-ttu-id="05a3e-127">Incluez les bits d’indicateur facultatifs dans la colonne type de la [table CustomAction](customaction-table.md) pour spécifier les options de planification de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="05a3e-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="05a3e-128">Ces options contrôlent l’exécution multiple des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="05a3e-128">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="05a3e-129">Pour obtenir une description des options, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="05a3e-129">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="05a3e-130">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="05a3e-130">In-Script Execution Options</span></span>

<span data-ttu-id="05a3e-131">L’action personnalisée n’utilise pas ces options.</span><span class="sxs-lookup"><span data-stu-id="05a3e-131">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="05a3e-132">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="05a3e-132">Return Values</span></span>

<span data-ttu-id="05a3e-133">Consultez [valeurs de retour de l’action personnalisée](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="05a3e-133">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05a3e-134">Notes</span><span class="sxs-lookup"><span data-stu-id="05a3e-134">Remarks</span></span>

<span data-ttu-id="05a3e-135">Si vous définissez une [propriété privée](private-properties.md) dans la séquence d’interface utilisateur en créant une action personnalisée dans l’une des tables de séquence de l’interface utilisateur, cette propriété n’est pas définie dans la séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="05a3e-135">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="05a3e-136">Pour définir la propriété dans la séquence d’exécution, vous devez également placer une action personnalisée dans une table de séquence d’exécution.</span><span class="sxs-lookup"><span data-stu-id="05a3e-136">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="05a3e-137">Vous pouvez également faire de la propriété une [propriété publique](public-properties.md) et l’inclure dans la [**propriété SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="05a3e-137">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05a3e-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05a3e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05a3e-139">Actions personnalisées \_</span><span class="sxs-lookup"><span data-stu-id="05a3e-139">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="05a3e-140">Actions personnalisées du texte mis en forme</span><span class="sxs-lookup"><span data-stu-id="05a3e-140">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



