---
title: bufinfo (SM5-ASM)
description: Interroge le nombre d’éléments sur une mémoire tampon (mais pas sur la mémoire tampon constante).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990761"
---
# <a name="bufinfo-sm5---asm"></a><span data-ttu-id="af96a-103">bufinfo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="af96a-103">bufinfo (sm5 - asm)</span></span>

<span data-ttu-id="af96a-104">Interroge le nombre d’éléments sur une mémoire tampon (mais pas sur la mémoire tampon constante).</span><span class="sxs-lookup"><span data-stu-id="af96a-104">Query the element count on a buffer (but not the constant buffer).</span></span>



| <span data-ttu-id="af96a-105">bufinfo dest \[ . Mask \] , srcResource</span><span class="sxs-lookup"><span data-stu-id="af96a-105">bufinfo dest\[.mask\], srcResource</span></span> |
|------------------------------------|



 



| <span data-ttu-id="af96a-106">Élément</span><span class="sxs-lookup"><span data-stu-id="af96a-106">Item</span></span>                                                                                                               | <span data-ttu-id="af96a-107">Description</span><span class="sxs-lookup"><span data-stu-id="af96a-107">Description</span></span>                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af96a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="af96a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="af96a-109">\[dans \] l’adresse des résultats.</span><span class="sxs-lookup"><span data-stu-id="af96a-109">\[in\] The address of the results.</span></span><br/>                                         |
| <span data-ttu-id="af96a-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="af96a-110"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="af96a-111">\[dans \] une mémoire tampon, autre qu’une mémoire tampon constante, dans un SRV (t \# ) ou un UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="af96a-111">\[in\] Buffer, other than a constant Buffer, in an SRV (t\#) or UAV (u\#).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af96a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="af96a-112">Remarks</span></span>

<span data-ttu-id="af96a-113">Tous les composants de *dest* reçoivent le nombre entier d’éléments dans l’affichage des ressources de nuanceur de tampon s.</span><span class="sxs-lookup"><span data-stu-id="af96a-113">All components in *dest* receive the integer number of elements in the buffer s shader resource view.</span></span> <span data-ttu-id="af96a-114">Le nombre d’éléments dépend des paramètres de vue tels que le format de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="af96a-114">The number of elements depends on the view parameters such as memory format.</span></span>

<span data-ttu-id="af96a-115">Pour une mémoire tampon typée SRV ou UAV, la valeur de retour est le nombre d’éléments dans la vue (où un élément est une unité du format typé).</span><span class="sxs-lookup"><span data-stu-id="af96a-115">For a typed buffer SRV or UAV, the return value is the number of elements in the view (where an element is one unit of the typed format).</span></span>

<span data-ttu-id="af96a-116">Pour une mémoire tampon brute SRV ou UAV, la valeur de retour est le nombre d’octets dans la vue.</span><span class="sxs-lookup"><span data-stu-id="af96a-116">For a raw buffer SRV or UAV, the return value is the number of bytes in the view.</span></span>

<span data-ttu-id="af96a-117">Pour une mémoire tampon structurée SRV ou UAV, la valeur de retour est le nombre de structures dans la vue.</span><span class="sxs-lookup"><span data-stu-id="af96a-117">For a structured buffer SRV or UAV, the return value is the number of structures in the view.</span></span>

<span data-ttu-id="af96a-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="af96a-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="af96a-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="af96a-119">Vertex</span></span> | <span data-ttu-id="af96a-120">Forme</span><span class="sxs-lookup"><span data-stu-id="af96a-120">Hull</span></span> | <span data-ttu-id="af96a-121">Domain</span><span class="sxs-lookup"><span data-stu-id="af96a-121">Domain</span></span> | <span data-ttu-id="af96a-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="af96a-122">Geometry</span></span> | <span data-ttu-id="af96a-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="af96a-123">Pixel</span></span> | <span data-ttu-id="af96a-124">Compute</span><span class="sxs-lookup"><span data-stu-id="af96a-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="af96a-125">X</span><span class="sxs-lookup"><span data-stu-id="af96a-125">X</span></span>      | <span data-ttu-id="af96a-126">X</span><span class="sxs-lookup"><span data-stu-id="af96a-126">X</span></span>    | <span data-ttu-id="af96a-127">X</span><span class="sxs-lookup"><span data-stu-id="af96a-127">X</span></span>      | <span data-ttu-id="af96a-128">X</span><span class="sxs-lookup"><span data-stu-id="af96a-128">X</span></span>        | <span data-ttu-id="af96a-129">X</span><span class="sxs-lookup"><span data-stu-id="af96a-129">X</span></span>     | <span data-ttu-id="af96a-130">X</span><span class="sxs-lookup"><span data-stu-id="af96a-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="af96a-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="af96a-131">Minimum Shader Model</span></span>

<span data-ttu-id="af96a-132">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="af96a-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="af96a-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="af96a-133">Shader Model</span></span>                                              | <span data-ttu-id="af96a-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="af96a-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="af96a-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="af96a-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="af96a-136">Oui</span><span class="sxs-lookup"><span data-stu-id="af96a-136">yes</span></span>       |
| [<span data-ttu-id="af96a-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="af96a-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="af96a-138">non</span><span class="sxs-lookup"><span data-stu-id="af96a-138">no</span></span>        |
| [<span data-ttu-id="af96a-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="af96a-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="af96a-140">non</span><span class="sxs-lookup"><span data-stu-id="af96a-140">no</span></span>        |
| [<span data-ttu-id="af96a-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af96a-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="af96a-142">non</span><span class="sxs-lookup"><span data-stu-id="af96a-142">no</span></span>        |
| [<span data-ttu-id="af96a-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af96a-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="af96a-144">non</span><span class="sxs-lookup"><span data-stu-id="af96a-144">no</span></span>        |
| [<span data-ttu-id="af96a-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af96a-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="af96a-146">non</span><span class="sxs-lookup"><span data-stu-id="af96a-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="af96a-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af96a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af96a-148">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af96a-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





