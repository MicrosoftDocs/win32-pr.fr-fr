---
description: Constantes de génération de mappages normales.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37985456e81b20af9b3e4396d10045d5e58c9b7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512856"
---
# <a name="d3dx_normalmap"></a><span data-ttu-id="fd79e-103">D3DX \_ NORMALMAP</span><span class="sxs-lookup"><span data-stu-id="fd79e-103">D3DX\_NORMALMAP</span></span>

<span data-ttu-id="fd79e-104">Constantes de génération de mappages normales.</span><span class="sxs-lookup"><span data-stu-id="fd79e-104">Normal maps generation constants.</span></span>



|                                     |                                                                                                                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd79e-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="fd79e-105">\#define</span></span>                            | <span data-ttu-id="fd79e-106">Description</span><span class="sxs-lookup"><span data-stu-id="fd79e-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="fd79e-107">\_NORMALMAP \_ en miroir \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="fd79e-107">D3DX\_NORMALMAP\_MIRROR\_U</span></span>          | <span data-ttu-id="fd79e-108">Indique que les pixels du bord de la texture sur l’axe des u doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="fd79e-108">Indicates that pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="fd79e-109">\_Miroir D3DX \_ NORMALMAP \_ V</span><span class="sxs-lookup"><span data-stu-id="fd79e-109">D3DX\_NORMALMAP\_MIRROR\_V</span></span>          | <span data-ttu-id="fd79e-110">Indique que les pixels du bord de la texture sur l’axe v doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="fd79e-110">Indicates that pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                   |
| <span data-ttu-id="fd79e-111">\_Miroir D3DX NORMALMAP \_</span><span class="sxs-lookup"><span data-stu-id="fd79e-111">D3DX\_NORMALMAP\_MIRROR</span></span>             | <span data-ttu-id="fd79e-112">Identique à la spécification de la mise en miroir de D3DX \_ NORMALMAP \_ MIRROR \_ U \| D3DX \_ NORMALMAP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="fd79e-112">Same as specifying D3DX\_NORMALMAP\_MIRROR\_U \| D3DX\_NORMALMAP\_MIRROR\_V.</span></span>                                                                                                                       |
| <span data-ttu-id="fd79e-113">D3DX \_ NORMALMAP \_ INVERTSIGN</span><span class="sxs-lookup"><span data-stu-id="fd79e-113">D3DX\_NORMALMAP\_INVERTSIGN</span></span>         | <span data-ttu-id="fd79e-114">Inverse la direction de chaque normal.</span><span class="sxs-lookup"><span data-stu-id="fd79e-114">Inverts the direction of each normal.</span></span>                                                                                                                                                              |
| <span data-ttu-id="fd79e-115">D3DX \_ NORMALMAP \_ calcul \_ occlusion</span><span class="sxs-lookup"><span data-stu-id="fd79e-115">D3DX\_NORMALMAP\_COMPUTE\_OCCLUSION</span></span> | <span data-ttu-id="fd79e-116">Calcule le terme d’occlusion par pixel et l’encode en alpha.</span><span class="sxs-lookup"><span data-stu-id="fd79e-116">Computes the per-pixel occlusion term and encodes it into the alpha.</span></span> <span data-ttu-id="fd79e-117">Une valeur alpha de 1 signifie que le pixel n’est pas masqué, et une valeur alpha de 0 signifie que le pixel est complètement masqué.</span><span class="sxs-lookup"><span data-stu-id="fd79e-117">An alpha of 1 means that the pixel is not obscured in any way, and an alpha of 0 means that the pixel is completely obscured.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="fd79e-118">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="fd79e-118">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="fd79e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd79e-119">Header</span></span>                   | <span data-ttu-id="fd79e-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="fd79e-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="fd79e-121">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="fd79e-121">Minimum operating system</span></span> | <span data-ttu-id="fd79e-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="fd79e-122">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fd79e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd79e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd79e-124">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="fd79e-124">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[<span data-ttu-id="fd79e-125">**D3DXComputeNormalMap**</span><span class="sxs-lookup"><span data-stu-id="fd79e-125">**D3DXComputeNormalMap**</span></span>](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



