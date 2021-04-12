---
description: Décrit une déclaration de vertex.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: DeclData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a26d667f853db3044db3155c55eb4a6d941c6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481113"
---
# <a name="decldata"></a><span data-ttu-id="d075a-103">DeclData</span><span class="sxs-lookup"><span data-stu-id="d075a-103">DeclData</span></span>

<span data-ttu-id="d075a-104">Décrit une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="d075a-104">Describes a vertex declaration.</span></span>

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="d075a-105">Où :</span><span class="sxs-lookup"><span data-stu-id="d075a-105">Where:</span></span>

-   <span data-ttu-id="d075a-106">nElements : nombre d’éléments de déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="d075a-106">nElements - Number of vertex declaration elements.</span></span>
-   <span data-ttu-id="d075a-107">Éléments \[ nElements \] -tableau d’éléments de déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="d075a-107">Elements\[nElements\] - Array of vertex declaration elements.</span></span>
-   <span data-ttu-id="d075a-108">nDWords : nombre de DWORDs.</span><span class="sxs-lookup"><span data-stu-id="d075a-108">nDWords - Number of DWORDS.</span></span>
-   <span data-ttu-id="d075a-109">Data \[ nDWords \] -tableau de DWORDS contenant les données de chaque élément vertex.</span><span class="sxs-lookup"><span data-stu-id="d075a-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="d075a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d075a-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d075a-111">Modèles</span><span class="sxs-lookup"><span data-stu-id="d075a-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



