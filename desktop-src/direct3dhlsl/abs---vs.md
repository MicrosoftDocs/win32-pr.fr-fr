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
ms.openlocfilehash: 612ed14fb538a419a0e7f0b1cf07904d654bb010
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343314"
---
# <a name="abs---vs"></a><span data-ttu-id="ae27a-104">ABS-vs</span><span class="sxs-lookup"><span data-stu-id="ae27a-104">abs - vs</span></span>

<span data-ttu-id="ae27a-105">Calcule la valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="ae27a-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae27a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae27a-106">Syntax</span></span>

<span data-ttu-id="ae27a-107">**ABS DST, SRC**</span><span class="sxs-lookup"><span data-stu-id="ae27a-107">**abs dst, src**</span></span>

<span data-ttu-id="ae27a-108">where</span><span class="sxs-lookup"><span data-stu-id="ae27a-108">where</span></span>

- <span data-ttu-id="ae27a-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="ae27a-109">dst is the destination register.</span></span>
- <span data-ttu-id="ae27a-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="ae27a-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae27a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ae27a-111">Remarks</span></span>



| <span data-ttu-id="ae27a-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="ae27a-112">Vertex shader versions</span></span> | <span data-ttu-id="ae27a-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="ae27a-113">1\_1</span></span> | <span data-ttu-id="ae27a-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ae27a-114">2\_0</span></span> | <span data-ttu-id="ae27a-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ae27a-115">2\_x</span></span> | <span data-ttu-id="ae27a-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ae27a-116">2\_sw</span></span> | <span data-ttu-id="ae27a-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ae27a-117">3\_0</span></span> | <span data-ttu-id="ae27a-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ae27a-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ae27a-119">abs</span><span class="sxs-lookup"><span data-stu-id="ae27a-119">abs</span></span>                    |      | <span data-ttu-id="ae27a-120">x</span><span class="sxs-lookup"><span data-stu-id="ae27a-120">x</span></span>    | <span data-ttu-id="ae27a-121">x</span><span class="sxs-lookup"><span data-stu-id="ae27a-121">x</span></span>    | <span data-ttu-id="ae27a-122">x</span><span class="sxs-lookup"><span data-stu-id="ae27a-122">x</span></span>     | <span data-ttu-id="ae27a-123">x</span><span class="sxs-lookup"><span data-stu-id="ae27a-123">x</span></span>    | <span data-ttu-id="ae27a-124">x</span><span class="sxs-lookup"><span data-stu-id="ae27a-124">x</span></span>     |



 

<span data-ttu-id="ae27a-125">Cette instruction fonctionne comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="ae27a-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="ae27a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae27a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae27a-127">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="ae27a-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




