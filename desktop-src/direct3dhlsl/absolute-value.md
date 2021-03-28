---
title: Valeur absolue
description: Prend la valeur absolue d’un opérande source utilisé dans une opération arithmétique.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313741"
---
# <a name="absolute-value"></a><span data-ttu-id="3d261-103">Valeur absolue</span><span class="sxs-lookup"><span data-stu-id="3d261-103">Absolute Value</span></span>

<span data-ttu-id="3d261-104">Prend la valeur absolue d’un opérande source utilisé dans une opération arithmétique.</span><span class="sxs-lookup"><span data-stu-id="3d261-104">Take the absolute value of a source operand used in an arithmetic operation.</span></span>



| <span data-ttu-id="3d261-105">\_absolue</span><span class="sxs-lookup"><span data-stu-id="3d261-105">\_abs</span></span> |
|-------|



 

<span data-ttu-id="3d261-106">Ce modificateur est utilisé pour les instructions à virgule flottante simple et double précision uniquement.</span><span class="sxs-lookup"><span data-stu-id="3d261-106">This modifier is used for single and double precision floating point and instructions only.</span></span> <span data-ttu-id="3d261-107">Le modificateur **\_ ABS** force le signe du ou des nombres sur l’opérande source positif, y compris sur les valeurs INF.</span><span class="sxs-lookup"><span data-stu-id="3d261-107">The **\_abs** modifier forces the sign of the number(s) on the source operand positive, including on INF values.</span></span>

<span data-ttu-id="3d261-108">L’application d' **\_ ABS** sur Nan préserve Nan, bien que le modèle binaire Nan particulier qui résulte n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="3d261-108">Applying **\_abs** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="3d261-109">Quand \_ ABS est combiné avec le modificateur de [négation](negate.md) , la combinaison force le signe à être négatif, comme si le modificateur **\_ ABS** était appliqué en premier, puis la **négation**.</span><span class="sxs-lookup"><span data-stu-id="3d261-109">When \_abs is combined with the [negate](negate.md) modifier, the combination forces the sign to be negative, as if the **\_abs** modifier is applied first, then the **negate**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3d261-110">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="3d261-110">Minimum Shader Model</span></span>

<span data-ttu-id="3d261-111">Ce modificateur est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="3d261-111">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="3d261-112">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="3d261-112">Shader Model</span></span>                                              | <span data-ttu-id="3d261-113">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="3d261-113">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3d261-114">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="3d261-114">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3d261-115">Oui</span><span class="sxs-lookup"><span data-stu-id="3d261-115">yes</span></span>       |
| [<span data-ttu-id="3d261-116">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="3d261-116">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3d261-117">Oui</span><span class="sxs-lookup"><span data-stu-id="3d261-117">yes</span></span>       |
| [<span data-ttu-id="3d261-118">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="3d261-118">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3d261-119">Oui</span><span class="sxs-lookup"><span data-stu-id="3d261-119">yes</span></span>       |
| [<span data-ttu-id="3d261-120">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d261-120">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3d261-121">non</span><span class="sxs-lookup"><span data-stu-id="3d261-121">no</span></span>        |
| [<span data-ttu-id="3d261-122">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d261-122">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3d261-123">non</span><span class="sxs-lookup"><span data-stu-id="3d261-123">no</span></span>        |
| [<span data-ttu-id="3d261-124">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3d261-124">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3d261-125">non</span><span class="sxs-lookup"><span data-stu-id="3d261-125">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3d261-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d261-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d261-127">Modificateurs d’instruction</span><span class="sxs-lookup"><span data-stu-id="3d261-127">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




