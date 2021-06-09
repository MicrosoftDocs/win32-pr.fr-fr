---
title: Objets modèle de nuanceur 5,1
description: Les objets suivants ont été ajoutés au nuanceur modèle 5,1.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376ce272e789501e21f5866be37f56daf31bc829
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825716"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="6c3ca-103">Objets modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="6c3ca-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="6c3ca-104">Les objets suivants ont été ajoutés au nuanceur modèle 5,1.</span><span class="sxs-lookup"><span data-stu-id="6c3ca-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="6c3ca-105">Pour les [vues](/windows/desktop/direct3d11/rasterizer-order-views) de l’ordre du rastériseur (disponible dans D3D 11.3 et D3D12), les objets suivants sont nouveaux et sont uniquement autorisés dans le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="6c3ca-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="6c3ca-106">Notez que les méthodes qu’ils prennent en charge sont identiques aux objets UAV correspondants.</span><span class="sxs-lookup"><span data-stu-id="6c3ca-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



| <span data-ttu-id="6c3ca-107">Objet rastériseur</span><span class="sxs-lookup"><span data-stu-id="6c3ca-107">Rasterizer object</span></span>                                   | <span data-ttu-id="6c3ca-108">Objet UAV</span><span class="sxs-lookup"><span data-stu-id="6c3ca-108">UAV object</span></span>                                                              |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6c3ca-109">RasterizerOrderedBuffer</span><span class="sxs-lookup"><span data-stu-id="6c3ca-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="6c3ca-110">**RWBuffer**</span><span class="sxs-lookup"><span data-stu-id="6c3ca-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="6c3ca-111">RasterizerOrderedByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="6c3ca-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="6c3ca-112">**RWByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="6c3ca-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="6c3ca-113">RasterizerOrderedStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="6c3ca-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="6c3ca-114">**RWStructuredBuffer**</span><span class="sxs-lookup"><span data-stu-id="6c3ca-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="6c3ca-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="6c3ca-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="6c3ca-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="6c3ca-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="6c3ca-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="6c3ca-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="6c3ca-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="6c3ca-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="6c3ca-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="6c3ca-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="6c3ca-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="6c3ca-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="6c3ca-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="6c3ca-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="6c3ca-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="6c3ca-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="6c3ca-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="6c3ca-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="6c3ca-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="6c3ca-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="6c3ca-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c3ca-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c3ca-126">Modèle de nuanceur 5,1</span><span class="sxs-lookup"><span data-stu-id="6c3ca-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="6c3ca-127">Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6c3ca-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
