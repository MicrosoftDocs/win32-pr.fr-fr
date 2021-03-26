---
title: def-PS
description: Définit des constantes à virgule flottante de nuanceur de pixels.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031798"
---
# <a name="def---ps"></a><span data-ttu-id="24747-103">def-PS</span><span class="sxs-lookup"><span data-stu-id="24747-103">def - ps</span></span>

<span data-ttu-id="24747-104">Définit des constantes à virgule flottante de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="24747-104">Defines pixel shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="24747-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24747-105">Syntax</span></span>



| <span data-ttu-id="24747-106">def DST, fVvalue1, fValue2, fValue3, fValue4</span><span class="sxs-lookup"><span data-stu-id="24747-106">def dst, fVvalue1, fValue2, fValue3, fValue4</span></span> |
|----------------------------------------------|



 

<span data-ttu-id="24747-107">Où :</span><span class="sxs-lookup"><span data-stu-id="24747-107">Where:</span></span>

-   <span data-ttu-id="24747-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="24747-108">dst is the destination register.</span></span>
-   <span data-ttu-id="24747-109">fValue1 à fValue4 sont des valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="24747-109">fValue1 to fValue4 are floating-point values..</span></span>

## <a name="remarks"></a><span data-ttu-id="24747-110">Notes</span><span class="sxs-lookup"><span data-stu-id="24747-110">Remarks</span></span>



| <span data-ttu-id="24747-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="24747-111">Pixel shader versions</span></span> | <span data-ttu-id="24747-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="24747-112">1\_1</span></span> | <span data-ttu-id="24747-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="24747-113">1\_2</span></span> | <span data-ttu-id="24747-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="24747-114">1\_3</span></span> | <span data-ttu-id="24747-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="24747-115">1\_4</span></span> | <span data-ttu-id="24747-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="24747-116">2\_0</span></span> | <span data-ttu-id="24747-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="24747-117">2\_x</span></span> | <span data-ttu-id="24747-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="24747-118">2\_sw</span></span> | <span data-ttu-id="24747-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="24747-119">3\_0</span></span> | <span data-ttu-id="24747-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="24747-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="24747-121">def</span><span class="sxs-lookup"><span data-stu-id="24747-121">def</span></span>                   | <span data-ttu-id="24747-122">x</span><span class="sxs-lookup"><span data-stu-id="24747-122">x</span></span>    | <span data-ttu-id="24747-123">x</span><span class="sxs-lookup"><span data-stu-id="24747-123">x</span></span>    | <span data-ttu-id="24747-124">x</span><span class="sxs-lookup"><span data-stu-id="24747-124">x</span></span>    | <span data-ttu-id="24747-125">x</span><span class="sxs-lookup"><span data-stu-id="24747-125">x</span></span>    | <span data-ttu-id="24747-126">x</span><span class="sxs-lookup"><span data-stu-id="24747-126">x</span></span>    | <span data-ttu-id="24747-127">x</span><span class="sxs-lookup"><span data-stu-id="24747-127">x</span></span>    | <span data-ttu-id="24747-128">x</span><span class="sxs-lookup"><span data-stu-id="24747-128">x</span></span>     | <span data-ttu-id="24747-129">x</span><span class="sxs-lookup"><span data-stu-id="24747-129">x</span></span>    | <span data-ttu-id="24747-130">x</span><span class="sxs-lookup"><span data-stu-id="24747-130">x</span></span>     |



 

<span data-ttu-id="24747-131">Il existe deux façons de définir une constante à virgule flottante dans un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="24747-131">There are two ways to set a floating-point constant in a pixel shader.</span></span>

1.  <span data-ttu-id="24747-132">Utilisez DEF pour définir la constante directement à l’intérieur d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="24747-132">Use def to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="24747-133">Utilisez l’API pour définir une constante avec [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="24747-133">Use the API to set a constant with [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="24747-134">def définit une constante de nuanceur dont la valeur est chargée à chaque fois qu’un nuanceur est défini sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="24747-134">def defines a shader constant whose value is loaded any time a shader is set to a device.</span></span> <span data-ttu-id="24747-135">Celles-ci sont appelées constantes immédiates.</span><span class="sxs-lookup"><span data-stu-id="24747-135">These are called immediate constants.</span></span> <span data-ttu-id="24747-136">Les constantes immédiates sont prioritaires sur les constantes définies par la méthode API.</span><span class="sxs-lookup"><span data-stu-id="24747-136">Immediate constants take precedence over constants set by the API method.</span></span>

-   <span data-ttu-id="24747-137">Doit apparaître avant la première instruction arithmétique ou d’adressage dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="24747-137">Must appear before the first arithmetic or addressing instruction in shader.</span></span>
-   <span data-ttu-id="24747-138">Peut être mélangé avec les instructions [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) (qui sont l’autre type d’instruction qui réside au début d’un nuanceur).</span><span class="sxs-lookup"><span data-stu-id="24747-138">Can be intermixed with [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) instructions (which are the other type of instruction that resides at the beginning of a shader).</span></span>
-   <span data-ttu-id="24747-139">le registre de l’heure d’été doit être un [Registre constant](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="24747-139">dst register must be a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>
-   <span data-ttu-id="24747-140">Le masque d’écriture doit être complet (par défaut).</span><span class="sxs-lookup"><span data-stu-id="24747-140">Write mask must be full (default).</span></span>
-   <span data-ttu-id="24747-141">Si un [Registre de constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) est défini plusieurs fois dans un nuanceur, le dernier est conservé.</span><span class="sxs-lookup"><span data-stu-id="24747-141">If a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) is defined multiple times in a shader, the last one persists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24747-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24747-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24747-143">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="24747-143">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 