---
title: Saturation (référence HLSL)
description: Attache le résultat d’une opération arithmétique à virgule flottante simple ou double précision à \ 0.0 f... 1.0 f \ plage.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104381267"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="f7242-103">Saturation (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7242-103">Saturate (HLSL reference)</span></span>

<span data-ttu-id="f7242-104">Attache le résultat d’une opération arithmétique à virgule flottante simple ou double précision à \[ 0.0 f... plage f 1.0 \] .</span><span class="sxs-lookup"><span data-stu-id="f7242-104">Clamps the result of a single or double precision floating point arithmetic operation to \[0.0f...1.0f\] range.</span></span>



| <span data-ttu-id="f7242-105">\_sot</span><span class="sxs-lookup"><span data-stu-id="f7242-105">\_sat</span></span> |
|-------|



 

<span data-ttu-id="f7242-106">Le modificateur de résultat d’instruction **saturé** effectue l’opération suivante sur les valeurs de résultat à partir d’une opération arithmétique à virgule flottante qui \_ lui est appliquée :</span><span class="sxs-lookup"><span data-stu-id="f7242-106">The **saturate** instruction result modifier performs the following operation on the result values(s) from a floating point arithmetic operation that has \_sat applied to it:</span></span>

`min(1.0f, max(0.0f, value))`

<span data-ttu-id="f7242-107">où min () et Max () dans l’expression ci-dessus se comportent de la façon dont [min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [DMin](dmin--sm5---asm-.md)ou [DMax](dmax--sm5---asm-.md) fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="f7242-107">where min() and max() in the above expression behave in the way [min](min--sm4---asm-.md), [max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md), or [dmax](dmax--sm5---asm-.md) operate.</span></span>

<span data-ttu-id="f7242-108">`_sat(NaN)` retourne 0, en fonction des règles min et max.</span><span class="sxs-lookup"><span data-stu-id="f7242-108">`_sat(NaN)` returns 0, by the rules for min and max.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f7242-109">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f7242-109">Minimum Shader Model</span></span>

<span data-ttu-id="f7242-110">Ce modificateur est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f7242-110">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="f7242-111">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f7242-111">Shader Model</span></span>                                              | <span data-ttu-id="f7242-112">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f7242-112">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f7242-113">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f7242-113">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f7242-114">Oui</span><span class="sxs-lookup"><span data-stu-id="f7242-114">yes</span></span>       |
| [<span data-ttu-id="f7242-115">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f7242-115">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f7242-116">Oui</span><span class="sxs-lookup"><span data-stu-id="f7242-116">yes</span></span>       |
| [<span data-ttu-id="f7242-117">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f7242-117">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f7242-118">Oui</span><span class="sxs-lookup"><span data-stu-id="f7242-118">yes</span></span>       |
| [<span data-ttu-id="f7242-119">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7242-119">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f7242-120">non</span><span class="sxs-lookup"><span data-stu-id="f7242-120">no</span></span>        |
| [<span data-ttu-id="f7242-121">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7242-121">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f7242-122">non</span><span class="sxs-lookup"><span data-stu-id="f7242-122">no</span></span>        |
| [<span data-ttu-id="f7242-123">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f7242-123">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f7242-124">non</span><span class="sxs-lookup"><span data-stu-id="f7242-124">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f7242-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7242-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7242-126">Modificateurs d’instruction</span><span class="sxs-lookup"><span data-stu-id="f7242-126">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




