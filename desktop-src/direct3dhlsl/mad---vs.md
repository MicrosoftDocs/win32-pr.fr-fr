---
title: Mad-vs
description: Multiplie et ajoute des sources.
ms.assetid: 059f0bf6-d143-4efc-b074-0ed026edb008
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01e96bb63395fe9e5dd27a17fbb5c0ddd9bf3c17
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313669"
---
# <a name="mad---vs"></a><span data-ttu-id="3b3a4-103">Mad-vs</span><span class="sxs-lookup"><span data-stu-id="3b3a4-103">mad - vs</span></span>

<span data-ttu-id="3b3a4-104">Multiplie et ajoute des sources.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-104">Multiplies and adds sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b3a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b3a4-105">Syntax</span></span>



| <span data-ttu-id="3b3a4-106">Mad DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="3b3a4-106">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="3b3a4-107">where</span><span class="sxs-lookup"><span data-stu-id="3b3a4-107">where</span></span>

-   <span data-ttu-id="3b3a4-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-108">dst is the destination register.</span></span>
-   <span data-ttu-id="3b3a4-109">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-109">src0 is a source register.</span></span>
-   <span data-ttu-id="3b3a4-110">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-110">src1 is a source register.</span></span>
-   <span data-ttu-id="3b3a4-111">src2 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b3a4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3b3a4-112">Remarks</span></span>



| <span data-ttu-id="3b3a4-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="3b3a4-113">Vertex shader versions</span></span> | <span data-ttu-id="3b3a4-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3b3a4-114">1\_1</span></span> | <span data-ttu-id="3b3a4-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b3a4-115">2\_0</span></span> | <span data-ttu-id="3b3a4-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3b3a4-116">2\_x</span></span> | <span data-ttu-id="3b3a4-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3b3a4-117">2\_sw</span></span> | <span data-ttu-id="3b3a4-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3b3a4-118">3\_0</span></span> | <span data-ttu-id="3b3a4-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3b3a4-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3b3a4-120">Mad</span><span class="sxs-lookup"><span data-stu-id="3b3a4-120">mad</span></span>                    | <span data-ttu-id="3b3a4-121">x</span><span class="sxs-lookup"><span data-stu-id="3b3a4-121">x</span></span>    | <span data-ttu-id="3b3a4-122">x</span><span class="sxs-lookup"><span data-stu-id="3b3a4-122">x</span></span>    | <span data-ttu-id="3b3a4-123">x</span><span class="sxs-lookup"><span data-stu-id="3b3a4-123">x</span></span>    | <span data-ttu-id="3b3a4-124">x</span><span class="sxs-lookup"><span data-stu-id="3b3a4-124">x</span></span>     | <span data-ttu-id="3b3a4-125">x</span><span class="sxs-lookup"><span data-stu-id="3b3a4-125">x</span></span>    | <span data-ttu-id="3b3a4-126">x</span><span class="sxs-lookup"><span data-stu-id="3b3a4-126">x</span></span>     |



 

<span data-ttu-id="3b3a4-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="3b3a4-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b3a4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b3a4-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3b3a4-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




