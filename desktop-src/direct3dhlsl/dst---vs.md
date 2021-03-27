---
title: DST-vs
description: Calcule un vecteur de distance. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869726"
---
# <a name="dst---vs"></a><span data-ttu-id="b6f8c-104">DST-vs</span><span class="sxs-lookup"><span data-stu-id="b6f8c-104">dst - vs</span></span>

<span data-ttu-id="b6f8c-105">Calcule un vecteur de distance.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-105">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f8c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6f8c-106">Syntax</span></span>



| <span data-ttu-id="b6f8c-107">DST dest, src0, src1</span><span class="sxs-lookup"><span data-stu-id="b6f8c-107">dst dest, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="b6f8c-108">where</span><span class="sxs-lookup"><span data-stu-id="b6f8c-108">where</span></span>

-   <span data-ttu-id="b6f8c-109">dest est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-109">dest is the destination register.</span></span>
-   <span data-ttu-id="b6f8c-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-110">src0 is a source register.</span></span>
-   <span data-ttu-id="b6f8c-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="b6f8c-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6f8c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b6f8c-112">Remarks</span></span>



| <span data-ttu-id="b6f8c-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="b6f8c-113">Vertex shader versions</span></span> | <span data-ttu-id="b6f8c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b6f8c-114">1\_1</span></span> | <span data-ttu-id="b6f8c-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6f8c-115">2\_0</span></span> | <span data-ttu-id="b6f8c-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b6f8c-116">2\_x</span></span> | <span data-ttu-id="b6f8c-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b6f8c-117">2\_sw</span></span> | <span data-ttu-id="b6f8c-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6f8c-118">3\_0</span></span> | <span data-ttu-id="b6f8c-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b6f8c-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b6f8c-120">destination</span><span class="sxs-lookup"><span data-stu-id="b6f8c-120">dst</span></span>                    | <span data-ttu-id="b6f8c-121">x</span><span class="sxs-lookup"><span data-stu-id="b6f8c-121">x</span></span>    | <span data-ttu-id="b6f8c-122">x</span><span class="sxs-lookup"><span data-stu-id="b6f8c-122">x</span></span>    | <span data-ttu-id="b6f8c-123">x</span><span class="sxs-lookup"><span data-stu-id="b6f8c-123">x</span></span>    | <span data-ttu-id="b6f8c-124">x</span><span class="sxs-lookup"><span data-stu-id="b6f8c-124">x</span></span>     | <span data-ttu-id="b6f8c-125">x</span><span class="sxs-lookup"><span data-stu-id="b6f8c-125">x</span></span>    | <span data-ttu-id="b6f8c-126">x</span><span class="sxs-lookup"><span data-stu-id="b6f8c-126">x</span></span>     |



 

<span data-ttu-id="b6f8c-127">Le fragment de code suivant montre les opérations effectuées :</span><span class="sxs-lookup"><span data-stu-id="b6f8c-127">The following code fragment shows the operations performed:</span></span>


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



<span data-ttu-id="b6f8c-128">Le premier opérande source (src0) est supposé être le vecteur (ignoré, d d, \* d \* , ignoré) et le deuxième opérande source (src1) est supposé être le vecteur (ignoré, 1/d, ignoré, 1/d).</span><span class="sxs-lookup"><span data-stu-id="b6f8c-128">The first source operand (src0) is assumed to be the vector (ignored, d\*d, d\*d, ignored) and the second source operand (src1) is assumed to be the vector (ignored, 1/d, ignored, 1/d).</span></span> <span data-ttu-id="b6f8c-129">La destination (dest) est le vecteur de résultat (1, d, d \* d, 1/d).</span><span class="sxs-lookup"><span data-stu-id="b6f8c-129">The destination (dest) is the result vector (1, d, d\*d, 1/d).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6f8c-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6f8c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6f8c-131">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="b6f8c-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




