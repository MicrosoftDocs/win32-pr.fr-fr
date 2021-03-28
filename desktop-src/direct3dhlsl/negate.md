---
title: Negate
description: Retourne le signe de la valeur d’un opérande source utilisé dans une opération arithmétique.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030568"
---
# <a name="negate"></a><span data-ttu-id="f4cc3-103">Negate</span><span class="sxs-lookup"><span data-stu-id="f4cc3-103">Negate</span></span>

<span data-ttu-id="f4cc3-104">Retourne le signe de la valeur d’un opérande source utilisé dans une opération arithmétique.</span><span class="sxs-lookup"><span data-stu-id="f4cc3-104">Flips the sign of the value of a source operand used in an arithmetic operation.</span></span>



| \-  |
|-----|



 

<span data-ttu-id="f4cc3-105">Pour les instructions et les points à virgule flottante simple et double précision, le modificateur de négation retourne le signe du ou des nombres dans l’opérande source, y compris sur les valeurs INF.</span><span class="sxs-lookup"><span data-stu-id="f4cc3-105">For single and double precision floating point and instructions, the negate modifier flips the sign of the number(s) in the source operand, including on INF values.</span></span> <span data-ttu-id="f4cc3-106">L’application de l' **inverse** sur Nan préserve Nan, bien que le modèle binaire Nan particulier qui résulte n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f4cc3-106">Applying **negate** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="f4cc3-107">Pour les instructions entières, le modificateur de **négation** prend le complément à 2 du ou des nombres dans l’opérande source.</span><span class="sxs-lookup"><span data-stu-id="f4cc3-107">For integer instructions, the **negate** modifier takes the 2's complement of the number(s) in the source operand.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f4cc3-108">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f4cc3-108">Minimum Shader Model</span></span>

<span data-ttu-id="f4cc3-109">Ce modificateur est pris en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f4cc3-109">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="f4cc3-110">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f4cc3-110">Shader Model</span></span>                                              | <span data-ttu-id="f4cc3-111">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f4cc3-111">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f4cc3-112">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f4cc3-112">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f4cc3-113">Oui</span><span class="sxs-lookup"><span data-stu-id="f4cc3-113">yes</span></span>       |
| [<span data-ttu-id="f4cc3-114">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f4cc3-114">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f4cc3-115">Oui</span><span class="sxs-lookup"><span data-stu-id="f4cc3-115">yes</span></span>       |
| [<span data-ttu-id="f4cc3-116">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f4cc3-116">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f4cc3-117">Oui</span><span class="sxs-lookup"><span data-stu-id="f4cc3-117">yes</span></span>       |
| [<span data-ttu-id="f4cc3-118">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4cc3-118">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f4cc3-119">non</span><span class="sxs-lookup"><span data-stu-id="f4cc3-119">no</span></span>        |
| [<span data-ttu-id="f4cc3-120">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4cc3-120">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f4cc3-121">non</span><span class="sxs-lookup"><span data-stu-id="f4cc3-121">no</span></span>        |
| [<span data-ttu-id="f4cc3-122">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4cc3-122">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f4cc3-123">non</span><span class="sxs-lookup"><span data-stu-id="f4cc3-123">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f4cc3-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4cc3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4cc3-125">Modificateurs d’instruction</span><span class="sxs-lookup"><span data-stu-id="f4cc3-125">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




