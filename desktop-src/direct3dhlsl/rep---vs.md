---
title: REP-vs
description: Démarrer un REP... bloc endrep.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381159"
---
# <a name="rep---vs"></a><span data-ttu-id="db3ac-103">REP-vs</span><span class="sxs-lookup"><span data-stu-id="db3ac-103">rep - vs</span></span>

<span data-ttu-id="db3ac-104">Démarrer un REP... bloc [endrep](endrep---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="db3ac-104">Start a rep...[endrep](endrep---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="db3ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db3ac-105">Syntax</span></span>



| <span data-ttu-id="db3ac-106">REP i\#</span><span class="sxs-lookup"><span data-stu-id="db3ac-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="db3ac-107">où i \# est un registre d’entiers qui spécifie le nombre de répétitions dans le composant. x.</span><span class="sxs-lookup"><span data-stu-id="db3ac-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="db3ac-108">Consultez [Registre d’entiers constant](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="db3ac-108">See [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db3ac-109">Notes</span><span class="sxs-lookup"><span data-stu-id="db3ac-109">Remarks</span></span>



| <span data-ttu-id="db3ac-110">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="db3ac-110">Vertex shader versions</span></span> | <span data-ttu-id="db3ac-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="db3ac-111">1\_1</span></span> | <span data-ttu-id="db3ac-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="db3ac-112">2\_0</span></span> | <span data-ttu-id="db3ac-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="db3ac-113">2\_x</span></span> | <span data-ttu-id="db3ac-114">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="db3ac-114">2\_sw</span></span> | <span data-ttu-id="db3ac-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="db3ac-115">3\_0</span></span> | <span data-ttu-id="db3ac-116">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="db3ac-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="db3ac-117">attaché</span><span class="sxs-lookup"><span data-stu-id="db3ac-117">rep</span></span>                    |      | <span data-ttu-id="db3ac-118">x</span><span class="sxs-lookup"><span data-stu-id="db3ac-118">x</span></span>    | <span data-ttu-id="db3ac-119">x</span><span class="sxs-lookup"><span data-stu-id="db3ac-119">x</span></span>    | <span data-ttu-id="db3ac-120">x</span><span class="sxs-lookup"><span data-stu-id="db3ac-120">x</span></span>     | <span data-ttu-id="db3ac-121">x</span><span class="sxs-lookup"><span data-stu-id="db3ac-121">x</span></span>    | <span data-ttu-id="db3ac-122">x</span><span class="sxs-lookup"><span data-stu-id="db3ac-122">x</span></span>     |



 

-   <span data-ttu-id="db3ac-123">i \# . x spécifie le nombre d’itérations.</span><span class="sxs-lookup"><span data-stu-id="db3ac-123">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="db3ac-124">La plage autorisée est \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="db3ac-124">The legal range is \[0, 255\].</span></span> <span data-ttu-id="db3ac-125">Notez que cette instruction n’incrémente pas ou ne décrémente pas la valeur de i \# . x.</span><span class="sxs-lookup"><span data-stu-id="db3ac-125">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="db3ac-126">i \# . YZW ne sont pas utilisés par le bloc REPEAT.</span><span class="sxs-lookup"><span data-stu-id="db3ac-126">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="db3ac-127">Les blocs REPEAT peuvent être imbriqués.</span><span class="sxs-lookup"><span data-stu-id="db3ac-127">Repeat blocks may be nested.</span></span> <span data-ttu-id="db3ac-128">Consultez [limites d’imbrication des contrôles de Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="db3ac-128">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="db3ac-129">Les blocs de répétition sont autorisés à se trouver complètement à l’intérieur d’un bloc if ou à l' \* entourer complètement.</span><span class="sxs-lookup"><span data-stu-id="db3ac-129">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="db3ac-130">Aucun chevauchement n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="db3ac-130">No straddling is allowed.</span></span>
-   <span data-ttu-id="db3ac-131">L’utilisation du même i \# pour des instructions de représentation différentes ou imbriquées est correcte. chaque boucle effectue une itération en fonction du nombre spécifié.</span><span class="sxs-lookup"><span data-stu-id="db3ac-131">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="db3ac-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="db3ac-132">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="db3ac-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db3ac-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db3ac-134">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="db3ac-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




