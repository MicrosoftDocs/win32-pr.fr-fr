---
description: La table de registre contient les informations de registre que l’application doit définir dans le registre système.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Table du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951904"
---
# <a name="registry-table"></a><span data-ttu-id="a8c54-103">Table du Registre</span><span class="sxs-lookup"><span data-stu-id="a8c54-103">Registry Table</span></span>

<span data-ttu-id="a8c54-104">La table de registre contient les informations de registre que l’application doit définir dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="a8c54-104">The Registry table holds the registry information that the application needs to set in the system registry.</span></span>

<span data-ttu-id="a8c54-105">La table du registre contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8c54-105">The Registry table has the following columns.</span></span>



| <span data-ttu-id="a8c54-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="a8c54-106">Column</span></span>      | <span data-ttu-id="a8c54-107">Type</span><span class="sxs-lookup"><span data-stu-id="a8c54-107">Type</span></span>                         | <span data-ttu-id="a8c54-108">Clé</span><span class="sxs-lookup"><span data-stu-id="a8c54-108">Key</span></span> | <span data-ttu-id="a8c54-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="a8c54-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="a8c54-110">Registre</span><span class="sxs-lookup"><span data-stu-id="a8c54-110">Registry</span></span>    | [<span data-ttu-id="a8c54-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a8c54-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="a8c54-112">O</span><span class="sxs-lookup"><span data-stu-id="a8c54-112">Y</span></span>   | <span data-ttu-id="a8c54-113">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-113">N</span></span>        |
| <span data-ttu-id="a8c54-114">Root</span><span class="sxs-lookup"><span data-stu-id="a8c54-114">Root</span></span>        | [<span data-ttu-id="a8c54-115">Integer</span><span class="sxs-lookup"><span data-stu-id="a8c54-115">Integer</span></span>](integer.md)       | <span data-ttu-id="a8c54-116">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-116">N</span></span>   | <span data-ttu-id="a8c54-117">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-117">N</span></span>        |
| <span data-ttu-id="a8c54-118">Clé</span><span class="sxs-lookup"><span data-stu-id="a8c54-118">Key</span></span>         | [<span data-ttu-id="a8c54-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="a8c54-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="a8c54-120">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-120">N</span></span>   | <span data-ttu-id="a8c54-121">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-121">N</span></span>        |
| <span data-ttu-id="a8c54-122">Nom</span><span class="sxs-lookup"><span data-stu-id="a8c54-122">Name</span></span>        | [<span data-ttu-id="a8c54-123">Correct</span><span class="sxs-lookup"><span data-stu-id="a8c54-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a8c54-124">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-124">N</span></span>   | <span data-ttu-id="a8c54-125">O</span><span class="sxs-lookup"><span data-stu-id="a8c54-125">Y</span></span>        |
| <span data-ttu-id="a8c54-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8c54-126">Value</span></span>       | [<span data-ttu-id="a8c54-127">Correct</span><span class="sxs-lookup"><span data-stu-id="a8c54-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a8c54-128">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-128">N</span></span>   | <span data-ttu-id="a8c54-129">O</span><span class="sxs-lookup"><span data-stu-id="a8c54-129">Y</span></span>        |
| <span data-ttu-id="a8c54-130">-\_</span><span class="sxs-lookup"><span data-stu-id="a8c54-130">Component\_</span></span> | [<span data-ttu-id="a8c54-131">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a8c54-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="a8c54-132">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-132">N</span></span>   | <span data-ttu-id="a8c54-133">N</span><span class="sxs-lookup"><span data-stu-id="a8c54-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a8c54-134">Colonnes</span><span class="sxs-lookup"><span data-stu-id="a8c54-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a8c54-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Du</span><span class="sxs-lookup"><span data-stu-id="a8c54-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry</span></span>
</dt> <dd>

<span data-ttu-id="a8c54-136">Clé primaire utilisée pour identifier un enregistrement de registre.</span><span class="sxs-lookup"><span data-stu-id="a8c54-136">Primary key used to identify a registry record.</span></span>

</dd> <dt>

<span data-ttu-id="a8c54-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Causes</span><span class="sxs-lookup"><span data-stu-id="a8c54-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="a8c54-138">Clé racine prédéfinie pour la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="a8c54-138">The predefined root key for the registry value.</span></span> <span data-ttu-id="a8c54-139">Entrez la valeur-1 dans ce champ pour que la clé racine dépende du type d’installation.</span><span class="sxs-lookup"><span data-stu-id="a8c54-139">Enter a value of -1 in this field to make the root key dependent on the type of installation.</span></span> <span data-ttu-id="a8c54-140">Entrez l’une des autres valeurs du tableau suivant pour forcer l’écriture de la valeur de Registre sous une clé racine particulière.</span><span class="sxs-lookup"><span data-stu-id="a8c54-140">Enter one of the other values in the following table to force the registry value to be written under a particular root key.</span></span>



| <span data-ttu-id="a8c54-141">Constante</span><span class="sxs-lookup"><span data-stu-id="a8c54-141">Constant</span></span>                          | <span data-ttu-id="a8c54-142">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="a8c54-142">Hexadecimal</span></span> | <span data-ttu-id="a8c54-143">Decimal</span><span class="sxs-lookup"><span data-stu-id="a8c54-143">Decimal</span></span> | <span data-ttu-id="a8c54-144">Clé racine</span><span class="sxs-lookup"><span data-stu-id="a8c54-144">Root key</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c54-145">(aucun)</span><span class="sxs-lookup"><span data-stu-id="a8c54-145">(none)</span></span>                            | <span data-ttu-id="a8c54-146">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="a8c54-146">\- 0x001</span></span>    | <span data-ttu-id="a8c54-147">-1</span><span class="sxs-lookup"><span data-stu-id="a8c54-147">-1</span></span>      | <span data-ttu-id="a8c54-148">S’il s’agit d’une installation par utilisateur, la valeur de Registre est écrite sous **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="a8c54-148">If this is a per-user installation, the registry value is written under **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="a8c54-149">S’il s’agit d’une installation par ordinateur, la valeur de Registre est écrite sous **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="a8c54-149">If this is a per-machine installation, the registry value is written under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="a8c54-150">Notez qu’une installation par ordinateur est spécifiée en affectant à la propriété [**ALLUSERS**](allusers.md) la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="a8c54-150">Note that a per-machine installation is specified by setting the [**ALLUSERS**](allusers.md) property to 1.</span></span><br/>                |
| <span data-ttu-id="a8c54-151">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="a8c54-151">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="a8c54-152">0x000</span><span class="sxs-lookup"><span data-stu-id="a8c54-152">0x000</span></span>       | <span data-ttu-id="a8c54-153">0</span><span class="sxs-lookup"><span data-stu-id="a8c54-153">0</span></span>       | <span data-ttu-id="a8c54-154">**HKEY \_ CLASSES \_ racine** le programme d’installation écrit ou supprime la valeur de la ruche des **\\ \\ classes logicielles HKCU** lors de l’installation dans le [contexte d’installation](installation-context.md)par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8c54-154">**HKEY\_CLASSES\_ROOT** The installer writes or removes the value from the **HKCU\\Software\\Classes** hive during installation in the per-user [installation context](installation-context.md).</span></span><br/> <span data-ttu-id="a8c54-155">Le programme d’installation écrit ou supprime la valeur de la ruche des **\\ \\ classes logicielles HKLM** lors des installations par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a8c54-155">The installer writes or removes the value from the **HKLM\\Software\\Classes** hive during per-machine installations.</span></span><br/> |
| <span data-ttu-id="a8c54-156">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="a8c54-156">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="a8c54-157">0x001</span><span class="sxs-lookup"><span data-stu-id="a8c54-157">0x001</span></span>       | <span data-ttu-id="a8c54-158">1</span><span class="sxs-lookup"><span data-stu-id="a8c54-158">1</span></span>       | <span data-ttu-id="a8c54-159">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="a8c54-159">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="a8c54-160">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="a8c54-160">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="a8c54-161">0x002</span><span class="sxs-lookup"><span data-stu-id="a8c54-161">0x002</span></span>       | <span data-ttu-id="a8c54-162">2</span><span class="sxs-lookup"><span data-stu-id="a8c54-162">2</span></span>       | <span data-ttu-id="a8c54-163">**HKEY \_ local \_ machine**</span><span class="sxs-lookup"><span data-stu-id="a8c54-163">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a8c54-164">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="a8c54-164">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="a8c54-165">0x003</span><span class="sxs-lookup"><span data-stu-id="a8c54-165">0x003</span></span>       | <span data-ttu-id="a8c54-166">3</span><span class="sxs-lookup"><span data-stu-id="a8c54-166">3</span></span>       | <span data-ttu-id="a8c54-167">**HKEY, \_ utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="a8c54-167">**HKEY\_USERS**</span></span>                                                                                                                                                                                                                                                                                                                              |



 

<span data-ttu-id="a8c54-168">Notez qu’il est recommandé que les entrées de Registre écrites dans la ruche **HKCU** fassent référence à un composant dont le bit RegistryKeyPath est défini dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8c54-168">Note that it is recommended that registry entries written to the **HKCU** hive reference a component having the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a8c54-169">Cela permet de s’assurer que le programme d’installation écrit les entrées de Registre nécessaires lorsqu’il y a plusieurs utilisateurs sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a8c54-169">This ensures that the installer writes the necessary registry entries when there are multiple users on the same computer.</span></span>

</dd> <dt>

<span data-ttu-id="a8c54-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel</span><span class="sxs-lookup"><span data-stu-id="a8c54-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="a8c54-171">Clé localisable pour la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="a8c54-171">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="a8c54-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="a8c54-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a8c54-173">Cette colonne contient le nom de la valeur de Registre (localisable).</span><span class="sxs-lookup"><span data-stu-id="a8c54-173">This column contains the registry value name (localizable).</span></span> <span data-ttu-id="a8c54-174">Si la valeur est null, les données entrées dans la colonne valeur sont écrites dans la clé de Registre par défaut.</span><span class="sxs-lookup"><span data-stu-id="a8c54-174">If this is Null, then the data entered into the Value column are written to the default registry key.</span></span>

<span data-ttu-id="a8c54-175">Si la colonne value est null, les chaînes affichées dans le tableau suivant de la colonne Name ont une signification spéciale.</span><span class="sxs-lookup"><span data-stu-id="a8c54-175">If the Value column is Null, then the strings shown in the following table in the Name column have special significance.</span></span>



| <span data-ttu-id="a8c54-176">String</span><span class="sxs-lookup"><span data-stu-id="a8c54-176">String</span></span> | <span data-ttu-id="a8c54-177">Signification</span><span class="sxs-lookup"><span data-stu-id="a8c54-177">Meaning</span></span>                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | <span data-ttu-id="a8c54-178">La clé doit être créée, si elle est absente, lorsque le composant est installé.</span><span class="sxs-lookup"><span data-stu-id="a8c54-178">The key is to be created, if absent, when the component is installed.</span></span>                                                                                                                            |
| \-     | <span data-ttu-id="a8c54-179">La clé doit être supprimée, le cas échéant, avec toutes ses valeurs et ses sous-clés, lorsque le composant est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="a8c54-179">The key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span>                                                                                     |
| \*     | <span data-ttu-id="a8c54-180">La clé doit être créée, si elle est absente, lorsque le composant est installé.</span><span class="sxs-lookup"><span data-stu-id="a8c54-180">The key is to be created, if absent, when the component is installed.</span></span> <span data-ttu-id="a8c54-181">En outre, la clé doit être supprimée, le cas échéant, avec toutes ses valeurs et sous-clés, lorsque le composant est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="a8c54-181">Additionally, the key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span> |



 

<span data-ttu-id="a8c54-182">Notez que la [table RemoveRegistry](removeregistry-table.md) doit être utilisée si une clé de Registre installée doit être supprimée, avec ses valeurs et ses sous-clés, lors de l’installation du composant.</span><span class="sxs-lookup"><span data-stu-id="a8c54-182">Note that the [RemoveRegistry table](removeregistry-table.md) must be used if an installed registry key is to be deleted, with its values and subkeys, when the component is installed.</span></span>

</dd> <dt>

<span data-ttu-id="a8c54-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="a8c54-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="a8c54-184">Cette colonne est la valeur de Registre localisable.</span><span class="sxs-lookup"><span data-stu-id="a8c54-184">This column is the localizable registry value.</span></span> <span data-ttu-id="a8c54-185">Le champ est [mis en forme](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="a8c54-185">The field is [Formatted](formatted.md).</span></span> <span data-ttu-id="a8c54-186">Si la valeur est attachée à l’un des préfixes suivants (par exemple \# % , *valeur*), la valeur est interprétée comme décrit dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a8c54-186">If the value is attached to one of the following prefixes (i.e. \#%*value*) then the value is interpreted as described in the table.</span></span> <span data-ttu-id="a8c54-187">Notez que chaque préfixe commence par un signe dièse ( \# ).</span><span class="sxs-lookup"><span data-stu-id="a8c54-187">Note that each prefix begins with a number sign (\#).</span></span> <span data-ttu-id="a8c54-188">Si la valeur commence par au moins deux signes dièse consécutifs ( \# ), la première \# est ignorée et la valeur est interprétée et stockée en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="a8c54-188">If the value begins with two or more consecutive number signs (\#), the first \# is ignored and value is interpreted and stored as a string.</span></span>



| <span data-ttu-id="a8c54-189">Préfixe</span><span class="sxs-lookup"><span data-stu-id="a8c54-189">Prefix</span></span> | <span data-ttu-id="a8c54-190">Signification</span><span class="sxs-lookup"><span data-stu-id="a8c54-190">Meaning</span></span>                                                                        |
|--------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a8c54-191">\#x</span><span class="sxs-lookup"><span data-stu-id="a8c54-191">\#x</span></span>    | <span data-ttu-id="a8c54-192">La valeur est interprétée et stockée sous la forme d’une valeur hexadécimale (REG \_ Binary).</span><span class="sxs-lookup"><span data-stu-id="a8c54-192">The value is interpreted and stored as a hexadecimal value (REG\_BINARY).</span></span>      |
| \#%    | <span data-ttu-id="a8c54-193">La valeur est interprétée et stockée sous la forme d’une chaîne extensible (REG \_ expand \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="a8c54-193">The value is interpreted and stored as an expandable string (REG\_EXPAND\_SZ).</span></span> |
| \#     | <span data-ttu-id="a8c54-194">La valeur est interprétée et stockée sous la forme d’un entier (REG \_ DWORD).</span><span class="sxs-lookup"><span data-stu-id="a8c54-194">The value is interpreted and stored as an integer (REG\_DWORD).</span></span>                |



 

-   <span data-ttu-id="a8c54-195">Si la valeur contient le tilde \[ ~ \] de séquence, la valeur est interprétée comme une liste de chaînes délimitée par des valeurs null (reg \_ \_ multisz).</span><span class="sxs-lookup"><span data-stu-id="a8c54-195">If the value contains the sequence tilde \[~\], then the value is interpreted as a Null-delimited list of strings (REG\_MULTI\_SZ).</span></span> <span data-ttu-id="a8c54-196">Par exemple, pour spécifier une liste contenant les trois chaînes a, b et c, utilisez « a \[ ~ \] b \[ ~ \] c ».</span><span class="sxs-lookup"><span data-stu-id="a8c54-196">For example, to specify a list containing the three strings a, b and c, use "a\[~\]b\[~\]c".</span></span>
-   <span data-ttu-id="a8c54-197">La séquence \[ ~ \] dans la valeur sépare les chaînes individuelles et est interprétée et stockée en tant que caractère null.</span><span class="sxs-lookup"><span data-stu-id="a8c54-197">The sequence \[~\] within the value separates the individual strings and is interpreted and stored as a Null character.</span></span>
-   <span data-ttu-id="a8c54-198">Si a \[ ~ \] précède la liste de chaînes, les chaînes doivent être ajoutées à toutes les chaînes de valeurs de Registre existantes.</span><span class="sxs-lookup"><span data-stu-id="a8c54-198">If a \[~\] precedes the string list, the strings are to be appended to any existing registry value strings.</span></span> <span data-ttu-id="a8c54-199">Si une chaîne d’ajout figure déjà dans la valeur de Registre, l’occurrence d’origine de la chaîne est supprimée.</span><span class="sxs-lookup"><span data-stu-id="a8c54-199">If an appending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="a8c54-200">Si un \[ ~ \] suit la fin de la liste de chaînes, les chaînes doivent être ajoutées à toute chaîne de valeur de Registre existante.</span><span class="sxs-lookup"><span data-stu-id="a8c54-200">If a \[~\] follows the end of the string list, the strings are to be prepended to any existing registry value strings.</span></span> <span data-ttu-id="a8c54-201">Si une chaîne de préattente se trouve déjà dans la valeur de Registre, l’occurrence d’origine de la chaîne est supprimée.</span><span class="sxs-lookup"><span data-stu-id="a8c54-201">If a prepending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="a8c54-202">Si un \[ ~ \] est à la fois au début et à la fin ou au début ou à la fin de la liste de chaînes, les chaînes remplacent les chaînes de valeur de Registre existantes.</span><span class="sxs-lookup"><span data-stu-id="a8c54-202">If a \[~\] is at both the beginning and the end or at neither the beginning nor the end of the string list, the strings are to replace any existing registry value strings.</span></span>
-   <span data-ttu-id="a8c54-203">Dans le cas contraire, la valeur est interprétée et stockée sous la forme d’une chaîne (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="a8c54-203">Otherwise, the value is interpreted and stored as a string (REG\_SZ).</span></span>

</dd> <dt>

<span data-ttu-id="a8c54-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="a8c54-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="a8c54-205">Clé externe dans la première colonne de la [table de composants](component-table.md) référençant le composant qui contrôle l’installation de la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="a8c54-205">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8c54-206">Notes</span><span class="sxs-lookup"><span data-stu-id="a8c54-206">Remarks</span></span>

<span data-ttu-id="a8c54-207">Les actions [WriteRegistryValues](writeregistryvalues-action.md) et [RemoveRegistryValues](removeregistryvalues-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="a8c54-207">The [WriteRegistryValues](writeregistryvalues-action.md) and [RemoveRegistryValues](removeregistryvalues-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="a8c54-208">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8c54-208">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="a8c54-209">Les informations de Registre sont écrites dans le registre système lorsque le composant correspondant a été sélectionné pour être installé localement ou exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="a8c54-209">The registry information is written out to the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="a8c54-210">Notez que le programme d’installation supprime une clé de registre après avoir supprimé la dernière valeur ou sous-clé sous la clé.</span><span class="sxs-lookup"><span data-stu-id="a8c54-210">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="a8c54-211">Pour empêcher une clé de Registre vide d’être supprimée lors de la désinstallation de, écrivez une valeur factice sous la clé que vous devez conserver et entrez + dans la colonne nom.</span><span class="sxs-lookup"><span data-stu-id="a8c54-211">To prevent an empty registry key from being removed when uninstalling, write a dummy value under the key you need to keep and enter + in the Name column.</span></span> <span data-ttu-id="a8c54-212">Si \* se trouve dans la colonne nom, la clé est supprimée, avec toutes ses valeurs et ses sous-clés, lorsque le composant est supprimé.</span><span class="sxs-lookup"><span data-stu-id="a8c54-212">If \* is in the Name column, the key is deleted, with all of its values and subkeys, when the component is removed.</span></span>

<span data-ttu-id="a8c54-213">Une action personnalisée peut être utilisée pour ajouter des lignes à la table du Registre pendant une transaction d’installation, de désinstallation ou de réparation.</span><span class="sxs-lookup"><span data-stu-id="a8c54-213">A custom action can be used to add rows to the Registry table during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="a8c54-214">Ces lignes ne sont pas conservées dans la table de Registre et les informations ne sont disponibles que pendant la transaction en cours.</span><span class="sxs-lookup"><span data-stu-id="a8c54-214">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="a8c54-215">L’action personnalisée doit donc être exécutée à chaque installation, désinstallation ou transaction de réparation qui requiert les informations contenues dans ces lignes supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="a8c54-215">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="a8c54-216">L’action personnalisée doit précéder les actions [RemoveRegistryValues](removeregistryvalues-action.md) et [WriteRegistryValues](writeregistryvalues-action.md) dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="a8c54-216">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

<span data-ttu-id="a8c54-217">Pour plus d’informations sur la sécurisation d’une clé de Registre, consultez la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) et la [table LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8c54-217">For information on how to secure a registry key see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="a8c54-218">Validation</span><span class="sxs-lookup"><span data-stu-id="a8c54-218">Validation</span></span>

<dl>

[<span data-ttu-id="a8c54-219">ICE02</span><span class="sxs-lookup"><span data-stu-id="a8c54-219">ICE02</span></span>](ice02.md)  
[<span data-ttu-id="a8c54-220">ICE03</span><span class="sxs-lookup"><span data-stu-id="a8c54-220">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a8c54-221">ICE06</span><span class="sxs-lookup"><span data-stu-id="a8c54-221">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a8c54-222">ICE32</span><span class="sxs-lookup"><span data-stu-id="a8c54-222">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="a8c54-223">ICE38</span><span class="sxs-lookup"><span data-stu-id="a8c54-223">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="a8c54-224">ICE43</span><span class="sxs-lookup"><span data-stu-id="a8c54-224">ICE43</span></span>](ice43.md)  
[<span data-ttu-id="a8c54-225">ICE46</span><span class="sxs-lookup"><span data-stu-id="a8c54-225">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="a8c54-226">ICE49</span><span class="sxs-lookup"><span data-stu-id="a8c54-226">ICE49</span></span>](ice49.md)  
[<span data-ttu-id="a8c54-227">ICE53</span><span class="sxs-lookup"><span data-stu-id="a8c54-227">ICE53</span></span>](ice53.md)  
[<span data-ttu-id="a8c54-228">ICE55</span><span class="sxs-lookup"><span data-stu-id="a8c54-228">ICE55</span></span>](ice55.md)  
[<span data-ttu-id="a8c54-229">ICE57</span><span class="sxs-lookup"><span data-stu-id="a8c54-229">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="a8c54-230">ICE70</span><span class="sxs-lookup"><span data-stu-id="a8c54-230">ICE70</span></span>](ice70.md)  
[<span data-ttu-id="a8c54-231">ICE80</span><span class="sxs-lookup"><span data-stu-id="a8c54-231">ICE80</span></span>](ice80.md)  
</dl>

 

 




