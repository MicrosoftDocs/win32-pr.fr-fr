---
title: des SLT-vs
description: Calcule le signe si la première source est inférieure à la deuxième source.
ms.assetid: 7573bcee-8f31-49ea-b515-5be59a7a508d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6476ec24f82295d56b04682dfa4320547672b43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030566"
---
# <a name="slt---vs"></a><span data-ttu-id="3b7e0-103">des SLT-vs</span><span class="sxs-lookup"><span data-stu-id="3b7e0-103">slt - vs</span></span>

<span data-ttu-id="3b7e0-104">Calcule le signe si la première source est inférieure à la deuxième source.</span><span class="sxs-lookup"><span data-stu-id="3b7e0-104">Computes the sign if the first source is less than the second source.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b7e0-105">Syntax</span></span>



| <span data-ttu-id="3b7e0-106">des SLT DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="3b7e0-106">slt dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="3b7e0-107">where</span><span class="sxs-lookup"><span data-stu-id="3b7e0-107">where</span></span>

-   <span data-ttu-id="3b7e0-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="3b7e0-108">dst is the destination register.</span></span>
-   <span data-ttu-id="3b7e0-109">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3b7e0-109">src0 is a source register.</span></span>
-   <span data-ttu-id="3b7e0-110">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3b7e0-110">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b7e0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3b7e0-111">Remarks</span></span>



| <span data-ttu-id="3b7e0-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="3b7e0-112">Vertex shader versions</span></span> | <span data-ttu-id="3b7e0-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="3b7e0-113">1\_1</span></span> | <span data-ttu-id="3b7e0-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b7e0-114">2\_0</span></span> | <span data-ttu-id="3b7e0-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3b7e0-115">2\_x</span></span> | <span data-ttu-id="3b7e0-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3b7e0-116">2\_sw</span></span> | <span data-ttu-id="3b7e0-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b7e0-117">3\_0</span></span> | <span data-ttu-id="3b7e0-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3b7e0-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3b7e0-119">des SLT</span><span class="sxs-lookup"><span data-stu-id="3b7e0-119">slt</span></span>                    | <span data-ttu-id="3b7e0-120">x</span><span class="sxs-lookup"><span data-stu-id="3b7e0-120">x</span></span>    | <span data-ttu-id="3b7e0-121">x</span><span class="sxs-lookup"><span data-stu-id="3b7e0-121">x</span></span>    | <span data-ttu-id="3b7e0-122">x</span><span class="sxs-lookup"><span data-stu-id="3b7e0-122">x</span></span>    | <span data-ttu-id="3b7e0-123">x</span><span class="sxs-lookup"><span data-stu-id="3b7e0-123">x</span></span>     | <span data-ttu-id="3b7e0-124">x</span><span class="sxs-lookup"><span data-stu-id="3b7e0-124">x</span></span>    | <span data-ttu-id="3b7e0-125">x</span><span class="sxs-lookup"><span data-stu-id="3b7e0-125">x</span></span>     |



 

<span data-ttu-id="3b7e0-126">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="3b7e0-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x < src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y < src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z < src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w < src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a><span data-ttu-id="3b7e0-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b7e0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b7e0-128">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3b7e0-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




