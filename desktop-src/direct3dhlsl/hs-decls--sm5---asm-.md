---
title: hs_decls (SM5-ASM)
description: Démarrez la phase declarations dans un nuanceur de coque.
ms.assetid: 1C8552B1-F649-4B73-A365-D449A9121DAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e57207e35aab507a1404efaf90131a9648918ae7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101101"
---
# <a name="hs_decls-sm5---asm"></a><span data-ttu-id="b8462-103">HS \_ decls (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="b8462-103">hs\_decls (sm5 - asm)</span></span>

<span data-ttu-id="b8462-104">Démarrez la phase declarations dans un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="b8462-104">Start the declarations phase in a hull shader.</span></span>



| <span data-ttu-id="b8462-105">\_decls HS</span><span class="sxs-lookup"><span data-stu-id="b8462-105">hs\_decls</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="b8462-106">Notes</span><span class="sxs-lookup"><span data-stu-id="b8462-106">Remarks</span></span>

<span data-ttu-id="b8462-107">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="b8462-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b8462-108">Sommet</span><span class="sxs-lookup"><span data-stu-id="b8462-108">Vertex</span></span> | <span data-ttu-id="b8462-109">Forme</span><span class="sxs-lookup"><span data-stu-id="b8462-109">Hull</span></span> | <span data-ttu-id="b8462-110">Domain</span><span class="sxs-lookup"><span data-stu-id="b8462-110">Domain</span></span> | <span data-ttu-id="b8462-111">Géométrie</span><span class="sxs-lookup"><span data-stu-id="b8462-111">Geometry</span></span> | <span data-ttu-id="b8462-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="b8462-112">Pixel</span></span> | <span data-ttu-id="b8462-113">Compute</span><span class="sxs-lookup"><span data-stu-id="b8462-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="b8462-114">X</span><span class="sxs-lookup"><span data-stu-id="b8462-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b8462-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="b8462-115">Minimum Shader Model</span></span>

<span data-ttu-id="b8462-116">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="b8462-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="b8462-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="b8462-117">Shader Model</span></span>                                              | <span data-ttu-id="b8462-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="b8462-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b8462-119">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="b8462-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b8462-120">Oui</span><span class="sxs-lookup"><span data-stu-id="b8462-120">yes</span></span>       |
| [<span data-ttu-id="b8462-121">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="b8462-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b8462-122">non</span><span class="sxs-lookup"><span data-stu-id="b8462-122">no</span></span>        |
| [<span data-ttu-id="b8462-123">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="b8462-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b8462-124">non</span><span class="sxs-lookup"><span data-stu-id="b8462-124">no</span></span>        |
| [<span data-ttu-id="b8462-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8462-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b8462-126">non</span><span class="sxs-lookup"><span data-stu-id="b8462-126">no</span></span>        |
| [<span data-ttu-id="b8462-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8462-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b8462-128">non</span><span class="sxs-lookup"><span data-stu-id="b8462-128">no</span></span>        |
| [<span data-ttu-id="b8462-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8462-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b8462-130">non</span><span class="sxs-lookup"><span data-stu-id="b8462-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b8462-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8462-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8462-132">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b8462-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




