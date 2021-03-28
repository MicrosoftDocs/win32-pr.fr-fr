---
title: dcl_temps (SM4-ASM)
description: DCL \_ temps (SM4-ASM)
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc3a468575b30836d4574edb13c4fc77a3505fc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990824"
---
# <a name="dcl_temps-sm4---asm"></a><span data-ttu-id="4ee42-103">DCL \_ temps (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4ee42-103">dcl\_temps (sm4 - asm)</span></span>

<span data-ttu-id="4ee42-104">Déclare des registres temporaires.</span><span class="sxs-lookup"><span data-stu-id="4ee42-104">Declares temporary registers.</span></span>



| <span data-ttu-id="4ee42-105">DCL- \_ temps N</span><span class="sxs-lookup"><span data-stu-id="4ee42-105">dcl\_temps N</span></span> |
|--------------|



 



| <span data-ttu-id="4ee42-106">Élément</span><span class="sxs-lookup"><span data-stu-id="4ee42-106">Item</span></span>                                                   | <span data-ttu-id="4ee42-107">Description</span><span class="sxs-lookup"><span data-stu-id="4ee42-107">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4ee42-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="4ee42-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="4ee42-109">\[dans \] le nombre de registres temporaires.</span><span class="sxs-lookup"><span data-stu-id="4ee42-109">\[in\] The number of temporary registers.</span></span><br/> |



 

<span data-ttu-id="4ee42-110">Chaque registre dispose d’espace pour une valeur de quatre composants de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4ee42-110">Each register has space for a 32-bit four-component value.</span></span> <span data-ttu-id="4ee42-111">Le nombre total de registres temporaires et [indexables-temporaires](dcl-indexabletemp.md) doit être inférieur ou égal à 4096.</span><span class="sxs-lookup"><span data-stu-id="4ee42-111">The total number of temporary and [indexable-temporary](dcl-indexabletemp.md) registers must be less than or equal to 4096.</span></span>

<span data-ttu-id="4ee42-112">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="4ee42-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4ee42-113">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="4ee42-113">Vertex Shader</span></span> | <span data-ttu-id="4ee42-114">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="4ee42-114">Geometry Shader</span></span> | <span data-ttu-id="4ee42-115">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="4ee42-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4ee42-116">x</span><span class="sxs-lookup"><span data-stu-id="4ee42-116">x</span></span>             | <span data-ttu-id="4ee42-117">x</span><span class="sxs-lookup"><span data-stu-id="4ee42-117">x</span></span>               | <span data-ttu-id="4ee42-118">x</span><span class="sxs-lookup"><span data-stu-id="4ee42-118">x</span></span>            |



 

<span data-ttu-id="4ee42-119">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="4ee42-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="4ee42-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="4ee42-120">Example</span></span>

<span data-ttu-id="4ee42-121">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="4ee42-121">Here is an example.</span></span>


```
dcl_temps 10; // Declare r0-r9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="4ee42-122">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="4ee42-122">Minimum Shader Model</span></span>

<span data-ttu-id="4ee42-123">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="4ee42-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4ee42-124">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4ee42-124">Shader Model</span></span>                                              | <span data-ttu-id="4ee42-125">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="4ee42-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4ee42-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4ee42-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4ee42-127">Oui</span><span class="sxs-lookup"><span data-stu-id="4ee42-127">yes</span></span>       |
| [<span data-ttu-id="4ee42-128">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="4ee42-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4ee42-129">Oui</span><span class="sxs-lookup"><span data-stu-id="4ee42-129">yes</span></span>       |
| [<span data-ttu-id="4ee42-130">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="4ee42-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4ee42-131">Oui</span><span class="sxs-lookup"><span data-stu-id="4ee42-131">yes</span></span>       |
| [<span data-ttu-id="4ee42-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ee42-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4ee42-133">non</span><span class="sxs-lookup"><span data-stu-id="4ee42-133">no</span></span>        |
| [<span data-ttu-id="4ee42-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ee42-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4ee42-135">non</span><span class="sxs-lookup"><span data-stu-id="4ee42-135">no</span></span>        |
| [<span data-ttu-id="4ee42-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ee42-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4ee42-137">non</span><span class="sxs-lookup"><span data-stu-id="4ee42-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4ee42-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ee42-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ee42-139">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4ee42-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





