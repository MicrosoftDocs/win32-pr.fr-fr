---
title: boucle-PS
description: Démarre une boucle... bloc ENDLOOP-PS.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030588"
---
# <a name="loop---ps"></a><span data-ttu-id="6a3f9-103">boucle-PS</span><span class="sxs-lookup"><span data-stu-id="6a3f9-103">loop - ps</span></span>

<span data-ttu-id="6a3f9-104">Démarre une boucle... bloc [ENDLOOP-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="6a3f9-104">Starts a loop...[endloop - ps](endloop---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a3f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a3f9-105">Syntax</span></span>



| <span data-ttu-id="6a3f9-106">boucle aL, i\#</span><span class="sxs-lookup"><span data-stu-id="6a3f9-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="6a3f9-107">Où :</span><span class="sxs-lookup"><span data-stu-id="6a3f9-107">Where:</span></span>

-   <span data-ttu-id="6a3f9-108">aL est le [Registre de compteur de boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) contenant le nombre de boucles actuel.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="6a3f9-109">Je suis \# un [Registre d’entiers constant](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="6a3f9-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span> <span data-ttu-id="6a3f9-110">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a3f9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6a3f9-111">Remarks</span></span>



| <span data-ttu-id="6a3f9-112">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6a3f9-112">Pixel shader versions</span></span> | <span data-ttu-id="6a3f9-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="6a3f9-113">1\_1</span></span> | <span data-ttu-id="6a3f9-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="6a3f9-114">1\_2</span></span> | <span data-ttu-id="6a3f9-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6a3f9-115">1\_3</span></span> | <span data-ttu-id="6a3f9-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="6a3f9-116">1\_4</span></span> | <span data-ttu-id="6a3f9-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6a3f9-117">2\_0</span></span> | <span data-ttu-id="6a3f9-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6a3f9-118">2\_x</span></span> | <span data-ttu-id="6a3f9-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="6a3f9-119">2\_sw</span></span> | <span data-ttu-id="6a3f9-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6a3f9-120">3\_0</span></span> | <span data-ttu-id="6a3f9-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="6a3f9-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6a3f9-122">loop</span><span class="sxs-lookup"><span data-stu-id="6a3f9-122">loop</span></span>                  |      |      |      |      |      |      |       | <span data-ttu-id="6a3f9-123">x</span><span class="sxs-lookup"><span data-stu-id="6a3f9-123">x</span></span>    | <span data-ttu-id="6a3f9-124">x</span><span class="sxs-lookup"><span data-stu-id="6a3f9-124">x</span></span>     |



 

-   <span data-ttu-id="6a3f9-125">Le [Registre de compteurs de boucles](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) contient le nombre de boucles actuel et peut être utilisé pour l’adressage relatif dans le [Registre de couleur d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) à l’intérieur du bloc de boucle.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-125">The [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) holds the current loop count and can be used for relative addressing into [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) inside the loop block.</span></span>
-   <span data-ttu-id="6a3f9-126">i \# . x spécifie le nombre d’itérations.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="6a3f9-127">La plage autorisée est \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="6a3f9-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="6a3f9-128">Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="6a3f9-129">i \# . y spécifie la valeur initiale du Registre du compteur de la [boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al).</span><span class="sxs-lookup"><span data-stu-id="6a3f9-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="6a3f9-130">La plage autorisée est \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="6a3f9-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="6a3f9-131">Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . y.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="6a3f9-132">i \# . z spécifie la taille de l’étape/du Stride.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="6a3f9-133">La plage autorisée est \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="6a3f9-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="6a3f9-134">i \# . w n’est pas utilisé par le bloc de boucle et doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-134">i\#.w is not used by the loop block and has to be 0.</span></span>
-   <span data-ttu-id="6a3f9-135">Les blocs de boucle peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-135">Loop blocks may be nested.</span></span> <span data-ttu-id="6a3f9-136">Consultez [limitations du contrôle de workflow](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="6a3f9-136">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="6a3f9-137">Lorsqu’elle est imbriquée, la valeur du [Registre de compteur de boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) fait référence au bloc de boucle englobant immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="6a3f9-138">Les blocs de boucle sont autorisés à se trouver complètement à l’intérieur d’un bloc if ou à l' \* entourer complètement.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="6a3f9-139">Aucun chevauchement n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="6a3f9-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="6a3f9-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="6a3f9-140">Example</span></span>


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="6a3f9-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6a3f9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a3f9-142">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6a3f9-142">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




