---
title: CRS-vs
description: Calcule un produit croisé à l’aide de la règle de droite. | CRS-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322001"
---
# <a name="crs---vs"></a><span data-ttu-id="8db18-104">CRS-vs</span><span class="sxs-lookup"><span data-stu-id="8db18-104">crs - vs</span></span>

<span data-ttu-id="8db18-105">Calcule un produit croisé à l’aide de la règle de droite.</span><span class="sxs-lookup"><span data-stu-id="8db18-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db18-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8db18-106">Syntax</span></span>



| <span data-ttu-id="8db18-107">CRS DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="8db18-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="8db18-108">where</span><span class="sxs-lookup"><span data-stu-id="8db18-108">where</span></span>

-   <span data-ttu-id="8db18-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="8db18-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8db18-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="8db18-110">src0 is a source register.</span></span>
-   <span data-ttu-id="8db18-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="8db18-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8db18-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8db18-112">Remarks</span></span>



| <span data-ttu-id="8db18-113">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="8db18-113">Vertex shader versions</span></span> | <span data-ttu-id="8db18-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8db18-114">1\_1</span></span> | <span data-ttu-id="8db18-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8db18-115">2\_0</span></span> | <span data-ttu-id="8db18-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8db18-116">2\_x</span></span> | <span data-ttu-id="8db18-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8db18-117">2\_sw</span></span> | <span data-ttu-id="8db18-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8db18-118">3\_0</span></span> | <span data-ttu-id="8db18-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8db18-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8db18-120">Sir</span><span class="sxs-lookup"><span data-stu-id="8db18-120">crs</span></span>                    |      | <span data-ttu-id="8db18-121">x</span><span class="sxs-lookup"><span data-stu-id="8db18-121">x</span></span>    | <span data-ttu-id="8db18-122">x</span><span class="sxs-lookup"><span data-stu-id="8db18-122">x</span></span>    | <span data-ttu-id="8db18-123">x</span><span class="sxs-lookup"><span data-stu-id="8db18-123">x</span></span>     | <span data-ttu-id="8db18-124">x</span><span class="sxs-lookup"><span data-stu-id="8db18-124">x</span></span>    | <span data-ttu-id="8db18-125">x</span><span class="sxs-lookup"><span data-stu-id="8db18-125">x</span></span>     |



 

<span data-ttu-id="8db18-126">Cette instruction fonctionne comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="8db18-126">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="8db18-127">Certaines restrictions sur l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="8db18-127">Some restrictions on use:</span></span>

-   <span data-ttu-id="8db18-128">src0 ne peut pas être le même registre que dest.</span><span class="sxs-lookup"><span data-stu-id="8db18-128">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="8db18-129">src1 ne peut pas être le même registre que dest.</span><span class="sxs-lookup"><span data-stu-id="8db18-129">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="8db18-130">src0 ne peut pas avoir d’Swizzle autre que le Swizzle par défaut (. XYZW).</span><span class="sxs-lookup"><span data-stu-id="8db18-130">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="8db18-131">src1 ne peut pas avoir d’Swizzle autre que le Swizzle par défaut (. XYZW).</span><span class="sxs-lookup"><span data-stu-id="8db18-131">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="8db18-132">dest doit avoir exactement l’un des sept masques suivants :. x.y.. \| z. \| \| XY \| . XZ \| . YZ \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="8db18-132">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="8db18-133">dest doit être un registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="8db18-133">dest must be a temporary register.</span></span>
-   <span data-ttu-id="8db18-134">dest ne doit pas être le même registre que src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="8db18-134">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="8db18-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8db18-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8db18-136">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="8db18-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




