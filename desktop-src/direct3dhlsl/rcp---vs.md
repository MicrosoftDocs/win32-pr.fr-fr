---
title: RCP-vs
description: Calcule la réciproque du scalaire source. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974383"
---
# <a name="rcp---vs"></a><span data-ttu-id="65956-104">RCP-vs</span><span class="sxs-lookup"><span data-stu-id="65956-104">rcp - vs</span></span>

<span data-ttu-id="65956-105">Calcule la réciproque du scalaire source.</span><span class="sxs-lookup"><span data-stu-id="65956-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="65956-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65956-106">Syntax</span></span>



| <span data-ttu-id="65956-107">RCP DST, SRC</span><span class="sxs-lookup"><span data-stu-id="65956-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="65956-108">where</span><span class="sxs-lookup"><span data-stu-id="65956-108">where</span></span>

-   <span data-ttu-id="65956-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="65956-109">dst is the destination register.</span></span>
-   <span data-ttu-id="65956-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="65956-110">src is a source register.</span></span> <span data-ttu-id="65956-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="65956-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="65956-112">Notes</span><span class="sxs-lookup"><span data-stu-id="65956-112">Remarks</span></span>



| <span data-ttu-id="65956-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="65956-113">Vertex shader versions</span></span> | <span data-ttu-id="65956-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="65956-114">1\_1</span></span> | <span data-ttu-id="65956-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="65956-115">2\_0</span></span> | <span data-ttu-id="65956-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="65956-116">2\_x</span></span> | <span data-ttu-id="65956-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="65956-117">2\_sw</span></span> | <span data-ttu-id="65956-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="65956-118">3\_0</span></span> | <span data-ttu-id="65956-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="65956-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="65956-120">rcp</span><span class="sxs-lookup"><span data-stu-id="65956-120">rcp</span></span>                    | <span data-ttu-id="65956-121">x</span><span class="sxs-lookup"><span data-stu-id="65956-121">x</span></span>    | <span data-ttu-id="65956-122">x</span><span class="sxs-lookup"><span data-stu-id="65956-122">x</span></span>    | <span data-ttu-id="65956-123">x</span><span class="sxs-lookup"><span data-stu-id="65956-123">x</span></span>    | <span data-ttu-id="65956-124">x</span><span class="sxs-lookup"><span data-stu-id="65956-124">x</span></span>     | <span data-ttu-id="65956-125">x</span><span class="sxs-lookup"><span data-stu-id="65956-125">x</span></span>    | <span data-ttu-id="65956-126">x</span><span class="sxs-lookup"><span data-stu-id="65956-126">x</span></span>     |



 

<span data-ttu-id="65956-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="65956-127">The following code fragment shows the operations performed.</span></span>


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



<span data-ttu-id="65956-128">La sortie doit être exactement 1,0 si l’entrée est exactement 1,0.</span><span class="sxs-lookup"><span data-stu-id="65956-128">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="65956-129">Une source de 0,0 donne l’infini.</span><span class="sxs-lookup"><span data-stu-id="65956-129">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="65956-130">La précision doit être d’au moins 1,0/(2 ² ²) erreur absolue sur la plage (1,0, 2,0), car les implémentations courantes séparent la mantisse et l’exposant.</span><span class="sxs-lookup"><span data-stu-id="65956-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="65956-131">Si la source n’a aucun sous-script, le composant x est utilisé.</span><span class="sxs-lookup"><span data-stu-id="65956-131">If the source has no subscripts, the x-component is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65956-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65956-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65956-133">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="65956-133">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




