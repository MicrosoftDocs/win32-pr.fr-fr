---
title: Objets modèle de nuanceur 5,1
description: Les objets suivants ont été ajoutés au nuanceur modèle 5,1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616afd8e4036988b6f91cb09cddf0db26c1dd480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315575"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="cebed-103">Objets modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="cebed-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="cebed-104">Les objets suivants ont été ajoutés au nuanceur modèle 5,1.</span><span class="sxs-lookup"><span data-stu-id="cebed-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="cebed-105">Pour les [vues](/windows/desktop/direct3d11/rasterizer-order-views) de l’ordre du rastériseur (disponible dans D3D 11.3 et D3D12), les objets suivants sont nouveaux et sont uniquement autorisés dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="cebed-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="cebed-106">Notez que les méthodes qu’ils prennent en charge sont identiques aux objets UAV correspondants.</span><span class="sxs-lookup"><span data-stu-id="cebed-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="cebed-107">Objet rastériseur</span><span class="sxs-lookup"><span data-stu-id="cebed-107">Rasterizer Object</span></span>                  | <span data-ttu-id="cebed-108">Objet UAV</span><span class="sxs-lookup"><span data-stu-id="cebed-108">UAV Object</span></span>                                                    |
| <span data-ttu-id="cebed-109">RasterizerOrderedBuffer</span><span class="sxs-lookup"><span data-stu-id="cebed-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="cebed-110">**RWBuffer**</span><span class="sxs-lookup"><span data-stu-id="cebed-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="cebed-111">RasterizerOrderedByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="cebed-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="cebed-112">**RWByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="cebed-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="cebed-113">RasterizerOrderedStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="cebed-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="cebed-114">**RWStructuredBuffer**</span><span class="sxs-lookup"><span data-stu-id="cebed-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="cebed-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="cebed-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="cebed-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="cebed-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="cebed-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="cebed-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="cebed-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="cebed-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="cebed-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="cebed-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="cebed-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="cebed-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="cebed-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="cebed-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="cebed-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="cebed-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="cebed-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="cebed-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="cebed-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="cebed-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="cebed-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cebed-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cebed-126">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="cebed-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="cebed-127">Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="cebed-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 