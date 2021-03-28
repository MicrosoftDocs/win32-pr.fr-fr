---
title: texm3x3pad-PS
description: Effectue la multiplication de la première ou de la deuxième ligne d’une multiplication de matrice de trois lignes. Cette instruction doit être utilisée en association avec texm3x3-PS, texm3x3spec-PS, texm3x3vspec-PS ou texm3x3tex-PS.
ms.assetid: 375526ee-cd58-4179-9b21-c63f17282f6b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0013c4d2baf9a404406982b5a8e984698a964f33
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381166"
---
# <a name="texm3x3pad---ps"></a><span data-ttu-id="62893-104">texm3x3pad-PS</span><span class="sxs-lookup"><span data-stu-id="62893-104">texm3x3pad - ps</span></span>

<span data-ttu-id="62893-105">Effectue la multiplication de la première ou de la deuxième ligne d’une multiplication de matrice de trois lignes.</span><span class="sxs-lookup"><span data-stu-id="62893-105">Performs the first or second row multiply of a three-row matrix multiply.</span></span> <span data-ttu-id="62893-106">Cette instruction doit être utilisée en association avec [texm3x3-PS](texm3x3---ps.md), [texm3x3spec-PS](texm3x3spec---ps.md), [texm3x3vspec-PS](texm3x3vspec---ps.md)ou [texm3x3tex-PS](texm3x3tex---ps.md).</span><span class="sxs-lookup"><span data-stu-id="62893-106">This instruction must be used in combination with [texm3x3 - ps](texm3x3---ps.md), [texm3x3spec - ps](texm3x3spec---ps.md), [texm3x3vspec - ps](texm3x3vspec---ps.md), or [texm3x3tex - ps](texm3x3tex---ps.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62893-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62893-107">Syntax</span></span>



| <span data-ttu-id="62893-108">texm3x3pad DST, SRC</span><span class="sxs-lookup"><span data-stu-id="62893-108">texm3x3pad dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="62893-109">where</span><span class="sxs-lookup"><span data-stu-id="62893-109">where</span></span>

-   <span data-ttu-id="62893-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="62893-110">dst is the destination register.</span></span>
-   <span data-ttu-id="62893-111">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="62893-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="62893-112">Notes</span><span class="sxs-lookup"><span data-stu-id="62893-112">Remarks</span></span>



| <span data-ttu-id="62893-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="62893-113">Pixel shader versions</span></span> | <span data-ttu-id="62893-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="62893-114">1\_1</span></span> | <span data-ttu-id="62893-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="62893-115">1\_2</span></span> | <span data-ttu-id="62893-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="62893-116">1\_3</span></span> | <span data-ttu-id="62893-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="62893-117">1\_4</span></span> | <span data-ttu-id="62893-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="62893-118">2\_0</span></span> | <span data-ttu-id="62893-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="62893-119">2\_x</span></span> | <span data-ttu-id="62893-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="62893-120">2\_sw</span></span> | <span data-ttu-id="62893-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="62893-121">3\_0</span></span> | <span data-ttu-id="62893-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="62893-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="62893-123">texm3x3pad</span><span class="sxs-lookup"><span data-stu-id="62893-123">texm3x3pad</span></span>            | <span data-ttu-id="62893-124">x</span><span class="sxs-lookup"><span data-stu-id="62893-124">x</span></span>    | <span data-ttu-id="62893-125">x</span><span class="sxs-lookup"><span data-stu-id="62893-125">x</span></span>    | <span data-ttu-id="62893-126">x</span><span class="sxs-lookup"><span data-stu-id="62893-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="62893-127">Cette instruction ne peut pas être utilisée par elle-même.</span><span class="sxs-lookup"><span data-stu-id="62893-127">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62893-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62893-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62893-129">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="62893-129">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




