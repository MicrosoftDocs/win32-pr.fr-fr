---
title: dcl_function_table (SM5-ASM)
description: Déclarez une table de fonctions.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990849"
---
# <a name="dcl_function_table-sm5---asm"></a><span data-ttu-id="de7f9-103">\_ \_ table de fonctions DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="de7f9-103">dcl\_function\_table (sm5 - asm)</span></span>

<span data-ttu-id="de7f9-104">Déclarez une table de fonctions.</span><span class="sxs-lookup"><span data-stu-id="de7f9-104">Declare a function table.</span></span>



| <span data-ttu-id="de7f9-105">\_ \_ table de fonctions DCL ft \# = {FB \# , FB \# ,...}</span><span class="sxs-lookup"><span data-stu-id="de7f9-105">dcl\_function\_table ft\# = {fb\#, fb\#, ...}</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="de7f9-106">Élément</span><span class="sxs-lookup"><span data-stu-id="de7f9-106">Item</span></span>                                                      | <span data-ttu-id="de7f9-107">Description</span><span class="sxs-lookup"><span data-stu-id="de7f9-107">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="de7f9-108"><span id="ft"></span><span id="FT"></span>*pied*</span><span class="sxs-lookup"><span data-stu-id="de7f9-108"><span id="ft"></span><span id="FT"></span>*ft*</span></span><br/> | <span data-ttu-id="de7f9-109">\[dans \] les entrées de la table de fonctions.</span><span class="sxs-lookup"><span data-stu-id="de7f9-109">\[in\] The function table entries.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de7f9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="de7f9-110">Remarks</span></span>

<span data-ttu-id="de7f9-111">Cette fonction déclare une table de fonctions comme un ensemble de corps de fonction qui ont été déclarés précédemment.</span><span class="sxs-lookup"><span data-stu-id="de7f9-111">This function declares a function table as a set of function bodies that have been declared earlier.</span></span>

<span data-ttu-id="de7f9-112">C’est comme une vtable C++, sauf qu’il existe une entrée par site d’appel pour une interface plutôt que par méthode.</span><span class="sxs-lookup"><span data-stu-id="de7f9-112">This is like a C++ vtable except there is an entry per call site for an interface instead of per method.</span></span>

<span data-ttu-id="de7f9-113">Il n’existe aucune limite au nombre de corps de fonction qui peuvent être listés dans une table de fonctions.</span><span class="sxs-lookup"><span data-stu-id="de7f9-113">There is no limit to how many function bodies can be listed in a function table.</span></span>

<span data-ttu-id="de7f9-114">Il est valide pour un corps de fonction en FB \# référencé à plusieurs moments dans une ou plusieurs tables de fonctions, comme un moyen de partager le code commun.</span><span class="sxs-lookup"><span data-stu-id="de7f9-114">It is valid for a given function body fb\# to be referenced multiple times in one or more function tables, as a way of sharing common code.</span></span>

<span data-ttu-id="de7f9-115">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="de7f9-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="de7f9-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="de7f9-116">Vertex</span></span> | <span data-ttu-id="de7f9-117">Forme</span><span class="sxs-lookup"><span data-stu-id="de7f9-117">Hull</span></span> | <span data-ttu-id="de7f9-118">Domain</span><span class="sxs-lookup"><span data-stu-id="de7f9-118">Domain</span></span> | <span data-ttu-id="de7f9-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="de7f9-119">Geometry</span></span> | <span data-ttu-id="de7f9-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="de7f9-120">Pixel</span></span> | <span data-ttu-id="de7f9-121">Compute</span><span class="sxs-lookup"><span data-stu-id="de7f9-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="de7f9-122">X</span><span class="sxs-lookup"><span data-stu-id="de7f9-122">X</span></span>      | <span data-ttu-id="de7f9-123">X</span><span class="sxs-lookup"><span data-stu-id="de7f9-123">X</span></span>    | <span data-ttu-id="de7f9-124">X</span><span class="sxs-lookup"><span data-stu-id="de7f9-124">X</span></span>      | <span data-ttu-id="de7f9-125">X</span><span class="sxs-lookup"><span data-stu-id="de7f9-125">X</span></span>        | <span data-ttu-id="de7f9-126">X</span><span class="sxs-lookup"><span data-stu-id="de7f9-126">X</span></span>     | <span data-ttu-id="de7f9-127">X</span><span class="sxs-lookup"><span data-stu-id="de7f9-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="de7f9-128">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="de7f9-128">Minimum Shader Model</span></span>

<span data-ttu-id="de7f9-129">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="de7f9-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="de7f9-130">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="de7f9-130">Shader Model</span></span>                                              | <span data-ttu-id="de7f9-131">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="de7f9-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="de7f9-132">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="de7f9-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="de7f9-133">Oui</span><span class="sxs-lookup"><span data-stu-id="de7f9-133">yes</span></span>       |
| [<span data-ttu-id="de7f9-134">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="de7f9-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="de7f9-135">non</span><span class="sxs-lookup"><span data-stu-id="de7f9-135">no</span></span>        |
| [<span data-ttu-id="de7f9-136">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="de7f9-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="de7f9-137">non</span><span class="sxs-lookup"><span data-stu-id="de7f9-137">no</span></span>        |
| [<span data-ttu-id="de7f9-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de7f9-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="de7f9-139">non</span><span class="sxs-lookup"><span data-stu-id="de7f9-139">no</span></span>        |
| [<span data-ttu-id="de7f9-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de7f9-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="de7f9-141">non</span><span class="sxs-lookup"><span data-stu-id="de7f9-141">no</span></span>        |
| [<span data-ttu-id="de7f9-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de7f9-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="de7f9-143">non</span><span class="sxs-lookup"><span data-stu-id="de7f9-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="de7f9-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de7f9-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de7f9-145">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de7f9-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





