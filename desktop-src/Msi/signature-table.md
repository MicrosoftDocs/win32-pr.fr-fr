---
description: La table de signatures contient les informations qui identifient de façon unique une signature de fichier. Pour plus d’informations sur les signatures, consultez signatures numériques et Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Table de signature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518763"
---
# <a name="signature-table"></a><span data-ttu-id="92906-104">Table de signature</span><span class="sxs-lookup"><span data-stu-id="92906-104">Signature Table</span></span>

<span data-ttu-id="92906-105">La table de signatures contient les informations qui identifient de façon unique une signature de fichier.</span><span class="sxs-lookup"><span data-stu-id="92906-105">The Signature table holds the information that uniquely identifies a file signature.</span></span> <span data-ttu-id="92906-106">Pour plus d’informations sur les signatures [, consultez signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="92906-106">For more information regarding signatures see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="92906-107">La table de signatures contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="92906-107">The Signature table has the following columns.</span></span>



| <span data-ttu-id="92906-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="92906-108">Column</span></span>     | <span data-ttu-id="92906-109">Type</span><span class="sxs-lookup"><span data-stu-id="92906-109">Type</span></span>                               | <span data-ttu-id="92906-110">Clé</span><span class="sxs-lookup"><span data-stu-id="92906-110">Key</span></span> | <span data-ttu-id="92906-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="92906-111">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="92906-112">Signature</span><span class="sxs-lookup"><span data-stu-id="92906-112">Signature</span></span>  | [<span data-ttu-id="92906-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="92906-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="92906-114">O</span><span class="sxs-lookup"><span data-stu-id="92906-114">Y</span></span>   | <span data-ttu-id="92906-115">N</span><span class="sxs-lookup"><span data-stu-id="92906-115">N</span></span>        |
| <span data-ttu-id="92906-116">FileName</span><span class="sxs-lookup"><span data-stu-id="92906-116">FileName</span></span>   | [<span data-ttu-id="92906-117">Text</span><span class="sxs-lookup"><span data-stu-id="92906-117">Text</span></span>](text.md)                   | <span data-ttu-id="92906-118">N</span><span class="sxs-lookup"><span data-stu-id="92906-118">N</span></span>   | <span data-ttu-id="92906-119">N</span><span class="sxs-lookup"><span data-stu-id="92906-119">N</span></span>        |
| <span data-ttu-id="92906-120">MinVersion</span><span class="sxs-lookup"><span data-stu-id="92906-120">MinVersion</span></span> | [<span data-ttu-id="92906-121">Text</span><span class="sxs-lookup"><span data-stu-id="92906-121">Text</span></span>](text.md)                   | <span data-ttu-id="92906-122">N</span><span class="sxs-lookup"><span data-stu-id="92906-122">N</span></span>   | <span data-ttu-id="92906-123">O</span><span class="sxs-lookup"><span data-stu-id="92906-123">Y</span></span>        |
| <span data-ttu-id="92906-124">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="92906-124">MaxVersion</span></span> | [<span data-ttu-id="92906-125">Text</span><span class="sxs-lookup"><span data-stu-id="92906-125">Text</span></span>](text.md)                   | <span data-ttu-id="92906-126">N</span><span class="sxs-lookup"><span data-stu-id="92906-126">N</span></span>   | <span data-ttu-id="92906-127">O</span><span class="sxs-lookup"><span data-stu-id="92906-127">Y</span></span>        |
| <span data-ttu-id="92906-128">MinSize</span><span class="sxs-lookup"><span data-stu-id="92906-128">MinSize</span></span>    | [<span data-ttu-id="92906-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="92906-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="92906-130">N</span><span class="sxs-lookup"><span data-stu-id="92906-130">N</span></span>   | <span data-ttu-id="92906-131">O</span><span class="sxs-lookup"><span data-stu-id="92906-131">Y</span></span>        |
| <span data-ttu-id="92906-132">MaxSize</span><span class="sxs-lookup"><span data-stu-id="92906-132">MaxSize</span></span>    | [<span data-ttu-id="92906-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="92906-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="92906-134">N</span><span class="sxs-lookup"><span data-stu-id="92906-134">N</span></span>   | <span data-ttu-id="92906-135">O</span><span class="sxs-lookup"><span data-stu-id="92906-135">Y</span></span>        |
| <span data-ttu-id="92906-136">À l’esprit</span><span class="sxs-lookup"><span data-stu-id="92906-136">MinDate</span></span>    | [<span data-ttu-id="92906-137">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="92906-137">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="92906-138">N</span><span class="sxs-lookup"><span data-stu-id="92906-138">N</span></span>   | <span data-ttu-id="92906-139">O</span><span class="sxs-lookup"><span data-stu-id="92906-139">Y</span></span>        |
| <span data-ttu-id="92906-140">MaxDate</span><span class="sxs-lookup"><span data-stu-id="92906-140">MaxDate</span></span>    | [<span data-ttu-id="92906-141">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="92906-141">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="92906-142">N</span><span class="sxs-lookup"><span data-stu-id="92906-142">N</span></span>   | <span data-ttu-id="92906-143">O</span><span class="sxs-lookup"><span data-stu-id="92906-143">Y</span></span>        |
| <span data-ttu-id="92906-144">Langages</span><span class="sxs-lookup"><span data-stu-id="92906-144">Languages</span></span>  | [<span data-ttu-id="92906-145">Text</span><span class="sxs-lookup"><span data-stu-id="92906-145">Text</span></span>](text.md)                   | <span data-ttu-id="92906-146">N</span><span class="sxs-lookup"><span data-stu-id="92906-146">N</span></span>   | <span data-ttu-id="92906-147">O</span><span class="sxs-lookup"><span data-stu-id="92906-147">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="92906-148">Colonnes</span><span class="sxs-lookup"><span data-stu-id="92906-148">Columns</span></span>

<dl> <dt>

<span data-ttu-id="92906-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span><span class="sxs-lookup"><span data-stu-id="92906-149"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="92906-150">La colonne signature est une signature de fichier unique.</span><span class="sxs-lookup"><span data-stu-id="92906-150">The Signature column is a unique file signature.</span></span>

</dd> <dt>

<span data-ttu-id="92906-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension</span><span class="sxs-lookup"><span data-stu-id="92906-151"><span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName</span></span>
</dt> <dd>

<span data-ttu-id="92906-152">Nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="92906-152">The name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="92906-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span><span class="sxs-lookup"><span data-stu-id="92906-153"><span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion</span></span>
</dt> <dd>

<span data-ttu-id="92906-154">Version minimale du fichier, avec une comparaison de langage.</span><span class="sxs-lookup"><span data-stu-id="92906-154">The minimum version of the file, with a language comparison.</span></span> <span data-ttu-id="92906-155">Si ce champ est spécifié, le fichier doit avoir une version qui est au moins égale à MinVersion.</span><span class="sxs-lookup"><span data-stu-id="92906-155">If this field is specified, then the file must have a version that is at least equal to MinVersion.</span></span> <span data-ttu-id="92906-156">Si le fichier a une version égale à la valeur du champ MinVersion, mais que la langue spécifiée dans la colonne languages diffère, le fichier ne répond pas aux critères de filtre de signature.</span><span class="sxs-lookup"><span data-stu-id="92906-156">If the file has an equal version to the MinVersion field value but the language specified in the Languages column differs, the file does not satisfy the signature filter criteria.</span></span>

> [!Note]  
> <span data-ttu-id="92906-157">La langue spécifiée dans la colonne langues est utilisée dans la comparaison et il n’existe aucun moyen d’ignorer la langue.</span><span class="sxs-lookup"><span data-stu-id="92906-157">The language specified in the Languages column is used in the comparison and there is no way to ignore language.</span></span> <span data-ttu-id="92906-158">Si vous souhaitez qu’un fichier respecte la spécification de champ MinVersion, quelle que soit la langue, vous devez entrer une valeur dans le champ MinVersion qui est inférieure d’une unité à la valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="92906-158">If you want a file to meet the MinVersion field requirement regardless of language, you must enter a value in the MinVersion field that is one less than the actual value.</span></span> <span data-ttu-id="92906-159">Par exemple, si la version minimale du filtre est 2.0.2600.1183, utilisez 2.0.2600.1182 pour rechercher le fichier sans faire correspondre les informations de langue.</span><span class="sxs-lookup"><span data-stu-id="92906-159">For example, if the minimum version for the filter is 2.0.2600.1183, use 2.0.2600.1182 to find the file without matching the language information.</span></span>

 

</dd> <dt>

<span data-ttu-id="92906-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span><span class="sxs-lookup"><span data-stu-id="92906-160"><span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="92906-161">Version maximale du fichier.</span><span class="sxs-lookup"><span data-stu-id="92906-161">The maximum version of the file.</span></span> <span data-ttu-id="92906-162">Si ce champ est spécifié, le fichier doit avoir une version qui est au plus égale à MaxVersion.</span><span class="sxs-lookup"><span data-stu-id="92906-162">If this field is specified, then the file must have a version that is at most equal to MaxVersion.</span></span>

</dd> <dt>

<span data-ttu-id="92906-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span><span class="sxs-lookup"><span data-stu-id="92906-163"><span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize</span></span>
</dt> <dd>

<span data-ttu-id="92906-164">Taille minimale du fichier.</span><span class="sxs-lookup"><span data-stu-id="92906-164">The minimum size of the file.</span></span> <span data-ttu-id="92906-165">Si ce champ est spécifié, le fichier sous inspection doit avoir une taille au moins égale à MinSize.</span><span class="sxs-lookup"><span data-stu-id="92906-165">If this field is specified, then the file under inspection must have a size that is at least equal to MinSize.</span></span> <span data-ttu-id="92906-166">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="92906-166">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="92906-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span><span class="sxs-lookup"><span data-stu-id="92906-167"><span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize</span></span>
</dt> <dd>

<span data-ttu-id="92906-168">Taille maximale du fichier.</span><span class="sxs-lookup"><span data-stu-id="92906-168">The maximum size of the file.</span></span> <span data-ttu-id="92906-169">Si ce champ est spécifié, le fichier sous inspection doit avoir une taille qui est au plus égale à MaxSize.</span><span class="sxs-lookup"><span data-stu-id="92906-169">If this field is specified, then the file under inspection must have a size that is at most equal to MaxSize.</span></span> <span data-ttu-id="92906-170">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="92906-170">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="92906-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>À l’esprit</span><span class="sxs-lookup"><span data-stu-id="92906-171"><span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate</span></span>
</dt> <dd>

<span data-ttu-id="92906-172">Date et heure de la modification minimale du fichier.</span><span class="sxs-lookup"><span data-stu-id="92906-172">The minimum modification date and time of the file.</span></span> <span data-ttu-id="92906-173">Si ce champ est spécifié, le fichier en cours d’inspection doit avoir une date et une heure de modification au moins égales à l’MinDate.</span><span class="sxs-lookup"><span data-stu-id="92906-173">If this field is specified, then the file under inspection must have a modification date and time that is at least equal to MinDate.</span></span> <span data-ttu-id="92906-174">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="92906-174">This must be a non-negative number.</span></span> <span data-ttu-id="92906-175">Le format de ce champ est deux valeurs 16 bits compressées de type **Word**.</span><span class="sxs-lookup"><span data-stu-id="92906-175">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="92906-176">La valeur de **mot** de poids fort spécifie la date au format de date ms-dos.</span><span class="sxs-lookup"><span data-stu-id="92906-176">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="92906-177">La valeur de **mot** de poids faible spécifie l’heure au format de temps ms-dos.</span><span class="sxs-lookup"><span data-stu-id="92906-177">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="92906-178">La valeur 0 pour la valeur d’heure représente minuit.</span><span class="sxs-lookup"><span data-stu-id="92906-178">A value of 0 for the time value represents midnight.</span></span> <span data-ttu-id="92906-179">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="92906-179">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="92906-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span><span class="sxs-lookup"><span data-stu-id="92906-180"><span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate</span></span>
</dt> <dd>

<span data-ttu-id="92906-181">Date de création maximale du fichier.</span><span class="sxs-lookup"><span data-stu-id="92906-181">The maximum creation date of the file.</span></span> <span data-ttu-id="92906-182">Si ce champ est spécifié, le fichier sous inspection doit avoir une date de création qui est au plus égale à MaxDate.</span><span class="sxs-lookup"><span data-stu-id="92906-182">If this field is specified, then the file under inspection must have a creation date that is at most equal to MaxDate.</span></span> <span data-ttu-id="92906-183">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="92906-183">This must be a non-negative number.</span></span> <span data-ttu-id="92906-184">Le format de ce champ est deux valeurs 16 bits compressées de type **Word**.</span><span class="sxs-lookup"><span data-stu-id="92906-184">The format of this field is two packed 16-bit values of type **WORD**.</span></span> <span data-ttu-id="92906-185">La valeur de **mot** de poids fort spécifie la date au format de date ms-dos.</span><span class="sxs-lookup"><span data-stu-id="92906-185">The high order **WORD** value specifies the date in MS-DOS date format.</span></span> <span data-ttu-id="92906-186">La valeur de **mot** de poids faible spécifie l’heure au format de temps ms-dos.</span><span class="sxs-lookup"><span data-stu-id="92906-186">The low order **WORD** value specifies the time in MS-DOS time format.</span></span> <span data-ttu-id="92906-187">La valeur 0 pour la valeur d’heure représente minuit.</span><span class="sxs-lookup"><span data-stu-id="92906-187">A value of 0 for the time value represent midnight.</span></span> <span data-ttu-id="92906-188">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="92906-188">See the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="92906-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Traduction</span><span class="sxs-lookup"><span data-stu-id="92906-189"><span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Languages</span></span>
</dt> <dd>

<span data-ttu-id="92906-190">Langues prises en charge par le fichier.</span><span class="sxs-lookup"><span data-stu-id="92906-190">The languages supported by the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92906-191">Notes</span><span class="sxs-lookup"><span data-stu-id="92906-191">Remarks</span></span>

<span data-ttu-id="92906-192">Cette table est utilisée avec la [table AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="92906-192">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="92906-193">La signature est recherchée à l’aide de la [table RegLocator](reglocator-table.md), de la table [IniLocator](inilocator-table.md), de la table [CompLocator](complocator-table.md)et de la [table DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="92906-193">The signature is searched for using the [RegLocator table](reglocator-table.md), the [IniLocator table](inilocator-table.md), the [CompLocator table](complocator-table.md), and the [DrLocator table](drlocator-table.md).</span></span> <span data-ttu-id="92906-194">Les colonnes de cette table ne sont généralement pas localisées.</span><span class="sxs-lookup"><span data-stu-id="92906-194">This table's columns are generally not localized.</span></span> <span data-ttu-id="92906-195">Si un auteur décide de rechercher des produits dans plusieurs langues, il peut y avoir une entrée distincte incluse dans le tableau pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="92906-195">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="92906-196">La table de signatures suit généralement les [règles](file-versioning-rules.md)de contrôle de version de fichier Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="92906-196">The Signature table generally follows the Windows Installer [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="92906-197">Les langues spécifiées dans la colonne languages de la table de signature ne sont pas évaluées à moins que les versions de fichiers soient équivalentes.</span><span class="sxs-lookup"><span data-stu-id="92906-197">Languages specified in the Languages column of the Signature table are not evaluated unless the file versions are equivalent.</span></span> <span data-ttu-id="92906-198">La colonne languages permet de garantir qu’un fichier est d’une langue particulière s’il s’agit de la version demandée.</span><span class="sxs-lookup"><span data-stu-id="92906-198">The Languages column will ensure that a file is of a particular language if it is of the requested version.</span></span> <span data-ttu-id="92906-199">Aucune méthode n’est disponible pour ignorer la colonne languages.</span><span class="sxs-lookup"><span data-stu-id="92906-199">There is no method available to ignore the Languages column.</span></span> <span data-ttu-id="92906-200">Une valeur NULL entrée dans la colonne Languages est traitée comme un fichier sans langage et ne correspond pas à la signature de fichier d’un fichier dont la langue apparaît dans la table de signature.</span><span class="sxs-lookup"><span data-stu-id="92906-200">A NULL value entered in the Languages column is treated as a file without a language and does not match the file signature of a file with a language appearing in the Signature table.</span></span> <span data-ttu-id="92906-201">L’exemple suivant recherche une version particulière de MSI.DLL.</span><span class="sxs-lookup"><span data-stu-id="92906-201">The following example searches for a particular version of MSI.DLL.</span></span>

[<span data-ttu-id="92906-202">Table DrLocator</span><span class="sxs-lookup"><span data-stu-id="92906-202">DrLocator table</span></span>](drlocator-table.md)

| <span data-ttu-id="92906-203">Signature\_</span><span class="sxs-lookup"><span data-stu-id="92906-203">Signature\_</span></span> | <span data-ttu-id="92906-204">Parent</span><span class="sxs-lookup"><span data-stu-id="92906-204">Parent</span></span> | <span data-ttu-id="92906-205">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="92906-205">Path</span></span>                  | <span data-ttu-id="92906-206">Profondeur</span><span class="sxs-lookup"><span data-stu-id="92906-206">Depth</span></span> |
|-------------|--------|-----------------------|-------|
| <span data-ttu-id="92906-207">MsiDll</span><span class="sxs-lookup"><span data-stu-id="92906-207">MsiDll</span></span>      | <span data-ttu-id="92906-208">nul</span><span class="sxs-lookup"><span data-stu-id="92906-208">{null}</span></span> | <span data-ttu-id="92906-209">c : \\ Windows \\ system32</span><span class="sxs-lookup"><span data-stu-id="92906-209">c:\\windows\\system32</span></span> | <span data-ttu-id="92906-210">0</span><span class="sxs-lookup"><span data-stu-id="92906-210">0</span></span>     |



 

[<span data-ttu-id="92906-211">Table AppSearch</span><span class="sxs-lookup"><span data-stu-id="92906-211">AppSearch Table</span></span>](appsearch-table.md)



| <span data-ttu-id="92906-212">Propriété</span><span class="sxs-lookup"><span data-stu-id="92906-212">Property</span></span> | <span data-ttu-id="92906-213">Signature\_</span><span class="sxs-lookup"><span data-stu-id="92906-213">Signature\_</span></span> |
|----------|-------------|
| <span data-ttu-id="92906-214">MSIDLL</span><span class="sxs-lookup"><span data-stu-id="92906-214">MSIDLL</span></span>   | <span data-ttu-id="92906-215">MsiDll</span><span class="sxs-lookup"><span data-stu-id="92906-215">MsiDll</span></span>      |



 

<span data-ttu-id="92906-216">Table de signature</span><span class="sxs-lookup"><span data-stu-id="92906-216">Signature table</span></span>



| <span data-ttu-id="92906-217">Signature</span><span class="sxs-lookup"><span data-stu-id="92906-217">Signature</span></span> | <span data-ttu-id="92906-218">FileName</span><span class="sxs-lookup"><span data-stu-id="92906-218">FileName</span></span> | <span data-ttu-id="92906-219">MinVersion</span><span class="sxs-lookup"><span data-stu-id="92906-219">MinVersion</span></span>    | <span data-ttu-id="92906-220">MaxVersion</span><span class="sxs-lookup"><span data-stu-id="92906-220">MaxVersion</span></span> | <span data-ttu-id="92906-221">MinSize</span><span class="sxs-lookup"><span data-stu-id="92906-221">MinSize</span></span> | <span data-ttu-id="92906-222">MaxSize</span><span class="sxs-lookup"><span data-stu-id="92906-222">MaxSize</span></span> | <span data-ttu-id="92906-223">À l’esprit</span><span class="sxs-lookup"><span data-stu-id="92906-223">MinDate</span></span> | <span data-ttu-id="92906-224">MaxDate</span><span class="sxs-lookup"><span data-stu-id="92906-224">MaxDate</span></span> | <span data-ttu-id="92906-225">Langages</span><span class="sxs-lookup"><span data-stu-id="92906-225">Languages</span></span> |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| <span data-ttu-id="92906-226">MsiDll</span><span class="sxs-lookup"><span data-stu-id="92906-226">MsiDll</span></span>    | <span data-ttu-id="92906-227">msi.dll</span><span class="sxs-lookup"><span data-stu-id="92906-227">msi.dll</span></span>  | <span data-ttu-id="92906-228">2.0.2600.1106</span><span class="sxs-lookup"><span data-stu-id="92906-228">2.0.2600.1106</span></span> | <span data-ttu-id="92906-229">nul</span><span class="sxs-lookup"><span data-stu-id="92906-229">{null}</span></span>     | <span data-ttu-id="92906-230">nul</span><span class="sxs-lookup"><span data-stu-id="92906-230">{null}</span></span>  | <span data-ttu-id="92906-231">nul</span><span class="sxs-lookup"><span data-stu-id="92906-231">{null}</span></span>  | <span data-ttu-id="92906-232">nul</span><span class="sxs-lookup"><span data-stu-id="92906-232">{null}</span></span>  | <span data-ttu-id="92906-233">nul</span><span class="sxs-lookup"><span data-stu-id="92906-233">{null}</span></span>  | <span data-ttu-id="92906-234">0</span><span class="sxs-lookup"><span data-stu-id="92906-234">0</span></span>         |



 

<span data-ttu-id="92906-235">Dans ce cas, et sur Windows XP SP1, l' [action AppSearch](appsearch-action.md) définit MSIDLL sur c : \\ Windows \\ system32 \\msi.dll, car MSI.DLL est un fichier indépendant de la langue.</span><span class="sxs-lookup"><span data-stu-id="92906-235">In this case, and on Windows XP SP1, the [AppSearch action](appsearch-action.md) sets MSIDLL to c:\\windows\\system32\\msi.dll because MSI.DLL is a language neutral file.</span></span> <span data-ttu-id="92906-236">Si la valeur de la colonne Languages est modifiée de 0 à 1033, l’action AppSearch ne parvient pas à trouver le msi.dll correspondant et la propriété MSIDLL n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="92906-236">If the value of the Languages column is changed from 0 to 1033, then the AppSearch action fails to find the matching msi.dll and the MSIDLL property is undefined.</span></span>

<span data-ttu-id="92906-237">Vous ne pouvez pas utiliser la table de signatures pour effectuer une requête sur des langues uniquement.</span><span class="sxs-lookup"><span data-stu-id="92906-237">You cannot use the Signature table to query on languages alone.</span></span> <span data-ttu-id="92906-238">Pour rechercher les différentes versions linguistiques d’un fichier, vous devez disposer d’une entrée distincte dans la table de signatures pour chaque version de langue.</span><span class="sxs-lookup"><span data-stu-id="92906-238">To search for different language versions of a file, you must have a separate entry in the Signature table for each language version.</span></span> <span data-ttu-id="92906-239">Si plusieurs langues sont fournies dans la colonne Languages, la recherche porte sur un fichier qui prend en charge toutes ces langues.</span><span class="sxs-lookup"><span data-stu-id="92906-239">If multiple languages are provided in the Languages column, then the search is for a file that supports all of those languages.</span></span>

<span data-ttu-id="92906-240">Le format des colonnes MinDate et MaxDate est deux valeurs 16 bits compressées de type **Word**.</span><span class="sxs-lookup"><span data-stu-id="92906-240">The format of MinDate and MaxDate columns are two packed 16-bit values of type **WORD**.</span></span>

<span data-ttu-id="92906-241">**Mot** de date</span><span class="sxs-lookup"><span data-stu-id="92906-241">Date **WORD**</span></span>



| <span data-ttu-id="92906-242">Bits</span><span class="sxs-lookup"><span data-stu-id="92906-242">Bits</span></span> | <span data-ttu-id="92906-243">Content</span><span class="sxs-lookup"><span data-stu-id="92906-243">Content</span></span>                                             |
|------|-----------------------------------------------------|
| <span data-ttu-id="92906-244">0 – 4</span><span class="sxs-lookup"><span data-stu-id="92906-244">0–4</span></span>  | <span data-ttu-id="92906-245">Jour du mois (1-31)</span><span class="sxs-lookup"><span data-stu-id="92906-245">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="92906-246">5-8</span><span class="sxs-lookup"><span data-stu-id="92906-246">5-8</span></span>  | <span data-ttu-id="92906-247">Month (1 = janvier, 2 = février, etc.)</span><span class="sxs-lookup"><span data-stu-id="92906-247">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="92906-248">9-15</span><span class="sxs-lookup"><span data-stu-id="92906-248">9-15</span></span> | <span data-ttu-id="92906-249">Décalage d’année à partir de 1980 (Ajouter 1980 pour atteindre l’année réelle)</span><span class="sxs-lookup"><span data-stu-id="92906-249">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

<span data-ttu-id="92906-250">**Mot** de temps</span><span class="sxs-lookup"><span data-stu-id="92906-250">Time **WORD**</span></span>



| <span data-ttu-id="92906-251">Bits</span><span class="sxs-lookup"><span data-stu-id="92906-251">Bits</span></span>  | <span data-ttu-id="92906-252">Content</span><span class="sxs-lookup"><span data-stu-id="92906-252">Content</span></span>                     |
|-------|-----------------------------|
| <span data-ttu-id="92906-253">0 – 4</span><span class="sxs-lookup"><span data-stu-id="92906-253">0–4</span></span>   | <span data-ttu-id="92906-254">Secondes divisées par 2</span><span class="sxs-lookup"><span data-stu-id="92906-254">Seconds divided by 2</span></span>        |
| <span data-ttu-id="92906-255">5-10</span><span class="sxs-lookup"><span data-stu-id="92906-255">5-10</span></span>  | <span data-ttu-id="92906-256">Minutes (0-59)</span><span class="sxs-lookup"><span data-stu-id="92906-256">Minutes (0-59)</span></span>              |
| <span data-ttu-id="92906-257">11-15</span><span class="sxs-lookup"><span data-stu-id="92906-257">11-15</span></span> | <span data-ttu-id="92906-258">Heure (de 0 à 23 sur 24 heures)</span><span class="sxs-lookup"><span data-stu-id="92906-258">Hour(0-23 on 24 hour clock)</span></span> |



 

<span data-ttu-id="92906-259">La formule permettant de calculer les valeurs des champs MinDate et MaxDate est la suivante :</span><span class="sxs-lookup"><span data-stu-id="92906-259">The formula for calculating the MinDate and MaxDate field values is:</span></span>

<span data-ttu-id="92906-260">((Année-1980) \* 512 + mois \* 32 + jour) \* 65536 + heures \* 2048 + minutes \* 32 + secondes/2</span><span class="sxs-lookup"><span data-stu-id="92906-260">( (Year - 1980) \* 512 + Month \* 32 + Day ) \* 65536 + Hours \* 2048 + Minutes \* 32 + Seconds/2</span></span>

## <a name="validation"></a><span data-ttu-id="92906-261">Validation</span><span class="sxs-lookup"><span data-stu-id="92906-261">Validation</span></span>

<dl>

[<span data-ttu-id="92906-262">ICE03</span><span class="sxs-lookup"><span data-stu-id="92906-262">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="92906-263">ICE06</span><span class="sxs-lookup"><span data-stu-id="92906-263">ICE06</span></span>](ice06.md)  
</dl>

 

 



