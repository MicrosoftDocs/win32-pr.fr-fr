---
title: phase-PS
description: L’instruction de phase marque la transition entre la phase 1 et la phase 2. Si aucune instruction de phase n’est présente, le nuanceur entier s’exécute comme s’il s’agissait d’un nuanceur de phase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030609"
---
# <a name="phase---ps"></a><span data-ttu-id="97aa7-104">phase-PS</span><span class="sxs-lookup"><span data-stu-id="97aa7-104">phase - ps</span></span>

<span data-ttu-id="97aa7-105">L’instruction de phase marque la transition entre la phase 1 et la phase 2.</span><span class="sxs-lookup"><span data-stu-id="97aa7-105">The phase instruction marks the transition between phase 1 and phase 2.</span></span> <span data-ttu-id="97aa7-106">Si aucune instruction de phase n’est présente, le nuanceur entier s’exécute comme s’il s’agissait d’un nuanceur de phase 2.</span><span class="sxs-lookup"><span data-stu-id="97aa7-106">If no phase instruction is present, the entire shader runs as if it is a phase 2 shader.</span></span>

<span data-ttu-id="97aa7-107">Cette instruction s’applique uniquement à la version 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="97aa7-107">This instruction applies to version 1\_4 only.</span></span>

## <a name="syntax"></a><span data-ttu-id="97aa7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97aa7-108">Syntax</span></span>


```
phase
```



## <a name="remarks"></a><span data-ttu-id="97aa7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="97aa7-109">Remarks</span></span>



| <span data-ttu-id="97aa7-110">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="97aa7-110">Pixel shader versions</span></span> | <span data-ttu-id="97aa7-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="97aa7-111">1\_1</span></span> | <span data-ttu-id="97aa7-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="97aa7-112">1\_2</span></span> | <span data-ttu-id="97aa7-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="97aa7-113">1\_3</span></span> | <span data-ttu-id="97aa7-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="97aa7-114">1\_4</span></span> | <span data-ttu-id="97aa7-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97aa7-115">2\_0</span></span> | <span data-ttu-id="97aa7-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="97aa7-116">2\_x</span></span> | <span data-ttu-id="97aa7-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="97aa7-117">2\_sw</span></span> | <span data-ttu-id="97aa7-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="97aa7-118">3\_0</span></span> | <span data-ttu-id="97aa7-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="97aa7-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="97aa7-120">phase</span><span class="sxs-lookup"><span data-stu-id="97aa7-120">phase</span></span>                 |      |      |      | <span data-ttu-id="97aa7-121">x</span><span class="sxs-lookup"><span data-stu-id="97aa7-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="97aa7-122">Les instructions de nuanceur qui se produisent avant l’instruction de phase sont des instructions de la phase 1.</span><span class="sxs-lookup"><span data-stu-id="97aa7-122">Shader instructions that occur before the phase instruction are phase 1 instructions.</span></span> <span data-ttu-id="97aa7-123">Toutes les autres instructions sont des instructions de la phase 2.</span><span class="sxs-lookup"><span data-stu-id="97aa7-123">All other instructions are phase 2 instructions.</span></span> <span data-ttu-id="97aa7-124">En ayant deux phases pour les instructions, le nombre maximal d’instructions par nuanceur est augmenté.</span><span class="sxs-lookup"><span data-stu-id="97aa7-124">By having two phases for instructions, the maximum number of instructions per shader is increased.</span></span>

<span data-ttu-id="97aa7-125">L’effet secondaire de la transition de phase est que le composant alpha des [registres temporaires](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) n’est pas persistant dans la transition.</span><span class="sxs-lookup"><span data-stu-id="97aa7-125">The unfortunate side-effect of the phase transition is that the alpha component of [temporary registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) do not persist across the transition.</span></span> <span data-ttu-id="97aa7-126">En d’autres termes, le composant alpha doit être réinitialisé après l’instruction de phase.</span><span class="sxs-lookup"><span data-stu-id="97aa7-126">In other words, the alpha component must be reinitialized after the phase instruction.</span></span>

## <a name="example"></a><span data-ttu-id="97aa7-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="97aa7-127">Example</span></span>

<span data-ttu-id="97aa7-128">Cet exemple montre comment regrouper des instructions en tant qu’instructions de phase 1 ou de phase 2 au sein d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="97aa7-128">This example shows how to group instructions as phase 1 or phase 2 instructions within a shader.</span></span>

<span data-ttu-id="97aa7-129">L’instruction de phase est également communément appelée marqueur de phase, car elle marque la transition entre les instructions de phase 1 et 2.</span><span class="sxs-lookup"><span data-stu-id="97aa7-129">The phase instruction is also commonly called the phase marker because it marks the transition between phase 1 and 2 instructions.</span></span> <span data-ttu-id="97aa7-130">Dans un \_ nuanceur de 4 pixels version 1, si le marqueur de phase n’est pas présent, le nuanceur est exécuté comme s’il s’exécutait à la phase 2.</span><span class="sxs-lookup"><span data-stu-id="97aa7-130">In a version 1\_4 pixel shader, if the phase marker is not present, the shader is run as if it is running in phase 2.</span></span> <span data-ttu-id="97aa7-131">C’est important, car il existe des différences entre les instructions de phase 1 et 2 et l’inscription de la disponibilité.</span><span class="sxs-lookup"><span data-stu-id="97aa7-131">This is important because there are differences between phase 1 and 2 instructions and register availability.</span></span> <span data-ttu-id="97aa7-132">Les différences sont indiquées dans la section de référence.</span><span class="sxs-lookup"><span data-stu-id="97aa7-132">The differences are noted throughout the reference section.</span></span>


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a><span data-ttu-id="97aa7-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97aa7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97aa7-134">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="97aa7-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




