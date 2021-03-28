---
title: breakp-PS
description: Quittez de manière conditionnelle la boucle actuelle au ENDLOOP-PS ou endrep-PS le plus proche. Utilisez l’un des composants de l’inscription de prédicat comme condition pour déterminer s’il convient ou non d’exécuter l’instruction.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381186"
---
# <a name="breakp---ps"></a><span data-ttu-id="6ed40-104">breakp-PS</span><span class="sxs-lookup"><span data-stu-id="6ed40-104">breakp - ps</span></span>

<span data-ttu-id="6ed40-105">Quittez de manière conditionnelle la boucle actuelle au [ENDLOOP-PS](endloop---ps.md) ou [endrep-PS](endrep---ps.md)le plus proche.</span><span class="sxs-lookup"><span data-stu-id="6ed40-105">Conditionally break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md).</span></span> <span data-ttu-id="6ed40-106">Utilisez l’un des composants de l’inscription de prédicat comme condition pour déterminer s’il convient ou non d’exécuter l’instruction.</span><span class="sxs-lookup"><span data-stu-id="6ed40-106">Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed40-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ed40-107">Syntax</span></span>



| <span data-ttu-id="6ed40-108">breakp \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="6ed40-108">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="6ed40-109">y</span><span class="sxs-lookup"><span data-stu-id="6ed40-109">y\</span></span>|<span data-ttu-id="6ed40-110">Lettre</span><span class="sxs-lookup"><span data-stu-id="6ed40-110">z\</span></span>|<span data-ttu-id="6ed40-111">s</span><span class="sxs-lookup"><span data-stu-id="6ed40-111">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="6ed40-112">Où :</span><span class="sxs-lookup"><span data-stu-id="6ed40-112">Where:</span></span>

-   <span data-ttu-id="6ed40-113">\[!\] est un modificateur de négation facultatif.</span><span class="sxs-lookup"><span data-stu-id="6ed40-113">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="6ed40-114">P0 correspond au [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="6ed40-114">p0 is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="6ed40-115">{x \| y \| z \| w} est le Swizzle de réplication requis sur P0.</span><span class="sxs-lookup"><span data-stu-id="6ed40-115">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed40-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6ed40-116">Remarks</span></span>



| <span data-ttu-id="6ed40-117">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6ed40-117">Pixel shader versions</span></span> | <span data-ttu-id="6ed40-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="6ed40-118">1\_1</span></span> | <span data-ttu-id="6ed40-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="6ed40-119">1\_2</span></span> | <span data-ttu-id="6ed40-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6ed40-120">1\_3</span></span> | <span data-ttu-id="6ed40-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="6ed40-121">1\_4</span></span> | <span data-ttu-id="6ed40-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ed40-122">2\_0</span></span> | <span data-ttu-id="6ed40-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6ed40-123">2\_x</span></span> | <span data-ttu-id="6ed40-124">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="6ed40-124">2\_sw</span></span> | <span data-ttu-id="6ed40-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ed40-125">3\_0</span></span> | <span data-ttu-id="6ed40-126">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="6ed40-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6ed40-127">breakp</span><span class="sxs-lookup"><span data-stu-id="6ed40-127">breakp</span></span>                |      |      |      |      |      | <span data-ttu-id="6ed40-128">x</span><span class="sxs-lookup"><span data-stu-id="6ed40-128">x</span></span>    | <span data-ttu-id="6ed40-129">x</span><span class="sxs-lookup"><span data-stu-id="6ed40-129">x</span></span>     | <span data-ttu-id="6ed40-130">x</span><span class="sxs-lookup"><span data-stu-id="6ed40-130">x</span></span>    | <span data-ttu-id="6ed40-131">x</span><span class="sxs-lookup"><span data-stu-id="6ed40-131">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="6ed40-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ed40-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed40-133">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6ed40-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




