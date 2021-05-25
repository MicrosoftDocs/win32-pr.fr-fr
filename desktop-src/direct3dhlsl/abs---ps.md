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
ms.openlocfilehash: f4f22261a114333ed77d67d7c0ac2738d3522054
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343325"
---
# <a name="abs---ps"></a><span data-ttu-id="f7b62-104">ABS-PS</span><span class="sxs-lookup"><span data-stu-id="f7b62-104">abs - ps</span></span>

<span data-ttu-id="f7b62-105">Calcule la valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="f7b62-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b62-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7b62-106">Syntax</span></span>

<span data-ttu-id="f7b62-107">**ABS DST, SRC**</span><span class="sxs-lookup"><span data-stu-id="f7b62-107">**abs dst, src**</span></span>

<span data-ttu-id="f7b62-108">where</span><span class="sxs-lookup"><span data-stu-id="f7b62-108">where</span></span>

-   <span data-ttu-id="f7b62-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="f7b62-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f7b62-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="f7b62-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b62-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7b62-111">Remarks</span></span>



| <span data-ttu-id="f7b62-112">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f7b62-112">Pixel shader versions</span></span> | <span data-ttu-id="f7b62-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="f7b62-113">1\_1</span></span> | <span data-ttu-id="f7b62-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="f7b62-114">1\_2</span></span> | <span data-ttu-id="f7b62-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f7b62-115">1\_3</span></span> | <span data-ttu-id="f7b62-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="f7b62-116">1\_4</span></span> | <span data-ttu-id="f7b62-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7b62-117">2\_0</span></span> | <span data-ttu-id="f7b62-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f7b62-118">2\_x</span></span> | <span data-ttu-id="f7b62-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="f7b62-119">2\_sw</span></span> | <span data-ttu-id="f7b62-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7b62-120">3\_0</span></span> | <span data-ttu-id="f7b62-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="f7b62-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f7b62-122">abs</span><span class="sxs-lookup"><span data-stu-id="f7b62-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="f7b62-123">x</span><span class="sxs-lookup"><span data-stu-id="f7b62-123">x</span></span>    | <span data-ttu-id="f7b62-124">x</span><span class="sxs-lookup"><span data-stu-id="f7b62-124">x</span></span>    | <span data-ttu-id="f7b62-125">x</span><span class="sxs-lookup"><span data-stu-id="f7b62-125">x</span></span>     | <span data-ttu-id="f7b62-126">x</span><span class="sxs-lookup"><span data-stu-id="f7b62-126">x</span></span>    | <span data-ttu-id="f7b62-127">x</span><span class="sxs-lookup"><span data-stu-id="f7b62-127">x</span></span>     |



 

<span data-ttu-id="f7b62-128">Cette instruction fonctionne comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="f7b62-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="f7b62-129">Informations sur les instructions</span><span class="sxs-lookup"><span data-stu-id="f7b62-129">Instruction Information</span></span>



| <span data-ttu-id="f7b62-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7b62-130">Requirement</span></span>                         | <span data-ttu-id="f7b62-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7b62-131">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="f7b62-132">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="f7b62-132">Minimum operating system</span></span> | <span data-ttu-id="f7b62-133">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f7b62-133">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f7b62-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f7b62-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7b62-135">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="f7b62-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




