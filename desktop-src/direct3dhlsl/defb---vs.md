---
title: defb-vs
description: Définit une valeur constante booléenne, qui doit être chargée chaque fois qu’un nuanceur est défini sur un appareil.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941016"
---
# <a name="defb---vs"></a><span data-ttu-id="64a2d-103">defb-vs</span><span class="sxs-lookup"><span data-stu-id="64a2d-103">defb - vs</span></span>

<span data-ttu-id="64a2d-104">Définit une valeur constante booléenne, qui doit être chargée chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="64a2d-104">Defines a Boolean constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="64a2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64a2d-105">Syntax</span></span>



| <span data-ttu-id="64a2d-106">defb dest, booleanValue</span><span class="sxs-lookup"><span data-stu-id="64a2d-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="64a2d-107">where</span><span class="sxs-lookup"><span data-stu-id="64a2d-107">where</span></span>

-   <span data-ttu-id="64a2d-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="64a2d-108">dst is the destination register.</span></span>
-   <span data-ttu-id="64a2d-109">booleanValue est une valeur booléenne, true ou false.</span><span class="sxs-lookup"><span data-stu-id="64a2d-109">booleanValue is a boolean value, either True or False.</span></span>

## <a name="remarks"></a><span data-ttu-id="64a2d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="64a2d-110">Remarks</span></span>



| <span data-ttu-id="64a2d-111">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="64a2d-111">Vertex shader versions</span></span> | <span data-ttu-id="64a2d-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="64a2d-112">1\_1</span></span> | <span data-ttu-id="64a2d-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64a2d-113">2\_0</span></span> | <span data-ttu-id="64a2d-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="64a2d-114">2\_x</span></span> | <span data-ttu-id="64a2d-115">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="64a2d-115">2\_sw</span></span> | <span data-ttu-id="64a2d-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64a2d-116">3\_0</span></span> | <span data-ttu-id="64a2d-117">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="64a2d-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="64a2d-118">defb</span><span class="sxs-lookup"><span data-stu-id="64a2d-118">defb</span></span>                   |      | <span data-ttu-id="64a2d-119">x</span><span class="sxs-lookup"><span data-stu-id="64a2d-119">x</span></span>    | <span data-ttu-id="64a2d-120">x</span><span class="sxs-lookup"><span data-stu-id="64a2d-120">x</span></span>    | <span data-ttu-id="64a2d-121">x</span><span class="sxs-lookup"><span data-stu-id="64a2d-121">x</span></span>     | <span data-ttu-id="64a2d-122">x</span><span class="sxs-lookup"><span data-stu-id="64a2d-122">x</span></span>    | <span data-ttu-id="64a2d-123">x</span><span class="sxs-lookup"><span data-stu-id="64a2d-123">x</span></span>     |



 

<span data-ttu-id="64a2d-124">L’instruction defb-vs définit une constante de nuanceur booléenne dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="64a2d-124">The defb - vs instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="64a2d-125">Celles-ci sont appelées constantes immédiates.</span><span class="sxs-lookup"><span data-stu-id="64a2d-125">These are called immediate constants.</span></span> <span data-ttu-id="64a2d-126">Les constantes immédiates sont prioritaires sur les constantes définies par la méthode d’API SetVertexShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="64a2d-126">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantB.</span></span>

<span data-ttu-id="64a2d-127">Il existe deux façons de définir une constante booléenne dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="64a2d-127">There are two ways to set a boolean constant in a shader.</span></span>

1.  <span data-ttu-id="64a2d-128">Utilisez defb-vs pour définir la constante directement à l’intérieur d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="64a2d-128">Use defb - vs to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="64a2d-129">Utilisez les méthodes de l’API pour définir une constante.</span><span class="sxs-lookup"><span data-stu-id="64a2d-129">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="64a2d-130">Utilisez [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) pour définir une constante booléenne.</span><span class="sxs-lookup"><span data-stu-id="64a2d-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64a2d-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64a2d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64a2d-132">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="64a2d-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="64a2d-133">def-vs</span><span class="sxs-lookup"><span data-stu-id="64a2d-133">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="64a2d-134">signatures-vs</span><span class="sxs-lookup"><span data-stu-id="64a2d-134">defi - vs</span></span>](defi---vs.md)
</dt> </dl>

 

 