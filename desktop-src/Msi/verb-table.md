---
description: La table de verbes contient des informations sur les verbes de commande associées aux extensions de noms de fichiers qui doivent être générées dans le cadre de la publication du produit. Chaque ligne génère un ensemble de clés et de valeurs de registre.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Table de verbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545179"
---
# <a name="verb-table"></a><span data-ttu-id="7eb4f-104">Table de verbes</span><span class="sxs-lookup"><span data-stu-id="7eb4f-104">Verb Table</span></span>

<span data-ttu-id="7eb4f-105">La table de verbes contient des informations sur les verbes de commande associées aux extensions de noms de fichiers qui doivent être générées dans le cadre de la publication du produit.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-105">The Verb table contains command-verb information associated with file name extensions that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="7eb4f-106">Chaque ligne génère un ensemble de clés et de valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="7eb4f-107">La table de verbes contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-107">The Verb table has the following columns.</span></span>



| <span data-ttu-id="7eb4f-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="7eb4f-108">Column</span></span>      | <span data-ttu-id="7eb4f-109">Type</span><span class="sxs-lookup"><span data-stu-id="7eb4f-109">Type</span></span>                       | <span data-ttu-id="7eb4f-110">Clé</span><span class="sxs-lookup"><span data-stu-id="7eb4f-110">Key</span></span> | <span data-ttu-id="7eb4f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="7eb4f-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="7eb4f-112">Extension\_</span><span class="sxs-lookup"><span data-stu-id="7eb4f-112">Extension\_</span></span> | [<span data-ttu-id="7eb4f-113">Text</span><span class="sxs-lookup"><span data-stu-id="7eb4f-113">Text</span></span>](text.md)           | <span data-ttu-id="7eb4f-114">O</span><span class="sxs-lookup"><span data-stu-id="7eb4f-114">Y</span></span>   | <span data-ttu-id="7eb4f-115">N</span><span class="sxs-lookup"><span data-stu-id="7eb4f-115">N</span></span>        |
| <span data-ttu-id="7eb4f-116">Verbe</span><span class="sxs-lookup"><span data-stu-id="7eb4f-116">Verb</span></span>        | [<span data-ttu-id="7eb4f-117">Text</span><span class="sxs-lookup"><span data-stu-id="7eb4f-117">Text</span></span>](text.md)           | <span data-ttu-id="7eb4f-118">O</span><span class="sxs-lookup"><span data-stu-id="7eb4f-118">Y</span></span>   | <span data-ttu-id="7eb4f-119">N</span><span class="sxs-lookup"><span data-stu-id="7eb4f-119">N</span></span>        |
| <span data-ttu-id="7eb4f-120">Séquence</span><span class="sxs-lookup"><span data-stu-id="7eb4f-120">Sequence</span></span>    | [<span data-ttu-id="7eb4f-121">Integer</span><span class="sxs-lookup"><span data-stu-id="7eb4f-121">Integer</span></span>](integer.md)     | <span data-ttu-id="7eb4f-122">N</span><span class="sxs-lookup"><span data-stu-id="7eb4f-122">N</span></span>   | <span data-ttu-id="7eb4f-123">Y</span><span class="sxs-lookup"><span data-stu-id="7eb4f-123">Y</span></span>        |
| <span data-ttu-id="7eb4f-124">Commande</span><span class="sxs-lookup"><span data-stu-id="7eb4f-124">Command</span></span>     | [<span data-ttu-id="7eb4f-125">Correct</span><span class="sxs-lookup"><span data-stu-id="7eb4f-125">Formatted</span></span>](formatted.md) | <span data-ttu-id="7eb4f-126">N</span><span class="sxs-lookup"><span data-stu-id="7eb4f-126">N</span></span>   | <span data-ttu-id="7eb4f-127">O</span><span class="sxs-lookup"><span data-stu-id="7eb4f-127">Y</span></span>        |
| <span data-ttu-id="7eb4f-128">Argument</span><span class="sxs-lookup"><span data-stu-id="7eb4f-128">Argument</span></span>    | [<span data-ttu-id="7eb4f-129">Correct</span><span class="sxs-lookup"><span data-stu-id="7eb4f-129">Formatted</span></span>](formatted.md) | <span data-ttu-id="7eb4f-130">N</span><span class="sxs-lookup"><span data-stu-id="7eb4f-130">N</span></span>   | <span data-ttu-id="7eb4f-131">O</span><span class="sxs-lookup"><span data-stu-id="7eb4f-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7eb4f-132">Colonnes</span><span class="sxs-lookup"><span data-stu-id="7eb4f-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7eb4f-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Poste\_</span><span class="sxs-lookup"><span data-stu-id="7eb4f-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="7eb4f-134">Extension associée à la ligne de table.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-134">The extension associated with the table row.</span></span> <span data-ttu-id="7eb4f-135">Cette colonne est une clé externe de la première colonne de la [table d’extension](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="7eb4f-135">This column is an external key to the first column of the [Extension table](extension-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="7eb4f-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>DoVerb</span><span class="sxs-lookup"><span data-stu-id="7eb4f-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span>
</dt> <dd>

