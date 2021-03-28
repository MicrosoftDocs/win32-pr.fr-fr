---
title: rsq-vs
description: Calcule la racine carrée réciproque (positive uniquement) du scalaire source. | rsq-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974271"
---
# <a name="rsq---vs"></a><span data-ttu-id="b5653-104">rsq-vs</span><span class="sxs-lookup"><span data-stu-id="b5653-104">rsq - vs</span></span>

<span data-ttu-id="b5653-105">Calcule la racine carrée réciproque (positive uniquement) du scalaire source.</span><span class="sxs-lookup"><span data-stu-id="b5653-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5653-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5653-106">Syntax</span></span>



| <span data-ttu-id="b5653-107">rsq DST, SRC</span><span class="sxs-lookup"><span data-stu-id="b5653-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="b5653-108">where</span><span class="sxs-lookup"><span data-stu-id="b5653-108">where</span></span>

-   <span data-ttu-id="b5653-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="b5653-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b5653-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="b5653-110">src is a source register.</span></span> <span data-ttu-id="b5653-111">Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="b5653-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5653-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b5653-112">Remarks</span></span>



| <span data-ttu-id="b5653-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="b5653-113">Vertex shader versions</span></span> | <span data-ttu-id="b5653-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b5653-114">1\_1</span></span> | <span data-ttu-id="b5653-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5653-115">2\_0</span></span> | <span data-ttu-id="b5653-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b5653-116">2\_x</span></span> | <span data-ttu-id="b5653-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b5653-117">2\_sw</span></span> | <span data-ttu-id="b5653-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5653-118">3\_0</span></span> | <span data-ttu-id="b5653-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b5653-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b5653-120">rsq</span><span class="sxs-lookup"><span data-stu-id="b5653-120">rsq</span></span>                    | <span data-ttu-id="b5653-121">x</span><span class="sxs-lookup"><span data-stu-id="b5653-121">x</span></span>    | <span data-ttu-id="b5653-122">x</span><span class="sxs-lookup"><span data-stu-id="b5653-122">x</span></span>    | <span data-ttu-id="b5653-123">x</span><span class="sxs-lookup"><span data-stu-id="b5653-123">x</span></span>    | <span data-ttu-id="b5653-124">x</span><span class="sxs-lookup"><span data-stu-id="b5653-124">x</span></span>     | <span data-ttu-id="b5653-125">x</span><span class="sxs-lookup"><span data-stu-id="b5653-125">x</span></span>    | <span data-ttu-id="b5653-126">x</span><span class="sxs-lookup"><span data-stu-id="b5653-126">x</span></span>     |



 

<span data-ttu-id="b5653-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="b5653-127">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



<span data-ttu-id="b5653-128">La valeur absolue est prise avant le traitement.</span><span class="sxs-lookup"><span data-stu-id="b5653-128">The absolute value is taken before processing.</span></span>

<span data-ttu-id="b5653-129">La précision doit être d’au moins 1,0/(2 ² ²) erreur absolue sur la plage (1,0, 4,0), car les implémentations courantes séparent la mantisse et l’exposant.</span><span class="sxs-lookup"><span data-stu-id="b5653-129">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="b5653-130">Si la source n’a aucun sous-script, le composant x est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b5653-130">If source has no subscripts, the x-component is used.</span></span> <span data-ttu-id="b5653-131">La sortie doit être exactement 1,0 si l’entrée est exactement 1,0.</span><span class="sxs-lookup"><span data-stu-id="b5653-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="b5653-132">Une source de 0,0 donne l’infini.</span><span class="sxs-lookup"><span data-stu-id="b5653-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5653-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5653-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5653-134">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="b5653-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




