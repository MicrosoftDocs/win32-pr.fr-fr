---
title: par défaut (SM4-ASM)
description: Étiquette facultative dans une instruction switch.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92364212e4d20a6e9229c057ba424f43f8f8556
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971542"
---
# <a name="default-sm4---asm"></a><span data-ttu-id="1c273-103">par défaut (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1c273-103">default (sm4 - asm)</span></span>

<span data-ttu-id="1c273-104">Étiquette facultative dans une instruction [switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="1c273-104">An optional label in a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="1c273-105">default</span><span class="sxs-lookup"><span data-stu-id="1c273-105">default</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="1c273-106">Notes</span><span class="sxs-lookup"><span data-stu-id="1c273-106">Remarks</span></span>

<span data-ttu-id="1c273-107">Cette instruction fonctionne comme **par défaut** dans C. la chute est valide uniquement si aucun code n’est ajouté. par conséquent, plusieurs cas (y compris la **valeur par défaut**) peuvent partager le même bloc de code.</span><span class="sxs-lookup"><span data-stu-id="1c273-107">This instruction operates just like **default** in C. Falling through is valid only if there is no code added, so multiple cases (including **default**) can share the same code block.</span></span>

<span data-ttu-id="1c273-108">Une seule instruction **par défaut** est autorisée dans une construction de **commutateur** .</span><span class="sxs-lookup"><span data-stu-id="1c273-108">Only one **default** statement is permitted in a **switch** construct.</span></span>

<span data-ttu-id="1c273-109">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="1c273-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1c273-110">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="1c273-110">Vertex Shader</span></span> | <span data-ttu-id="1c273-111">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="1c273-111">Geometry Shader</span></span> | <span data-ttu-id="1c273-112">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1c273-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1c273-113">x</span><span class="sxs-lookup"><span data-stu-id="1c273-113">x</span></span>             | <span data-ttu-id="1c273-114">x</span><span class="sxs-lookup"><span data-stu-id="1c273-114">x</span></span>               | <span data-ttu-id="1c273-115">x</span><span class="sxs-lookup"><span data-stu-id="1c273-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1c273-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="1c273-116">Minimum Shader Model</span></span>

<span data-ttu-id="1c273-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="1c273-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1c273-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="1c273-118">Shader Model</span></span>                                              | <span data-ttu-id="1c273-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="1c273-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1c273-120">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="1c273-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1c273-121">Oui</span><span class="sxs-lookup"><span data-stu-id="1c273-121">yes</span></span>       |
| [<span data-ttu-id="1c273-122">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="1c273-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1c273-123">Oui</span><span class="sxs-lookup"><span data-stu-id="1c273-123">yes</span></span>       |
| [<span data-ttu-id="1c273-124">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="1c273-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1c273-125">Oui</span><span class="sxs-lookup"><span data-stu-id="1c273-125">yes</span></span>       |
| [<span data-ttu-id="1c273-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c273-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1c273-127">non</span><span class="sxs-lookup"><span data-stu-id="1c273-127">no</span></span>        |
| [<span data-ttu-id="1c273-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c273-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1c273-129">non</span><span class="sxs-lookup"><span data-stu-id="1c273-129">no</span></span>        |
| [<span data-ttu-id="1c273-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c273-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1c273-131">non</span><span class="sxs-lookup"><span data-stu-id="1c273-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1c273-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c273-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c273-133">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c273-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




