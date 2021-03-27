---
title: dcl_resource structuré (SM5-ASM)
description: Déclarez une entrée de ressource de nuanceur et affectez-la à un registre d’espace réservé t \ a pour la ressource. | dcl_resource structuré (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211429"
---
# <a name="dcl_resource-structured-sm5---asm"></a><span data-ttu-id="5ad7d-104">\_ressource DCL structurée (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="5ad7d-104">dcl\_resource structured (sm5 - asm)</span></span>

<span data-ttu-id="5ad7d-105">Déclarez une entrée de ressource de nuanceur et affectez-la à un \# Registre d’espace réservé t-a pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="5ad7d-105">Declare a shader resource input and assign it to a t\# - a placeholder register for the resource.</span></span>



| <span data-ttu-id="5ad7d-106">\_ \_ dstSRV structurée des ressources DCL, structByteStride</span><span class="sxs-lookup"><span data-stu-id="5ad7d-106">dcl\_resource\_structured dstSRV, structByteStride</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="5ad7d-107">Élément</span><span class="sxs-lookup"><span data-stu-id="5ad7d-107">Item</span></span>                                                                                                                                   | <span data-ttu-id="5ad7d-108">Description</span><span class="sxs-lookup"><span data-stu-id="5ad7d-108">Description</span></span>                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad7d-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span><span class="sxs-lookup"><span data-stu-id="5ad7d-109"><span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*</span></span><br/>                                         | <span data-ttu-id="5ad7d-110">\[dans \] un \# Registre t déclaré comme référence à un ShaderResourceView d’une mémoire tampon structurée avec la valeur Stride spécifiée qui doit être liée à \# l’emplacement SRV au niveau de l’API.</span><span class="sxs-lookup"><span data-stu-id="5ad7d-110">\[in\] A t\# register declared as a reference to a ShaderResourceView of a structured buffer with the specified stride that must be bound to SRV slot \# at the API.</span></span> <br/> |
| <span data-ttu-id="5ad7d-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="5ad7d-111"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="5ad7d-112">\[dans \] un uint qui spécifie la taille de la structure en octets dans la mémoire tampon en cours de déclaration.</span><span class="sxs-lookup"><span data-stu-id="5ad7d-112">\[in\] A uint that specifies the size of the structure in bytes in the buffer being declared.</span></span> <span data-ttu-id="5ad7d-113">Cette valeur doit être supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="5ad7d-113">This value must be greater than zero.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="5ad7d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5ad7d-114">Remarks</span></span>

<span data-ttu-id="5ad7d-115">Le contenu de la structure n’a pas de type ; les opérations effectuées sur la mémoire peuvent interpréter implicitement les données comme ayant un type.</span><span class="sxs-lookup"><span data-stu-id="5ad7d-115">The contents of the structure have no type; operations performed on the memory may implicitly interpret the data as having a type.</span></span>

<span data-ttu-id="5ad7d-116">Les instructions qui font référence à un t structuré \# acceptent une adresse 2D, où le premier composant choisit la \[ structure \] , et le deuxième composant choisit le \[ décalage dans le struct, multiple de 32 bits \] .</span><span class="sxs-lookup"><span data-stu-id="5ad7d-116">Instructions that reference a structured t\# take a 2D address, where the first component picks \[struct\], and the second component picks \[offset within struct, multiple of 32-bits\].</span></span>

<span data-ttu-id="5ad7d-117">CS \_ 4 \_ 0 et CS \_ 4 \_ 1 prennent en charge cette instruction.</span><span class="sxs-lookup"><span data-stu-id="5ad7d-117">cs\_4\_0 and cs\_4\_1 support this instruction.</span></span>

<span data-ttu-id="5ad7d-118">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="5ad7d-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5ad7d-119">Sommet</span><span class="sxs-lookup"><span data-stu-id="5ad7d-119">Vertex</span></span> | <span data-ttu-id="5ad7d-120">Forme</span><span class="sxs-lookup"><span data-stu-id="5ad7d-120">Hull</span></span> | <span data-ttu-id="5ad7d-121">Domain</span><span class="sxs-lookup"><span data-stu-id="5ad7d-121">Domain</span></span> | <span data-ttu-id="5ad7d-122">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5ad7d-122">Geometry</span></span> | <span data-ttu-id="5ad7d-123">Pixel</span><span class="sxs-lookup"><span data-stu-id="5ad7d-123">Pixel</span></span> | <span data-ttu-id="5ad7d-124">Compute</span><span class="sxs-lookup"><span data-stu-id="5ad7d-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5ad7d-125">X</span><span class="sxs-lookup"><span data-stu-id="5ad7d-125">X</span></span>      | <span data-ttu-id="5ad7d-126">X</span><span class="sxs-lookup"><span data-stu-id="5ad7d-126">X</span></span>    | <span data-ttu-id="5ad7d-127">X</span><span class="sxs-lookup"><span data-stu-id="5ad7d-127">X</span></span>      | <span data-ttu-id="5ad7d-128">X</span><span class="sxs-lookup"><span data-stu-id="5ad7d-128">X</span></span>        | <span data-ttu-id="5ad7d-129">X</span><span class="sxs-lookup"><span data-stu-id="5ad7d-129">X</span></span>     | <span data-ttu-id="5ad7d-130">X</span><span class="sxs-lookup"><span data-stu-id="5ad7d-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5ad7d-131">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5ad7d-131">Minimum Shader Model</span></span>

<span data-ttu-id="5ad7d-132">Cette instruction est prise en charge dans les modèles de nuanceur suivants :</span><span class="sxs-lookup"><span data-stu-id="5ad7d-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="5ad7d-133">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5ad7d-133">Shader Model</span></span>                                              | <span data-ttu-id="5ad7d-134">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5ad7d-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5ad7d-135">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5ad7d-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5ad7d-136">Oui</span><span class="sxs-lookup"><span data-stu-id="5ad7d-136">yes</span></span>       |
| [<span data-ttu-id="5ad7d-137">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="5ad7d-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5ad7d-138">non</span><span class="sxs-lookup"><span data-stu-id="5ad7d-138">no</span></span>        |
| [<span data-ttu-id="5ad7d-139">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5ad7d-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5ad7d-140">non</span><span class="sxs-lookup"><span data-stu-id="5ad7d-140">no</span></span>        |
| [<span data-ttu-id="5ad7d-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ad7d-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5ad7d-142">non</span><span class="sxs-lookup"><span data-stu-id="5ad7d-142">no</span></span>        |
| [<span data-ttu-id="5ad7d-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ad7d-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5ad7d-144">non</span><span class="sxs-lookup"><span data-stu-id="5ad7d-144">no</span></span>        |
| [<span data-ttu-id="5ad7d-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ad7d-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5ad7d-146">non</span><span class="sxs-lookup"><span data-stu-id="5ad7d-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5ad7d-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ad7d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ad7d-148">Assembly modèle 5 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ad7d-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





