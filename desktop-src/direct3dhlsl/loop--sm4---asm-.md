---
title: boucle (SM4-ASM)
description: Spécifie une boucle qui itère jusqu’à ce qu’une instruction Break soit rencontrée.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990776"
---
# <a name="loop-sm4---asm"></a><span data-ttu-id="8e85e-103">boucle (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8e85e-103">loop (sm4 - asm)</span></span>

<span data-ttu-id="8e85e-104">Spécifie une boucle qui itère jusqu’à ce qu’une instruction Break soit rencontrée.</span><span class="sxs-lookup"><span data-stu-id="8e85e-104">Specifies a loop which iterates until a break instruction is encountered.</span></span>



| <span data-ttu-id="8e85e-105">loop</span><span class="sxs-lookup"><span data-stu-id="8e85e-105">loop</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="8e85e-106">Notes</span><span class="sxs-lookup"><span data-stu-id="8e85e-106">Remarks</span></span>

<span data-ttu-id="8e85e-107">**Loop** peut itérer indéfiniment, bien que l’exécution globale du nuanceur puisse être forcée à se terminer après l’exécution d’un certain nombre d’instructions.</span><span class="sxs-lookup"><span data-stu-id="8e85e-107">**loop** can iterate indefinitely, although overall execution of the Shader may be forced to terminate after some number of instructions are executed.</span></span>

<span data-ttu-id="8e85e-108">Les blocs de contrôle de Flow peuvent imbriquer jusqu’à 64 de profondeur par sous-routine et main.</span><span class="sxs-lookup"><span data-stu-id="8e85e-108">Flow control blocks can nest up to 64 deep per subroutine and main.</span></span> <span data-ttu-id="8e85e-109">Le compilateur HLSL ne génère pas de sous-routines qui dépassent cette limite.</span><span class="sxs-lookup"><span data-stu-id="8e85e-109">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="8e85e-110">Le comportement des instructions de workflow de contrôle au-delà de 64 niveaux de profondeur par sous-routine n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8e85e-110">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="8e85e-111">Le format de jeton contient le décalage de l’instruction [ENDLOOP](endloop--sm4---asm-.md) correspondante dans le nuanceur pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="8e85e-111">The token format contains the offset of the corresponding [endloop](endloop--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="8e85e-112">L’exemple suivant montre comment utiliser l’instruction de boucle.</span><span class="sxs-lookup"><span data-stu-id="8e85e-112">The following example shows how to use the loop instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="8e85e-113">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="8e85e-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8e85e-114">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="8e85e-114">Vertex Shader</span></span> | <span data-ttu-id="8e85e-115">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="8e85e-115">Geometry Shader</span></span> | <span data-ttu-id="8e85e-116">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8e85e-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8e85e-117">x</span><span class="sxs-lookup"><span data-stu-id="8e85e-117">x</span></span>             | <span data-ttu-id="8e85e-118">x</span><span class="sxs-lookup"><span data-stu-id="8e85e-118">x</span></span>               | <span data-ttu-id="8e85e-119">x</span><span class="sxs-lookup"><span data-stu-id="8e85e-119">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8e85e-120">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8e85e-120">Minimum Shader Model</span></span>

<span data-ttu-id="8e85e-121">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="8e85e-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8e85e-122">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8e85e-122">Shader Model</span></span>                                              | <span data-ttu-id="8e85e-123">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8e85e-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8e85e-124">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8e85e-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8e85e-125">Oui</span><span class="sxs-lookup"><span data-stu-id="8e85e-125">yes</span></span>       |
| [<span data-ttu-id="8e85e-126">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="8e85e-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8e85e-127">Oui</span><span class="sxs-lookup"><span data-stu-id="8e85e-127">yes</span></span>       |
| [<span data-ttu-id="8e85e-128">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="8e85e-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8e85e-129">Oui</span><span class="sxs-lookup"><span data-stu-id="8e85e-129">yes</span></span>       |
| [<span data-ttu-id="8e85e-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e85e-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8e85e-131">non</span><span class="sxs-lookup"><span data-stu-id="8e85e-131">no</span></span>        |
| [<span data-ttu-id="8e85e-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e85e-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8e85e-133">non</span><span class="sxs-lookup"><span data-stu-id="8e85e-133">no</span></span>        |
| [<span data-ttu-id="8e85e-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e85e-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8e85e-135">non</span><span class="sxs-lookup"><span data-stu-id="8e85e-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8e85e-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e85e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e85e-137">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8e85e-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