<span data-ttu-id="7eb4f-137">Verbe pour la commande.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-137">The verb for the command.</span></span>

</dd> <dt>

<span data-ttu-id="7eb4f-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="7eb4f-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="7eb4f-139">Séquence des commandes.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-139">The sequence of the commands.</span></span> <span data-ttu-id="7eb4f-140">Seuls les verbes pour lesquels la colonne Sequence est non NULL sont utilisés pour préparer une liste triée pour la valeur par défaut de la clé de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-140">Only verbs for which the Sequence column is non-Null are used to prepare an ordered list for the default value of the shell key.</span></span> <span data-ttu-id="7eb4f-141">Le verbe avec la valeur la plus faible dans cette colonne devient le verbe par défaut.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-141">The Verb with the lowest value in this column becomes the default verb.</span></span>

</dd> <dt>

<span data-ttu-id="7eb4f-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Commande</span><span class="sxs-lookup"><span data-stu-id="7eb4f-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="7eb4f-143">Texte localisable affiché dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-143">The localizable text displayed on the context menu.</span></span>

</dd> <dt>

<span data-ttu-id="7eb4f-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span><span class="sxs-lookup"><span data-stu-id="7eb4f-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="7eb4f-145">Valeur pour les arguments de commande.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-145">Value for the command arguments.</span></span>

<span data-ttu-id="7eb4f-146">Notez que la résolution des propriétés dans le champ argument est limitée.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-146">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="7eb4f-147">Une propriété mise en forme en tant que \[ *propriété* \] dans ce champ ne peut être résolue que si la propriété a déjà la valeur prévue lorsque le composant propriétaire du verbe est installé.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-147">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component owning the verb is installed.</span></span> <span data-ttu-id="7eb4f-148">Par exemple, pour que l’argument « \[ \#MyDoc.doc\] » soit résolu à la valeur correcte, le même processus doit installer le fichier MyDoc.doc et le composant qui possède le verbe.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-148">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7eb4f-149">Notes</span><span class="sxs-lookup"><span data-stu-id="7eb4f-149">Remarks</span></span>

<span data-ttu-id="7eb4f-150">Cette table est référencée lorsque l' [action RegisterExtensionInfo](registerextensioninfo-action.md) ou l' [action UnregisterExtensionInfo](unregisterextensioninfo-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="7eb4f-150">This table is referred to when the [RegisterExtensionInfo action](registerextensioninfo-action.md) or the [UnregisterExtensionInfo action](unregisterextensioninfo-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="7eb4f-151">Validation</span><span class="sxs-lookup"><span data-stu-id="7eb4f-151">Validation</span></span>

<dl>

[<span data-ttu-id="7eb4f-152">ICE03</span><span class="sxs-lookup"><span data-stu-id="7eb4f-152">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7eb4f-153">ICE06</span><span class="sxs-lookup"><span data-stu-id="7eb4f-153">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7eb4f-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="7eb4f-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="7eb4f-155">ICE46</span><span class="sxs-lookup"><span data-stu-id="7eb4f-155">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="7eb4f-156">ICE69</span><span class="sxs-lookup"><span data-stu-id="7eb4f-156">ICE69</span></span>](ice69.md)  
</dl>

 

 



