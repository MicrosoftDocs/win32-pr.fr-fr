---
title: cas (SM4-ASM)
description: Étiquette dans une instruction switch.
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971558"
---
# <a name="case-sm4---asm"></a><span data-ttu-id="29bb5-103">cas (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="29bb5-103">case (sm4 - asm)</span></span>

<span data-ttu-id="29bb5-104">Étiquette dans une instruction switch.</span><span class="sxs-lookup"><span data-stu-id="29bb5-104">A label in a switch instruction.</span></span>



| <span data-ttu-id="29bb5-105">cas \[ 32-bit immédiat\]</span><span class="sxs-lookup"><span data-stu-id="29bb5-105">case \[32-bit immediate\]</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="29bb5-106">Notes</span><span class="sxs-lookup"><span data-stu-id="29bb5-106">Remarks</span></span>

<span data-ttu-id="29bb5-107">Étant donné que la chute des **cas** n’est valide que si aucun code n’est ajouté, plusieurs **cas** (y compris la [valeur par défaut](default--sm4---asm-.md)) peuvent partager le même bloc de code.</span><span class="sxs-lookup"><span data-stu-id="29bb5-107">Because falling through **cases** is valid only if there is no code added, multiple **cases** (including [default](default--sm4---asm-.md)) can share the same code block.</span></span>

<span data-ttu-id="29bb5-108">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="29bb5-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="29bb5-109">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="29bb5-109">Vertex Shader</span></span> | <span data-ttu-id="29bb5-110">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="29bb5-110">Geometry Shader</span></span> | <span data-ttu-id="29bb5-111">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="29bb5-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="29bb5-112">x</span><span class="sxs-lookup"><span data-stu-id="29bb5-112">x</span></span>             | <span data-ttu-id="29bb5-113">x</span><span class="sxs-lookup"><span data-stu-id="29bb5-113">x</span></span>               | <span data-ttu-id="29bb5-114">x</span><span class="sxs-lookup"><span data-stu-id="29bb5-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="29bb5-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="29bb5-115">Minimum Shader Model</span></span>

<span data-ttu-id="29bb5-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="29bb5-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="29bb5-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="29bb5-117">Shader Model</span></span>                                              | <span data-ttu-id="29bb5-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="29bb5-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="29bb5-119">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="29bb5-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="29bb5-120">Oui</span><span class="sxs-lookup"><span data-stu-id="29bb5-120">yes</span></span>       |
| [<span data-ttu-id="29bb5-121">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="29bb5-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="29bb5-122">Oui</span><span class="sxs-lookup"><span data-stu-id="29bb5-122">yes</span></span>       |
| [<span data-ttu-id="29bb5-123">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="29bb5-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="29bb5-124">Oui</span><span class="sxs-lookup"><span data-stu-id="29bb5-124">yes</span></span>       |
| [<span data-ttu-id="29bb5-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="29bb5-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="29bb5-126">non</span><span class="sxs-lookup"><span data-stu-id="29bb5-126">no</span></span>        |
| [<span data-ttu-id="29bb5-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="29bb5-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="29bb5-128">non</span><span class="sxs-lookup"><span data-stu-id="29bb5-128">no</span></span>        |
| [<span data-ttu-id="29bb5-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="29bb5-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="29bb5-130">non</span><span class="sxs-lookup"><span data-stu-id="29bb5-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="29bb5-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29bb5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29bb5-132">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="29bb5-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




