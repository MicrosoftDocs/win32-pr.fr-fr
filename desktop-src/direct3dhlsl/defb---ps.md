---
title: defb-PS
description: Définit une valeur constante booléenne, qui doit être chargée à chaque fois qu’un nuanceur est défini sur un appareil.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729173"
---
# <a name="defb---ps"></a><span data-ttu-id="caa91-103">defb-PS</span><span class="sxs-lookup"><span data-stu-id="caa91-103">defb - ps</span></span>

<span data-ttu-id="caa91-104">Définit une valeur constante booléenne, qui doit être chargée à chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="caa91-104">Defines a boolean constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="caa91-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caa91-105">Syntax</span></span>



| <span data-ttu-id="caa91-106">defb dest, booleanValue</span><span class="sxs-lookup"><span data-stu-id="caa91-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="caa91-107">where</span><span class="sxs-lookup"><span data-stu-id="caa91-107">where</span></span>

-   <span data-ttu-id="caa91-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="caa91-108">dst is the destination register.</span></span>
-   <span data-ttu-id="caa91-109">booleanValue est une valeur booléenne unique, true ou false.</span><span class="sxs-lookup"><span data-stu-id="caa91-109">booleanValue is a single boolean value, either true or false.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa91-110">Notes</span><span class="sxs-lookup"><span data-stu-id="caa91-110">Remarks</span></span>



| <span data-ttu-id="caa91-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="caa91-111">Pixel shader versions</span></span> | <span data-ttu-id="caa91-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="caa91-112">1\_1</span></span> | <span data-ttu-id="caa91-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="caa91-113">1\_2</span></span> | <span data-ttu-id="caa91-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="caa91-114">1\_3</span></span> | <span data-ttu-id="caa91-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="caa91-115">1\_4</span></span> | <span data-ttu-id="caa91-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="caa91-116">2\_0</span></span> | <span data-ttu-id="caa91-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="caa91-117">2\_x</span></span> | <span data-ttu-id="caa91-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="caa91-118">2\_sw</span></span> | <span data-ttu-id="caa91-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="caa91-119">3\_0</span></span> | <span data-ttu-id="caa91-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="caa91-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="caa91-121">defb</span><span class="sxs-lookup"><span data-stu-id="caa91-121">defb</span></span>                  |      |      |      |      |      | <span data-ttu-id="caa91-122">x</span><span class="sxs-lookup"><span data-stu-id="caa91-122">x</span></span>    | <span data-ttu-id="caa91-123">x</span><span class="sxs-lookup"><span data-stu-id="caa91-123">x</span></span>     | <span data-ttu-id="caa91-124">x</span><span class="sxs-lookup"><span data-stu-id="caa91-124">x</span></span>    | <span data-ttu-id="caa91-125">x</span><span class="sxs-lookup"><span data-stu-id="caa91-125">x</span></span>     |



 

<span data-ttu-id="caa91-126">L’instruction defb définit une constante de nuanceur booléenne dont la valeur est chargée chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="caa91-126">The defb instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="caa91-127">Celles-ci sont appelées constantes immédiates.</span><span class="sxs-lookup"><span data-stu-id="caa91-127">These are called immediate constants.</span></span> <span data-ttu-id="caa91-128">Les constantes immédiates sont prioritaires sur les constantes définies par la méthode d’API SetPixelShaderConstantB.</span><span class="sxs-lookup"><span data-stu-id="caa91-128">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="caa91-129">Il existe deux façons de définir un BooleanConstant dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="caa91-129">There are two ways to set a booleanconstant in a shader.</span></span>

1.  <span data-ttu-id="caa91-130">Utilisez defb pour définir la constante directement à l’intérieur d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="caa91-130">Use defb to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="caa91-131">Utilisez les méthodes de l’API pour définir une constante.</span><span class="sxs-lookup"><span data-stu-id="caa91-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="caa91-132">Utilisez [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) pour définir une constante booléenne.</span><span class="sxs-lookup"><span data-stu-id="caa91-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="caa91-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="caa91-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caa91-134">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="caa91-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="caa91-135">def-PS</span><span class="sxs-lookup"><span data-stu-id="caa91-135">def - ps</span></span>](def---ps.md)
</dt> <dt>

[<span data-ttu-id="caa91-136">DEFAUT-PS</span><span class="sxs-lookup"><span data-stu-id="caa91-136">defi - ps</span></span>](defi---ps.md)
</dt> </dl>

 

 