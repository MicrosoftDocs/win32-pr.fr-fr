---
description: Définit un correctif de \# contrôle p&233 ;. Le tableau définit les points de contrôle pour le correctif.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Correctif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845738"
---
# <a name="patch"></a><span data-ttu-id="f002a-104">Correctif</span><span class="sxs-lookup"><span data-stu-id="f002a-104">Patch</span></span>

<span data-ttu-id="f002a-105">Définit un correctif de contrôle de Bézier.</span><span class="sxs-lookup"><span data-stu-id="f002a-105">Defines a Bézier control patch.</span></span> <span data-ttu-id="f002a-106">Le tableau définit les points de contrôle pour le correctif.</span><span class="sxs-lookup"><span data-stu-id="f002a-106">The array defines the control points for the patch.</span></span>

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

<span data-ttu-id="f002a-107">Où :</span><span class="sxs-lookup"><span data-stu-id="f002a-107">Where:</span></span>

-   <span data-ttu-id="f002a-108">nControlIndices : nombre d’index du point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f002a-108">nControlIndices - Number of control point indices.</span></span>
-   <span data-ttu-id="f002a-109">Tableau DWORD controlIndices \[ nControlIndices \] -tableau d’index du point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f002a-109">array DWORD controlIndices\[nControlIndices\] - Array of control point indices.</span></span>

<span data-ttu-id="f002a-110">Le type de correctif est défini par le nombre de points de contrôle, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f002a-110">The type of patch is defined by the number of control points, as shown in the following table.</span></span>



| <span data-ttu-id="f002a-111">Nombre de points de contrôle</span><span class="sxs-lookup"><span data-stu-id="f002a-111">Number of control points</span></span> | <span data-ttu-id="f002a-112">Type</span><span class="sxs-lookup"><span data-stu-id="f002a-112">Type</span></span>                              |
|--------------------------|-----------------------------------|
| <span data-ttu-id="f002a-113">10</span><span class="sxs-lookup"><span data-stu-id="f002a-113">10</span></span>                       | <span data-ttu-id="f002a-114">Correctif triangulaire de la Bézier cubique</span><span class="sxs-lookup"><span data-stu-id="f002a-114">Cubic Bézier triangular patch</span></span>     |
| <span data-ttu-id="f002a-115">15</span><span class="sxs-lookup"><span data-stu-id="f002a-115">15</span></span>                       | <span data-ttu-id="f002a-116">Correctif triangulaire de Bézier quart</span><span class="sxs-lookup"><span data-stu-id="f002a-116">Quartic Bézier triangular patch</span></span>   |
| <span data-ttu-id="f002a-117">16</span><span class="sxs-lookup"><span data-stu-id="f002a-117">16</span></span>                       | <span data-ttu-id="f002a-118">Correctif du rectangle à quatre rectangles de Bézier cubique</span><span class="sxs-lookup"><span data-stu-id="f002a-118">Cubic Bézier quad rectangle patch</span></span> |



 

<span data-ttu-id="f002a-119">L’ordre des points de contrôle est indiqué dans un motif en spirale, comme indiqué dans les diagrammes suivants pour les correctifs triangulaires et rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="f002a-119">The order of the control points are given in a spiral pattern, as shown in the following diagrams for triangular and rectangular patches.</span></span>

<span data-ttu-id="f002a-120">Les correctifs triangulaires utilisent le modèle suivant.</span><span class="sxs-lookup"><span data-stu-id="f002a-120">Triangular patches use the following pattern.</span></span>

![diagramme du modèle pour les correctifs triangulaires](images/tripatch.png)

<span data-ttu-id="f002a-122">Les correctifs rectangulaires utilisent le modèle suivant.</span><span class="sxs-lookup"><span data-stu-id="f002a-122">Rectangular patches use the following pattern.</span></span>

![diagramme du modèle pour les correctifs rectangulaires](images/quadpatch.png)

## <a name="see-also"></a><span data-ttu-id="f002a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f002a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f002a-125">Modèles</span><span class="sxs-lookup"><span data-stu-id="f002a-125">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



