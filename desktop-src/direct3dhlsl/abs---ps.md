---
title: ABS-PS
description: Calcule la valeur absolue. | ABS-PS
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 070a513aaa0d336d5ac404b1748fdd162edfd532
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321838"
---
# <a name="abs---ps"></a><span data-ttu-id="f39e5-104">ABS-PS</span><span class="sxs-lookup"><span data-stu-id="f39e5-104">abs - ps</span></span>

<span data-ttu-id="f39e5-105">Calcule la valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="f39e5-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f39e5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f39e5-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="f39e5-107">ABS DST, SRC</span><span class="sxs-lookup"><span data-stu-id="f39e5-107">abs dst, src</span></span> |



 

<span data-ttu-id="f39e5-108">where</span><span class="sxs-lookup"><span data-stu-id="f39e5-108">where</span></span>

-   <span data-ttu-id="f39e5-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="f39e5-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f39e5-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="f39e5-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f39e5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f39e5-111">Remarks</span></span>



|                       |      |      |      |      |      |      |       |      |       |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f39e5-112">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f39e5-112">Pixel shader versions</span></span> | <span data-ttu-id="f39e5-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="f39e5-113">1\_1</span></span> | <span data-ttu-id="f39e5-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="f39e5-114">1\_2</span></span> | <span data-ttu-id="f39e5-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f39e5-115">1\_3</span></span> | <span data-ttu-id="f39e5-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="f39e5-116">1\_4</span></span> | <span data-ttu-id="f39e5-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f39e5-117">2\_0</span></span> | <span data-ttu-id="f39e5-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f39e5-118">2\_x</span></span> | <span data-ttu-id="f39e5-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="f39e5-119">2\_sw</span></span> | <span data-ttu-id="f39e5-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f39e5-120">3\_0</span></span> | <span data-ttu-id="f39e5-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="f39e5-121">3\_sw</span></span> |
| <span data-ttu-id="f39e5-122">abs</span><span class="sxs-lookup"><span data-stu-id="f39e5-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="f39e5-123">x</span><span class="sxs-lookup"><span data-stu-id="f39e5-123">x</span></span>    | <span data-ttu-id="f39e5-124">x</span><span class="sxs-lookup"><span data-stu-id="f39e5-124">x</span></span>    | <span data-ttu-id="f39e5-125">x</span><span class="sxs-lookup"><span data-stu-id="f39e5-125">x</span></span>     | <span data-ttu-id="f39e5-126">x</span><span class="sxs-lookup"><span data-stu-id="f39e5-126">x</span></span>    | <span data-ttu-id="f39e5-127">x</span><span class="sxs-lookup"><span data-stu-id="f39e5-127">x</span></span>     |



 

<span data-ttu-id="f39e5-128">Cette instruction fonctionne comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="f39e5-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="f39e5-129">Informations sur les instructions</span><span class="sxs-lookup"><span data-stu-id="f39e5-129">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f39e5-130">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="f39e5-130">Minimum operating system</span></span> | <span data-ttu-id="f39e5-131">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f39e5-131">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f39e5-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f39e5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f39e5-133">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f39e5-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




