---
title: LRP-PS
description: Interpole de manière linéaire entre les deuxième et troisième registres sources d’une proportion spécifiée dans le premier registre source. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043064"
---
# <a name="lrp---ps"></a><span data-ttu-id="1f7f2-104">LRP-PS</span><span class="sxs-lookup"><span data-stu-id="1f7f2-104">lrp - ps</span></span>

<span data-ttu-id="1f7f2-105">Interpole de manière linéaire entre les deuxième et troisième registres sources d’une proportion spécifiée dans le premier registre source.</span><span class="sxs-lookup"><span data-stu-id="1f7f2-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f7f2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f7f2-106">Syntax</span></span>



| <span data-ttu-id="1f7f2-107">LRP DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="1f7f2-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="1f7f2-108">where</span><span class="sxs-lookup"><span data-stu-id="1f7f2-108">where</span></span>

-   <span data-ttu-id="1f7f2-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="1f7f2-109">dst is the destination register.</span></span>
-   <span data-ttu-id="1f7f2-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="1f7f2-110">src0 is a source register.</span></span>
-   <span data-ttu-id="1f7f2-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="1f7f2-111">src1 is a source register.</span></span>
-   <span data-ttu-id="1f7f2-112">src2 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="1f7f2-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f7f2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1f7f2-113">Remarks</span></span>



| <span data-ttu-id="1f7f2-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1f7f2-114">Pixel shader versions</span></span> | <span data-ttu-id="1f7f2-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="1f7f2-115">1\_1</span></span> | <span data-ttu-id="1f7f2-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="1f7f2-116">1\_2</span></span> | <span data-ttu-id="1f7f2-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1f7f2-117">1\_3</span></span> | <span data-ttu-id="1f7f2-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="1f7f2-118">1\_4</span></span> | <span data-ttu-id="1f7f2-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1f7f2-119">2\_0</span></span> | <span data-ttu-id="1f7f2-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-120">2\_x</span></span> | <span data-ttu-id="1f7f2-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="1f7f2-121">2\_sw</span></span> | <span data-ttu-id="1f7f2-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1f7f2-122">3\_0</span></span> | <span data-ttu-id="1f7f2-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="1f7f2-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1f7f2-124">lrp</span><span class="sxs-lookup"><span data-stu-id="1f7f2-124">lrp</span></span>                   | <span data-ttu-id="1f7f2-125">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-125">x</span></span>    | <span data-ttu-id="1f7f2-126">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-126">x</span></span>    | <span data-ttu-id="1f7f2-127">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-127">x</span></span>    | <span data-ttu-id="1f7f2-128">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-128">x</span></span>    | <span data-ttu-id="1f7f2-129">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-129">x</span></span>    | <span data-ttu-id="1f7f2-130">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-130">x</span></span>    | <span data-ttu-id="1f7f2-131">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-131">x</span></span>     | <span data-ttu-id="1f7f2-132">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-132">x</span></span>    | <span data-ttu-id="1f7f2-133">x</span><span class="sxs-lookup"><span data-stu-id="1f7f2-133">x</span></span>     |



 

<span data-ttu-id="1f7f2-134">Cette instruction effectue l’interpolation linéaire basée sur la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="1f7f2-134">This instruction performs the linear interpolation based on the following formula.</span></span>


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a><span data-ttu-id="1f7f2-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f7f2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f7f2-136">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="1f7f2-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




