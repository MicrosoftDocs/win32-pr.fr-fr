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
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129928"
---
# <a name="bem---ps"></a><span data-ttu-id="ea293-103">Bem-PS</span><span class="sxs-lookup"><span data-stu-id="ea293-103">bem - ps</span></span>

<span data-ttu-id="ea293-104">Appliquez une transformation de mappage d’environnement factice.</span><span class="sxs-lookup"><span data-stu-id="ea293-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea293-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea293-105">Syntax</span></span>



| <span data-ttu-id="ea293-106">Bem DST. RG, src0, src1</span><span class="sxs-lookup"><span data-stu-id="ea293-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="ea293-107">where</span><span class="sxs-lookup"><span data-stu-id="ea293-107">where</span></span>

-   <span data-ttu-id="ea293-108">DST. RG DST est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="ea293-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="ea293-109">Le masque d’écriture du composant rouge et vert doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="ea293-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="ea293-110">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="ea293-110">src0 is a source register.</span></span>
-   <span data-ttu-id="ea293-111">src1 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="ea293-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea293-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea293-112">Remarks</span></span>



| <span data-ttu-id="ea293-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ea293-113">Pixel shader versions</span></span> | <span data-ttu-id="ea293-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="ea293-114">1\_1</span></span> | <span data-ttu-id="ea293-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="ea293-115">1\_2</span></span> | <span data-ttu-id="ea293-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ea293-116">1\_3</span></span> | <span data-ttu-id="ea293-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="ea293-117">1\_4</span></span> | <span data-ttu-id="ea293-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea293-118">2\_0</span></span> | <span data-ttu-id="ea293-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ea293-119">2\_x</span></span> | <span data-ttu-id="ea293-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ea293-120">2\_sw</span></span> | <span data-ttu-id="ea293-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ea293-121">3\_0</span></span> | <span data-ttu-id="ea293-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="ea293-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ea293-123">bem</span><span class="sxs-lookup"><span data-stu-id="ea293-123">bem</span></span>                   |      |      |      | <span data-ttu-id="ea293-124">x</span><span class="sxs-lookup"><span data-stu-id="ea293-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="ea293-125">Cette instruction effectue le calcul suivant.</span><span class="sxs-lookup"><span data-stu-id="ea293-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="ea293-126">Règles d’utilisation de BEM :</span><span class="sxs-lookup"><span data-stu-id="ea293-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="ea293-127">Bem doit apparaître dans la première phase d’un nuanceur (c’est-à-dire avant un marqueur de phase).</span><span class="sxs-lookup"><span data-stu-id="ea293-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="ea293-128">Bem consomme deux emplacements d’instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="ea293-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="ea293-129">Une seule utilisation de cette instruction est autorisée par nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ea293-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="ea293-130">Le writemask de destination doit être. RG/.XY.</span><span class="sxs-lookup"><span data-stu-id="ea293-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="ea293-131">Cette instruction ne peut pas être co-émise.</span><span class="sxs-lookup"><span data-stu-id="ea293-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="ea293-132">Hormis la restriction selon laquelle le masque d’écriture de destination est. RG, les modificateurs sur la source src0, src1 et les modificateurs d’instruction ne sont pas restreints.</span><span class="sxs-lookup"><span data-stu-id="ea293-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="ea293-133">Informations sur les instructions</span><span class="sxs-lookup"><span data-stu-id="ea293-133">Instruction Information</span></span>



| <span data-ttu-id="ea293-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea293-134">Requirement</span></span>                         | <span data-ttu-id="ea293-135">Value</span><span class="sxs-lookup"><span data-stu-id="ea293-135">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="ea293-136">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="ea293-136">Minimum operating system</span></span> | <span data-ttu-id="ea293-137">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ea293-137">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ea293-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea293-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea293-139">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="ea293-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




