---
title: NRM-PS
description: Normaliser un vecteur 3D. | NRM-PS
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322121"
---
# <a name="nrm---ps"></a><span data-ttu-id="01112-104">NRM-PS</span><span class="sxs-lookup"><span data-stu-id="01112-104">nrm - ps</span></span>

<span data-ttu-id="01112-105">Normaliser un vecteur 3D.</span><span class="sxs-lookup"><span data-stu-id="01112-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="01112-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01112-106">Syntax</span></span>



| <span data-ttu-id="01112-107">NRM DST, SRC</span><span class="sxs-lookup"><span data-stu-id="01112-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="01112-108">where</span><span class="sxs-lookup"><span data-stu-id="01112-108">where</span></span>

-   <span data-ttu-id="01112-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="01112-109">dst is the destination register.</span></span>
-   <span data-ttu-id="01112-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="01112-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="01112-111">Notes</span><span class="sxs-lookup"><span data-stu-id="01112-111">Remarks</span></span>



| <span data-ttu-id="01112-112">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="01112-112">Pixel shader versions</span></span> | <span data-ttu-id="01112-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="01112-113">1\_1</span></span> | <span data-ttu-id="01112-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="01112-114">1\_2</span></span> | <span data-ttu-id="01112-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="01112-115">1\_3</span></span> | <span data-ttu-id="01112-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="01112-116">1\_4</span></span> | <span data-ttu-id="01112-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="01112-117">2\_0</span></span> | <span data-ttu-id="01112-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="01112-118">2\_x</span></span> | <span data-ttu-id="01112-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="01112-119">2\_sw</span></span> | <span data-ttu-id="01112-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="01112-120">3\_0</span></span> | <span data-ttu-id="01112-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="01112-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="01112-122">nrm</span><span class="sxs-lookup"><span data-stu-id="01112-122">nrm</span></span>                   |      |      |      |      | <span data-ttu-id="01112-123">x</span><span class="sxs-lookup"><span data-stu-id="01112-123">x</span></span>    | <span data-ttu-id="01112-124">x</span><span class="sxs-lookup"><span data-stu-id="01112-124">x</span></span>    | <span data-ttu-id="01112-125">x</span><span class="sxs-lookup"><span data-stu-id="01112-125">x</span></span>     | <span data-ttu-id="01112-126">x</span><span class="sxs-lookup"><span data-stu-id="01112-126">x</span></span>    | <span data-ttu-id="01112-127">x</span><span class="sxs-lookup"><span data-stu-id="01112-127">x</span></span>     |



 

<span data-ttu-id="01112-128">Cette instruction fonctionne conceptuellement comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="01112-128">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="01112-129">squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="01112-129">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="01112-130">Les registres dest et SRC ne peuvent pas être identiques.</span><span class="sxs-lookup"><span data-stu-id="01112-130">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="01112-131">Le registre de dest doit être un registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="01112-131">The dest register must be a temporary register.</span></span>

<span data-ttu-id="01112-132">Cette instruction effectue l’interpolation linéaire basée sur la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="01112-132">This instruction performs the linear interpolation based on the following formula.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="01112-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01112-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01112-134">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="01112-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




