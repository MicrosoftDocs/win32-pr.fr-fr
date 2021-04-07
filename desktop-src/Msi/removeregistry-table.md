---
description: La table RemoveRegistry contient les informations de registre que l’application doit supprimer du Registre système.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Table RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952232"
---
# <a name="removeregistry-table"></a><span data-ttu-id="d8c3b-103">Table RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="d8c3b-103">RemoveRegistry Table</span></span>

<span data-ttu-id="d8c3b-104">La table RemoveRegistry contient les informations de registre que l’application doit supprimer du Registre système.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-104">The RemoveRegistry table contains the registry information the application needs to delete from the system registry.</span></span>

<span data-ttu-id="d8c3b-105">La table RemoveRegistry contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-105">The RemoveRegistry table has the following columns.</span></span>



| <span data-ttu-id="d8c3b-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="d8c3b-106">Column</span></span>         | <span data-ttu-id="d8c3b-107">Type</span><span class="sxs-lookup"><span data-stu-id="d8c3b-107">Type</span></span>                         | <span data-ttu-id="d8c3b-108">Clé</span><span class="sxs-lookup"><span data-stu-id="d8c3b-108">Key</span></span> | <span data-ttu-id="d8c3b-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="d8c3b-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="d8c3b-110">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="d8c3b-110">RemoveRegistry</span></span> | [<span data-ttu-id="d8c3b-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="d8c3b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d8c3b-112">O</span><span class="sxs-lookup"><span data-stu-id="d8c3b-112">Y</span></span>   | <span data-ttu-id="d8c3b-113">N</span><span class="sxs-lookup"><span data-stu-id="d8c3b-113">N</span></span>        |
| <span data-ttu-id="d8c3b-114">Root</span><span class="sxs-lookup"><span data-stu-id="d8c3b-114">Root</span></span>           | [<span data-ttu-id="d8c3b-115">Integer</span><span class="sxs-lookup"><span data-stu-id="d8c3b-115">Integer</span></span>](integer.md)       | <span data-ttu-id="d8c3b-116">N</span><span class="sxs-lookup"><span data-stu-id="d8c3b-116">N</span></span>   | <span data-ttu-id="d8c3b-117">N</span><span class="sxs-lookup"><span data-stu-id="d8c3b-117">N</span></span>        |
| <span data-ttu-id="d8c3b-118">Clé</span><span class="sxs-lookup"><span data-stu-id="d8c3b-118">Key</span></span>            | [<span data-ttu-id="d8c3b-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="d8c3b-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="d8c3b-120">N</span><span class="sxs-lookup"><span data-stu-id="d8c3b-120">N</span></span>   | <span data-ttu-id="d8c3b-121">N</span><span class="sxs-lookup"><span data-stu-id="d8c3b-121">N</span></span>        |
| <span data-ttu-id="d8c3b-122">Nom</span><span class="sxs-lookup"><span data-stu-id="d8c3b-122">Name</span></span>           | [<span data-ttu-id="d8c3b-123">Correct</span><span class="sxs-lookup"><span data-stu-id="d8c3b-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d8c3b-124">N</span><span class="sxs-lookup"><span data-stu-id="d8c3b-124">N</span></span>   | <span data-ttu-id="d8c3b-125">O</span><span class="sxs-lookup"><span data-stu-id="d8c3b-125">Y</span></span>        |
| <span data-ttu-id="d8c3b-126">-\_</span><span class="sxs-lookup"><span data-stu-id="d8c3b-126">Component\_</span></span>    | [<span data-ttu-id="d8c3b-127">Identificateur</span><span class="sxs-lookup"><span data-stu-id="d8c3b-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="d8c3b-128">N</span><span class="sxs-lookup"><span data-stu-id="d8c3b-128">N</span></span>   | <span data-ttu-id="d8c3b-129">N</span><span class="sxs-lookup"><span data-stu-id="d8c3b-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d8c3b-130">Colonnes</span><span class="sxs-lookup"><span data-stu-id="d8c3b-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d8c3b-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="d8c3b-131"><span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry</span></span>
</dt> <dd>

<span data-ttu-id="d8c3b-132">Clé de cette table.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-132">The key for this table.</span></span>

</dd> <dt>

<span data-ttu-id="d8c3b-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Causes</span><span class="sxs-lookup"><span data-stu-id="d8c3b-133"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="d8c3b-134">Clé racine prédéfinie pour la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-134">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="d8c3b-135">Constante</span><span class="sxs-lookup"><span data-stu-id="d8c3b-135">Constant</span></span>                          | <span data-ttu-id="d8c3b-136">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="d8c3b-136">Hexadecimal</span></span> | <span data-ttu-id="d8c3b-137">Decimal</span><span class="sxs-lookup"><span data-stu-id="d8c3b-137">Decimal</span></span> | <span data-ttu-id="d8c3b-138">Clé racine</span><span class="sxs-lookup"><span data-stu-id="d8c3b-138">Root key</span></span>                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c3b-139">(aucun)</span><span class="sxs-lookup"><span data-stu-id="d8c3b-139">(none)</span></span>                            | <span data-ttu-id="d8c3b-140">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="d8c3b-140">\- 0x001</span></span>    | <span data-ttu-id="d8c3b-141">-1</span><span class="sxs-lookup"><span data-stu-id="d8c3b-141">-1</span></span>      | <span data-ttu-id="d8c3b-142">**HKEY \_ Le \_** programme d’installation de l’utilisateur actuel définit cette clé lors de l’installation par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-142">**HKEY\_CURRENT\_USER** Installer sets this key while doing a per-user installation.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="d8c3b-143">(aucun)</span><span class="sxs-lookup"><span data-stu-id="d8c3b-143">(none)</span></span>                            | <span data-ttu-id="d8c3b-144">-0x001</span><span class="sxs-lookup"><span data-stu-id="d8c3b-144">-0x001</span></span>      | <span data-ttu-id="d8c3b-145">-1</span><span class="sxs-lookup"><span data-stu-id="d8c3b-145">-1</span></span>      | <span data-ttu-id="d8c3b-146">**HKEY \_ Le \_** programme d’installation de l’ordinateur local définit cette clé lors de l’installation de tous les utilisateurs avec [**ALLUSERS**](allusers.md) défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-146">**HKEY\_LOCAL\_MACHINE** Installer sets this key while doing an all-users installation with [**ALLUSERS**](allusers.md) set to 1.</span></span><br/>                                                                       |
| <span data-ttu-id="d8c3b-147">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="d8c3b-147">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="d8c3b-148">0x000</span><span class="sxs-lookup"><span data-stu-id="d8c3b-148">0x000</span></span>       | <span data-ttu-id="d8c3b-149">0</span><span class="sxs-lookup"><span data-stu-id="d8c3b-149">0</span></span>       | <span data-ttu-id="d8c3b-150">**HKEY \_ CLASSES \_ racine** le programme d’installation supprime la valeur de la ruche des **\\ \\ classes logicielles HKCU** lors des installations dans le contexte d' [installation](installation-context.md)par utilisateur et par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-150">**HKEY\_CLASSES\_ROOT** The installer removes the value from the **HKCU\\Software\\Classes** hive during installations in the per-user and per-machine [installation context](installation-context.md).</span></span><br/> |
| <span data-ttu-id="d8c3b-151">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="d8c3b-151">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="d8c3b-152">0x001</span><span class="sxs-lookup"><span data-stu-id="d8c3b-152">0x001</span></span>       | <span data-ttu-id="d8c3b-153">1</span><span class="sxs-lookup"><span data-stu-id="d8c3b-153">1</span></span>       | <span data-ttu-id="d8c3b-154">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="d8c3b-154">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="d8c3b-155">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="d8c3b-155">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="d8c3b-156">0x002</span><span class="sxs-lookup"><span data-stu-id="d8c3b-156">0x002</span></span>       | <span data-ttu-id="d8c3b-157">2</span><span class="sxs-lookup"><span data-stu-id="d8c3b-157">2</span></span>       | <span data-ttu-id="d8c3b-158">**HKEY \_ local \_ machine**</span><span class="sxs-lookup"><span data-stu-id="d8c3b-158">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="d8c3b-159">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="d8c3b-159">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="d8c3b-160">0x003</span><span class="sxs-lookup"><span data-stu-id="d8c3b-160">0x003</span></span>       | <span data-ttu-id="d8c3b-161">3</span><span class="sxs-lookup"><span data-stu-id="d8c3b-161">3</span></span>       | <span data-ttu-id="d8c3b-162">**HKEY, \_ utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="d8c3b-162">**HKEY\_USERS**</span></span>                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="d8c3b-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel</span><span class="sxs-lookup"><span data-stu-id="d8c3b-163"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="d8c3b-164">Clé localisable pour la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-164">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="d8c3b-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="d8c3b-165"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="d8c3b-166">Nom de la valeur de Registre localisable.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-166">The localizable registry value name.</span></span>

<span data-ttu-id="d8c3b-167">La chaîne suivante dans la colonne Name a une signification spéciale.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-167">The following string in the Name column has special significance.</span></span>



| <span data-ttu-id="d8c3b-168">String</span><span class="sxs-lookup"><span data-stu-id="d8c3b-168">String</span></span> | <span data-ttu-id="d8c3b-169">Signification</span><span class="sxs-lookup"><span data-stu-id="d8c3b-169">Meaning</span></span>                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c3b-170">"-"</span><span class="sxs-lookup"><span data-stu-id="d8c3b-170">"-"</span></span>    | <span data-ttu-id="d8c3b-171">La clé doit être supprimée, le cas échéant, avec toutes ses valeurs et ses sous-clés, lorsque le composant est installé.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-171">The key is to be deleted, if present, with all of its values and subkeys, when the component is installed.</span></span> |



 

<span data-ttu-id="d8c3b-172">Notez que la [table de Registre](registry-table.md) doit être utilisée pour créer ou supprimer une clé de registre lors de la suppression du composant.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-172">Note that the [Registry table](registry-table.md) should be used to create or remove a registry key when the component is removed.</span></span>

</dd> <dt>

<span data-ttu-id="d8c3b-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="d8c3b-173"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d8c3b-174">Clé externe dans la première colonne de la [table de composants](component-table.md) référençant le composant qui contrôle la suppression de la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-174">External key into the first column of the [Component table](component-table.md) referencing the component that controls the deletion of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8c3b-175">Notes</span><span class="sxs-lookup"><span data-stu-id="d8c3b-175">Remarks</span></span>

<span data-ttu-id="d8c3b-176">Les informations de Registre sont supprimées du Registre système lorsque le composant correspondant a été sélectionné pour être installé localement ou exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-176">The registry information is deleted from the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="d8c3b-177">Cette table est référencée lorsque l' [action RemoveRegistryValues](removeregistryvalues-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="d8c3b-177">This table is referred to when the [RemoveRegistryValues action](removeregistryvalues-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="d8c3b-178">Validation</span><span class="sxs-lookup"><span data-stu-id="d8c3b-178">Validation</span></span>

<dl>

[<span data-ttu-id="d8c3b-179">ICE03</span><span class="sxs-lookup"><span data-stu-id="d8c3b-179">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d8c3b-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="d8c3b-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d8c3b-181">ICE32</span><span class="sxs-lookup"><span data-stu-id="d8c3b-181">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d8c3b-182">ICE46</span><span class="sxs-lookup"><span data-stu-id="d8c3b-182">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="d8c3b-183">ICE69</span><span class="sxs-lookup"><span data-stu-id="d8c3b-183">ICE69</span></span>](ice69.md)  
</dl>

 

 




