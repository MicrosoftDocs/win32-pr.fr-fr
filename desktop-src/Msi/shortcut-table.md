---
description: Le tableau de raccourcis contient les informations dont l’application a besoin pour créer des raccourcis sur l’ordinateur de l’utilisateur.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tableau de raccourcis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866282"
---
# <a name="shortcut-table"></a><span data-ttu-id="3f6ae-103">Tableau de raccourcis</span><span class="sxs-lookup"><span data-stu-id="3f6ae-103">Shortcut Table</span></span>

<span data-ttu-id="3f6ae-104">Le tableau de raccourcis contient les informations dont l’application a besoin pour créer des raccourcis sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-104">The Shortcut table holds the information the application needs to create shortcuts on the user's computer.</span></span>

<span data-ttu-id="3f6ae-105">Le tableau de raccourcis contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-105">The Shortcut table has the following columns.</span></span>



| <span data-ttu-id="3f6ae-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="3f6ae-106">Column</span></span>                 | <span data-ttu-id="3f6ae-107">Type</span><span class="sxs-lookup"><span data-stu-id="3f6ae-107">Type</span></span>                         | <span data-ttu-id="3f6ae-108">Clé</span><span class="sxs-lookup"><span data-stu-id="3f6ae-108">Key</span></span> | <span data-ttu-id="3f6ae-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="3f6ae-109">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="3f6ae-110">Raccourci</span><span class="sxs-lookup"><span data-stu-id="3f6ae-110">Shortcut</span></span>               | [<span data-ttu-id="3f6ae-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3f6ae-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="3f6ae-112">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-112">Y</span></span>   | <span data-ttu-id="3f6ae-113">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-113">N</span></span>        |
| <span data-ttu-id="3f6ae-114">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="3f6ae-114">Directory\_</span></span>            | [<span data-ttu-id="3f6ae-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3f6ae-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="3f6ae-116">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-116">N</span></span>   | <span data-ttu-id="3f6ae-117">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-117">N</span></span>        |
| <span data-ttu-id="3f6ae-118">Nom</span><span class="sxs-lookup"><span data-stu-id="3f6ae-118">Name</span></span>                   | [<span data-ttu-id="3f6ae-119">Nom du fichier</span><span class="sxs-lookup"><span data-stu-id="3f6ae-119">Filename</span></span>](filename.md)     | <span data-ttu-id="3f6ae-120">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-120">N</span></span>   | <span data-ttu-id="3f6ae-121">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-121">N</span></span>        |
| <span data-ttu-id="3f6ae-122">-\_</span><span class="sxs-lookup"><span data-stu-id="3f6ae-122">Component\_</span></span>            | [<span data-ttu-id="3f6ae-123">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3f6ae-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="3f6ae-124">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-124">N</span></span>   | <span data-ttu-id="3f6ae-125">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-125">N</span></span>        |
| <span data-ttu-id="3f6ae-126">Cible</span><span class="sxs-lookup"><span data-stu-id="3f6ae-126">Target</span></span>                 | [<span data-ttu-id="3f6ae-127">Raccourci</span><span class="sxs-lookup"><span data-stu-id="3f6ae-127">Shortcut</span></span>](shortcut.md)     | <span data-ttu-id="3f6ae-128">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-128">N</span></span>   | <span data-ttu-id="3f6ae-129">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-129">N</span></span>        |
| <span data-ttu-id="3f6ae-130">Arguments</span><span class="sxs-lookup"><span data-stu-id="3f6ae-130">Arguments</span></span>              | [<span data-ttu-id="3f6ae-131">Correct</span><span class="sxs-lookup"><span data-stu-id="3f6ae-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3f6ae-132">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-132">N</span></span>   | <span data-ttu-id="3f6ae-133">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-133">Y</span></span>        |
| <span data-ttu-id="3f6ae-134">Description</span><span class="sxs-lookup"><span data-stu-id="3f6ae-134">Description</span></span>            | [<span data-ttu-id="3f6ae-135">Text</span><span class="sxs-lookup"><span data-stu-id="3f6ae-135">Text</span></span>](text.md)             | <span data-ttu-id="3f6ae-136">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-136">N</span></span>   | <span data-ttu-id="3f6ae-137">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-137">Y</span></span>        |
| <span data-ttu-id="3f6ae-138">Touche d’accès rapide</span><span class="sxs-lookup"><span data-stu-id="3f6ae-138">Hotkey</span></span>                 | [<span data-ttu-id="3f6ae-139">Integer</span><span class="sxs-lookup"><span data-stu-id="3f6ae-139">Integer</span></span>](integer.md)       | <span data-ttu-id="3f6ae-140">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-140">N</span></span>   | <span data-ttu-id="3f6ae-141">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-141">Y</span></span>        |
| <span data-ttu-id="3f6ae-142">Icône\_</span><span class="sxs-lookup"><span data-stu-id="3f6ae-142">Icon\_</span></span>                 | [<span data-ttu-id="3f6ae-143">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3f6ae-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="3f6ae-144">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-144">N</span></span>   | <span data-ttu-id="3f6ae-145">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-145">Y</span></span>        |
| <span data-ttu-id="3f6ae-146">IndexIcône</span><span class="sxs-lookup"><span data-stu-id="3f6ae-146">IconIndex</span></span>              | [<span data-ttu-id="3f6ae-147">Integer</span><span class="sxs-lookup"><span data-stu-id="3f6ae-147">Integer</span></span>](integer.md)       | <span data-ttu-id="3f6ae-148">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-148">N</span></span>   | <span data-ttu-id="3f6ae-149">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-149">Y</span></span>        |
| <span data-ttu-id="3f6ae-150">ShowCmd</span><span class="sxs-lookup"><span data-stu-id="3f6ae-150">ShowCmd</span></span>                | [<span data-ttu-id="3f6ae-151">Integer</span><span class="sxs-lookup"><span data-stu-id="3f6ae-151">Integer</span></span>](integer.md)       | <span data-ttu-id="3f6ae-152">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-152">N</span></span>   | <span data-ttu-id="3f6ae-153">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-153">Y</span></span>        |
| <span data-ttu-id="3f6ae-154">WkDir</span><span class="sxs-lookup"><span data-stu-id="3f6ae-154">WkDir</span></span>                  | [<span data-ttu-id="3f6ae-155">Identificateur</span><span class="sxs-lookup"><span data-stu-id="3f6ae-155">Identifier</span></span>](identifier.md) | <span data-ttu-id="3f6ae-156">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-156">N</span></span>   | <span data-ttu-id="3f6ae-157">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-157">Y</span></span>        |
| <span data-ttu-id="3f6ae-158">DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="3f6ae-158">DisplayResourceDLL</span></span>     | [<span data-ttu-id="3f6ae-159">Correct</span><span class="sxs-lookup"><span data-stu-id="3f6ae-159">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3f6ae-160">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-160">N</span></span>   | <span data-ttu-id="3f6ae-161">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-161">Y</span></span>        |
| <span data-ttu-id="3f6ae-162">DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6ae-162">DisplayResourceId</span></span>      | [<span data-ttu-id="3f6ae-163">Integer</span><span class="sxs-lookup"><span data-stu-id="3f6ae-163">Integer</span></span>](integer.md)       | <span data-ttu-id="3f6ae-164">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-164">N</span></span>   | <span data-ttu-id="3f6ae-165">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-165">Y</span></span>        |
| <span data-ttu-id="3f6ae-166">DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="3f6ae-166">DescriptionResourceDLL</span></span> | [<span data-ttu-id="3f6ae-167">Correct</span><span class="sxs-lookup"><span data-stu-id="3f6ae-167">Formatted</span></span>](formatted.md)   | <span data-ttu-id="3f6ae-168">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-168">N</span></span>   | <span data-ttu-id="3f6ae-169">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-169">Y</span></span>        |
| <span data-ttu-id="3f6ae-170">DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6ae-170">DescriptionResourceId</span></span>  | [<span data-ttu-id="3f6ae-171">Integer</span><span class="sxs-lookup"><span data-stu-id="3f6ae-171">Integer</span></span>](integer.md)       | <span data-ttu-id="3f6ae-172">N</span><span class="sxs-lookup"><span data-stu-id="3f6ae-172">N</span></span>   | <span data-ttu-id="3f6ae-173">O</span><span class="sxs-lookup"><span data-stu-id="3f6ae-173">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3f6ae-174">Colonnes</span><span class="sxs-lookup"><span data-stu-id="3f6ae-174">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3f6ae-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Gestionnaires</span><span class="sxs-lookup"><span data-stu-id="3f6ae-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Shortcut</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-176">Valeur de clé pour cette table.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-176">The key value for this table.</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span><span class="sxs-lookup"><span data-stu-id="3f6ae-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-178">Clé externe dans la première colonne de la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-178">The external key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="3f6ae-179">Cette colonne spécifie le répertoire dans lequel le fichier de raccourci est créé.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-179">This column specifies the directory in which the Shortcut file is created.</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="3f6ae-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-181">Nom localisable du raccourci à créer.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-181">The localizable name of the shortcut to be created.</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="3f6ae-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-183">Clé externe dans la première colonne de la [table de composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-183">The external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="3f6ae-184">Le programme d’installation utilise l’état d’installation du composant spécifié dans cette colonne pour déterminer si le raccourci est créé ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-184">The installer uses the installation state of the component specified in this column to determine whether the shortcut is created or deleted.</span></span> <span data-ttu-id="3f6ae-185">Ce composant doit avoir un chemin d’accès de clé valide pour l’installation du raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-185">This component must have a valid key path for the shortcut to be installed.</span></span> <span data-ttu-id="3f6ae-186">Si la colonne cible contient le nom d’une fonctionnalité, le fichier lancé par le raccourci est le fichier de clé du composant indiqué dans cet article.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-186">If the Target column contains the name of a feature, the file launched by the shortcut is the key file of the component listed in this column.</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif</span><span class="sxs-lookup"><span data-stu-id="3f6ae-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-188">Cible de raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-188">The shortcut target.</span></span>

<span data-ttu-id="3f6ae-189">Pour un raccourci publié, cette colonne doit être une clé externe dans la première colonne du tableau des [fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-189">For an advertised shortcut, this column must be an external key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="3f6ae-190">Le programme d’installation évalue l’entrée dans le champ cible en tant qu' [identificateur](identifier.md) et l’entrée doit être une clé étrangère valide dans la [table des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-190">The installer evaluates the entry in the Target field as an [Identifier](identifier.md) and the entry must be a valid foreign key into the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="3f6ae-191">Dans ce cas, le fichier lancé par le raccourci est le fichier de clé du composant listé dans la \_ colonne composant.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-191">The file launched by the shortcut in this case is the key file of the component listed in the Component\_ column.</span></span> <span data-ttu-id="3f6ae-192">Lorsque le raccourci est activé, le programme d’installation vérifie que tous les composants de la fonctionnalité sont installés avant de lancer ce fichier.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-192">When the shortcut is activated, the installer verifies that all the components in the feature are installed before launching this file.</span></span>

<span data-ttu-id="3f6ae-193">Pour un raccourci non publié, le programme d’installation évalue ce champ comme une chaîne [mise en forme](formatted.md) .</span><span class="sxs-lookup"><span data-stu-id="3f6ae-193">For a non-advertised shortcut, the installer evaluates this field as a [Formatted](formatted.md) string.</span></span> <span data-ttu-id="3f6ae-194">Le champ doit contenir un identificateur de propriété entouré de crochets ( \[ \] ), qui est développé dans le fichier ou dans un dossier désigné par le raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-194">The field should contains a property identifier enclosed by square brackets (\[ \]), that is expanded into the file or a folder pointed to by the shortcut.</span></span> <span data-ttu-id="3f6ae-195">Pour plus d’informations, consultez l' [action CreateShortcuts](createshortcuts-action.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-195">For more information, see the [CreateShortcuts action](createshortcuts-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span><span class="sxs-lookup"><span data-stu-id="3f6ae-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-197">Arguments de ligne de commande pour le raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-197">The command-line arguments for the shortcut.</span></span>

<span data-ttu-id="3f6ae-198">Notez que la résolution des propriétés dans le champ arguments est limitée.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-198">Note that the resolution of properties in the Arguments field is limited.</span></span> <span data-ttu-id="3f6ae-199">Une propriété mise en forme en tant que \[ *propriété* \] dans ce champ ne peut être résolue que si la propriété a déjà la valeur prévue lorsque le composant qui possède le raccourci est installé.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-199">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component that owns the shortcut is installed.</span></span> <span data-ttu-id="3f6ae-200">Par exemple, pour résoudre la valeur correcte pour l’argument « \[ \#MyDoc.doc\] », le même processus doit installer le fichier MyDoc.doc et le composant qui possède le raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-200">For example, to resolve to the correct value for the argument "\[\#MyDoc.doc\]", the same process must be installing the file MyDoc.doc and the component that owns the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="3f6ae-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-202">Description localisable du raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-202">The localizable description of the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Séquence</span><span class="sxs-lookup"><span data-stu-id="3f6ae-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-204">Raccourci clavier du raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-204">The hotkey for the shortcut.</span></span> <span data-ttu-id="3f6ae-205">L’octet de poids faible contient le code de touche virtuelle pour la clé, et l’octet de poids fort contient des indicateurs de modificateur.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-205">The low-order byte contains the virtual-key code for the key, and the high-order byte contains modifier flags.</span></span> <span data-ttu-id="3f6ae-206">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-206">This must be a non-negative number.</span></span> <span data-ttu-id="3f6ae-207">Les auteurs des packages d’installation sont généralement recommandés pour ne pas définir cette option, car le paramètre de cette option peut ajouter des touches d’activation en double sur le Bureau d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-207">Authors of installation packages are generally recommended not to set this option, because the setting of this option can add duplicate hotkeys to a user's desktop.</span></span> <span data-ttu-id="3f6ae-208">En outre, la pratique consistant à assigner des touches d’accès rapide aux raccourcis peut être problématique pour les utilisateurs qui utilisent des touches d’accès rapide pour l' [accessibilité](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-208">In addition, the practice of assigning hotkeys to shortcuts can be problematic for users using hotkeys for [accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Située\_</span><span class="sxs-lookup"><span data-stu-id="3f6ae-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-210">Clé externe de la colonne de l’une des [tables d’icônes](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-210">The external key to column one of the [Icon table](icon-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IndexIcône</span><span class="sxs-lookup"><span data-stu-id="3f6ae-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-212">Index d’icône pour le raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-212">The icon index for the shortcut.</span></span> <span data-ttu-id="3f6ae-213">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-213">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span><span class="sxs-lookup"><span data-stu-id="3f6ae-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-215">Commande Show pour la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-215">The Show command for the application window.</span></span>

<span data-ttu-id="3f6ae-216">Les valeurs suivantes peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-216">The following values may be used.</span></span> <span data-ttu-id="3f6ae-217">Les valeurs sont définies pour la fonction d’API Windows ShowWindow.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-217">The values are as defined for the Windows API function ShowWindow.</span></span>



| <span data-ttu-id="3f6ae-218">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f6ae-218">Value</span></span> | <span data-ttu-id="3f6ae-219">Signification</span><span class="sxs-lookup"><span data-stu-id="3f6ae-219">Meaning</span></span>             |
|-------|---------------------|
| <span data-ttu-id="3f6ae-220">1</span><span class="sxs-lookup"><span data-stu-id="3f6ae-220">1</span></span>     | <span data-ttu-id="3f6ae-221">\_SHOWNORMAL SW</span><span class="sxs-lookup"><span data-stu-id="3f6ae-221">SW\_SHOWNORMAL</span></span>      |
| <span data-ttu-id="3f6ae-222">3</span><span class="sxs-lookup"><span data-stu-id="3f6ae-222">3</span></span>     | <span data-ttu-id="3f6ae-223">\_SHOWMAXIMIZED SW</span><span class="sxs-lookup"><span data-stu-id="3f6ae-223">SW\_SHOWMAXIMIZED</span></span>   |
| <span data-ttu-id="3f6ae-224">7</span><span class="sxs-lookup"><span data-stu-id="3f6ae-224">7</span></span>     | <span data-ttu-id="3f6ae-225">\_SHOWMINNOACTIVE SW</span><span class="sxs-lookup"><span data-stu-id="3f6ae-225">SW\_SHOWMINNOACTIVE</span></span> |



 

</dd> <dt>

<span data-ttu-id="3f6ae-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span><span class="sxs-lookup"><span data-stu-id="3f6ae-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-227">Nom de la propriété qui contient le chemin d’accès du répertoire de travail du raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-227">The name of the property that has the path of the working directory for the shortcut.</span></span> <span data-ttu-id="3f6ae-228">La valeur peut utiliser le format Windows pour référencer des variables d’environnement, par exemple% USERPROFILE%.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-228">The value can use the Windows format to reference environment variables, for example %USERPROFILE%.</span></span> <span data-ttu-id="3f6ae-229">Les références sont résolues en chemin d’accès réel lorsque le programme d’installation résout le répertoire de travail pour créer le raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-229">The references are resolved to an actual path when the installer resolves the working directory to create the shortcut.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3f6ae-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="3f6ae-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-231">Ce champ contient une valeur de chaîne [mise en forme](formatted.md) pour le chemin d’accès complet au fichier exécutable portable indépendant du langage (fichier LN) qui contient les données de configuration de ressource (RC config).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-231">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="3f6ae-232">La chaîne mise en forme peut utiliser la \[ \# \] Convention filekey.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-232">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="3f6ae-233">Si ce champ contient une valeur, la colonne de nom est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-233">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="3f6ae-234">Si ce champ est vide, le programme d’installation utilise la valeur dans la colonne nom.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-234">If this field is empty, the installer uses the value in the Name column.</span></span> <span data-ttu-id="3f6ae-235">Lorsque ce champ contient une valeur, le champ **DisplayResourceId** doit également contenir une valeur, sinon l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-235">When this field contains a value, the **DisplayResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="3f6ae-236">Cette colonne du tableau de raccourcis est utilisée uniquement lors de l’exécution sur Windows Vista ou Windows Server 2008 et elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-236">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="3f6ae-237">Cette colonne est disponible avec les versions antérieures à Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-237">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="3f6ae-238">Pour plus d’informations sur l’ajout de raccourcis à une table de raccourcis pour une utilisation avec des ressources MUI, consultez [un exemple de raccourci MUI](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-238">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6ae-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-240">Index du nom complet du raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-240">The display name index for the shortcut.</span></span> <span data-ttu-id="3f6ae-241">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-241">This must be a non-negative number.</span></span> <span data-ttu-id="3f6ae-242">Lorsque ce champ contient une valeur, le champ **DisplayResourceDLL** doit également contenir une valeur, sinon l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-242">When this field contains a value, the **DisplayResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="3f6ae-243">Cette colonne du tableau de raccourcis est utilisée uniquement lors de l’exécution sur Windows Vista ou Windows Server 2008 et elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-243">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="3f6ae-244">Cette colonne est disponible avec les versions antérieures à Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-244">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="3f6ae-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-246">Ce champ contient une valeur de chaîne [mise en forme](formatted.md) pour le chemin d’accès complet au fichier exécutable portable indépendant du langage (fichier LN) qui contient les données de configuration de ressource (RC config).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-246">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="3f6ae-247">La chaîne mise en forme peut utiliser la \[ \# \] Convention filekey.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-247">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="3f6ae-248">Si ce champ contient une valeur, la colonne de nom est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-248">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="3f6ae-249">Si ce champ est vide, le programme d’installation utilise la valeur dans la colonne Description.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-249">If this field is empty, the installer uses the value in the Description column.</span></span> <span data-ttu-id="3f6ae-250">Lorsque ce champ contient une valeur, le champ **DescriptionResourceId** doit également contenir une valeur, sinon l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-250">When this field contains a value, the **DescriptionResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="3f6ae-251">Cette colonne du tableau de raccourcis est utilisée uniquement lors de l’exécution sur Windows Vista ou Windows Server 2008 et elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-251">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="3f6ae-252">Cette colonne est disponible avec les versions antérieures à Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-252">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="3f6ae-253">Pour plus d’informations sur l’ajout de raccourcis à une table de raccourcis pour une utilisation avec des ressources MUI, consultez [un exemple de raccourci MUI](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="3f6ae-253">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f6ae-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="3f6ae-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span></span>
</dt> <dd>

<span data-ttu-id="3f6ae-255">Index du nom de description pour le raccourci.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-255">The description name index for the shortcut.</span></span> <span data-ttu-id="3f6ae-256">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-256">This must be a non-negative number.</span></span> <span data-ttu-id="3f6ae-257">Lorsque ce champ contient une valeur, le champ **DescriptionResourceDLL** doit également contenir une valeur, sinon l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-257">When this field contains a value, the **DescriptionResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="3f6ae-258">Cette colonne du tableau de raccourcis est utilisée uniquement lors de l’exécution sur Windows Vista ou Windows Server 2008 et elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-258">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="3f6ae-259">Cette colonne est disponible avec les versions antérieures à Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-259">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f6ae-260">Notes</span><span class="sxs-lookup"><span data-stu-id="3f6ae-260">Remarks</span></span>

<span data-ttu-id="3f6ae-261">L’activation d’une fonctionnalité crée un raccourci publié uniquement si l’interface IShellLink du système prend en charge la résolution du descripteur du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-261">The enabling of a feature creates an advertised shortcut only if the system's IShellLink interface supports installer descriptor resolution.</span></span> <span data-ttu-id="3f6ae-262">Cela est pris en charge par Microsoft Windows 2000 et les systèmes exécutant Microsoft Internet Explorer 4,01.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-262">This is supported by Microsoft Windows 2000 and systems running Microsoft Internet Explorer 4.01.</span></span> <span data-ttu-id="3f6ae-263">S’il n’est pas pris en charge, le programme d’installation crée un raccourci non publié lors de l’installation du composant de la fonctionnalité, localement ou exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-263">If unsupported, the installer creates a non-advertised shortcut upon the installation of the feature's component, either locally or run from source.</span></span>

<span data-ttu-id="3f6ae-264">Notez que les raccourcis publiés pointent toujours vers une application particulière, identifiés par un [**ProductCode**](productcode.md), et ne doivent pas être partagés entre les applications.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-264">Note that advertised shortcuts always point at a particular application, identified by a [**ProductCode**](productcode.md), and should not be shared between applications.</span></span> <span data-ttu-id="3f6ae-265">Les raccourcis publiés ne fonctionnent que pour l’application la plus récemment installée, et sont supprimés lors de la suppression de cette dernière.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-265">Advertised shortcuts only work for the most recently installed application, and are removed when that application is removed.</span></span>

<span data-ttu-id="3f6ae-266">Cette table est référencée lorsque l' [action CreateShortcuts](createshortcuts-action.md) et l' [action RemoveShortcuts](removeshortcuts-action.md) sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="3f6ae-266">This table is referred to when the [CreateShortcuts action](createshortcuts-action.md) and the [RemoveShortcuts action](removeshortcuts-action.md) is executed.</span></span>

<span data-ttu-id="3f6ae-267">Consultez également la propriété [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) .</span><span class="sxs-lookup"><span data-stu-id="3f6ae-267">See also the [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="3f6ae-268">Validation</span><span class="sxs-lookup"><span data-stu-id="3f6ae-268">Validation</span></span>

<dl>

[<span data-ttu-id="3f6ae-269">ICE03</span><span class="sxs-lookup"><span data-stu-id="3f6ae-269">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3f6ae-270">ICE06</span><span class="sxs-lookup"><span data-stu-id="3f6ae-270">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3f6ae-271">ICE19</span><span class="sxs-lookup"><span data-stu-id="3f6ae-271">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="3f6ae-272">ICE32</span><span class="sxs-lookup"><span data-stu-id="3f6ae-272">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="3f6ae-273">ICE36</span><span class="sxs-lookup"><span data-stu-id="3f6ae-273">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="3f6ae-274">ICE46</span><span class="sxs-lookup"><span data-stu-id="3f6ae-274">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="3f6ae-275">ICE50</span><span class="sxs-lookup"><span data-stu-id="3f6ae-275">ICE50</span></span>](ice50.md)  
[<span data-ttu-id="3f6ae-276">ICE57</span><span class="sxs-lookup"><span data-stu-id="3f6ae-276">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="3f6ae-277">ICE59</span><span class="sxs-lookup"><span data-stu-id="3f6ae-277">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="3f6ae-278">ICE67</span><span class="sxs-lookup"><span data-stu-id="3f6ae-278">ICE67</span></span>](ice67.md)  
[<span data-ttu-id="3f6ae-279">ICE69</span><span class="sxs-lookup"><span data-stu-id="3f6ae-279">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="3f6ae-280">ICE80</span><span class="sxs-lookup"><span data-stu-id="3f6ae-280">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="3f6ae-281">ICE90</span><span class="sxs-lookup"><span data-stu-id="3f6ae-281">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="3f6ae-282">ICE91</span><span class="sxs-lookup"><span data-stu-id="3f6ae-282">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="3f6ae-283">ICE94</span><span class="sxs-lookup"><span data-stu-id="3f6ae-283">ICE94</span></span>](ice94.md)  
</dl>

 

 



