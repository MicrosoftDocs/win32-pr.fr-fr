---
description: La table SFPCatalog contient les catalogues utilisés par Windows Me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Table SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe887644faf6cf0a5cda626bbf757e9f448ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201696"
---
# <a name="sfpcatalog-table"></a><span data-ttu-id="686e9-103">Table SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="686e9-103">SFPCatalog Table</span></span>

<span data-ttu-id="686e9-104">La table SFPCatalog contient les catalogues utilisés par Windows Me.</span><span class="sxs-lookup"><span data-stu-id="686e9-104">The SFPCatalog table contains the catalogs used by Windows Me.</span></span>

<span data-ttu-id="686e9-105">La table SFPCatalog contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="686e9-105">The SFPCatalog table has the following columns.</span></span>



| <span data-ttu-id="686e9-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="686e9-106">Column</span></span>     | <span data-ttu-id="686e9-107">Type</span><span class="sxs-lookup"><span data-stu-id="686e9-107">Type</span></span>                       | <span data-ttu-id="686e9-108">Clé</span><span class="sxs-lookup"><span data-stu-id="686e9-108">Key</span></span> | <span data-ttu-id="686e9-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="686e9-109">Nullable</span></span> |
|------------|----------------------------|-----|----------|
| <span data-ttu-id="686e9-110">SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="686e9-110">SFPCatalog</span></span> | [<span data-ttu-id="686e9-111">Nom du fichier</span><span class="sxs-lookup"><span data-stu-id="686e9-111">Filename</span></span>](filename.md)   | <span data-ttu-id="686e9-112">O</span><span class="sxs-lookup"><span data-stu-id="686e9-112">Y</span></span>   | <span data-ttu-id="686e9-113">N</span><span class="sxs-lookup"><span data-stu-id="686e9-113">N</span></span>        |
| <span data-ttu-id="686e9-114">Catalogue</span><span class="sxs-lookup"><span data-stu-id="686e9-114">Catalog</span></span>    | [<span data-ttu-id="686e9-115">Binaire</span><span class="sxs-lookup"><span data-stu-id="686e9-115">Binary</span></span>](binary.md)       | <span data-ttu-id="686e9-116">N</span><span class="sxs-lookup"><span data-stu-id="686e9-116">N</span></span>   | <span data-ttu-id="686e9-117">N</span><span class="sxs-lookup"><span data-stu-id="686e9-117">N</span></span>        |
| <span data-ttu-id="686e9-118">Dépendance</span><span class="sxs-lookup"><span data-stu-id="686e9-118">Dependency</span></span> | [<span data-ttu-id="686e9-119">Correct</span><span class="sxs-lookup"><span data-stu-id="686e9-119">Formatted</span></span>](formatted.md) | <span data-ttu-id="686e9-120">N</span><span class="sxs-lookup"><span data-stu-id="686e9-120">N</span></span>   | <span data-ttu-id="686e9-121">O</span><span class="sxs-lookup"><span data-stu-id="686e9-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="686e9-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="686e9-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="686e9-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span><span class="sxs-lookup"><span data-stu-id="686e9-123"><span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog</span></span>
</dt> <dd>

<span data-ttu-id="686e9-124">Nom de fichier abrégé du catalogue.</span><span class="sxs-lookup"><span data-stu-id="686e9-124">The short file name for the catalog.</span></span> <span data-ttu-id="686e9-125">Étant donné que les catalogues n’ont pas de version, le catalogue spécifié dans cette colonne peut remplacer un catalogue qui porte le même nom et qui est déjà installé sur le système local.</span><span class="sxs-lookup"><span data-stu-id="686e9-125">Because catalogs have no version, the catalog specified in this column can overwrite a catalog that has the same name and is already installed on the local system.</span></span> <span data-ttu-id="686e9-126">Consultez la rubrique contrôle de version des fichiers, mais [aucun fichier n’a une version](neither-file-has-a-version.md).</span><span class="sxs-lookup"><span data-stu-id="686e9-126">See the file versioning topic [Neither File Has a Version](neither-file-has-a-version.md).</span></span>

</dd> <dt>

<span data-ttu-id="686e9-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalogue</span><span class="sxs-lookup"><span data-stu-id="686e9-127"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span>
</dt> <dd>

<span data-ttu-id="686e9-128">Données binaires du catalogue.</span><span class="sxs-lookup"><span data-stu-id="686e9-128">Binary data for the catalog.</span></span>

</dd> <dt>

<span data-ttu-id="686e9-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dépendance</span><span class="sxs-lookup"><span data-stu-id="686e9-129"><span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependency</span></span>
</dt> <dd>

<span data-ttu-id="686e9-130">Le catalogue spécifié dans ce champ est le parent du catalogue dépendant spécifié dans le champ SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="686e9-130">The catalog specified in this field is the parent of the dependent catalog specified in the SFPCatalog field.</span></span> <span data-ttu-id="686e9-131">Entrez le nom de fichier abrégé du catalogue parent dans le champ dépendance.</span><span class="sxs-lookup"><span data-stu-id="686e9-131">Enter the short file name of the parent catalog into the Dependency field.</span></span> <span data-ttu-id="686e9-132">Ce champ est une clé de retour dans la colonne SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="686e9-132">This field is a key back into the SFPCatalog column.</span></span> <span data-ttu-id="686e9-133">La correspondance de dépendance est sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="686e9-133">The dependency match is case sensitive.</span></span>

<span data-ttu-id="686e9-134">Si le champ de dépendance fait référence à un autre enregistrement dans cette table SFPCatalog, le catalogue parent est installé avant le catalogue dépendant.</span><span class="sxs-lookup"><span data-stu-id="686e9-134">If the Dependency field references another record in this SFPCatalog table, the parent catalog is installed before the dependent catalog.</span></span>

<span data-ttu-id="686e9-135">Si le champ de dépendance fait référence à un catalogue parent qui n’est pas présent dans le champ SFPCatalog de cette table, et si le catalogue parent n’est pas déjà installé, l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="686e9-135">If the Dependency field references a parent catalog that is not present in the SFPCatalog field of this table, and if the parent catalog is not already installed, the installation fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="686e9-136">Notes</span><span class="sxs-lookup"><span data-stu-id="686e9-136">Remarks</span></span>

<span data-ttu-id="686e9-137">L' [action InstallSFPCatalogFile](installsfpcatalogfile-action.md) interroge la table de [composants](component-table.md), la [table de fichiers](file-table.md), la [table FileSFPCatalog](filesfpcatalog-table.md) et la table SFPCatalog.</span><span class="sxs-lookup"><span data-stu-id="686e9-137">The [InstallSFPCatalogFile action](installsfpcatalogfile-action.md) queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and SFPCatalog table.</span></span>

## <a name="validation"></a><span data-ttu-id="686e9-138">Validation</span><span class="sxs-lookup"><span data-stu-id="686e9-138">Validation</span></span>

<dl>

[<span data-ttu-id="686e9-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="686e9-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="686e9-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="686e9-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="686e9-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="686e9-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="686e9-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="686e9-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="686e9-143">ICE46</span><span class="sxs-lookup"><span data-stu-id="686e9-143">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="686e9-144">ICE66</span><span class="sxs-lookup"><span data-stu-id="686e9-144">ICE66</span></span>](ice66.md)  
</dl>

 

 



