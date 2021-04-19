---
title: Application d’une mise à jour à un catalogue
description: Application d’une mise à jour à un catalogue
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player Online stores, application de mises à jour aux catalogues
- magasins en ligne, appliquer des mises à jour à des catalogues
- tapez 1 magasins en ligne, en appliquant des mises à jour aux catalogues
- Windows Media Player Online stores, mise à jour des catalogues
- magasins en ligne, mise à jour des catalogues
- types 1 magasins en ligne, mise à jour des catalogues
- Windows Media Player Online stores, mises à jour de catalogue
- magasins en ligne, mises à jour de catalogue
- types 1 magasins en ligne, mises à jour de catalogue
- mises à jour du catalogue
- mise à jour des catalogues
- application de mises à jour aux catalogues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510035"
---
# <a name="applying-an-update-to-a-catalog"></a><span data-ttu-id="012d0-115">Application d’une mise à jour à un catalogue</span><span class="sxs-lookup"><span data-stu-id="012d0-115">Applying an Update To a Catalog</span></span>

> [!Note]  
> <span data-ttu-id="012d0-116">Cela n’est généralement pas fait, sauf à des fins de diagnostic, par exemple pour vous aider à vérifier qu’un fichier de différences est valide.</span><span class="sxs-lookup"><span data-stu-id="012d0-116">This is not normally done except for diagnostic purposes—for instance, to help verify that a difference file is valid.</span></span> <span data-ttu-id="012d0-117">Le catalogue généré de cette façon n’est pas au format compressé et ne doit pas être transmis au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="012d0-117">The catalog generated in this way is not in compressed form and should not be passed to Windows Media Player.</span></span>

 

<span data-ttu-id="012d0-118">Un nouveau fichier de catalogue peut être créé à l’aide de la syntaxe ci-dessous, où *inputcatalog* est l’emplacement du catalogue d’origine et *inputdiff* est l’emplacement du fichier de différences à appliquer.</span><span class="sxs-lookup"><span data-stu-id="012d0-118">A new catalog file can be created by using the syntax below, where *inputcatalog* is the location of the original catalog, and *inputdiff* is the location of the difference file to apply.</span></span> <span data-ttu-id="012d0-119">Les fichiers de catalogue doivent être au format non compressé.</span><span class="sxs-lookup"><span data-stu-id="012d0-119">The catalog files must be in uncompressed form.</span></span>


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



<span data-ttu-id="012d0-120">Par exemple, le code suivant crée un nouveau catalogue à partir de C : \\ Catalog210 \\ Catalog. WMDB et de c : \\ Catalog210 \\ Catalog. diff.</span><span class="sxs-lookup"><span data-stu-id="012d0-120">For example, the following creates a new catalog from C:\\Catalog210\\catalog.wmdb and C:\\Catalog210\\catalog.diff.</span></span>


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



<span data-ttu-id="012d0-121">Si la compilation réussit, catcomp.exe crée les fichiers de sortie suivants.</span><span class="sxs-lookup"><span data-stu-id="012d0-121">If compilation is successful, catcomp.exe creates the follow output files.</span></span>



| <span data-ttu-id="012d0-122">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="012d0-122">File name</span></span>        | <span data-ttu-id="012d0-123">Description</span><span class="sxs-lookup"><span data-stu-id="012d0-123">Description</span></span>       |
|------------------|-------------------|
| <span data-ttu-id="012d0-124">Catalog. WMDB. New</span><span class="sxs-lookup"><span data-stu-id="012d0-124">catalog.wmdb.new</span></span> | <span data-ttu-id="012d0-125">Nouveau fichier de catalogue.</span><span class="sxs-lookup"><span data-stu-id="012d0-125">New catalog file.</span></span> |



 

 

 




