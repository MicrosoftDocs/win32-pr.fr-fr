---
title: Modificateurs de Registre source du nuanceur de sommets
description: Les modificateurs sources peuvent être appliqués pour modifier les données lues à partir d’un registre source avant que les données ne soient utilisées par l’instruction.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380152"
---
# <a name="vertex-shader-source-register-modifiers"></a><span data-ttu-id="82863-103">Modificateurs de Registre source du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="82863-103">Vertex Shader Source Register Modifiers</span></span>

<span data-ttu-id="82863-104">Les modificateurs sources peuvent être appliqués pour modifier les données lues à partir d’un registre source avant que les données ne soient utilisées par l’instruction.</span><span class="sxs-lookup"><span data-stu-id="82863-104">Source modifiers can be applied to modify the data read from a source register before the data is used by the instruction.</span></span>

## <a name="negate"></a><span data-ttu-id="82863-105">Negate</span><span class="sxs-lookup"><span data-stu-id="82863-105">Negate</span></span>

<span data-ttu-id="82863-106">Nie le contenu du Registre source.</span><span class="sxs-lookup"><span data-stu-id="82863-106">Negate the contents of the source register.</span></span>



| <span data-ttu-id="82863-107">Modificateur de composant</span><span class="sxs-lookup"><span data-stu-id="82863-107">Component modifier</span></span> | <span data-ttu-id="82863-108">Description</span><span class="sxs-lookup"><span data-stu-id="82863-108">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="82863-109">\- r</span><span class="sxs-lookup"><span data-stu-id="82863-109">\- r</span></span>               | <span data-ttu-id="82863-110">Négation source</span><span class="sxs-lookup"><span data-stu-id="82863-110">Source negation</span></span> |



 

<span data-ttu-id="82863-111">Le modificateur de négation ne peut pas être utilisé dans le deuxième Registre source de ces instructions : [M3X2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [M4X4-vs](m4x4---vs.md).</span><span class="sxs-lookup"><span data-stu-id="82863-111">The negate modifier cannot be used on second source register of these instructions: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).</span></span>



| <span data-ttu-id="82863-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="82863-112">Vertex shader versions</span></span> | <span data-ttu-id="82863-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="82863-113">1\_1</span></span> | <span data-ttu-id="82863-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82863-114">2\_0</span></span> | <span data-ttu-id="82863-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="82863-115">2\_x</span></span> | <span data-ttu-id="82863-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="82863-116">2\_sw</span></span> | <span data-ttu-id="82863-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82863-117">3\_0</span></span> | <span data-ttu-id="82863-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="82863-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| \-                     | <span data-ttu-id="82863-119">x</span><span class="sxs-lookup"><span data-stu-id="82863-119">x</span></span>    | <span data-ttu-id="82863-120">x</span><span class="sxs-lookup"><span data-stu-id="82863-120">x</span></span>    | <span data-ttu-id="82863-121">x</span><span class="sxs-lookup"><span data-stu-id="82863-121">x</span></span>    | <span data-ttu-id="82863-122">x</span><span class="sxs-lookup"><span data-stu-id="82863-122">x</span></span>     | <span data-ttu-id="82863-123">x</span><span class="sxs-lookup"><span data-stu-id="82863-123">x</span></span>    | <span data-ttu-id="82863-124">x</span><span class="sxs-lookup"><span data-stu-id="82863-124">x</span></span>     |



 

## <a name="absolute-value"></a><span data-ttu-id="82863-125">Valeur absolue</span><span class="sxs-lookup"><span data-stu-id="82863-125">Absolute Value</span></span>

<span data-ttu-id="82863-126">Prenez la valeur absolue du Registre.</span><span class="sxs-lookup"><span data-stu-id="82863-126">Take the absolute value of the register.</span></span>



| <span data-ttu-id="82863-127">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="82863-127">Vertex shader versions</span></span> | <span data-ttu-id="82863-128">1\_1</span><span class="sxs-lookup"><span data-stu-id="82863-128">1\_1</span></span> | <span data-ttu-id="82863-129">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82863-129">2\_0</span></span> | <span data-ttu-id="82863-130">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="82863-130">2\_x</span></span> | <span data-ttu-id="82863-131">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="82863-131">2\_sw</span></span> | <span data-ttu-id="82863-132">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="82863-132">3\_0</span></span> | <span data-ttu-id="82863-133">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="82863-133">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="82863-134">abs</span><span class="sxs-lookup"><span data-stu-id="82863-134">abs</span></span>                    |      |      |      |       | <span data-ttu-id="82863-135">x</span><span class="sxs-lookup"><span data-stu-id="82863-135">x</span></span>    | <span data-ttu-id="82863-136">x</span><span class="sxs-lookup"><span data-stu-id="82863-136">x</span></span>     |



 

<span data-ttu-id="82863-137">Si un nuanceur de version 3 lit à partir d’un ou de plusieurs registres à virgule flottante constants (c \# ), l’une des conditions suivantes doit être vraie.</span><span class="sxs-lookup"><span data-stu-id="82863-137">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="82863-138">Tous les registres à virgule flottante constantes doivent utiliser le modificateur ABS.</span><span class="sxs-lookup"><span data-stu-id="82863-138">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="82863-139">Aucun des registres à virgule flottante constantes ne peut utiliser le modificateur ABS.</span><span class="sxs-lookup"><span data-stu-id="82863-139">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82863-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82863-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82863-141">Modificateurs de registre de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="82863-141">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




