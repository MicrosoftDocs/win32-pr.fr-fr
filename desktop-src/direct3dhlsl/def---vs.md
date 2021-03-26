---
title: def-vs
description: Définit des constantes de nuanceur de sommets.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199359"
---
# <a name="def---vs"></a><span data-ttu-id="27675-103">def-vs</span><span class="sxs-lookup"><span data-stu-id="27675-103">def - vs</span></span>

<span data-ttu-id="27675-104">Définit des constantes de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="27675-104">Defines vertex shader constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="27675-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27675-105">Syntax</span></span>



| <span data-ttu-id="27675-106">def DST, float1, float2, float3, float4</span><span class="sxs-lookup"><span data-stu-id="27675-106">def dst, float1, float2, float3, float4</span></span> |
|-----------------------------------------|



 

<span data-ttu-id="27675-107">where</span><span class="sxs-lookup"><span data-stu-id="27675-107">where</span></span>

-   <span data-ttu-id="27675-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="27675-108">dst is the destination register.</span></span>
-   <span data-ttu-id="27675-109">float1, float2, float3, float4 sont des nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="27675-109">float1, float2, float3, float4 are four floating point numbers.</span></span>

## <a name="remarks"></a><span data-ttu-id="27675-110">Notes</span><span class="sxs-lookup"><span data-stu-id="27675-110">Remarks</span></span>



| <span data-ttu-id="27675-111">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="27675-111">Vertex shader versions</span></span> | <span data-ttu-id="27675-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="27675-112">1\_1</span></span> | <span data-ttu-id="27675-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27675-113">2\_0</span></span> | <span data-ttu-id="27675-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="27675-114">2\_x</span></span> | <span data-ttu-id="27675-115">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="27675-115">2\_sw</span></span> | <span data-ttu-id="27675-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27675-116">3\_0</span></span> | <span data-ttu-id="27675-117">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="27675-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="27675-118">def</span><span class="sxs-lookup"><span data-stu-id="27675-118">def</span></span>                    | <span data-ttu-id="27675-119">x</span><span class="sxs-lookup"><span data-stu-id="27675-119">x</span></span>    | <span data-ttu-id="27675-120">x</span><span class="sxs-lookup"><span data-stu-id="27675-120">x</span></span>    | <span data-ttu-id="27675-121">x</span><span class="sxs-lookup"><span data-stu-id="27675-121">x</span></span>    | <span data-ttu-id="27675-122">x</span><span class="sxs-lookup"><span data-stu-id="27675-122">x</span></span>     | <span data-ttu-id="27675-123">x</span><span class="sxs-lookup"><span data-stu-id="27675-123">x</span></span>    | <span data-ttu-id="27675-124">x</span><span class="sxs-lookup"><span data-stu-id="27675-124">x</span></span>     |



 

<span data-ttu-id="27675-125">L’instruction def définit une constante de nuanceur dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="27675-125">The def instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="27675-126">Celles-ci sont appelées constantes immédiates.</span><span class="sxs-lookup"><span data-stu-id="27675-126">These are called immediate constants.</span></span> <span data-ttu-id="27675-127">Les constantes immédiates sont prioritaires sur les constantes définies par les méthodes d’API SetVertexShaderConstantF.</span><span class="sxs-lookup"><span data-stu-id="27675-127">Immediate constants take precedence over constants set by API methods SetVertexShaderConstantF.</span></span>

<span data-ttu-id="27675-128">Il existe deux façons de définir une constante dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="27675-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="27675-129">Utilisez DEF-vs pour définir la constante directement à l’intérieur d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="27675-129">Use def - vs to define the constant directly inside a shader.</span></span>

    <span data-ttu-id="27675-130">def-vs ne peut définir que des constantes à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="27675-130">def - vs can only define floating-point constants.</span></span>

2.  <span data-ttu-id="27675-131">Utilisez les méthodes de l’API pour définir une constante.</span><span class="sxs-lookup"><span data-stu-id="27675-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="27675-132">Utilisez [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) pour définir une constante à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="27675-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) to set a floating-point constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27675-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27675-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27675-134">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="27675-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="27675-135">signatures-vs</span><span class="sxs-lookup"><span data-stu-id="27675-135">defi - vs</span></span>](defi---vs.md)
</dt> <dt>

[<span data-ttu-id="27675-136">defb-vs</span><span class="sxs-lookup"><span data-stu-id="27675-136">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 