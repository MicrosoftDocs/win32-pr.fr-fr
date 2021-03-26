---
title: Cut (SM4-ASM)
description: Instruction de nuanceur Geometry qui termine la topologie primitive actuelle (si des vertex ont été émis) et démarre une nouvelle topologie du type déclaré par le nuanceur Geometry.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971535"
---
# <a name="cut-sm4---asm"></a><span data-ttu-id="074a9-103">Cut (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="074a9-103">cut (sm4 - asm)</span></span>

<span data-ttu-id="074a9-104">Instruction de nuanceur Geometry qui termine la topologie primitive actuelle (si des vertex ont été émis) et démarre une nouvelle topologie du type déclaré par le nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="074a9-104">Geometry Shader instruction that completes the current primitive topology (if any vertices have been emitted), and starts a new topology of the type declared by the Geometry Shader.</span></span>



| <span data-ttu-id="074a9-105">cut</span><span class="sxs-lookup"><span data-stu-id="074a9-105">cut</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="074a9-106">Notes</span><span class="sxs-lookup"><span data-stu-id="074a9-106">Remarks</span></span>

<span data-ttu-id="074a9-107">Lors de l’exécution de **Cut** , la première chose qui se produit est que toute topologie précédemment émise par l’appel de nuanceur Geometry est terminée.</span><span class="sxs-lookup"><span data-stu-id="074a9-107">When **cut** is executed, the first thing that happens is that any previously emitted topology by the Geometry Shader invocation is completed.</span></span> <span data-ttu-id="074a9-108">Si le nombre de vertex non suffisant a été émis pour la topologie primitive précédente, ceux-ci sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="074a9-108">If not enough vertices were emitted for the previous primitive topology, they are discarded.</span></span> <span data-ttu-id="074a9-109">Étant donné que les seules topologies de sortie disponibles pour le nuanceur Geometry sont PointList, linestrip et TriangleStrip, il n’y a jamais de sommets restants lors de la **coupe**.</span><span class="sxs-lookup"><span data-stu-id="074a9-109">Because the only available output topologies for the Geometry Shader are pointlist, linestrip, and trianglestrip, there are never any leftover vertices upon **cut**.</span></span>

<span data-ttu-id="074a9-110">Une fois la topologie précédente terminée, le cas échéant, **Cut** provoque le début d’une nouvelle topologie, à l’aide de la topologie déclarée comme sortie du nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="074a9-110">After the previous topology, if any, is completed, **cut** causes a new topology to begin, using the topology declared as the Geometry Shader output.</span></span>

## <a name="restrictions"></a><span data-ttu-id="074a9-111">Restrictions</span><span class="sxs-lookup"><span data-stu-id="074a9-111">Restrictions</span></span>

-   <span data-ttu-id="074a9-112">L’instruction **Cut** s’applique uniquement au nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="074a9-112">The **cut** instruction applies only to the Geometry Shader.</span></span>
-   <span data-ttu-id="074a9-113">**Cut** peut apparaître un nombre quelconque de fois dans le nuanceur Geometry, y compris dans le contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="074a9-113">**cut** can appear any number of times in the Geometry Shader, including within flow control.</span></span>
-   <span data-ttu-id="074a9-114">Si le nuanceur Geometry se termine et que les vertex ont été émis, la topologie qu’ils génèrent est terminée, comme si une **coupe** avait été exécutée en tant que dernière instruction.</span><span class="sxs-lookup"><span data-stu-id="074a9-114">If the Geometry Shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut** was executed as the last instruction.</span></span>
-   <span data-ttu-id="074a9-115">Si des flux ont été déclarés, le [ \_ flux](cut-stream---sm5---asm-.md) doit être utilisé à la place de **Cut**.</span><span class="sxs-lookup"><span data-stu-id="074a9-115">If streams have been declared, then [cut\_stream](cut-stream---sm5---asm-.md) must be used instead of **cut**.</span></span>

<span data-ttu-id="074a9-116">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="074a9-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="074a9-117">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="074a9-117">Vertex Shader</span></span> | <span data-ttu-id="074a9-118">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="074a9-118">Geometry Shader</span></span> | <span data-ttu-id="074a9-119">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="074a9-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="074a9-120">x</span><span class="sxs-lookup"><span data-stu-id="074a9-120">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="074a9-121">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="074a9-121">Minimum Shader Model</span></span>

<span data-ttu-id="074a9-122">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="074a9-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="074a9-123">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="074a9-123">Shader Model</span></span>                                              | <span data-ttu-id="074a9-124">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="074a9-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="074a9-125">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="074a9-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="074a9-126">Oui</span><span class="sxs-lookup"><span data-stu-id="074a9-126">yes</span></span>       |
| [<span data-ttu-id="074a9-127">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="074a9-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="074a9-128">Oui</span><span class="sxs-lookup"><span data-stu-id="074a9-128">yes</span></span>       |
| [<span data-ttu-id="074a9-129">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="074a9-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="074a9-130">Oui</span><span class="sxs-lookup"><span data-stu-id="074a9-130">yes</span></span>       |
| [<span data-ttu-id="074a9-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="074a9-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="074a9-132">non</span><span class="sxs-lookup"><span data-stu-id="074a9-132">no</span></span>        |
| [<span data-ttu-id="074a9-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="074a9-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="074a9-134">non</span><span class="sxs-lookup"><span data-stu-id="074a9-134">no</span></span>        |
| [<span data-ttu-id="074a9-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="074a9-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="074a9-136">non</span><span class="sxs-lookup"><span data-stu-id="074a9-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="074a9-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="074a9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="074a9-138">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="074a9-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




