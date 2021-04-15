---
title: LRP-vs
description: Interpole de manière linéaire entre les deuxième et troisième registres sources d’une proportion spécifiée dans le premier registre source. | LRP-vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 485d7720dc2c71ee599db93d179de8e665bfab77
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992008"
---
# <a name="lrp---vs"></a><span data-ttu-id="81d47-104">LRP-vs</span><span class="sxs-lookup"><span data-stu-id="81d47-104">lrp - vs</span></span>

<span data-ttu-id="81d47-105">Interpole de manière linéaire entre les deuxième et troisième registres sources d’une proportion spécifiée dans le premier registre source.</span><span class="sxs-lookup"><span data-stu-id="81d47-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d47-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81d47-106">Syntax</span></span>



| <span data-ttu-id="81d47-107">LRP DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="81d47-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="81d47-108">where</span><span class="sxs-lookup"><span data-stu-id="81d47-108">where</span></span>

-   <span data-ttu-id="81d47-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="81d47-109">dst is the destination register.</span></span>
-   <span data-ttu-id="81d47-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="81d47-110">src0 is a source register.</span></span>
-   <span data-ttu-id="81d47-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="81d47-111">src1 is a source register.</span></span>
-   <span data-ttu-id="81d47-112">src2 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="81d47-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="81d47-113">Notes</span><span class="sxs-lookup"><span data-stu-id="81d47-113">Remarks</span></span>



| <span data-ttu-id="81d47-114">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="81d47-114">Vertex shader versions</span></span> | <span data-ttu-id="81d47-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="81d47-115">1\_1</span></span> | <span data-ttu-id="81d47-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="81d47-116">2\_0</span></span> | <span data-ttu-id="81d47-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="81d47-117">2\_x</span></span> | <span data-ttu-id="81d47-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="81d47-118">2\_sw</span></span> | <span data-ttu-id="81d47-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="81d47-119">3\_0</span></span> | <span data-ttu-id="81d47-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="81d47-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="81d47-121">lrp</span><span class="sxs-lookup"><span data-stu-id="81d47-121">lrp</span></span>                    |      | <span data-ttu-id="81d47-122">x</span><span class="sxs-lookup"><span data-stu-id="81d47-122">x</span></span>    | <span data-ttu-id="81d47-123">x</span><span class="sxs-lookup"><span data-stu-id="81d47-123">x</span></span>    | <span data-ttu-id="81d47-124">x</span><span class="sxs-lookup"><span data-stu-id="81d47-124">x</span></span>     | <span data-ttu-id="81d47-125">x</span><span class="sxs-lookup"><span data-stu-id="81d47-125">x</span></span>    | <span data-ttu-id="81d47-126">x</span><span class="sxs-lookup"><span data-stu-id="81d47-126">x</span></span>     |



 

<span data-ttu-id="81d47-127">Cette instruction effectue l’interpolation linéaire basée sur la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="81d47-127">This instruction performs the linear interpolation based on the following formula.</span></span>


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="81d47-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="81d47-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81d47-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="81d47-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




