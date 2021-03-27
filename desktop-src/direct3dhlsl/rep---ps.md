---
title: REP-PS
description: Démarrer un REP... bloc endrep-PS.
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679125"
---
# <a name="rep---ps"></a><span data-ttu-id="9e06e-103">REP-PS</span><span class="sxs-lookup"><span data-stu-id="9e06e-103">rep - ps</span></span>

<span data-ttu-id="9e06e-104">Démarrer un REP... bloc [endrep-PS](endrep---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="9e06e-104">Start a rep...[endrep - ps](endrep---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e06e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e06e-105">Syntax</span></span>



| <span data-ttu-id="9e06e-106">REP i\#</span><span class="sxs-lookup"><span data-stu-id="9e06e-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="9e06e-107">où i \# est un registre d’entiers qui spécifie le nombre de répétitions dans le composant. x.</span><span class="sxs-lookup"><span data-stu-id="9e06e-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="9e06e-108">Consultez [Registre d’entiers constant](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="9e06e-108">See [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e06e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9e06e-109">Remarks</span></span>



| <span data-ttu-id="9e06e-110">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="9e06e-110">Pixel shader versions</span></span> | <span data-ttu-id="9e06e-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="9e06e-111">1\_1</span></span> | <span data-ttu-id="9e06e-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="9e06e-112">1\_2</span></span> | <span data-ttu-id="9e06e-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9e06e-113">1\_3</span></span> | <span data-ttu-id="9e06e-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="9e06e-114">1\_4</span></span> | <span data-ttu-id="9e06e-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9e06e-115">2\_0</span></span> | <span data-ttu-id="9e06e-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9e06e-116">2\_x</span></span> | <span data-ttu-id="9e06e-117">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="9e06e-117">2\_sw</span></span> | <span data-ttu-id="9e06e-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9e06e-118">3\_0</span></span> | <span data-ttu-id="9e06e-119">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="9e06e-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9e06e-120">attaché</span><span class="sxs-lookup"><span data-stu-id="9e06e-120">rep</span></span>                   |      |      |      |      |      | <span data-ttu-id="9e06e-121">x</span><span class="sxs-lookup"><span data-stu-id="9e06e-121">x</span></span>    | <span data-ttu-id="9e06e-122">x</span><span class="sxs-lookup"><span data-stu-id="9e06e-122">x</span></span>     | <span data-ttu-id="9e06e-123">x</span><span class="sxs-lookup"><span data-stu-id="9e06e-123">x</span></span>    | <span data-ttu-id="9e06e-124">x</span><span class="sxs-lookup"><span data-stu-id="9e06e-124">x</span></span>     |



 

-   <span data-ttu-id="9e06e-125">i \# . x spécifie le nombre d’itérations.</span><span class="sxs-lookup"><span data-stu-id="9e06e-125">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="9e06e-126">La plage autorisée est \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="9e06e-126">The legal range is \[0, 255\].</span></span> <span data-ttu-id="9e06e-127">Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="9e06e-127">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="9e06e-128">i \# . YZW ne sont pas utilisés par le bloc REPEAT.</span><span class="sxs-lookup"><span data-stu-id="9e06e-128">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="9e06e-129">Les blocs REPEAT peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="9e06e-129">Repeat blocks may be nested.</span></span> <span data-ttu-id="9e06e-130">Consultez [limitations du contrôle de workflow](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="9e06e-130">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="9e06e-131">Les blocs de répétition sont autorisés à se trouver complètement à l’intérieur d’un bloc if ou à l' \* entourer complètement.</span><span class="sxs-lookup"><span data-stu-id="9e06e-131">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="9e06e-132">Aucun chevauchement n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="9e06e-132">No straddling is allowed.</span></span>
-   <span data-ttu-id="9e06e-133">L’utilisation du même i \# pour des instructions de représentation différentes ou imbriquées est correcte. chaque boucle effectue une itération en fonction du nombre spécifié.</span><span class="sxs-lookup"><span data-stu-id="9e06e-133">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="9e06e-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="9e06e-134">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="9e06e-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9e06e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e06e-136">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="9e06e-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




