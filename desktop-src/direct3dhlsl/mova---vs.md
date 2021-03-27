---
title: Mova-vs
description: Déplacez des données à partir d’un registre à virgule flottante vers le registre d’adresses, a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971610"
---
# <a name="mova---vs"></a><span data-ttu-id="96687-103">Mova-vs</span><span class="sxs-lookup"><span data-stu-id="96687-103">mova - vs</span></span>

<span data-ttu-id="96687-104">Déplacez des données à partir d’un registre à virgule flottante vers le [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="96687-104">Move data from a floating point register to the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>

## <a name="syntax"></a><span data-ttu-id="96687-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96687-105">Syntax</span></span>



| <span data-ttu-id="96687-106">Mova DST, SRC</span><span class="sxs-lookup"><span data-stu-id="96687-106">mova dst, src</span></span> |
|---------------|



 

<span data-ttu-id="96687-107">where</span><span class="sxs-lookup"><span data-stu-id="96687-107">where</span></span>

-   <span data-ttu-id="96687-108">l’heure d’été doit être le [Registre d’adresses](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span><span class="sxs-lookup"><span data-stu-id="96687-108">dst must be the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md), a0.</span></span>
-   <span data-ttu-id="96687-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="96687-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="96687-110">Notes</span><span class="sxs-lookup"><span data-stu-id="96687-110">Remarks</span></span>



| <span data-ttu-id="96687-111">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="96687-111">Vertex shader versions</span></span> | <span data-ttu-id="96687-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="96687-112">1\_1</span></span> | <span data-ttu-id="96687-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96687-113">2\_0</span></span> | <span data-ttu-id="96687-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="96687-114">2\_x</span></span> | <span data-ttu-id="96687-115">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="96687-115">2\_sw</span></span> | <span data-ttu-id="96687-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96687-116">3\_0</span></span> | <span data-ttu-id="96687-117">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="96687-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="96687-118">mova</span><span class="sxs-lookup"><span data-stu-id="96687-118">mova</span></span>                   |      | <span data-ttu-id="96687-119">x</span><span class="sxs-lookup"><span data-stu-id="96687-119">x</span></span>    | <span data-ttu-id="96687-120">x</span><span class="sxs-lookup"><span data-stu-id="96687-120">x</span></span>    | <span data-ttu-id="96687-121">x</span><span class="sxs-lookup"><span data-stu-id="96687-121">x</span></span>     | <span data-ttu-id="96687-122">x</span><span class="sxs-lookup"><span data-stu-id="96687-122">x</span></span>    | <span data-ttu-id="96687-123">x</span><span class="sxs-lookup"><span data-stu-id="96687-123">x</span></span>     |



 

<span data-ttu-id="96687-124">Déplace les données à virgule flottante vers un registre d’entiers.</span><span class="sxs-lookup"><span data-stu-id="96687-124">Moves floating point data to an integer register.</span></span> <span data-ttu-id="96687-125">Les valeurs sont converties de la virgule flottante à l’aide de l’arrondi au plus proche.</span><span class="sxs-lookup"><span data-stu-id="96687-125">The values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="96687-126">Le registre d’adresses est le seul registre de destination autorisé.</span><span class="sxs-lookup"><span data-stu-id="96687-126">The address register is the only destination register allowed.</span></span>

<span data-ttu-id="96687-127">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="96687-127">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



<span data-ttu-id="96687-128">Pour les versions 2 \_ x et ultérieures, le registre d’adresses est un vecteur de composant.</span><span class="sxs-lookup"><span data-stu-id="96687-128">For versions 2\_x and above, the address register is a component vector.</span></span> <span data-ttu-id="96687-129">Par conséquent, n’importe quel masque d’écriture est autorisé.</span><span class="sxs-lookup"><span data-stu-id="96687-129">Therefore, any write mask is allowed.</span></span>


```
mova a0.xz, r0
```



## <a name="related-topics"></a><span data-ttu-id="96687-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96687-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96687-131">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="96687-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




