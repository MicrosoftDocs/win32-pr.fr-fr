---
title: sous-PS
description: Soustrait des sources. | sous-PS
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4998892aa06eff55632600a9c2f7fe359c11f830
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761606"
---
# <a name="sub---ps"></a><span data-ttu-id="a5c0d-104">sous-PS</span><span class="sxs-lookup"><span data-stu-id="a5c0d-104">sub - ps</span></span>

<span data-ttu-id="a5c0d-105">Soustrait des sources.</span><span class="sxs-lookup"><span data-stu-id="a5c0d-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c0d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5c0d-106">Syntax</span></span>



| <span data-ttu-id="a5c0d-107">Sub DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="a5c0d-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a5c0d-108">where</span><span class="sxs-lookup"><span data-stu-id="a5c0d-108">where</span></span>

-   <span data-ttu-id="a5c0d-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="a5c0d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a5c0d-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="a5c0d-110">src0 is a source register.</span></span>
-   <span data-ttu-id="a5c0d-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="a5c0d-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c0d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a5c0d-112">Remarks</span></span>



| <span data-ttu-id="a5c0d-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a5c0d-113">Pixel shader versions</span></span> | <span data-ttu-id="a5c0d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a5c0d-114">1\_1</span></span> | <span data-ttu-id="a5c0d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="a5c0d-115">1\_2</span></span> | <span data-ttu-id="a5c0d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a5c0d-116">1\_3</span></span> | <span data-ttu-id="a5c0d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="a5c0d-117">1\_4</span></span> | <span data-ttu-id="a5c0d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a5c0d-118">2\_0</span></span> | <span data-ttu-id="a5c0d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-119">2\_x</span></span> | <span data-ttu-id="a5c0d-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a5c0d-120">2\_sw</span></span> | <span data-ttu-id="a5c0d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a5c0d-121">3\_0</span></span> | <span data-ttu-id="a5c0d-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="a5c0d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a5c0d-123">sub</span><span class="sxs-lookup"><span data-stu-id="a5c0d-123">sub</span></span>                   | <span data-ttu-id="a5c0d-124">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-124">x</span></span>    | <span data-ttu-id="a5c0d-125">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-125">x</span></span>    | <span data-ttu-id="a5c0d-126">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-126">x</span></span>    | <span data-ttu-id="a5c0d-127">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-127">x</span></span>    | <span data-ttu-id="a5c0d-128">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-128">x</span></span>    | <span data-ttu-id="a5c0d-129">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-129">x</span></span>    | <span data-ttu-id="a5c0d-130">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-130">x</span></span>     | <span data-ttu-id="a5c0d-131">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-131">x</span></span>    | <span data-ttu-id="a5c0d-132">x</span><span class="sxs-lookup"><span data-stu-id="a5c0d-132">x</span></span>     |



 

<span data-ttu-id="a5c0d-133">Cette instruction effectue la soustraction affichée dans cette formule.</span><span class="sxs-lookup"><span data-stu-id="a5c0d-133">This instruction performs the subtraction shown in this formula.</span></span>


```
dest = src0 - src1
```



## <a name="related-topics"></a><span data-ttu-id="a5c0d-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5c0d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5c0d-135">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a5c0d-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




