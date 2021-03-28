---
title: dcl_output oMask (SM5-ASM)
description: Déclarez un registre de sortie à écrire par le nuanceur.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381232"
---
# <a name="dcl_output-omask-sm5---asm"></a><span data-ttu-id="8750f-103">\_oMask de sortie DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8750f-103">dcl\_output oMask (sm5 - asm)</span></span>

<span data-ttu-id="8750f-104">Déclarez un registre de sortie à écrire par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8750f-104">Declare an output register to be written by the shader.</span></span>



| <span data-ttu-id="8750f-105">la \_ sortie DCL o \# \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="8750f-105">dcl\_output o\#\[.mask\]</span></span> |
|--------------------------|



 



| <span data-ttu-id="8750f-106">Élément</span><span class="sxs-lookup"><span data-stu-id="8750f-106">Item</span></span>                                                   | <span data-ttu-id="8750f-107">Description</span><span class="sxs-lookup"><span data-stu-id="8750f-107">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="8750f-108"><span id="o"></span><span id="O"></span>*sorties*</span><span class="sxs-lookup"><span data-stu-id="8750f-108"><span id="o"></span><span id="O"></span>*o*</span></span><br/> | <span data-ttu-id="8750f-109">\[dans \] le registre de sortie.</span><span class="sxs-lookup"><span data-stu-id="8750f-109">\[in\] The output register.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8750f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8750f-110">Remarks</span></span>


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a><span data-ttu-id="8750f-111">Restrictions</span><span class="sxs-lookup"><span data-stu-id="8750f-111">Restrictions</span></span>

-   <span data-ttu-id="8750f-112">Le masque de composant peut être n’importe quel sous-ensemble de \[ XYZW \] .</span><span class="sxs-lookup"><span data-stu-id="8750f-112">The component mask can be any subset of \[xyzw\].</span></span> <span data-ttu-id="8750f-113">Toutefois, laisser des écarts entre les composants gaspille de l’espace.</span><span class="sxs-lookup"><span data-stu-id="8750f-113">However, leaving gaps between components wastes space.</span></span>
-   <span data-ttu-id="8750f-114">Il est légal de déclarer un sur-ensemble du masque de composant déclaré pour l’entrée à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="8750f-114">It is legal to declare a superset of the component mask declared for input by the next stage.</span></span> <span data-ttu-id="8750f-115">Toutefois, les masques mutuellement exclusifs ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="8750f-115">However mutually exclusive masks are not allowed.</span></span> <span data-ttu-id="8750f-116">Le nuanceur de sommets, à partir de O3. XY, signifie que le nuanceur de pixels qui entre v3. z n’est pas valide, mais où v3. x ou v3. y ou v3. XY est valide.</span><span class="sxs-lookup"><span data-stu-id="8750f-116">The vertex shader outputting o3.xy, means the pixel shader inputting v3.z is invalid, but inputting v3.x or v3.y or v3.xy is valid.</span></span>

<span data-ttu-id="8750f-117">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="8750f-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8750f-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="8750f-118">Vertex</span></span> | <span data-ttu-id="8750f-119">Forme</span><span class="sxs-lookup"><span data-stu-id="8750f-119">Hull</span></span> | <span data-ttu-id="8750f-120">Domain</span><span class="sxs-lookup"><span data-stu-id="8750f-120">Domain</span></span> | <span data-ttu-id="8750f-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="8750f-121">Geometry</span></span> | <span data-ttu-id="8750f-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="8750f-122">Pixel</span></span> | <span data-ttu-id="8750f-123">Compute</span><span class="sxs-lookup"><span data-stu-id="8750f-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8750f-124">X</span><span class="sxs-lookup"><span data-stu-id="8750f-124">X</span></span>      | <span data-ttu-id="8750f-125">X</span><span class="sxs-lookup"><span data-stu-id="8750f-125">X</span></span>    | <span data-ttu-id="8750f-126">X</span><span class="sxs-lookup"><span data-stu-id="8750f-126">X</span></span>      | <span data-ttu-id="8750f-127">X</span><span class="sxs-lookup"><span data-stu-id="8750f-127">X</span></span>        | <span data-ttu-id="8750f-128">X</span><span class="sxs-lookup"><span data-stu-id="8750f-128">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8750f-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="8750f-129">Minimum Shader Model</span></span>

<span data-ttu-id="8750f-130">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="8750f-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8750f-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="8750f-131">Shader Model</span></span>                                              | <span data-ttu-id="8750f-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="8750f-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8750f-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="8750f-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8750f-134">Oui</span><span class="sxs-lookup"><span data-stu-id="8750f-134">yes</span></span>       |
| [<span data-ttu-id="8750f-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="8750f-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8750f-136">non</span><span class="sxs-lookup"><span data-stu-id="8750f-136">no</span></span>        |
| [<span data-ttu-id="8750f-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="8750f-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8750f-138">non</span><span class="sxs-lookup"><span data-stu-id="8750f-138">no</span></span>        |
| [<span data-ttu-id="8750f-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8750f-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8750f-140">non</span><span class="sxs-lookup"><span data-stu-id="8750f-140">no</span></span>        |
| [<span data-ttu-id="8750f-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8750f-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8750f-142">non</span><span class="sxs-lookup"><span data-stu-id="8750f-142">no</span></span>        |
| [<span data-ttu-id="8750f-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8750f-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8750f-144">non</span><span class="sxs-lookup"><span data-stu-id="8750f-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8750f-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8750f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8750f-146">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8750f-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





