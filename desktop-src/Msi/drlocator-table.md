---
description: La table DrLocator contient les informations nécessaires pour trouver un fichier ou un répertoire en recherchant dans l’arborescence de répertoires.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Table DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534358"
---
# <a name="drlocator-table"></a><span data-ttu-id="072f9-103">Table DrLocator</span><span class="sxs-lookup"><span data-stu-id="072f9-103">DrLocator Table</span></span>

<span data-ttu-id="072f9-104">La table DrLocator contient les informations nécessaires pour trouver un fichier ou un répertoire en recherchant dans l’arborescence de répertoires.</span><span class="sxs-lookup"><span data-stu-id="072f9-104">The DrLocator table holds the information needed to find a file or directory by searching the directory tree.</span></span>

<span data-ttu-id="072f9-105">La table DrLocator contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="072f9-105">The DrLocator table has the following columns.</span></span>



| <span data-ttu-id="072f9-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="072f9-106">Column</span></span>      | <span data-ttu-id="072f9-107">Type</span><span class="sxs-lookup"><span data-stu-id="072f9-107">Type</span></span>                         | <span data-ttu-id="072f9-108">Clé</span><span class="sxs-lookup"><span data-stu-id="072f9-108">Key</span></span> | <span data-ttu-id="072f9-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="072f9-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="072f9-110">Signature\_</span><span class="sxs-lookup"><span data-stu-id="072f9-110">Signature\_</span></span> | [<span data-ttu-id="072f9-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="072f9-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="072f9-112">O</span><span class="sxs-lookup"><span data-stu-id="072f9-112">Y</span></span>   | <span data-ttu-id="072f9-113">N</span><span class="sxs-lookup"><span data-stu-id="072f9-113">N</span></span>        |
| <span data-ttu-id="072f9-114">Parent</span><span class="sxs-lookup"><span data-stu-id="072f9-114">Parent</span></span>      | [<span data-ttu-id="072f9-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="072f9-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="072f9-116">O</span><span class="sxs-lookup"><span data-stu-id="072f9-116">Y</span></span>   | <span data-ttu-id="072f9-117">O</span><span class="sxs-lookup"><span data-stu-id="072f9-117">Y</span></span>        |
| <span data-ttu-id="072f9-118">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="072f9-118">Path</span></span>        | [<span data-ttu-id="072f9-119">AnyPath</span><span class="sxs-lookup"><span data-stu-id="072f9-119">AnyPath</span></span>](anypath.md)       | <span data-ttu-id="072f9-120">O</span><span class="sxs-lookup"><span data-stu-id="072f9-120">Y</span></span>   | <span data-ttu-id="072f9-121">O</span><span class="sxs-lookup"><span data-stu-id="072f9-121">Y</span></span>        |
| <span data-ttu-id="072f9-122">Profondeur</span><span class="sxs-lookup"><span data-stu-id="072f9-122">Depth</span></span>       | [<span data-ttu-id="072f9-123">Integer</span><span class="sxs-lookup"><span data-stu-id="072f9-123">Integer</span></span>](integer.md)       | <span data-ttu-id="072f9-124">N</span><span class="sxs-lookup"><span data-stu-id="072f9-124">N</span></span>   | <span data-ttu-id="072f9-125">O</span><span class="sxs-lookup"><span data-stu-id="072f9-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="072f9-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="072f9-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="072f9-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span><span class="sxs-lookup"><span data-stu-id="072f9-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="072f9-128">La \_ colonne signature est une clé externe de la première colonne de la [table de signature](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="072f9-128">The Signature\_ column is an external key to the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="072f9-129">Ce champ peut représenter une signature de fichier unique figurant dans la table de signatures.</span><span class="sxs-lookup"><span data-stu-id="072f9-129">This field may represent a unique file signature listed in the Signature table.</span></span> <span data-ttu-id="072f9-130">Si la valeur de cette colonne est absente de la table de signature, la recherche est supposée être pour un répertoire désigné par la table DrLocator.</span><span class="sxs-lookup"><span data-stu-id="072f9-130">If the value in this column is absent from the Signature table, then the search is assumed to be for a directory pointed to by the DrLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="072f9-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent</span><span class="sxs-lookup"><span data-stu-id="072f9-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent</span></span>
</dt> <dd>

<span data-ttu-id="072f9-132">Cette colonne est la signature du répertoire parent du fichier ou du répertoire dans la colonne signature \_ .</span><span class="sxs-lookup"><span data-stu-id="072f9-132">This column is the signature of the parent directory of the file or directory in the Signature\_ column.</span></span> <span data-ttu-id="072f9-133">Si ce champ a la valeur null et que la colonne de chemin d’accès ne se développe pas en chemin d’accès complet, tous les lecteurs fixes du système de l’utilisateur sont recherchés à l’aide du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="072f9-133">If this field is null, and the Path column does not expand to a full path, then all the fixed drives of the user's system are searched by using the Path.</span></span>

<span data-ttu-id="072f9-134">Ce champ est une clé dans l’une des tables suivantes : [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)ou DrLocator.</span><span class="sxs-lookup"><span data-stu-id="072f9-134">This field is a key into one of the following tables: the [RegLocator](reglocator-table.md), the [IniLocator](inilocator-table.md), the [CompLocator](complocator-table.md), or the DrLocator tables.</span></span>

</dd> <dt>

<span data-ttu-id="072f9-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>D</span><span class="sxs-lookup"><span data-stu-id="072f9-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="072f9-136">La colonne Path contient le chemin d’accès sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="072f9-136">The Path column contains the path on the user's system.</span></span> <span data-ttu-id="072f9-137">Il s’agit d’un chemin d’accès complet ou d’un sous-chemin d’accès relatif sous le répertoire spécifié dans la colonne parente.</span><span class="sxs-lookup"><span data-stu-id="072f9-137">This is a either a full path or a relative subpath below the directory specified in the Parent column.</span></span> <span data-ttu-id="072f9-138">Consultez les restrictions sur le type de données [AnyPath](anypath.md) .</span><span class="sxs-lookup"><span data-stu-id="072f9-138">See the restrictions on the [AnyPath](anypath.md) data type.</span></span>

</dd> <dt>

<span data-ttu-id="072f9-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Profondeur</span><span class="sxs-lookup"><span data-stu-id="072f9-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Depth</span></span>
</dt> <dd>

<span data-ttu-id="072f9-140">Profondeur en dessous du chemin d’accès que le programme d’installation recherche pour le fichier ou le répertoire spécifié dans la \_ colonne signature.</span><span class="sxs-lookup"><span data-stu-id="072f9-140">The depth below the path that the installer searches for the file or directory specified in the Signature\_ column.</span></span> <span data-ttu-id="072f9-141">La valeur utilisée dans le champ profondeur est basée sur zéro.</span><span class="sxs-lookup"><span data-stu-id="072f9-141">The value used in the Depth field is based on zero.</span></span> <span data-ttu-id="072f9-142">Par exemple, si le champ path est c:/Program Files/bin, la colonne Depth doit avoir la valeur 0 ou une valeur supérieure pour détecter un fichier situé dans le dossier bin.</span><span class="sxs-lookup"><span data-stu-id="072f9-142">For example, if the Path field is c:/Program Files/bin, the Depth column must be set to 0 or greater, to detect a file located inside the folder bin.</span></span> <span data-ttu-id="072f9-143">Si le champ profondeur est vide, la profondeur est supposée être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="072f9-143">If the Depth field is empty, the depth is assumed to be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="072f9-144">Notes</span><span class="sxs-lookup"><span data-stu-id="072f9-144">Remarks</span></span>

<span data-ttu-id="072f9-145">Cette table est utilisée avec la [table AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="072f9-145">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="072f9-146">Les colonnes de cette table ne sont généralement pas localisées.</span><span class="sxs-lookup"><span data-stu-id="072f9-146">This table's columns are generally not localized.</span></span> <span data-ttu-id="072f9-147">Si un auteur décide de rechercher des produits dans plusieurs langues, il doit y avoir une entrée distincte incluse dans le tableau pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="072f9-147">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="072f9-148">Consultez [recherche d’applications, de fichiers, d’entrées de registre ou d’entrées de fichier. ini existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="072f9-148">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="072f9-149">Validation</span><span class="sxs-lookup"><span data-stu-id="072f9-149">Validation</span></span>

<dl>

[<span data-ttu-id="072f9-150">ICE03</span><span class="sxs-lookup"><span data-stu-id="072f9-150">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="072f9-151">ICE06</span><span class="sxs-lookup"><span data-stu-id="072f9-151">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="072f9-152">ICE46</span><span class="sxs-lookup"><span data-stu-id="072f9-152">ICE46</span></span>](ice46.md)  
</dl>

 

 



