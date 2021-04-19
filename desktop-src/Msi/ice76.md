---
description: ICE76 vérifie l’utilisation du catalogue SFP (WFP) au sein des packages Windows Installer pour Windows Me. Cette ICE vérifie également qu’aucun fichier de la table BindImage ne fait référence aux catalogues SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518959"
---
# <a name="ice76"></a><span data-ttu-id="2733a-104">ICE76</span><span class="sxs-lookup"><span data-stu-id="2733a-104">ICE76</span></span>

<span data-ttu-id="2733a-105">ICE76 vérifie l’utilisation du catalogue SFP (WFP) au sein des packages Windows Installer pour Windows Me.</span><span class="sxs-lookup"><span data-stu-id="2733a-105">ICE76 verifies the use of the SFP (WFP) catalog within Windows Installer packages for Windows Me.</span></span> <span data-ttu-id="2733a-106">Cette ICE vérifie également qu’aucun fichier de la [table](bindimage-table.md) BindImage ne fait référence aux catalogues SFP.</span><span class="sxs-lookup"><span data-stu-id="2733a-106">This ICE also verifies that no files in the BindImage [table](bindimage-table.md) reference SFP catalogs.</span></span>

<span data-ttu-id="2733a-107">La protection des fichiers Windows requiert une correspondance exacte entre le fichier et la signature incorporée dans le fichier catalogue.</span><span class="sxs-lookup"><span data-stu-id="2733a-107">Windows File Protection requires an exact match between the file and the signature embedded in the catalog file.</span></span> <span data-ttu-id="2733a-108">Les fichiers qui font référence à un catalogue SFP ne doivent pas figurer dans la table BindImage, car l’effet de l' [action BindImage](bindimage-action.md) sur ces fichiers diffère entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="2733a-108">Files that reference a SFP catalog must not be listed in the BindImage table because the effect of the [BindImage action](bindimage-action.md) on these files differs between computers.</span></span> <span data-ttu-id="2733a-109">Les fichiers référencés par les catalogues SFP doivent se trouver dans des composants permanents ou installés localement.</span><span class="sxs-lookup"><span data-stu-id="2733a-109">Files referenced by SFP catalogs must be in components that are permanent or installed locally.</span></span>

## <a name="result"></a><span data-ttu-id="2733a-110">Résultats</span><span class="sxs-lookup"><span data-stu-id="2733a-110">Result</span></span>

<span data-ttu-id="2733a-111">ICE76 publie une erreur pour chaque fichier de la [table BindImage](bindimage-table.md) qui se trouve également dans la [table FileSFPCatalog](filesfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="2733a-111">ICE76 posts an error for each file in the [BindImage table](bindimage-table.md) that is also in the [FileSFPCatalog table](filesfpcatalog-table.md).</span></span>

<span data-ttu-id="2733a-112">ICE76 génère une erreur si un fichier de la table FileSFPCatalog appartient à un composant avec l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="2733a-112">ICE76 outputs an error if a file in the FileSFPCatalog table belongs to a component with any of the following true:</span></span>

-   <span data-ttu-id="2733a-113">**msidbComponentAttributesPermanent** n’est pas défini dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="2733a-113">**msidbComponentAttributesPermanent** is not set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="2733a-114">**msidbComponentAttributesSourceOnly** est défini dans la colonne attributs de la table des composants.</span><span class="sxs-lookup"><span data-stu-id="2733a-114">**msidbComponentAttributesSourceOnly** is set in the Attributes column of the Component table.</span></span>
-   <span data-ttu-id="2733a-115">**msidbAttributesOptional** est défini dans la colonne attributs de la table des composants.</span><span class="sxs-lookup"><span data-stu-id="2733a-115">**msidbAttributesOptional** is set in the Attributes column of the Component table.</span></span>

## <a name="example"></a><span data-ttu-id="2733a-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="2733a-116">Example</span></span>

<span data-ttu-id="2733a-117">ICE76 signale l’erreur suivante pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="2733a-117">ICE76 reports the following error for the example:</span></span>

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

<span data-ttu-id="2733a-118">[Table FileSFPCatalog](filesfpcatalog-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="2733a-118">[FileSFPCatalog Table](filesfpcatalog-table.md) (partial)</span></span>



| <span data-ttu-id="2733a-119">fichier\_</span><span class="sxs-lookup"><span data-stu-id="2733a-119">File\_</span></span> | <span data-ttu-id="2733a-120">SFPCatalog\_</span><span class="sxs-lookup"><span data-stu-id="2733a-120">SFPCatalog\_</span></span> |
|--------|--------------|
| <span data-ttu-id="2733a-121">Fichier1</span><span class="sxs-lookup"><span data-stu-id="2733a-121">File1</span></span>  | <span data-ttu-id="2733a-122">Catalog1.Cat</span><span class="sxs-lookup"><span data-stu-id="2733a-122">Catalog1.Cat</span></span> |



 

<span data-ttu-id="2733a-123">[Table BindImage](bindimage-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="2733a-123">[BindImage Table](bindimage-table.md) (partial)</span></span>



| <span data-ttu-id="2733a-124">fichier\_</span><span class="sxs-lookup"><span data-stu-id="2733a-124">File\_</span></span> |
|--------|
| <span data-ttu-id="2733a-125">Fichier1</span><span class="sxs-lookup"><span data-stu-id="2733a-125">File1</span></span>  |



 

<span data-ttu-id="2733a-126">Pour résoudre ce problème, n’entrez aucun fichier référençant les catalogues SFP dans la table BindImage.</span><span class="sxs-lookup"><span data-stu-id="2733a-126">To fix this do not enter any files that reference SFP catalogs into the BindImage table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2733a-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2733a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2733a-128">Table BindImage</span><span class="sxs-lookup"><span data-stu-id="2733a-128">BindImage Table</span></span>](bindimage-table.md)
</dt> <dt>

[<span data-ttu-id="2733a-129">Table des composants</span><span class="sxs-lookup"><span data-stu-id="2733a-129">Component Table</span></span>](component-table.md)
</dt> <dt>

[<span data-ttu-id="2733a-130">Table FileSFPCatalog</span><span class="sxs-lookup"><span data-stu-id="2733a-130">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
</dt> <dt>

[<span data-ttu-id="2733a-131">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="2733a-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



