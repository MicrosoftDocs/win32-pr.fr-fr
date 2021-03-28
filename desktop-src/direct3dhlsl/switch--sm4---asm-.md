---
title: Switch (SM4-ASM)
description: Transfère le contrôle à un autre bloc d’instructions dans le corps du commutateur en fonction de la valeur d’un sélecteur.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feed346b8aa33feecc13fe2a6ffad59c961b0173
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030584"
---
# <a name="switch-sm4---asm"></a><span data-ttu-id="accde-103">Switch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="accde-103">switch (sm4 - asm)</span></span>

<span data-ttu-id="accde-104">Transfère le contrôle à un autre bloc d’instructions dans le corps du commutateur en fonction de la valeur d’un sélecteur.</span><span class="sxs-lookup"><span data-stu-id="accde-104">Transfers control to a different statement block within the switch body depending on the value of a selector.</span></span>



| <span data-ttu-id="accde-105">basculer le composant src0. Selected \_</span><span class="sxs-lookup"><span data-stu-id="accde-105">switch src0.selected\_component</span></span> |
|---------------------------------|



 



| <span data-ttu-id="accde-106">Élément</span><span class="sxs-lookup"><span data-stu-id="accde-106">Item</span></span>                                                            | <span data-ttu-id="accde-107">Description</span><span class="sxs-lookup"><span data-stu-id="accde-107">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="accde-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="accde-108"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="accde-109">\[dans \] le sélecteur de l’instruction switch.</span><span class="sxs-lookup"><span data-stu-id="accde-109">\[in\] The selector for the switch statement.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="accde-110">Notes</span><span class="sxs-lookup"><span data-stu-id="accde-110">Remarks</span></span>

<span data-ttu-id="accde-111">Une  / construction [endswitch](endswitch--sm4---asm-.md) de commutateur se comporte exactement comme une construction de **commutateur** dans le langage C, avec l’exception suivante : pour [](case--sm4---asm-.md)les / instructions [par défaut](default--sm4---asm-.md) du cas d3d11 qui passent à la **casse** suivante / **par défaut** sans [saut](break--sm4---asm-.md) de code, il ne peut pas y avoir de code.</span><span class="sxs-lookup"><span data-stu-id="accde-111">A **switch**/[endswitch](endswitch--sm4---asm-.md) construct behaves exactly as a **switch** construct in the C language, with the following exception: for D3D11 [case](case--sm4---asm-.md)/[default](default--sm4---asm-.md) statements that fall through to the next **case**/**default** without a [break](break--sm4---asm-.md) cannot have any code in them.</span></span> <span data-ttu-id="accde-112">Il est possible que plusieurs instructions **case** , y compris **default**, apparaissent séquentiellement, partageant le même bloc de code.</span><span class="sxs-lookup"><span data-stu-id="accde-112">It is permitted for multiple **case** statements, including **default**, to appear sequentially, sharing the same code block.</span></span>

<span data-ttu-id="accde-113">La condition doit être un composant de Registre 32 bits ou une quantité immédiate.</span><span class="sxs-lookup"><span data-stu-id="accde-113">The condition must be a 32-bit register component or immediate quantity.</span></span> <span data-ttu-id="accde-114">La comparaison d’égalité est une opération au niveau du bit (Integer).</span><span class="sxs-lookup"><span data-stu-id="accde-114">The equality comparison is bitwise (integer).</span></span>

<span data-ttu-id="accde-115">Comme pour toute instruction de nuanceur dans le D3D11, le matériel peut ou non implémenter directement la construction de **commutateur** .</span><span class="sxs-lookup"><span data-stu-id="accde-115">As with any Shader instruction in the D3D11, hardware may or may not implement the **switch** construct directly.</span></span>

<span data-ttu-id="accde-116">Les instructions **switch** peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="accde-116">**Switch** statements can be nested.</span></span> <span data-ttu-id="accde-117">Chaque bloc **switch** compte 1 niveau par rapport à la limite de profondeur d’imbrication de contrôle de flow de 64 par sous-routine et main, indépendamment du nombre d’instructions **case** .</span><span class="sxs-lookup"><span data-stu-id="accde-117">Each **switch** block counts as 1 level against the flow control nesting depth limit of 64 per subroutine and main, independent of the number of **case** statements.</span></span> <span data-ttu-id="accde-118">Le compilateur HLSL ne génère pas de sous-routines qui dépassent cette limite.</span><span class="sxs-lookup"><span data-stu-id="accde-118">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="accde-119">Le comportement des instructions de workflow de contrôle au-delà de 64 niveaux de profondeur par sous-routine n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="accde-119">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="accde-120">L’exemple suivant montre comment utiliser cette instruction.</span><span class="sxs-lookup"><span data-stu-id="accde-120">The following example shows how to use this instruction.</span></span>

``` syntax
                ...
                switch r0.x
                default: // falling through
                case 3
                    switch r1.x
                    case 4
                        ...
                        break
                    case 5
                        ...
                        break
                    endswitch
                    break
                case 0
                    break
                endswitch
```

<span data-ttu-id="accde-121">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="accde-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="accde-122">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="accde-122">Vertex Shader</span></span> | <span data-ttu-id="accde-123">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="accde-123">Geometry Shader</span></span> | <span data-ttu-id="accde-124">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="accde-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="accde-125">x</span><span class="sxs-lookup"><span data-stu-id="accde-125">x</span></span>             | <span data-ttu-id="accde-126">x</span><span class="sxs-lookup"><span data-stu-id="accde-126">x</span></span>               | <span data-ttu-id="accde-127">x</span><span class="sxs-lookup"><span data-stu-id="accde-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="accde-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="accde-128">Minimum Shader Model</span></span>

<span data-ttu-id="accde-129">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="accde-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="accde-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="accde-130">Shader Model</span></span>                                              | <span data-ttu-id="accde-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="accde-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="accde-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="accde-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="accde-133">Oui</span><span class="sxs-lookup"><span data-stu-id="accde-133">yes</span></span>       |
| [<span data-ttu-id="accde-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="accde-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="accde-135">Oui</span><span class="sxs-lookup"><span data-stu-id="accde-135">yes</span></span>       |
| [<span data-ttu-id="accde-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="accde-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="accde-137">Oui</span><span class="sxs-lookup"><span data-stu-id="accde-137">yes</span></span>       |
| [<span data-ttu-id="accde-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="accde-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="accde-139">non</span><span class="sxs-lookup"><span data-stu-id="accde-139">no</span></span>        |
| [<span data-ttu-id="accde-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="accde-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="accde-141">non</span><span class="sxs-lookup"><span data-stu-id="accde-141">no</span></span>        |
| [<span data-ttu-id="accde-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="accde-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="accde-143">non</span><span class="sxs-lookup"><span data-stu-id="accde-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="accde-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="accde-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="accde-145">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="accde-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





