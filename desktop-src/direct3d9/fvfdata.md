---
description: Spécifie les données de maillage moins les données de position.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: FVFData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52af6096357c4855d2dc34442c6cd4814b6713b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108738"
---
# <a name="fvfdata"></a><span data-ttu-id="34220-103">FVFData</span><span class="sxs-lookup"><span data-stu-id="34220-103">FVFData</span></span>

<span data-ttu-id="34220-104">Spécifie les données de maillage moins les données de position.</span><span class="sxs-lookup"><span data-stu-id="34220-104">Specifies the mesh data minus the position data.</span></span>

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="34220-105">Où :</span><span class="sxs-lookup"><span data-stu-id="34220-105">Where:</span></span>

-   <span data-ttu-id="34220-106">dwFVF : code de la Commission.</span><span class="sxs-lookup"><span data-stu-id="34220-106">dwFVF - A FVF code.</span></span>
-   <span data-ttu-id="34220-107">nDWords-données binaires.</span><span class="sxs-lookup"><span data-stu-id="34220-107">nDWords - Binary data.</span></span> <span data-ttu-id="34220-108">Nombre de DWORDs.</span><span class="sxs-lookup"><span data-stu-id="34220-108">The number of DWORDS.</span></span>
-   <span data-ttu-id="34220-109">Data \[ nDWords \] -tableau de DWORDS contenant les données de chaque élément vertex.</span><span class="sxs-lookup"><span data-stu-id="34220-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="34220-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34220-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34220-111">Modèles</span><span class="sxs-lookup"><span data-stu-id="34220-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



