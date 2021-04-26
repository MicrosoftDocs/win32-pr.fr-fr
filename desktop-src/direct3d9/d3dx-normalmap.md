---
description: Constantes de génération de mappages normales.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f76b6afe6eb68e8ddbc3ca28085861a518effc
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996326"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="50849-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="50849-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="50849-104">Constantes de génération de mappages normales.</span><span class="sxs-lookup"><span data-stu-id="50849-104">Normal maps generation constants.</span></span>



| <span data-ttu-id="50849-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="50849-105">\#define</span></span>                            | <span data-ttu-id="50849-106">Description</span><span class="sxs-lookup"><span data-stu-id="50849-106">Description</span></span>                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50849-107">\_NORMALMAP \_ en miroir \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="50849-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="50849-108">Indique que les pixels du bord de la texture sur l’axe des u doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="50849-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="50849-109">\_Miroir D3DX \_ NORMALMAP \_ V</span><span class="sxs-lookup"><span data-stu-id="50849-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="50849-110">Indique que les pixels du bord de la texture sur l’axe v doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="50849-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="50849-111">\_Miroir D3DX NORMALMAP \_</span><span class="sxs-lookup"><span data-stu-id="50849-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="50849-112">Identique à la spécification de la mise en miroir de D3DX \_ NORMALMAP \_ MIRROR \_ U \| D3DX \_ NORMALMAP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="50849-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="50849-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="50849-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="50849-114">Inverse la direction de chaque normal.</span><span class="sxs-lookup"><span data-stu-id="50849-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="50849-115">D3DX \_ NORMALMAP \_ calcul \_ occlusion</span><span class="sxs-lookup"><span data-stu-id="50849-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="50849-116">Calcule le terme d’occlusion par pixel et l’encode en alpha.</span><span class="sxs-lookup"><span data-stu-id="50849-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="50849-117">Une valeur alpha de 1 signifie que le pixel n’est pas masqué, et une valeur alpha de 0 signifie que le pixel est complètement masqué.</span><span class="sxs-lookup"><span data-stu-id="50849-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="50849-118">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="50849-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="50849-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="50849-119">Header</span></span>                   | <span data-ttu-id="50849-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="50849-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="50849-121">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="50849-121">Minimum operating system</span></span> | <span data-ttu-id="50849-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="50849-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="50849-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50849-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50849-124">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="50849-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="50849-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="50849-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



