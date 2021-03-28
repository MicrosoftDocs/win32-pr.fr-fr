---
title: boucle-vs
description: Démarrer une boucle... bloc ENDLOOP.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990777"
---
# <a name="loop---vs"></a><span data-ttu-id="af625-103">boucle-vs</span><span class="sxs-lookup"><span data-stu-id="af625-103">loop - vs</span></span>

<span data-ttu-id="af625-104">Démarrer une boucle... bloc [ENDLOOP](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="af625-104">Start a loop...[endloop](endloop---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="af625-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af625-105">Syntax</span></span>



| <span data-ttu-id="af625-106">boucle aL, i\#</span><span class="sxs-lookup"><span data-stu-id="af625-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="af625-107">Où :</span><span class="sxs-lookup"><span data-stu-id="af625-107">Where:</span></span>

-   <span data-ttu-id="af625-108">aL est le [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) contenant le nombre de boucles actuel.</span><span class="sxs-lookup"><span data-stu-id="af625-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="af625-109">Je suis \# un [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="af625-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span> <span data-ttu-id="af625-110">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="af625-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="af625-111">Notes</span><span class="sxs-lookup"><span data-stu-id="af625-111">Remarks</span></span>



| <span data-ttu-id="af625-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="af625-112">Vertex shader versions</span></span> | <span data-ttu-id="af625-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="af625-113">1\_1</span></span> | <span data-ttu-id="af625-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af625-114">2\_0</span></span> | <span data-ttu-id="af625-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="af625-115">2\_x</span></span> | <span data-ttu-id="af625-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="af625-116">2\_sw</span></span> | <span data-ttu-id="af625-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af625-117">3\_0</span></span> | <span data-ttu-id="af625-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="af625-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="af625-119">loop</span><span class="sxs-lookup"><span data-stu-id="af625-119">loop</span></span>                   |      | <span data-ttu-id="af625-120">x</span><span class="sxs-lookup"><span data-stu-id="af625-120">x</span></span>    | <span data-ttu-id="af625-121">x</span><span class="sxs-lookup"><span data-stu-id="af625-121">x</span></span>    | <span data-ttu-id="af625-122">x</span><span class="sxs-lookup"><span data-stu-id="af625-122">x</span></span>     | <span data-ttu-id="af625-123">x</span><span class="sxs-lookup"><span data-stu-id="af625-123">x</span></span>    | <span data-ttu-id="af625-124">x</span><span class="sxs-lookup"><span data-stu-id="af625-124">x</span></span>     |



 

-   <span data-ttu-id="af625-125">Le [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) contient le nombre de boucles actuel et peut être utilisé pour l’adressage relatif dans un [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) ou des registres de [sortie](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) à l’intérieur du bloc de boucle.</span><span class="sxs-lookup"><span data-stu-id="af625-125">The [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) holds the current loop count, and can be used for relative addressing into [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c\#) or [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) inside the loop block.</span></span>
-   <span data-ttu-id="af625-126">i \# . x spécifie le nombre d’itérations.</span><span class="sxs-lookup"><span data-stu-id="af625-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="af625-127">La plage autorisée est \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="af625-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="af625-128">Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="af625-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="af625-129">i \# . y spécifie la valeur initiale du Registre du compteur de la [boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al).</span><span class="sxs-lookup"><span data-stu-id="af625-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="af625-130">La plage autorisée est \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="af625-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="af625-131">Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . y.</span><span class="sxs-lookup"><span data-stu-id="af625-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="af625-132">i \# . z spécifie la taille de l’étape/du Stride.</span><span class="sxs-lookup"><span data-stu-id="af625-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="af625-133">La plage autorisée est \[ -128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="af625-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="af625-134">i \# . w n’est pas utilisé et doit être défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="af625-134">i\#.w is not used and must be set to 0.</span></span>
-   <span data-ttu-id="af625-135">Les blocs de boucle peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="af625-135">Loop blocks may be nested.</span></span> <span data-ttu-id="af625-136">Consultez [limites d’imbrication des contrôles de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="af625-136">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="af625-137">Lorsqu’elle est imbriquée, la valeur du [Registre de compteur de boucle](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) fait référence au bloc de boucle englobant immédiatement.</span><span class="sxs-lookup"><span data-stu-id="af625-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="af625-138">Les blocs de boucle sont autorisés à se trouver complètement à l’intérieur d’un bloc if ou à l' \* entourer complètement.</span><span class="sxs-lookup"><span data-stu-id="af625-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="af625-139">Aucun chevauchement n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="af625-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="af625-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="af625-140">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="af625-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af625-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af625-142">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="af625-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




