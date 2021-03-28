---
title: breakp-vs
description: Quittez de manière conditionnelle la boucle actuelle à la valeur ENDLOOP-vs ou endrep-vs la plus proche. Utilisez l’un des composants du registre de prédicat comme condition pour déterminer s’il faut ou non effectuer l’instruction.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030582"
---
# <a name="breakp---vs"></a><span data-ttu-id="16408-103">breakp-vs</span><span class="sxs-lookup"><span data-stu-id="16408-103">breakp - vs</span></span>

<span data-ttu-id="16408-104">Décomposer de manière conditionnelle de la boucle actuelle à l’instruction [ENDLOOP-vs](endloop---vs.md) ou [endrep-vs](endrep---vs.md). Utilisez l’un des composants de l’inscription de prédicat comme condition pour déterminer s’il convient ou non d’exécuter l’instruction.</span><span class="sxs-lookup"><span data-stu-id="16408-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md). Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="16408-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16408-105">Syntax</span></span>



| <span data-ttu-id="16408-106">breakp \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="16408-106">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="16408-107">y</span><span class="sxs-lookup"><span data-stu-id="16408-107">y\</span></span>|<span data-ttu-id="16408-108">Lettre</span><span class="sxs-lookup"><span data-stu-id="16408-108">z\</span></span>|<span data-ttu-id="16408-109">s</span><span class="sxs-lookup"><span data-stu-id="16408-109">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="16408-110">Où :</span><span class="sxs-lookup"><span data-stu-id="16408-110">Where:</span></span>

-   <span data-ttu-id="16408-111">\[!\] valeur booléenne facultative.</span><span class="sxs-lookup"><span data-stu-id="16408-111">\[!\] optional boolean NOT.</span></span>
-   <span data-ttu-id="16408-112">P0 correspond au registre de prédicat.</span><span class="sxs-lookup"><span data-stu-id="16408-112">p0 is the predicate register.</span></span> <span data-ttu-id="16408-113">Consultez [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="16408-113">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="16408-114">{x \| y \| z \| w} est le Swizzle de réplication requis sur P0.</span><span class="sxs-lookup"><span data-stu-id="16408-114">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="16408-115">Notes</span><span class="sxs-lookup"><span data-stu-id="16408-115">Remarks</span></span>



| <span data-ttu-id="16408-116">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="16408-116">Vertex shader versions</span></span> | <span data-ttu-id="16408-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="16408-117">1\_1</span></span> | <span data-ttu-id="16408-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16408-118">2\_0</span></span> | <span data-ttu-id="16408-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="16408-119">2\_x</span></span> | <span data-ttu-id="16408-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="16408-120">2\_sw</span></span> | <span data-ttu-id="16408-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16408-121">3\_0</span></span> | <span data-ttu-id="16408-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="16408-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="16408-123">breakp</span><span class="sxs-lookup"><span data-stu-id="16408-123">breakp</span></span>                 |      |      | <span data-ttu-id="16408-124">x</span><span class="sxs-lookup"><span data-stu-id="16408-124">x</span></span>    | <span data-ttu-id="16408-125">x</span><span class="sxs-lookup"><span data-stu-id="16408-125">x</span></span>     | <span data-ttu-id="16408-126">x</span><span class="sxs-lookup"><span data-stu-id="16408-126">x</span></span>    | <span data-ttu-id="16408-127">x</span><span class="sxs-lookup"><span data-stu-id="16408-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="16408-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="16408-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16408-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="16408-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




