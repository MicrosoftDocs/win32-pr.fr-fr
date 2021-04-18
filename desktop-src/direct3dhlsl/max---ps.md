---
title: Max-PS
description: Calcule le nombre maximal de sources. | Max-PS
ms.assetid: 3d3bef5b-0ff7-441b-8681-a3f4cde0ae4f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6186f0bd57acd4862a62a4c0a30ae92118b75ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974423"
---
# <a name="max---ps"></a><span data-ttu-id="c2159-104">Max-PS</span><span class="sxs-lookup"><span data-stu-id="c2159-104">max - ps</span></span>

<span data-ttu-id="c2159-105">Calcule le nombre maximal de sources.</span><span class="sxs-lookup"><span data-stu-id="c2159-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2159-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2159-106">Syntax</span></span>



| <span data-ttu-id="c2159-107">DST Max, src0, src1</span><span class="sxs-lookup"><span data-stu-id="c2159-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="c2159-108">where</span><span class="sxs-lookup"><span data-stu-id="c2159-108">where</span></span>

-   <span data-ttu-id="c2159-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="c2159-109">dst is the destination register.</span></span>
-   <span data-ttu-id="c2159-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="c2159-110">src0 is a source register.</span></span>
-   <span data-ttu-id="c2159-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="c2159-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2159-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c2159-112">Remarks</span></span>



| <span data-ttu-id="c2159-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c2159-113">Pixel shader versions</span></span> | <span data-ttu-id="c2159-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c2159-114">1\_1</span></span> | <span data-ttu-id="c2159-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c2159-115">1\_2</span></span> | <span data-ttu-id="c2159-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c2159-116">1\_3</span></span> | <span data-ttu-id="c2159-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c2159-117">1\_4</span></span> | <span data-ttu-id="c2159-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2159-118">2\_0</span></span> | <span data-ttu-id="c2159-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c2159-119">2\_x</span></span> | <span data-ttu-id="c2159-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c2159-120">2\_sw</span></span> | <span data-ttu-id="c2159-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c2159-121">3\_0</span></span> | <span data-ttu-id="c2159-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c2159-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c2159-123">max</span><span class="sxs-lookup"><span data-stu-id="c2159-123">max</span></span>                   |      |      |      |      | <span data-ttu-id="c2159-124">x</span><span class="sxs-lookup"><span data-stu-id="c2159-124">x</span></span>    | <span data-ttu-id="c2159-125">x</span><span class="sxs-lookup"><span data-stu-id="c2159-125">x</span></span>    | <span data-ttu-id="c2159-126">x</span><span class="sxs-lookup"><span data-stu-id="c2159-126">x</span></span>     | <span data-ttu-id="c2159-127">x</span><span class="sxs-lookup"><span data-stu-id="c2159-127">x</span></span>    | <span data-ttu-id="c2159-128">x</span><span class="sxs-lookup"><span data-stu-id="c2159-128">x</span></span>     |



 

<span data-ttu-id="c2159-129">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="c2159-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="c2159-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2159-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2159-131">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c2159-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




