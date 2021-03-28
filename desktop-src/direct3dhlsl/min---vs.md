---
title: min-vs
description: Calcule la valeur minimale des sources. | min-vs
ms.assetid: cecfe98b-8efd-4fbf-a7b5-d228de724e71
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eda47b75398b8643f7010ff7468f72f4a7d8c199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974259"
---
# <a name="min---vs"></a><span data-ttu-id="37161-104">min-vs</span><span class="sxs-lookup"><span data-stu-id="37161-104">min - vs</span></span>

<span data-ttu-id="37161-105">Calcule la valeur minimale des sources.</span><span class="sxs-lookup"><span data-stu-id="37161-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="37161-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37161-106">Syntax</span></span>



| <span data-ttu-id="37161-107">heure d’été min, src0, src1</span><span class="sxs-lookup"><span data-stu-id="37161-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="37161-108">where</span><span class="sxs-lookup"><span data-stu-id="37161-108">where</span></span>

-   <span data-ttu-id="37161-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="37161-109">dst is the destination register.</span></span>
-   <span data-ttu-id="37161-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="37161-110">src0 is a source register.</span></span>
-   <span data-ttu-id="37161-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="37161-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="37161-112">Notes</span><span class="sxs-lookup"><span data-stu-id="37161-112">Remarks</span></span>



| <span data-ttu-id="37161-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="37161-113">Vertex shader versions</span></span> | <span data-ttu-id="37161-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="37161-114">1\_1</span></span> | <span data-ttu-id="37161-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37161-115">2\_0</span></span> | <span data-ttu-id="37161-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="37161-116">2\_x</span></span> | <span data-ttu-id="37161-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="37161-117">2\_sw</span></span> | <span data-ttu-id="37161-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37161-118">3\_0</span></span> | <span data-ttu-id="37161-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="37161-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="37161-120">minute(s)</span><span class="sxs-lookup"><span data-stu-id="37161-120">min</span></span>                    | <span data-ttu-id="37161-121">x</span><span class="sxs-lookup"><span data-stu-id="37161-121">x</span></span>    | <span data-ttu-id="37161-122">x</span><span class="sxs-lookup"><span data-stu-id="37161-122">x</span></span>    | <span data-ttu-id="37161-123">x</span><span class="sxs-lookup"><span data-stu-id="37161-123">x</span></span>    | <span data-ttu-id="37161-124">x</span><span class="sxs-lookup"><span data-stu-id="37161-124">x</span></span>     | <span data-ttu-id="37161-125">x</span><span class="sxs-lookup"><span data-stu-id="37161-125">x</span></span>    | <span data-ttu-id="37161-126">x</span><span class="sxs-lookup"><span data-stu-id="37161-126">x</span></span>     |



 

<span data-ttu-id="37161-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="37161-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="37161-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37161-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37161-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="37161-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




