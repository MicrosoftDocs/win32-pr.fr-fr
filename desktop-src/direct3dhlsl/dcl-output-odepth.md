---
title: dcl_output oDepth (SM4-ASM)
description: '\_oDepth de sortie DCL (SM4-ASM)'
ms.assetid: 7ee3026d-507f-4aa8-8335-d92c5f649f46
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43580a542c1a66961cfa7434c65cd8d271fb0367
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313756"
---
# <a name="dcl_output-odepth-sm4---asm"></a><span data-ttu-id="f3987-103">\_oDepth de sortie DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f3987-103">dcl\_output oDepth (sm4 - asm)</span></span>

<span data-ttu-id="f3987-104">Déclare qu’un nuanceur de pixels utilise le registre de profondeur de sortie.</span><span class="sxs-lookup"><span data-stu-id="f3987-104">Declares that a pixel shader will use the output-depth register.</span></span>



| <span data-ttu-id="f3987-105">\_oDepth de sortie DCL</span><span class="sxs-lookup"><span data-stu-id="f3987-105">dcl\_output oDepth</span></span> |
|--------------------|



 

<span data-ttu-id="f3987-106">La valeur du registre de profondeur de sortie est utilisée au cours d’une comparaison de profondeur (si la comparaison de profondeur est activée).</span><span class="sxs-lookup"><span data-stu-id="f3987-106">The value in the output-depth register is used during a depth comparison (if depth compare is enabled).</span></span>

<span data-ttu-id="f3987-107">Cette instruction s’applique aux étapes suivantes du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="f3987-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f3987-108">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="f3987-108">Vertex Shader</span></span> | <span data-ttu-id="f3987-109">Nuanceur de géométrie</span><span class="sxs-lookup"><span data-stu-id="f3987-109">Geometry Shader</span></span> | <span data-ttu-id="f3987-110">Nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f3987-110">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="f3987-111">x</span><span class="sxs-lookup"><span data-stu-id="f3987-111">x</span></span>            |



 

<span data-ttu-id="f3987-112">Cette instruction est incluse pour faciliter le débogage d’un nuanceur dans l’assembly. vous ne pouvez pas créer de nuanceur dans un langage assembleur à l’aide du nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="f3987-112">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="f3987-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="f3987-113">Example</span></span>

<span data-ttu-id="f3987-114">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="f3987-114">Here are some examples.</span></span>


```
dcl_output oDepth
```



## <a name="minimum-shader-model"></a><span data-ttu-id="f3987-115">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="f3987-115">Minimum Shader Model</span></span>

<span data-ttu-id="f3987-116">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="f3987-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f3987-117">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f3987-117">Shader Model</span></span>                                              | <span data-ttu-id="f3987-118">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="f3987-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f3987-119">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="f3987-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f3987-120">Oui</span><span class="sxs-lookup"><span data-stu-id="f3987-120">yes</span></span>       |
| [<span data-ttu-id="f3987-121">Modèle de nuanceur 4,1</span><span class="sxs-lookup"><span data-stu-id="f3987-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f3987-122">Oui</span><span class="sxs-lookup"><span data-stu-id="f3987-122">yes</span></span>       |
| [<span data-ttu-id="f3987-123">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="f3987-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f3987-124">Oui</span><span class="sxs-lookup"><span data-stu-id="f3987-124">yes</span></span>       |
| [<span data-ttu-id="f3987-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3987-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f3987-126">non</span><span class="sxs-lookup"><span data-stu-id="f3987-126">no</span></span>        |
| [<span data-ttu-id="f3987-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3987-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f3987-128">non</span><span class="sxs-lookup"><span data-stu-id="f3987-128">no</span></span>        |
| [<span data-ttu-id="f3987-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3987-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f3987-130">non</span><span class="sxs-lookup"><span data-stu-id="f3987-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f3987-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3987-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3987-132">Assembly modèle 4 du nuanceur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f3987-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




