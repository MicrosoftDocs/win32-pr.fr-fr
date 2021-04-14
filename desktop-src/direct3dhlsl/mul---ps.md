---
title: Mul-PS
description: Multiplie les sources dans la destination. | Mul-PS
ms.assetid: 03823c10-9631-4468-8488-4bd17224d16c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fefe89d4fdbe5f75965f2707a5ceb2c1673e1326
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992084"
---
# <a name="mul---ps"></a><span data-ttu-id="439c1-104">Mul-PS</span><span class="sxs-lookup"><span data-stu-id="439c1-104">mul - ps</span></span>

<span data-ttu-id="439c1-105">Multiplie les sources dans la destination.</span><span class="sxs-lookup"><span data-stu-id="439c1-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="439c1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="439c1-106">Syntax</span></span>



| <span data-ttu-id="439c1-107">Mul DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="439c1-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="439c1-108">where</span><span class="sxs-lookup"><span data-stu-id="439c1-108">where</span></span>

-   <span data-ttu-id="439c1-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="439c1-109">dst is the destination register.</span></span>
-   <span data-ttu-id="439c1-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="439c1-110">src0 is a source register.</span></span>
-   <span data-ttu-id="439c1-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="439c1-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="439c1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="439c1-112">Remarks</span></span>



| <span data-ttu-id="439c1-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="439c1-113">Pixel shader versions</span></span> | <span data-ttu-id="439c1-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="439c1-114">1\_1</span></span> | <span data-ttu-id="439c1-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="439c1-115">1\_2</span></span> | <span data-ttu-id="439c1-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="439c1-116">1\_3</span></span> | <span data-ttu-id="439c1-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="439c1-117">1\_4</span></span> | <span data-ttu-id="439c1-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="439c1-118">2\_0</span></span> | <span data-ttu-id="439c1-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="439c1-119">2\_x</span></span> | <span data-ttu-id="439c1-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="439c1-120">2\_sw</span></span> | <span data-ttu-id="439c1-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="439c1-121">3\_0</span></span> | <span data-ttu-id="439c1-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="439c1-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="439c1-123">mul</span><span class="sxs-lookup"><span data-stu-id="439c1-123">mul</span></span>                   | <span data-ttu-id="439c1-124">x</span><span class="sxs-lookup"><span data-stu-id="439c1-124">x</span></span>    | <span data-ttu-id="439c1-125">x</span><span class="sxs-lookup"><span data-stu-id="439c1-125">x</span></span>    | <span data-ttu-id="439c1-126">x</span><span class="sxs-lookup"><span data-stu-id="439c1-126">x</span></span>    | <span data-ttu-id="439c1-127">x</span><span class="sxs-lookup"><span data-stu-id="439c1-127">x</span></span>    | <span data-ttu-id="439c1-128">x</span><span class="sxs-lookup"><span data-stu-id="439c1-128">x</span></span>    | <span data-ttu-id="439c1-129">x</span><span class="sxs-lookup"><span data-stu-id="439c1-129">x</span></span>    | <span data-ttu-id="439c1-130">x</span><span class="sxs-lookup"><span data-stu-id="439c1-130">x</span></span>     | <span data-ttu-id="439c1-131">x</span><span class="sxs-lookup"><span data-stu-id="439c1-131">x</span></span>    | <span data-ttu-id="439c1-132">x</span><span class="sxs-lookup"><span data-stu-id="439c1-132">x</span></span>     |



 

<span data-ttu-id="439c1-133">L’extrait de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="439c1-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="439c1-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="439c1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439c1-135">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="439c1-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




