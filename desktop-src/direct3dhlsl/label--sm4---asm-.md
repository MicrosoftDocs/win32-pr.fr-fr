---
title: Label (SM4-ASM)
description: Indique le début d’une sous-routine.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679145"
---
# <a name="label-sm4---asm"></a><span data-ttu-id="ca3b5-103">Label (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ca3b5-103">label (sm4 - asm)</span></span>

<span data-ttu-id="ca3b5-104">Indique le début d’une sous-routine.</span><span class="sxs-lookup"><span data-stu-id="ca3b5-104">Indicates the beginning of a subroutine.</span></span>



| <span data-ttu-id="ca3b5-105">étiquette l\#</span><span class="sxs-lookup"><span data-stu-id="ca3b5-105">label l\#</span></span> |
|-----------|



 



| <span data-ttu-id="ca3b5-106">Élément</span><span class="sxs-lookup"><span data-stu-id="ca3b5-106">Item</span></span>                                                       | <span data-ttu-id="ca3b5-107">Description</span><span class="sxs-lookup"><span data-stu-id="ca3b5-107">Description</span></span>                         |
|------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="ca3b5-108"><span id="l_"></span><span id="L_"></span>*budget\#*</span><span class="sxs-lookup"><span data-stu-id="ca3b5-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="ca3b5-109">\[dans \] le numéro d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="ca3b5-109">\[in\] The label number.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca3b5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ca3b5-110">Remarks</span></span>

<span data-ttu-id="ca3b5-111">Une **étiquette** peut uniquement apparaître directement après une instruction [**RET**](ret--sm4---asm-.md) qui n’est imbriquée dans aucune instruction de contrôle de Flow.</span><span class="sxs-lookup"><span data-stu-id="ca3b5-111">A **label** can only appear directly after a [**ret**](ret--sm4---asm-.md) instruction which is not nested in any flow control statements.</span></span>

<span data-ttu-id="ca3b5-112">Le code précédant la première **étiquette** d’un programme est le programme principal.</span><span class="sxs-lookup"><span data-stu-id="ca3b5-112">The code before the first **label** in a program is the main program.</span></span> <span data-ttu-id="ca3b5-113">Toutes les sous-routines apparaissent à la fin du programme, indiquées par des instructions **label** .</span><span class="sxs-lookup"><span data-stu-id="ca3b5-113">All subroutines appear at the end of the program, indicated by **label** statements.</span></span>

<span data-ttu-id="ca3b5-114">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="ca3b5-114">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

<span data-ttu-id="ca3b5-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="ca3b5-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ca3b5-116">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="ca3b5-116">Vertex Shader</span></span> | <span data-ttu-id="ca3b5-117">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="ca3b5-117">Geometry Shader</span></span> | <span data-ttu-id="ca3b5-118">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ca3b5-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ca3b5-119">x</span><span class="sxs-lookup"><span data-stu-id="ca3b5-119">x</span></span>             | <span data-ttu-id="ca3b5-120">x</span><span class="sxs-lookup"><span data-stu-id="ca3b5-120">x</span></span>               | <span data-ttu-id="ca3b5-121">x</span><span class="sxs-lookup"><span data-stu-id="ca3b5-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ca3b5-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="ca3b5-122">Minimum Shader Model</span></span>

<span data-ttu-id="ca3b5-123">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="ca3b5-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ca3b5-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ca3b5-124">Shader Model</span></span>                                              | <span data-ttu-id="ca3b5-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="ca3b5-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ca3b5-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="ca3b5-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ca3b5-127">Oui</span><span class="sxs-lookup"><span data-stu-id="ca3b5-127">yes</span></span>       |
| [<span data-ttu-id="ca3b5-128">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="ca3b5-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ca3b5-129">Oui</span><span class="sxs-lookup"><span data-stu-id="ca3b5-129">yes</span></span>       |
| [<span data-ttu-id="ca3b5-130">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="ca3b5-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ca3b5-131">Oui</span><span class="sxs-lookup"><span data-stu-id="ca3b5-131">yes</span></span>       |
| [<span data-ttu-id="ca3b5-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca3b5-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ca3b5-133">non</span><span class="sxs-lookup"><span data-stu-id="ca3b5-133">no</span></span>        |
| [<span data-ttu-id="ca3b5-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca3b5-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ca3b5-135">non</span><span class="sxs-lookup"><span data-stu-id="ca3b5-135">no</span></span>        |
| [<span data-ttu-id="ca3b5-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca3b5-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ca3b5-137">non</span><span class="sxs-lookup"><span data-stu-id="ca3b5-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ca3b5-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca3b5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca3b5-139">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca3b5-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





