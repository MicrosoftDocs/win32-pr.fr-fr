---
title: dcl_input vPrim (SM4-ASM)
description: '\_vPrim d’entrée DCL (SM4-ASM)'
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9742c6066d66d7aa4121c1d1d1df98a37cb0147e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381235"
---
# <a name="dcl_input-vprim-sm4---asm"></a><span data-ttu-id="69871-103">\_vPrim d’entrée DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="69871-103">dcl\_input vPrim (sm4 - asm)</span></span>

<span data-ttu-id="69871-104">Déclare qu’un nuanceur Geometry utilise son vPrim de registre d’entrée scalaire.</span><span class="sxs-lookup"><span data-stu-id="69871-104">Declares that a geometry shader uses its scalar input-register vPrim.</span></span>



| <span data-ttu-id="69871-105">\_ *vPrim* d’entrée DCL</span><span class="sxs-lookup"><span data-stu-id="69871-105">dcl\_input *vPrim*</span></span> |
|--------------------|



 



| <span data-ttu-id="69871-106">Élément</span><span class="sxs-lookup"><span data-stu-id="69871-106">Item</span></span>                                                                                       | <span data-ttu-id="69871-107">Description</span><span class="sxs-lookup"><span data-stu-id="69871-107">Description</span></span>                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69871-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span><span class="sxs-lookup"><span data-stu-id="69871-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span></span><br/> | <span data-ttu-id="69871-109">\[dans \] une scalaire 32 bits, qui peut être appliquée à chaque primitive intérieure dans un nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="69871-109">\[in\] A 32-bit scalar, which can be applied to each interior primitive in a geometry shader.</span></span><br/> |



 

<span data-ttu-id="69871-110">Le scalaire ne peut pas être appliqué à des primitives adjacentes.</span><span class="sxs-lookup"><span data-stu-id="69871-110">The scalar cannot be applied to any adjacent primitives.</span></span>

<span data-ttu-id="69871-111">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="69871-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="69871-112">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="69871-112">Vertex Shader</span></span> | <span data-ttu-id="69871-113">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="69871-113">Geometry Shader</span></span> | <span data-ttu-id="69871-114">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="69871-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="69871-115">x</span><span class="sxs-lookup"><span data-stu-id="69871-115">x</span></span>               |              |



 

<span data-ttu-id="69871-116">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="69871-116">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="69871-117">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="69871-117">Minimum Shader Model</span></span>

<span data-ttu-id="69871-118">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="69871-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="69871-119">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="69871-119">Shader Model</span></span>                                              | <span data-ttu-id="69871-120">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="69871-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="69871-121">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="69871-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="69871-122">Oui</span><span class="sxs-lookup"><span data-stu-id="69871-122">yes</span></span>       |
| [<span data-ttu-id="69871-123">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="69871-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="69871-124">Oui</span><span class="sxs-lookup"><span data-stu-id="69871-124">yes</span></span>       |
| [<span data-ttu-id="69871-125">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="69871-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="69871-126">Oui</span><span class="sxs-lookup"><span data-stu-id="69871-126">yes</span></span>       |
| [<span data-ttu-id="69871-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69871-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="69871-128">non</span><span class="sxs-lookup"><span data-stu-id="69871-128">no</span></span>        |
| [<span data-ttu-id="69871-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69871-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="69871-130">non</span><span class="sxs-lookup"><span data-stu-id="69871-130">no</span></span>        |
| [<span data-ttu-id="69871-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69871-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="69871-132">non</span><span class="sxs-lookup"><span data-stu-id="69871-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="69871-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69871-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69871-134">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69871-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





