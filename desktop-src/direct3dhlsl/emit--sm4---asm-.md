---
title: émission (SM4-ASM)
description: Émettez un sommet.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b17711b6f9cf5d707fb8eae3465100a78620c0c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679105"
---
# <a name="emit-sm4---asm"></a><span data-ttu-id="71af9-103">émission (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="71af9-103">emit (sm4 - asm)</span></span>

<span data-ttu-id="71af9-104">Émettez un sommet.</span><span class="sxs-lookup"><span data-stu-id="71af9-104">Emit a vertex.</span></span>



| <span data-ttu-id="71af9-105">émettra</span><span class="sxs-lookup"><span data-stu-id="71af9-105">emit</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="71af9-106">Notes</span><span class="sxs-lookup"><span data-stu-id="71af9-106">Remarks</span></span>

<span data-ttu-id="71af9-107">l' **émission** entraîne la lecture de tous les registres o déclarés \# à partir du nuanceur Geometry pour générer un vertex.</span><span class="sxs-lookup"><span data-stu-id="71af9-107">**emit** causes all declared o\# registers to be read out of the Geometry Shader to generate a vertex.</span></span>

<span data-ttu-id="71af9-108">À mesure que plusieurs appels d' **émission** sont émis, des primitives sont générées.</span><span class="sxs-lookup"><span data-stu-id="71af9-108">As multiple **emit** calls are issued, primitives are generated.</span></span>

<span data-ttu-id="71af9-109">l' **émission** peut apparaître un nombre quelconque de fois dans un nuanceur Geometry, y compris dans le contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="71af9-109">**emit** can appear any number of times in a Geometry Shader, including within flow control.</span></span>

<span data-ttu-id="71af9-110">Si des flux ont été déclarés, vous devez utiliser l' [émission de \_ flux](emit-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="71af9-110">If streams have been declared, you must use [emit\_stream](emit-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="71af9-111">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="71af9-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="71af9-112">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="71af9-112">Vertex Shader</span></span> | <span data-ttu-id="71af9-113">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="71af9-113">Geometry Shader</span></span> | <span data-ttu-id="71af9-114">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="71af9-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="71af9-115">x</span><span class="sxs-lookup"><span data-stu-id="71af9-115">x</span></span>               |              |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="71af9-116">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="71af9-116">Minimum Shader Model</span></span>

<span data-ttu-id="71af9-117">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="71af9-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="71af9-118">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="71af9-118">Shader Model</span></span>                                              | <span data-ttu-id="71af9-119">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="71af9-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="71af9-120">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="71af9-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="71af9-121">Oui</span><span class="sxs-lookup"><span data-stu-id="71af9-121">yes</span></span>       |
| [<span data-ttu-id="71af9-122">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="71af9-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="71af9-123">Oui</span><span class="sxs-lookup"><span data-stu-id="71af9-123">yes</span></span>       |
| [<span data-ttu-id="71af9-124">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="71af9-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="71af9-125">Oui</span><span class="sxs-lookup"><span data-stu-id="71af9-125">yes</span></span>       |
| [<span data-ttu-id="71af9-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71af9-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="71af9-127">non</span><span class="sxs-lookup"><span data-stu-id="71af9-127">no</span></span>        |
| [<span data-ttu-id="71af9-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71af9-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="71af9-129">non</span><span class="sxs-lookup"><span data-stu-id="71af9-129">no</span></span>        |
| [<span data-ttu-id="71af9-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71af9-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="71af9-131">non</span><span class="sxs-lookup"><span data-stu-id="71af9-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="71af9-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71af9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71af9-133">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="71af9-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




