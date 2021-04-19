---
description: Non pris en charge. Utilisé en interne par DirectX.
ms.assetid: 8a07357f-d4e8-4104-9d21-51c3e8b8d6d2
title: PMInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4217e2a044e39a7125705f1d3863b9737120e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106543642"
---
# <a name="pminfo"></a><span data-ttu-id="d48c2-104">PMInfo</span><span class="sxs-lookup"><span data-stu-id="d48c2-104">PMInfo</span></span>

<span data-ttu-id="d48c2-105">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d48c2-105">Not supported.</span></span> <span data-ttu-id="d48c2-106">Utilisé en interne par DirectX.</span><span class="sxs-lookup"><span data-stu-id="d48c2-106">Used internally by DirectX.</span></span>

``` syntax
template PMInfo 
{ 
    < B6C3E656-EC8B-4b92-9B62-681659522947 > 
    DWORD nAttributes; 
    array PMAttributeRange attributeRanges[nAttributes]; 
    DWORD nMaxValence; 
    DWORD nMinLogicalVertices; 
    DWORD nMaxLogicalVertices; 
    DWORD nVSplits; 
    array PMVSplitRecord splitRecords[nVSplits]; 
    DWORD nAttributeMispredicts; 
    array DWORD attributeMispredicts[nAttributeMispredicts]; 
}
```

## <a name="see-also"></a><span data-ttu-id="d48c2-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d48c2-107">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48c2-108">Modèles</span><span class="sxs-lookup"><span data-stu-id="d48c2-108">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



