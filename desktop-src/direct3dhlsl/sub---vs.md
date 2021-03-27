---
title: sous-vs
description: Soustrait des sources. | sous-vs
ms.assetid: ccd7ca57-05a9-4ee8-8bda-c8c875476aaf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4bf15522798e1da5ec0bde5b729f241ff9dabde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953671"
---
# <a name="sub---vs"></a><span data-ttu-id="3cbd3-104">sous-vs</span><span class="sxs-lookup"><span data-stu-id="3cbd3-104">sub - vs</span></span>

<span data-ttu-id="3cbd3-105">Soustrait des sources.</span><span class="sxs-lookup"><span data-stu-id="3cbd3-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cbd3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cbd3-106">Syntax</span></span>



| <span data-ttu-id="3cbd3-107">Sub DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="3cbd3-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="3cbd3-108">where</span><span class="sxs-lookup"><span data-stu-id="3cbd3-108">where</span></span>

-   <span data-ttu-id="3cbd3-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="3cbd3-109">dst is the destination register.</span></span>
-   <span data-ttu-id="3cbd3-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3cbd3-110">src0 is a source register.</span></span>
-   <span data-ttu-id="3cbd3-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3cbd3-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cbd3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3cbd3-112">Remarks</span></span>



| <span data-ttu-id="3cbd3-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="3cbd3-113">Vertex shader versions</span></span> | <span data-ttu-id="3cbd3-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3cbd3-114">1\_1</span></span> | <span data-ttu-id="3cbd3-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3cbd3-115">2\_0</span></span> | <span data-ttu-id="3cbd3-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3cbd3-116">2\_x</span></span> | <span data-ttu-id="3cbd3-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3cbd3-117">2\_sw</span></span> | <span data-ttu-id="3cbd3-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3cbd3-118">3\_0</span></span> | <span data-ttu-id="3cbd3-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3cbd3-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3cbd3-120">sub</span><span class="sxs-lookup"><span data-stu-id="3cbd3-120">sub</span></span>                    | <span data-ttu-id="3cbd3-121">x</span><span class="sxs-lookup"><span data-stu-id="3cbd3-121">x</span></span>    | <span data-ttu-id="3cbd3-122">x</span><span class="sxs-lookup"><span data-stu-id="3cbd3-122">x</span></span>    | <span data-ttu-id="3cbd3-123">x</span><span class="sxs-lookup"><span data-stu-id="3cbd3-123">x</span></span>    | <span data-ttu-id="3cbd3-124">x</span><span class="sxs-lookup"><span data-stu-id="3cbd3-124">x</span></span>     | <span data-ttu-id="3cbd3-125">x</span><span class="sxs-lookup"><span data-stu-id="3cbd3-125">x</span></span>    | <span data-ttu-id="3cbd3-126">x</span><span class="sxs-lookup"><span data-stu-id="3cbd3-126">x</span></span>     |



 

<span data-ttu-id="3cbd3-127">Cette instruction effectue la soustraction affichée dans cette formule.</span><span class="sxs-lookup"><span data-stu-id="3cbd3-127">This instruction performs the subtraction shown in this formula.</span></span>


```
dest.x = src0.x - src1.x
dest.y = src0.y - src1.y
dest.z = src0.z - src1.z
dest.w = src0.w - src1.w
```



## <a name="related-topics"></a><span data-ttu-id="3cbd3-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3cbd3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cbd3-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3cbd3-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




