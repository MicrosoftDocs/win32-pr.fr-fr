---
description: La table RegLocator contient les informations nécessaires à la recherche d’un fichier ou d’un répertoire à l’aide du Registre, ou à la recherche d’une entrée de Registre particulière. Cette table contient les colonnes suivantes.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Table RegLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518238"
---
# <a name="reglocator-table"></a><span data-ttu-id="798cf-104">Table RegLocator</span><span class="sxs-lookup"><span data-stu-id="798cf-104">RegLocator Table</span></span>

<span data-ttu-id="798cf-105">La table RegLocator contient les informations nécessaires à la recherche d’un fichier ou d’un répertoire à l’aide du Registre, ou à la recherche d’une entrée de Registre particulière.</span><span class="sxs-lookup"><span data-stu-id="798cf-105">The RegLocator table holds the information needed to search for a file or directory using the registry, or to search for a particular registry entry itself.</span></span> <span data-ttu-id="798cf-106">Cette table contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="798cf-106">This table has the following columns.</span></span>



| <span data-ttu-id="798cf-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="798cf-107">Column</span></span>      | <span data-ttu-id="798cf-108">Type</span><span class="sxs-lookup"><span data-stu-id="798cf-108">Type</span></span>                         | <span data-ttu-id="798cf-109">Clé</span><span class="sxs-lookup"><span data-stu-id="798cf-109">Key</span></span> | <span data-ttu-id="798cf-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="798cf-110">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="798cf-111">Signature\_</span><span class="sxs-lookup"><span data-stu-id="798cf-111">Signature\_</span></span> | [<span data-ttu-id="798cf-112">Identificateur</span><span class="sxs-lookup"><span data-stu-id="798cf-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="798cf-113">O</span><span class="sxs-lookup"><span data-stu-id="798cf-113">Y</span></span>   | <span data-ttu-id="798cf-114">N</span><span class="sxs-lookup"><span data-stu-id="798cf-114">N</span></span>        |
| <span data-ttu-id="798cf-115">Root</span><span class="sxs-lookup"><span data-stu-id="798cf-115">Root</span></span>        | [<span data-ttu-id="798cf-116">Integer</span><span class="sxs-lookup"><span data-stu-id="798cf-116">Integer</span></span>](integer.md)       | <span data-ttu-id="798cf-117">N</span><span class="sxs-lookup"><span data-stu-id="798cf-117">N</span></span>   | <span data-ttu-id="798cf-118">N</span><span class="sxs-lookup"><span data-stu-id="798cf-118">N</span></span>        |
| <span data-ttu-id="798cf-119">Clé</span><span class="sxs-lookup"><span data-stu-id="798cf-119">Key</span></span>         | [<span data-ttu-id="798cf-120">RegPath</span><span class="sxs-lookup"><span data-stu-id="798cf-120">RegPath</span></span>](regpath.md)       | <span data-ttu-id="798cf-121">N</span><span class="sxs-lookup"><span data-stu-id="798cf-121">N</span></span>   | <span data-ttu-id="798cf-122">N</span><span class="sxs-lookup"><span data-stu-id="798cf-122">N</span></span>        |
| <span data-ttu-id="798cf-123">Nom</span><span class="sxs-lookup"><span data-stu-id="798cf-123">Name</span></span>        | [<span data-ttu-id="798cf-124">Correct</span><span class="sxs-lookup"><span data-stu-id="798cf-124">Formatted</span></span>](formatted.md)   | <span data-ttu-id="798cf-125">N</span><span class="sxs-lookup"><span data-stu-id="798cf-125">N</span></span>   | <span data-ttu-id="798cf-126">O</span><span class="sxs-lookup"><span data-stu-id="798cf-126">Y</span></span>        |
| <span data-ttu-id="798cf-127">Type</span><span class="sxs-lookup"><span data-stu-id="798cf-127">Type</span></span>        | [<span data-ttu-id="798cf-128">Integer</span><span class="sxs-lookup"><span data-stu-id="798cf-128">Integer</span></span>](integer.md)       | <span data-ttu-id="798cf-129">N</span><span class="sxs-lookup"><span data-stu-id="798cf-129">N</span></span>   | <span data-ttu-id="798cf-130">O</span><span class="sxs-lookup"><span data-stu-id="798cf-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="798cf-131">Colonnes</span><span class="sxs-lookup"><span data-stu-id="798cf-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="798cf-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="798cf-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="798cf-133">La valeur du champ signature \_ représente une signature unique qui est une clé externe dans la colonne une de la table de [signature](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="798cf-133">The value in the Signature\_ field represents a unique signature that is an external key into column one of the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="798cf-134">Si cette signature est présente dans la table de signatures, la recherche porte sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="798cf-134">If this signature is present in the Signature table, the search is for a file.</span></span> <span data-ttu-id="798cf-135">Si cette signature est absente de la table de signature et que la valeur de la colonne de type est **msidbLocatorTypeRawValue**, la recherche porte sur le nom de la clé de Registre désignée par la table RegLocator.</span><span class="sxs-lookup"><span data-stu-id="798cf-135">If this signature is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the registry key name pointed to by the RegLocator table.</span></span> <span data-ttu-id="798cf-136">Dans le cas contraire, la recherche concerne un répertoire vers lequel pointe la table RegLocator.</span><span class="sxs-lookup"><span data-stu-id="798cf-136">Otherwise the search is for a directory pointed to by the RegLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="798cf-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Causes</span><span class="sxs-lookup"><span data-stu-id="798cf-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="798cf-138">Clé racine prédéfinie pour la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="798cf-138">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="798cf-139">Constante</span><span class="sxs-lookup"><span data-stu-id="798cf-139">Constant</span></span>                          | <span data-ttu-id="798cf-140">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="798cf-140">Hexadecimal</span></span> | <span data-ttu-id="798cf-141">Decimal</span><span class="sxs-lookup"><span data-stu-id="798cf-141">Decimal</span></span> | <span data-ttu-id="798cf-142">Clé racine</span><span class="sxs-lookup"><span data-stu-id="798cf-142">Root key</span></span>             |
|-----------------------------------|-------------|---------|----------------------|
| <span data-ttu-id="798cf-143">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="798cf-143">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="798cf-144">0x000</span><span class="sxs-lookup"><span data-stu-id="798cf-144">0x000</span></span>       | <span data-ttu-id="798cf-145">0</span><span class="sxs-lookup"><span data-stu-id="798cf-145">0</span></span>       | <span data-ttu-id="798cf-146">\_racine des classes HKEY \_</span><span class="sxs-lookup"><span data-stu-id="798cf-146">HKEY\_CLASSES\_ROOT</span></span>  |
| <span data-ttu-id="798cf-147">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="798cf-147">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="798cf-148">0x001</span><span class="sxs-lookup"><span data-stu-id="798cf-148">0x001</span></span>       | <span data-ttu-id="798cf-149">1</span><span class="sxs-lookup"><span data-stu-id="798cf-149">1</span></span>       | <span data-ttu-id="798cf-150">HKEY \_ Current \_ User</span><span class="sxs-lookup"><span data-stu-id="798cf-150">HKEY\_CURRENT\_USER</span></span>  |
| <span data-ttu-id="798cf-151">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="798cf-151">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="798cf-152">0x002</span><span class="sxs-lookup"><span data-stu-id="798cf-152">0x002</span></span>       | <span data-ttu-id="798cf-153">2</span><span class="sxs-lookup"><span data-stu-id="798cf-153">2</span></span>       | <span data-ttu-id="798cf-154">HKEY \_ local \_ machine</span><span class="sxs-lookup"><span data-stu-id="798cf-154">HKEY\_LOCAL\_MACHINE</span></span> |
| <span data-ttu-id="798cf-155">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="798cf-155">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="798cf-156">0x003</span><span class="sxs-lookup"><span data-stu-id="798cf-156">0x003</span></span>       | <span data-ttu-id="798cf-157">3</span><span class="sxs-lookup"><span data-stu-id="798cf-157">3</span></span>       | <span data-ttu-id="798cf-158">HKEY, \_ utilisateurs</span><span class="sxs-lookup"><span data-stu-id="798cf-158">HKEY\_USERS</span></span>          |



 

</dd> <dt>

<span data-ttu-id="798cf-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel</span><span class="sxs-lookup"><span data-stu-id="798cf-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="798cf-160">Clé pour la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="798cf-160">The key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="798cf-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="798cf-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="798cf-162">Nom de la valeur de Registre.</span><span class="sxs-lookup"><span data-stu-id="798cf-162">The registry value name.</span></span> <span data-ttu-id="798cf-163">Si cette valeur est null, la valeur de la valeur sans nom ou par défaut de la clé, le cas échéant, est récupérée.</span><span class="sxs-lookup"><span data-stu-id="798cf-163">If this value is null, then the value from the key's unnamed or default value, if any, is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="798cf-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer</span><span class="sxs-lookup"><span data-stu-id="798cf-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="798cf-165">Valeur qui détermine si la valeur de Registre est un nom de fichier, un emplacement de répertoire ou une valeur de Registre brute.</span><span class="sxs-lookup"><span data-stu-id="798cf-165">A value that determines if the registry value is a file name, a directory location, or raw registry value.</span></span>

<span data-ttu-id="798cf-166">Le tableau suivant répertorie les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="798cf-166">The following table lists valid values.</span></span> <span data-ttu-id="798cf-167">Définissez l’une des trois premières valeurs et **msidbLocatorType64bit** si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="798cf-167">Set one of the first three values and **msidbLocatorType64bit** if necessary.</span></span> <span data-ttu-id="798cf-168">Si l’entrée de ce champ est absente, le type est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="798cf-168">If the entry in this field is absent, Type is set to be 1.</span></span>



| <span data-ttu-id="798cf-169">Constante</span><span class="sxs-lookup"><span data-stu-id="798cf-169">Constant</span></span>                      | <span data-ttu-id="798cf-170">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="798cf-170">Hexadecimal</span></span> | <span data-ttu-id="798cf-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="798cf-171">Decimal</span></span> | <span data-ttu-id="798cf-172">Description</span><span class="sxs-lookup"><span data-stu-id="798cf-172">Description</span></span>                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="798cf-173">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="798cf-173">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="798cf-174">0x000</span><span class="sxs-lookup"><span data-stu-id="798cf-174">0x000</span></span>       | <span data-ttu-id="798cf-175">0</span><span class="sxs-lookup"><span data-stu-id="798cf-175">0</span></span>       | <span data-ttu-id="798cf-176">Le chemin d’accès de la clé est un répertoire.</span><span class="sxs-lookup"><span data-stu-id="798cf-176">Key path is a directory.</span></span>                                                                                                                                           |
| <span data-ttu-id="798cf-177">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="798cf-177">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="798cf-178">0x001</span><span class="sxs-lookup"><span data-stu-id="798cf-178">0x001</span></span>       | <span data-ttu-id="798cf-179">1</span><span class="sxs-lookup"><span data-stu-id="798cf-179">1</span></span>       | <span data-ttu-id="798cf-180">Le chemin d’accès de la clé est un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="798cf-180">Key path is a file name.</span></span>                                                                                                                                           |
| <span data-ttu-id="798cf-181">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="798cf-181">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="798cf-182">0x002</span><span class="sxs-lookup"><span data-stu-id="798cf-182">0x002</span></span>       | <span data-ttu-id="798cf-183">2</span><span class="sxs-lookup"><span data-stu-id="798cf-183">2</span></span>       | <span data-ttu-id="798cf-184">Le chemin d’accès de la clé est une valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="798cf-184">Key path is a registry value.</span></span>                                                                                                                                      |
| <span data-ttu-id="798cf-185">**msidbLocatorType64bit**</span><span class="sxs-lookup"><span data-stu-id="798cf-185">**msidbLocatorType64bit**</span></span>     | <span data-ttu-id="798cf-186">0x010</span><span class="sxs-lookup"><span data-stu-id="798cf-186">0x010</span></span>       | <span data-ttu-id="798cf-187">16</span><span class="sxs-lookup"><span data-stu-id="798cf-187">16</span></span>      | <span data-ttu-id="798cf-188">Définissez ce bit pour que le programme d’installation recherche la partie 64 bits du Registre.</span><span class="sxs-lookup"><span data-stu-id="798cf-188">Set this bit to have the installer search the 64-bit portion of the registry.</span></span> <span data-ttu-id="798cf-189">Ne définissez pas ce bit pour que le programme d’installation recherche la partie 32 bits du Registre.</span><span class="sxs-lookup"><span data-stu-id="798cf-189">Do not set this bit to have the installer search the 32-bit portion of the registry.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="798cf-190">Notes</span><span class="sxs-lookup"><span data-stu-id="798cf-190">Remarks</span></span>

<span data-ttu-id="798cf-191">Notez que si la valeur du champ de type est **msidbLocatorTypeRawValue**, le programme d’installation définit la valeur de registre de la propriété spécifiée dans le champ de propriété de la table [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="798cf-191">Note that if the value in the Type field is **msidbLocatorTypeRawValue**, the installer sets the value of the property specified in the Property field of the [AppSearch](appsearch-table.md) table to the registry value.</span></span> <span data-ttu-id="798cf-192">Le programme d’installation ajoute un préfixe à la valeur de Registre qui identifie le type de valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="798cf-192">The installer adds a prefix to the registry value that identifies the type of registry value.</span></span> <span data-ttu-id="798cf-193">Pour plus d’informations sur les types de valeurs de Registre, consultez [types de valeur de Registre](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="798cf-193">For more information about types of registry values, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>



| <span data-ttu-id="798cf-194">Type de registre</span><span class="sxs-lookup"><span data-stu-id="798cf-194">Registry type</span></span>   | <span data-ttu-id="798cf-195">Préfixe ajouté par le programme d’installation</span><span class="sxs-lookup"><span data-stu-id="798cf-195">Prefix added by Installer</span></span>                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="798cf-196">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="798cf-196">REG\_SZ</span></span>         | <span data-ttu-id="798cf-197">Aucun, mais si le premier caractère de la valeur de Registre est \# , le programme d’installation échappe le caractère en préfixant un autre caractère \# .</span><span class="sxs-lookup"><span data-stu-id="798cf-197">None, but if the first character of the registry value is \#, the installer escapes the character by prefixing a another \#.</span></span>            |
| <span data-ttu-id="798cf-198">DWORD</span><span class="sxs-lookup"><span data-stu-id="798cf-198">DWORD</span></span>           | <span data-ttu-id="798cf-199">" \# " éventuellement suivi de' + 'ou'-'</span><span class="sxs-lookup"><span data-stu-id="798cf-199">"\#" optionally followed by '+' or '-'</span></span>                                                                                                  |
| <span data-ttu-id="798cf-200">REG \_ développer \_ SZ</span><span class="sxs-lookup"><span data-stu-id="798cf-200">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="798cf-201">"\#%"</span><span class="sxs-lookup"><span data-stu-id="798cf-201">"\#%"</span></span>                                                                                                                                   |
| <span data-ttu-id="798cf-202">REG \_ multiple \_ SZ</span><span class="sxs-lookup"><span data-stu-id="798cf-202">REG\_MULTI\_SZ</span></span>  | <span data-ttu-id="798cf-203">Null.</span><span class="sxs-lookup"><span data-stu-id="798cf-203">Null.</span></span> <span data-ttu-id="798cf-204">Le programme d’installation définit la propriété sur une valeur qui commence par null et se termine par une valeur null.</span><span class="sxs-lookup"><span data-stu-id="798cf-204">The installer sets the property to a value beginning with a null and ending with a null.</span></span>                                          |
| <span data-ttu-id="798cf-205">\_fichier binaire reg</span><span class="sxs-lookup"><span data-stu-id="798cf-205">REG\_BINARY</span></span>     | <span data-ttu-id="798cf-206">« \# x » dans le cas de reg \_ Binary, le programme d’installation convertit et enregistre chaque chiffre hexadécimal (grignoter) sous la forme d’un caractère ASCII préfixé par « \# x ».</span><span class="sxs-lookup"><span data-stu-id="798cf-206">"\#x" In case of REG\_BINARY, the installer converts and saves each hexadecimal digit (nibble) as an ASCII character prefixed by "\#x".</span></span> |



 

<span data-ttu-id="798cf-207">En règle générale, les colonnes de cette table ne sont pas localisées.</span><span class="sxs-lookup"><span data-stu-id="798cf-207">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="798cf-208">Si un auteur décide de rechercher des produits dans plusieurs langues, il doit y avoir une entrée distincte incluse dans le tableau pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="798cf-208">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="798cf-209">Notez qu’il n’est pas possible d’utiliser la table RegLocator pour vérifier uniquement la présence de la clé.</span><span class="sxs-lookup"><span data-stu-id="798cf-209">Note that it is not possible to use the RegLocator table to check only for the presence of the key.</span></span> <span data-ttu-id="798cf-210">Toutefois, vous pouvez rechercher la valeur par défaut d’une clé et récupérer sa valeur si elle n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="798cf-210">However, you can search for the default value of a key and retrieve its value if it is not empty.</span></span>

<span data-ttu-id="798cf-211">Pour plus d’informations, consultez [recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="798cf-211">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="798cf-212">Validation</span><span class="sxs-lookup"><span data-stu-id="798cf-212">Validation</span></span>

<dl>

[<span data-ttu-id="798cf-213">ICE03</span><span class="sxs-lookup"><span data-stu-id="798cf-213">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="798cf-214">ICE06</span><span class="sxs-lookup"><span data-stu-id="798cf-214">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="798cf-215">ICE46</span><span class="sxs-lookup"><span data-stu-id="798cf-215">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="798cf-216">ICE80</span><span class="sxs-lookup"><span data-stu-id="798cf-216">ICE80</span></span>](ice80.md)  
</dl>

 

 
