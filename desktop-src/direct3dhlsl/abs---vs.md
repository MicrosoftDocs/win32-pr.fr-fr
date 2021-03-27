---
title: ABS-vs
description: Calcule la valeur absolue. | ABS-vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07667954de97e2a1da3999237930fb33796d9030
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211376"
---
# <a name="abs---vs"></a><span data-ttu-id="8e360-104">ABS-vs</span><span class="sxs-lookup"><span data-stu-id="8e360-104">abs - vs</span></span>

<span data-ttu-id="8e360-105">Calcule la valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="8e360-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e360-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e360-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="8e360-107">ABS DST, SRC</span><span class="sxs-lookup"><span data-stu-id="8e360-107">abs dst, src</span></span> |



 

<span data-ttu-id="8e360-108">where</span><span class="sxs-lookup"><span data-stu-id="8e360-108">where</span></span>

-   <span data-ttu-id="8e360-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="8e360-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8e360-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="8e360-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e360-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8e360-111">Remarks</span></span>



|                        |      |      |      |       |      |       |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8e360-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="8e360-112">Vertex shader versions</span></span> | <span data-ttu-id="8e360-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="8e360-113">1\_1</span></span> | <span data-ttu-id="8e360-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8e360-114">2\_0</span></span> | <span data-ttu-id="8e360-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8e360-115">2\_x</span></span> | <span data-ttu-id="8e360-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8e360-116">2\_sw</span></span> | <span data-ttu-id="8e360-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8e360-117">3\_0</span></span> | <span data-ttu-id="8e360-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8e360-118">3\_sw</span></span> |
| <span data-ttu-id="8e360-119">abs</span><span class="sxs-lookup"><span data-stu-id="8e360-119">abs</span></span>                    |      | <span data-ttu-id="8e360-120">x</span><span class="sxs-lookup"><span data-stu-id="8e360-120">x</span></span>    | <span data-ttu-id="8e360-121">x</span><span class="sxs-lookup"><span data-stu-id="8e360-121">x</span></span>    | <span data-ttu-id="8e360-122">x</span><span class="sxs-lookup"><span data-stu-id="8e360-122">x</span></span>     | <span data-ttu-id="8e360-123">x</span><span class="sxs-lookup"><span data-stu-id="8e360-123">x</span></span>    | <span data-ttu-id="8e360-124">x</span><span class="sxs-lookup"><span data-stu-id="8e360-124">x</span></span>     |



 

<span data-ttu-id="8e360-125">Cette instruction fonctionne comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="8e360-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="8e360-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e360-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e360-127">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="8e360-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




