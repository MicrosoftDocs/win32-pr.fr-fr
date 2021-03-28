---
title: dcl_function_body (SM5-ASM)
description: Déclarez un corps de fonction.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101113"
---
# <a name="dcl_function_body-sm5---asm"></a><span data-ttu-id="6a835-103">\_corps de la fonction DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="6a835-103">dcl\_function\_body (sm5 - asm)</span></span>

<span data-ttu-id="6a835-104">Déclarez un corps de fonction.</span><span class="sxs-lookup"><span data-stu-id="6a835-104">Declare a function body.</span></span>



| <span data-ttu-id="6a835-105">corps de la \_ fonction DCL \_ FB\#</span><span class="sxs-lookup"><span data-stu-id="6a835-105">dcl\_function\_body fb\#</span></span> |
|--------------------------|



 



| <span data-ttu-id="6a835-106">Élément</span><span class="sxs-lookup"><span data-stu-id="6a835-106">Item</span></span>                                                          | <span data-ttu-id="6a835-107">Description</span><span class="sxs-lookup"><span data-stu-id="6a835-107">Description</span></span>                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="6a835-108"><span id="fb_"></span><span id="FB_"></span>*disposez\#*</span><span class="sxs-lookup"><span data-stu-id="6a835-108"><span id="fb_"></span><span id="FB_"></span>*fb\#*</span></span><br/> | <span data-ttu-id="6a835-109">\[dans \] l’étiquette de l’emplacement où la fonction apparaît.</span><span class="sxs-lookup"><span data-stu-id="6a835-109">\[in\] The label of the place where the function will appear.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a835-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6a835-110">Remarks</span></span>

<span data-ttu-id="6a835-111">Cette instruction déclare un corps de fonction unique dont le code apparaîtra ultérieurement dans le programme à l’étiquette FB \# .</span><span class="sxs-lookup"><span data-stu-id="6a835-111">This instruction declares a unique function body whose code will appear later in the program at label fb\#.</span></span>

<span data-ttu-id="6a835-112">Les corps de fonction sont utilisés dans les déclarations de table de fonctions.</span><span class="sxs-lookup"><span data-stu-id="6a835-112">Function bodies are used in function table declarations.</span></span> <span data-ttu-id="6a835-113">Pour plus d’informations, [consultez \_ \_ table de fonctions DCL](dcl-function-table---sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="6a835-113">For more info, see [dcl\_function\_table](dcl-function-table---sm5---asm-.md).</span></span>

<span data-ttu-id="6a835-114">Dans le nuanceur de coque et le nuanceur de domaine, où il y a plusieurs phases (phase de point de contrôle, phase de branchement et phase de jointure), tous les corps de fonction (étiquette FB \# ) apparaissent après toutes les phases, au lieu d’être regroupés par phase.</span><span class="sxs-lookup"><span data-stu-id="6a835-114">In the hull shader and domain shader, where there are multiple phases (control point phase, fork phase, and join phase), all function bodies (label fb\#) appear after all the phases, rather than being grouped by phase.</span></span>

<span data-ttu-id="6a835-115">Il n’existe aucune limite au nombre de corps de fonction qui peuvent être présents.</span><span class="sxs-lookup"><span data-stu-id="6a835-115">There is no limit to how many function bodies can be present.</span></span>

<span data-ttu-id="6a835-116">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="6a835-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a835-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="6a835-117">Vertex</span></span> | <span data-ttu-id="6a835-118">Forme</span><span class="sxs-lookup"><span data-stu-id="6a835-118">Hull</span></span> | <span data-ttu-id="6a835-119">Domain</span><span class="sxs-lookup"><span data-stu-id="6a835-119">Domain</span></span> | <span data-ttu-id="6a835-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="6a835-120">Geometry</span></span> | <span data-ttu-id="6a835-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="6a835-121">Pixel</span></span> | <span data-ttu-id="6a835-122">Compute</span><span class="sxs-lookup"><span data-stu-id="6a835-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="6a835-123">X</span><span class="sxs-lookup"><span data-stu-id="6a835-123">X</span></span>      | <span data-ttu-id="6a835-124">X</span><span class="sxs-lookup"><span data-stu-id="6a835-124">X</span></span>    | <span data-ttu-id="6a835-125">X</span><span class="sxs-lookup"><span data-stu-id="6a835-125">X</span></span>      | <span data-ttu-id="6a835-126">X</span><span class="sxs-lookup"><span data-stu-id="6a835-126">X</span></span>        | <span data-ttu-id="6a835-127">X</span><span class="sxs-lookup"><span data-stu-id="6a835-127">X</span></span>     | <span data-ttu-id="6a835-128">X</span><span class="sxs-lookup"><span data-stu-id="6a835-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a835-129">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="6a835-129">Minimum Shader Model</span></span>

<span data-ttu-id="6a835-130">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="6a835-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="6a835-131">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="6a835-131">Shader Model</span></span>                                              | <span data-ttu-id="6a835-132">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="6a835-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a835-133">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="6a835-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a835-134">Oui</span><span class="sxs-lookup"><span data-stu-id="6a835-134">yes</span></span>       |
| [<span data-ttu-id="6a835-135">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="6a835-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a835-136">non</span><span class="sxs-lookup"><span data-stu-id="6a835-136">no</span></span>        |
| [<span data-ttu-id="6a835-137">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="6a835-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a835-138">non</span><span class="sxs-lookup"><span data-stu-id="6a835-138">no</span></span>        |
| [<span data-ttu-id="6a835-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a835-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a835-140">non</span><span class="sxs-lookup"><span data-stu-id="6a835-140">no</span></span>        |
| [<span data-ttu-id="6a835-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a835-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a835-142">non</span><span class="sxs-lookup"><span data-stu-id="6a835-142">no</span></span>        |
| [<span data-ttu-id="6a835-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a835-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a835-144">non</span><span class="sxs-lookup"><span data-stu-id="6a835-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a835-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a835-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a835-146">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a835-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





