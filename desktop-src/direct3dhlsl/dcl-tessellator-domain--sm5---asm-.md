---
title: dcl_tessellator_domain (SM5-ASM)
description: Déclarez le domaine du paveur dans une section de déclaration de nuanceur de coque et le nuanceur de domaine.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381226"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a><span data-ttu-id="4add5-103">\_domaine du paveur DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4add5-103">dcl\_tessellator\_domain (sm5 - asm)</span></span>

<span data-ttu-id="4add5-104">Déclarez le domaine du paveur dans une section de déclaration de nuanceur de coque et le nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="4add5-104">Declare the tessellator domain in a hull shader declaration section, and the domain shader.</span></span>



| <span data-ttu-id="4add5-105">DCL \_ du paveur \_ domaine {domaine \_ isoligne </span><span class="sxs-lookup"><span data-stu-id="4add5-105">dcl\_tessellator\_domain {domain\_isoline </span></span>\| <span data-ttu-id="4add5-106">domaine \_ Tri </span><span class="sxs-lookup"><span data-stu-id="4add5-106">domain\_tri </span></span>\| <span data-ttu-id="4add5-107">domaine \_ Quad}</span><span class="sxs-lookup"><span data-stu-id="4add5-107">domain\_quad}</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="4add5-108">Élément</span><span class="sxs-lookup"><span data-stu-id="4add5-108">Item</span></span>                                                                                                                                                                                | <span data-ttu-id="4add5-109">Description</span><span class="sxs-lookup"><span data-stu-id="4add5-109">Description</span></span>                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="4add5-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*Domain \_ isoligne Domain tri domaine- \| \_ \| \_ Quad*</span><span class="sxs-lookup"><span data-stu-id="4add5-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domain\_isoline \| domain\_tri \| domain\_quad*</span></span><br/> | <span data-ttu-id="4add5-111">\[dans \] le domaine.</span><span class="sxs-lookup"><span data-stu-id="4add5-111">\[in\] The domain.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4add5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4add5-112">Remarks</span></span>

<span data-ttu-id="4add5-113">Le comportement n’est pas défini si le nuanceur de coque et le nuanceur de domaine fournissent des domaines incompatibles ou tout autre decalarations en conflit.</span><span class="sxs-lookup"><span data-stu-id="4add5-113">Behavior is undefined if the hull shader and domain shader provide mismatching domains or any other conflicting decalarations.</span></span>

<span data-ttu-id="4add5-114">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4add5-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4add5-115">Sommet</span><span class="sxs-lookup"><span data-stu-id="4add5-115">Vertex</span></span> | <span data-ttu-id="4add5-116">Forme</span><span class="sxs-lookup"><span data-stu-id="4add5-116">Hull</span></span>                 | <span data-ttu-id="4add5-117">Domain</span><span class="sxs-lookup"><span data-stu-id="4add5-117">Domain</span></span> | <span data-ttu-id="4add5-118">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4add5-118">Geometry</span></span> | <span data-ttu-id="4add5-119">Pixel</span><span class="sxs-lookup"><span data-stu-id="4add5-119">Pixel</span></span> | <span data-ttu-id="4add5-120">Compute</span><span class="sxs-lookup"><span data-stu-id="4add5-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="4add5-121">Section déclarations</span><span class="sxs-lookup"><span data-stu-id="4add5-121">Declarations Section</span></span> | <span data-ttu-id="4add5-122">X</span><span class="sxs-lookup"><span data-stu-id="4add5-122">X</span></span>      |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4add5-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4add5-123">Minimum Shader Model</span></span>

<span data-ttu-id="4add5-124">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="4add5-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4add5-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4add5-125">Shader Model</span></span>                                              | <span data-ttu-id="4add5-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4add5-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4add5-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4add5-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4add5-128">Oui</span><span class="sxs-lookup"><span data-stu-id="4add5-128">yes</span></span>       |
| [<span data-ttu-id="4add5-129">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4add5-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4add5-130">non</span><span class="sxs-lookup"><span data-stu-id="4add5-130">no</span></span>        |
| [<span data-ttu-id="4add5-131">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4add5-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4add5-132">non</span><span class="sxs-lookup"><span data-stu-id="4add5-132">no</span></span>        |
| [<span data-ttu-id="4add5-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4add5-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4add5-134">non</span><span class="sxs-lookup"><span data-stu-id="4add5-134">no</span></span>        |
| [<span data-ttu-id="4add5-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4add5-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4add5-136">non</span><span class="sxs-lookup"><span data-stu-id="4add5-136">no</span></span>        |
| [<span data-ttu-id="4add5-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4add5-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4add5-138">non</span><span class="sxs-lookup"><span data-stu-id="4add5-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4add5-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4add5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4add5-140">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4add5-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





