---
title: hs_fork_phase (SM5-ASM)
description: Démarrez la phase de fourche dans un nuanceur de coque.
ms.assetid: 13D6A06C-F001-45BE-8AB4-D7ACA73BF535
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9316cc92c1bf5683afa620927b3c6f38432c3c4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381211"
---
# <a name="hs_fork_phase-sm5---asm"></a><span data-ttu-id="05eb8-103">\_ \_ phase de fourche SH (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="05eb8-103">hs\_fork\_phase (sm5 - asm)</span></span>

<span data-ttu-id="05eb8-104">Démarrez la phase de fourche dans un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="05eb8-104">Start the fork phase in a hull shader.</span></span>



| <span data-ttu-id="05eb8-105">\_phase de fourche HS \_</span><span class="sxs-lookup"><span data-stu-id="05eb8-105">hs\_fork\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="05eb8-106">Notes</span><span class="sxs-lookup"><span data-stu-id="05eb8-106">Remarks</span></span>

<span data-ttu-id="05eb8-107">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="05eb8-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="05eb8-108">Sommet</span><span class="sxs-lookup"><span data-stu-id="05eb8-108">Vertex</span></span> | <span data-ttu-id="05eb8-109">Forme</span><span class="sxs-lookup"><span data-stu-id="05eb8-109">Hull</span></span> | <span data-ttu-id="05eb8-110">Domain</span><span class="sxs-lookup"><span data-stu-id="05eb8-110">Domain</span></span> | <span data-ttu-id="05eb8-111">Géométrie</span><span class="sxs-lookup"><span data-stu-id="05eb8-111">Geometry</span></span> | <span data-ttu-id="05eb8-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="05eb8-112">Pixel</span></span> | <span data-ttu-id="05eb8-113">Compute</span><span class="sxs-lookup"><span data-stu-id="05eb8-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="05eb8-114">X</span><span class="sxs-lookup"><span data-stu-id="05eb8-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="05eb8-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="05eb8-115">Minimum Shader Model</span></span>

<span data-ttu-id="05eb8-116">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="05eb8-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="05eb8-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="05eb8-117">Shader Model</span></span>                                              | <span data-ttu-id="05eb8-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="05eb8-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="05eb8-119">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="05eb8-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="05eb8-120">Oui</span><span class="sxs-lookup"><span data-stu-id="05eb8-120">yes</span></span>       |
| [<span data-ttu-id="05eb8-121">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="05eb8-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="05eb8-122">non</span><span class="sxs-lookup"><span data-stu-id="05eb8-122">no</span></span>        |
| [<span data-ttu-id="05eb8-123">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="05eb8-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="05eb8-124">non</span><span class="sxs-lookup"><span data-stu-id="05eb8-124">no</span></span>        |
| [<span data-ttu-id="05eb8-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05eb8-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="05eb8-126">non</span><span class="sxs-lookup"><span data-stu-id="05eb8-126">no</span></span>        |
| [<span data-ttu-id="05eb8-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05eb8-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="05eb8-128">non</span><span class="sxs-lookup"><span data-stu-id="05eb8-128">no</span></span>        |
| [<span data-ttu-id="05eb8-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05eb8-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="05eb8-130">non</span><span class="sxs-lookup"><span data-stu-id="05eb8-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="05eb8-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05eb8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05eb8-132">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="05eb8-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




