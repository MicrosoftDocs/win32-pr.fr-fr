---
title: Bem-PS
description: Appliquez une transformation de mappage d’environnement factice.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381195"
---
# <a name="bem---ps"></a><span data-ttu-id="c5d8f-103">Bem-PS</span><span class="sxs-lookup"><span data-stu-id="c5d8f-103">bem - ps</span></span>

<span data-ttu-id="c5d8f-104">Appliquez une transformation de mappage d’environnement factice.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d8f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5d8f-105">Syntax</span></span>



| <span data-ttu-id="c5d8f-106">Bem DST. RG, src0, src1</span><span class="sxs-lookup"><span data-stu-id="c5d8f-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="c5d8f-107">where</span><span class="sxs-lookup"><span data-stu-id="c5d8f-107">where</span></span>

-   <span data-ttu-id="c5d8f-108">DST. RG DST est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="c5d8f-109">Le masque d’écriture du composant rouge et vert doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="c5d8f-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-110">src0 is a source register.</span></span>
-   <span data-ttu-id="c5d8f-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5d8f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c5d8f-112">Remarks</span></span>



| <span data-ttu-id="c5d8f-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c5d8f-113">Pixel shader versions</span></span> | <span data-ttu-id="c5d8f-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c5d8f-114">1\_1</span></span> | <span data-ttu-id="c5d8f-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c5d8f-115">1\_2</span></span> | <span data-ttu-id="c5d8f-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c5d8f-116">1\_3</span></span> | <span data-ttu-id="c5d8f-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c5d8f-117">1\_4</span></span> | <span data-ttu-id="c5d8f-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5d8f-118">2\_0</span></span> | <span data-ttu-id="c5d8f-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c5d8f-119">2\_x</span></span> | <span data-ttu-id="c5d8f-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c5d8f-120">2\_sw</span></span> | <span data-ttu-id="c5d8f-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5d8f-121">3\_0</span></span> | <span data-ttu-id="c5d8f-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="c5d8f-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c5d8f-123">bem</span><span class="sxs-lookup"><span data-stu-id="c5d8f-123">bem</span></span>                   |      |      |      | <span data-ttu-id="c5d8f-124">x</span><span class="sxs-lookup"><span data-stu-id="c5d8f-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="c5d8f-125">Cette instruction effectue le calcul suivant.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="c5d8f-126">Règles d’utilisation de BEM :</span><span class="sxs-lookup"><span data-stu-id="c5d8f-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="c5d8f-127">Bem doit apparaître dans la première phase d’un nuanceur (c’est-à-dire avant un marqueur de phase).</span><span class="sxs-lookup"><span data-stu-id="c5d8f-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="c5d8f-128">Bem consomme deux emplacements d’instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="c5d8f-129">Une seule utilisation de cette instruction est autorisée par nuanceur.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="c5d8f-130">Le writemask de destination doit être. RG/.XY.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="c5d8f-131">Cette instruction ne peut pas être co-émise.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="c5d8f-132">Hormis la restriction selon laquelle le masque d’écriture de destination est. RG, les modificateurs sur la source src0, src1 et les modificateurs d’instruction ne sont pas restreints.</span><span class="sxs-lookup"><span data-stu-id="c5d8f-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="c5d8f-133">Informations sur les instructions</span><span class="sxs-lookup"><span data-stu-id="c5d8f-133">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="c5d8f-134">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="c5d8f-134">Minimum operating system</span></span> | <span data-ttu-id="c5d8f-135">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c5d8f-135">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c5d8f-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5d8f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5d8f-137">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c5d8f-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




