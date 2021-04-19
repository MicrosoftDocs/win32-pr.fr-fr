---
description: La table IniLocator contient les informations nécessaires pour rechercher un fichier ou un répertoire à l’aide d’un fichier. ini ou pour rechercher une entrée. ini particulière. Le fichier. ini doit être présent dans le répertoire par défaut de Microsoft Windows.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Table IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527424"
---
# <a name="inilocator-table"></a><span data-ttu-id="c8c1d-104">Table IniLocator</span><span class="sxs-lookup"><span data-stu-id="c8c1d-104">IniLocator Table</span></span>

<span data-ttu-id="c8c1d-105">La table IniLocator contient les informations nécessaires pour rechercher un fichier ou un répertoire à l’aide d’un fichier. ini ou pour rechercher une entrée. ini particulière.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-105">The IniLocator table holds the information needed to search for a file or directory using an .ini file or to search for a particular .ini entry itself.</span></span> <span data-ttu-id="c8c1d-106">Le fichier. ini doit être présent dans le répertoire par défaut de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-106">The .ini file must be present in the default Microsoft Windows directory.</span></span>

<span data-ttu-id="c8c1d-107">La table IniLocator contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-107">The IniLocator table has the following columns.</span></span>



| <span data-ttu-id="c8c1d-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="c8c1d-108">Column</span></span>      | <span data-ttu-id="c8c1d-109">Type</span><span class="sxs-lookup"><span data-stu-id="c8c1d-109">Type</span></span>                         | <span data-ttu-id="c8c1d-110">Clé</span><span class="sxs-lookup"><span data-stu-id="c8c1d-110">Key</span></span> | <span data-ttu-id="c8c1d-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="c8c1d-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="c8c1d-112">Signature\_</span><span class="sxs-lookup"><span data-stu-id="c8c1d-112">Signature\_</span></span> | [<span data-ttu-id="c8c1d-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="c8c1d-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="c8c1d-114">O</span><span class="sxs-lookup"><span data-stu-id="c8c1d-114">Y</span></span>   | <span data-ttu-id="c8c1d-115">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-115">N</span></span>        |
| <span data-ttu-id="c8c1d-116">FileName</span><span class="sxs-lookup"><span data-stu-id="c8c1d-116">FileName</span></span>    | [<span data-ttu-id="c8c1d-117">FileName</span><span class="sxs-lookup"><span data-stu-id="c8c1d-117">FileName</span></span>](text.md)         | <span data-ttu-id="c8c1d-118">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-118">N</span></span>   | <span data-ttu-id="c8c1d-119">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-119">N</span></span>        |
| <span data-ttu-id="c8c1d-120">Section</span><span class="sxs-lookup"><span data-stu-id="c8c1d-120">Section</span></span>     | [<span data-ttu-id="c8c1d-121">Text</span><span class="sxs-lookup"><span data-stu-id="c8c1d-121">Text</span></span>](text.md)             | <span data-ttu-id="c8c1d-122">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-122">N</span></span>   | <span data-ttu-id="c8c1d-123">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-123">N</span></span>        |
| <span data-ttu-id="c8c1d-124">Clé</span><span class="sxs-lookup"><span data-stu-id="c8c1d-124">Key</span></span>         | [<span data-ttu-id="c8c1d-125">Text</span><span class="sxs-lookup"><span data-stu-id="c8c1d-125">Text</span></span>](text.md)             | <span data-ttu-id="c8c1d-126">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-126">N</span></span>   | <span data-ttu-id="c8c1d-127">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-127">N</span></span>        |
| <span data-ttu-id="c8c1d-128">Champ</span><span class="sxs-lookup"><span data-stu-id="c8c1d-128">Field</span></span>       | [<span data-ttu-id="c8c1d-129">Integer</span><span class="sxs-lookup"><span data-stu-id="c8c1d-129">Integer</span></span>](integer.md)       | <span data-ttu-id="c8c1d-130">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-130">N</span></span>   | <span data-ttu-id="c8c1d-131">O</span><span class="sxs-lookup"><span data-stu-id="c8c1d-131">Y</span></span>        |
| <span data-ttu-id="c8c1d-132">Type</span><span class="sxs-lookup"><span data-stu-id="c8c1d-132">Type</span></span>        | [<span data-ttu-id="c8c1d-133">Integer</span><span class="sxs-lookup"><span data-stu-id="c8c1d-133">Integer</span></span>](integer.md)       | <span data-ttu-id="c8c1d-134">N</span><span class="sxs-lookup"><span data-stu-id="c8c1d-134">N</span></span>   | <span data-ttu-id="c8c1d-135">O</span><span class="sxs-lookup"><span data-stu-id="c8c1d-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c8c1d-136">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c8c1d-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c8c1d-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="c8c1d-137"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="c8c1d-138">Clé externe dans la première colonne de la [table de signatures](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8c1d-138">An external key into the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="c8c1d-139">La signature \_ représente une signature unique et est également la clé externe dans la colonne une de la table de signature.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-139">The Signature\_ represents a unique signature and is also the external key into column one of the Signature table.</span></span> <span data-ttu-id="c8c1d-140">Si cette signature est présente dans la table de signatures, la recherche porte sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-140">If this signature is present in the Signature table, then the search is for a file.</span></span> <span data-ttu-id="c8c1d-141">Si cette clé est absente de la table de signature et que la valeur de la colonne de type est **msidbLocatorTypeRawValue**, la recherche porte sur l’entrée. ini spécifiée par la table IniLocator.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-141">If this key is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the .ini entry specified by the IniLocator table.</span></span> <span data-ttu-id="c8c1d-142">Dans le cas contraire, la recherche concerne un répertoire spécifié par la table IniLocator.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-142">Otherwise the search is for a directory specified by the IniLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="c8c1d-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension</span><span class="sxs-lookup"><span data-stu-id="c8c1d-143"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="c8c1d-144">Nom du fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-144">The .ini file name.</span></span>

</dd> <dt>

<span data-ttu-id="c8c1d-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span><span class="sxs-lookup"><span data-stu-id="c8c1d-145"><span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section</span></span>
</dt> <dd>

<span data-ttu-id="c8c1d-146">Nom de la section dans le fichier. ini.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-146">Section name within the .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="c8c1d-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Essentiel</span><span class="sxs-lookup"><span data-stu-id="c8c1d-147"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="c8c1d-148">Valeur de clé dans la section.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-148">Key value within the section.</span></span>

</dd> <dt>

<span data-ttu-id="c8c1d-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Case</span><span class="sxs-lookup"><span data-stu-id="c8c1d-149"><span id="Field"></span><span id="field"></span><span id="FIELD"></span>Field</span></span>
</dt> <dd>

<span data-ttu-id="c8c1d-150">Champ de la ligne. ini.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-150">The field in the .ini line.</span></span> <span data-ttu-id="c8c1d-151">Si le champ a la valeur null ou est égal à 0, la ligne entière est lue.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-151">If Field is Null or 0, then the entire line is read.</span></span> <span data-ttu-id="c8c1d-152">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-152">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="c8c1d-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer</span><span class="sxs-lookup"><span data-stu-id="c8c1d-153"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="c8c1d-154">Valeur qui détermine si la valeur. ini est un emplacement de fichier, un emplacement de répertoire ou une valeur RAW. ini.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-154">A value that determines whether the .ini value is a file location, a directory location, or raw .ini value.</span></span>

<span data-ttu-id="c8c1d-155">Le tableau suivant répertorie les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-155">The following table lists valid values.</span></span> <span data-ttu-id="c8c1d-156">Si elle est absente, le type est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-156">If absent, Type is set to be 1.</span></span>



| <span data-ttu-id="c8c1d-157">Constante</span><span class="sxs-lookup"><span data-stu-id="c8c1d-157">Constant</span></span>                      | <span data-ttu-id="c8c1d-158">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="c8c1d-158">Hexadecimal</span></span> | <span data-ttu-id="c8c1d-159">Decimal</span><span class="sxs-lookup"><span data-stu-id="c8c1d-159">Decimal</span></span> | <span data-ttu-id="c8c1d-160">Description</span><span class="sxs-lookup"><span data-stu-id="c8c1d-160">Description</span></span>           |
|-------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="c8c1d-161">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="c8c1d-161">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="c8c1d-162">0x000</span><span class="sxs-lookup"><span data-stu-id="c8c1d-162">0x000</span></span>       | <span data-ttu-id="c8c1d-163">0</span><span class="sxs-lookup"><span data-stu-id="c8c1d-163">0</span></span>       | <span data-ttu-id="c8c1d-164">Emplacement du répertoire.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-164">A directory location.</span></span> |
| <span data-ttu-id="c8c1d-165">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="c8c1d-165">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="c8c1d-166">0x001</span><span class="sxs-lookup"><span data-stu-id="c8c1d-166">0x001</span></span>       | <span data-ttu-id="c8c1d-167">1</span><span class="sxs-lookup"><span data-stu-id="c8c1d-167">1</span></span>       | <span data-ttu-id="c8c1d-168">Emplacement de fichier.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-168">A file location.</span></span>      |
| <span data-ttu-id="c8c1d-169">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="c8c1d-169">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="c8c1d-170">0x002</span><span class="sxs-lookup"><span data-stu-id="c8c1d-170">0x002</span></span>       | <span data-ttu-id="c8c1d-171">2</span><span class="sxs-lookup"><span data-stu-id="c8c1d-171">2</span></span>       | <span data-ttu-id="c8c1d-172">Valeur RAW. ini.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-172">A raw .ini value.</span></span>     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8c1d-173">Notes</span><span class="sxs-lookup"><span data-stu-id="c8c1d-173">Remarks</span></span>

<span data-ttu-id="c8c1d-174">Cette table est utilisée avec la [table AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8c1d-174">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="c8c1d-175">Les colonnes de cette table ne sont généralement pas localisées.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-175">This table's columns are generally not localized.</span></span> <span data-ttu-id="c8c1d-176">Si un auteur décide de rechercher des produits dans plusieurs langues, il peut y avoir une entrée distincte incluse dans le tableau pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="c8c1d-176">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="c8c1d-177">Le texte localisé associé à l’affichage de progression ou à la journalisation est spécifié dans la [table ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8c1d-177">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="c8c1d-178">Consultez [recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="c8c1d-178">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="c8c1d-179">Validation</span><span class="sxs-lookup"><span data-stu-id="c8c1d-179">Validation</span></span>

<dl>

[<span data-ttu-id="c8c1d-180">ICE03</span><span class="sxs-lookup"><span data-stu-id="c8c1d-180">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c8c1d-181">ICE06</span><span class="sxs-lookup"><span data-stu-id="c8c1d-181">ICE06</span></span>](ice06.md)  
</dl>

 

 



