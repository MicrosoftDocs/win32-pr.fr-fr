---
title: Supprimer des attributs de métadonnées
description: Supprimer des attributs de métadonnées
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media Format SDK, supprimer des attributs de métadonnées
- ASF (Advanced Systems Format), supprimer les attributs de métadonnées
- ASF (format des systèmes avancés), supprimer les attributs de métadonnées
- métadonnées, supprimer des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104381687"
---
# <a name="removing-metadata-attributes"></a><span data-ttu-id="bdcae-107">Supprimer des attributs de métadonnées</span><span class="sxs-lookup"><span data-stu-id="bdcae-107">Removing Metadata Attributes</span></span>

<span data-ttu-id="bdcae-108">Vous pouvez supprimer un attribut de métadonnées en passant son numéro d’index et de flux à la méthode [**IWMHeaderInfo3 ::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) .</span><span class="sxs-lookup"><span data-stu-id="bdcae-108">You can remove a metadata attribute by passing its index and stream number to the [**IWMHeaderInfo3::DeleteAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) method.</span></span> <span data-ttu-id="bdcae-109">L’ordre dans lequel les attributs restants sont indexés après la suppression d’un attribut ne change pas ; les valeurs d’index de tous les attributs restants ayant une valeur d’index supérieure à celle supprimée sont réduites d’une unité.</span><span class="sxs-lookup"><span data-stu-id="bdcae-109">The order in which the remaining attributes are indexed after removing an attribute does not change; all remaining attributes that originally had an index value greater than the one removed have their index values reduced by one.</span></span> <span data-ttu-id="bdcae-110">Lors de la suppression de plusieurs attributs, faites-le dans l’ordre décroissant par index pour éviter d’avoir à calculer l’ajustement dans l’indexation.</span><span class="sxs-lookup"><span data-stu-id="bdcae-110">When removing multiple attributes, do so in descending order by index to avoid having to calculate the adjustment in indexing.</span></span>

<span data-ttu-id="bdcae-111">Pour faciliter la suppression des valeurs, la méthode [**IWMHeaderInfo3 :: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) retourne les valeurs d’index dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="bdcae-111">For convenience in removing values, the [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) method returns the index values in descending order.</span></span>

> [!Note]  
> <span data-ttu-id="bdcae-112">Les valeurs d’index obtenues à l’aide des méthodes de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) ne sont pas compatibles avec les valeurs d’index obtenues à l’aide des méthodes de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="bdcae-112">Index values obtained by using the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) are not compatible with index values obtained by using the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span> <span data-ttu-id="bdcae-113">Si vous utilisez les méthodes d’une interface pour modifier les attributs d’un fichier, vous devez supposer que toutes les valeurs d’index précédemment récupérées à partir de l’autre interface ne sont plus valides et doivent être retirées.</span><span class="sxs-lookup"><span data-stu-id="bdcae-113">If you use the methods of one interface to change attributes in a file, you should assume that any index values previously retrieved from the other interface are no longer valid and must be obtained again.</span></span> <span data-ttu-id="bdcae-114">Vous devez éviter d’utiliser les méthodes de **IWMHeaderInfo** si possible.</span><span class="sxs-lookup"><span data-stu-id="bdcae-114">You should avoid using the methods of **IWMHeaderInfo** if possible.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bdcae-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdcae-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdcae-116">**Utilisation des métadonnées**</span><span class="sxs-lookup"><span data-stu-id="bdcae-116">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




