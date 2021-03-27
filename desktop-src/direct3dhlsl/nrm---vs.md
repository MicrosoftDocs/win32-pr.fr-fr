---
title: NRM-vs
description: Normaliser un vecteur 3D. | NRM-vs
ms.assetid: 735e9971-c0c3-4648-8362-58bda6fac46a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e696277136826294392149c4b7430e4c75f9d9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211504"
---
# <a name="nrm---vs"></a><span data-ttu-id="cd74e-104">NRM-vs</span><span class="sxs-lookup"><span data-stu-id="cd74e-104">nrm - vs</span></span>

<span data-ttu-id="cd74e-105">Normaliser un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="cd74e-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd74e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd74e-106">Syntax</span></span>



| <span data-ttu-id="cd74e-107">NRM DST, SRC</span><span class="sxs-lookup"><span data-stu-id="cd74e-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="cd74e-108">where</span><span class="sxs-lookup"><span data-stu-id="cd74e-108">where</span></span>

-   <span data-ttu-id="cd74e-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="cd74e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="cd74e-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="cd74e-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd74e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cd74e-111">Remarks</span></span>



| <span data-ttu-id="cd74e-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="cd74e-112">Vertex shader versions</span></span> | <span data-ttu-id="cd74e-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="cd74e-113">1\_1</span></span> | <span data-ttu-id="cd74e-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd74e-114">2\_0</span></span> | <span data-ttu-id="cd74e-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cd74e-115">2\_x</span></span> | <span data-ttu-id="cd74e-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cd74e-116">2\_sw</span></span> | <span data-ttu-id="cd74e-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd74e-117">3\_0</span></span> | <span data-ttu-id="cd74e-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cd74e-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="cd74e-119">nrm</span><span class="sxs-lookup"><span data-stu-id="cd74e-119">nrm</span></span>                    |      | <span data-ttu-id="cd74e-120">x</span><span class="sxs-lookup"><span data-stu-id="cd74e-120">x</span></span>    | <span data-ttu-id="cd74e-121">x</span><span class="sxs-lookup"><span data-stu-id="cd74e-121">x</span></span>    | <span data-ttu-id="cd74e-122">x</span><span class="sxs-lookup"><span data-stu-id="cd74e-122">x</span></span>     | <span data-ttu-id="cd74e-123">x</span><span class="sxs-lookup"><span data-stu-id="cd74e-123">x</span></span>    | <span data-ttu-id="cd74e-124">x</span><span class="sxs-lookup"><span data-stu-id="cd74e-124">x</span></span>     |



 

<span data-ttu-id="cd74e-125">Cette instruction fonctionne conceptuellement comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="cd74e-125">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="cd74e-126">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="cd74e-126">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="cd74e-127">Les registres dest et SRC ne peuvent pas être identiques.</span><span class="sxs-lookup"><span data-stu-id="cd74e-127">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="cd74e-128">Le registre de dest doit être un registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="cd74e-128">The dest register must be a temporary register.</span></span>

<span data-ttu-id="cd74e-129">Cette instruction effectue l’interpolation linéaire basée sur la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="cd74e-129">This instruction performs the linear interpolation based on the following formula.</span></span>


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a><span data-ttu-id="cd74e-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd74e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd74e-131">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="cd74e-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




