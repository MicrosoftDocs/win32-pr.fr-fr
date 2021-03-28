---
title: CRS-PS
description: Calcule un produit croisé à l’aide de la règle de droite. | CRS-PS
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322002"
---
# <a name="crs---ps"></a><span data-ttu-id="ea594-104">CRS-PS</span><span class="sxs-lookup"><span data-stu-id="ea594-104">crs - ps</span></span>

<span data-ttu-id="ea594-105">Calcule un produit croisé à l’aide de la règle de droite.</span><span class="sxs-lookup"><span data-stu-id="ea594-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea594-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea594-106">Syntax</span></span>



| <span data-ttu-id="ea594-107">CRS DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="ea594-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="ea594-108">where</span><span class="sxs-lookup"><span data-stu-id="ea594-108">where</span></span>

-   <span data-ttu-id="ea594-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="ea594-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ea594-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="ea594-110">src0 is a source register.</span></span>
-   <span data-ttu-id="ea594-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="ea594-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea594-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ea594-112">Remarks</span></span>



| <span data-ttu-id="ea594-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ea594-113">Pixel shader versions</span></span> | <span data-ttu-id="ea594-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="ea594-114">1\_1</span></span> | <span data-ttu-id="ea594-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="ea594-115">1\_2</span></span> | <span data-ttu-id="ea594-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ea594-116">1\_3</span></span> | <span data-ttu-id="ea594-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="ea594-117">1\_4</span></span> | <span data-ttu-id="ea594-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea594-118">2\_0</span></span> | <span data-ttu-id="ea594-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ea594-119">2\_x</span></span> | <span data-ttu-id="ea594-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ea594-120">2\_sw</span></span> | <span data-ttu-id="ea594-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea594-121">3\_0</span></span> | <span data-ttu-id="ea594-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ea594-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ea594-123">Sir</span><span class="sxs-lookup"><span data-stu-id="ea594-123">crs</span></span>                   |      |      |      |      | <span data-ttu-id="ea594-124">x</span><span class="sxs-lookup"><span data-stu-id="ea594-124">x</span></span>    | <span data-ttu-id="ea594-125">x</span><span class="sxs-lookup"><span data-stu-id="ea594-125">x</span></span>    | <span data-ttu-id="ea594-126">x</span><span class="sxs-lookup"><span data-stu-id="ea594-126">x</span></span>     | <span data-ttu-id="ea594-127">x</span><span class="sxs-lookup"><span data-stu-id="ea594-127">x</span></span>    | <span data-ttu-id="ea594-128">x</span><span class="sxs-lookup"><span data-stu-id="ea594-128">x</span></span>     |



 

<span data-ttu-id="ea594-129">Cette instruction fonctionne comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="ea594-129">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="ea594-130">Certaines restrictions sur l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="ea594-130">Some restrictions on use:</span></span>

-   <span data-ttu-id="ea594-131">src0 ne peut pas être le même registre que dest.</span><span class="sxs-lookup"><span data-stu-id="ea594-131">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="ea594-132">src1 ne peut pas être le même registre que dest.</span><span class="sxs-lookup"><span data-stu-id="ea594-132">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="ea594-133">src0 ne peut pas avoir d’Swizzle autre que le Swizzle par défaut (. XYZW).</span><span class="sxs-lookup"><span data-stu-id="ea594-133">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="ea594-134">src1 ne peut pas avoir d’Swizzle autre que le Swizzle par défaut (. XYZW).</span><span class="sxs-lookup"><span data-stu-id="ea594-134">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="ea594-135">dest doit avoir exactement l’un des sept masques suivants :. x.y.. \| z. \| \| XY \| . XZ \| . YZ \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="ea594-135">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="ea594-136">dest doit être un registre temporaire.</span><span class="sxs-lookup"><span data-stu-id="ea594-136">dest must be a temporary register.</span></span>
-   <span data-ttu-id="ea594-137">dest ne doit pas être le même registre que src0 ou src1</span><span class="sxs-lookup"><span data-stu-id="ea594-137">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea594-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea594-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea594-139">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ea594-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




