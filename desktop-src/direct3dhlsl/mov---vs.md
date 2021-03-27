---
title: MOV-vs
description: Déplacer des données à virgule flottante entre registres.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103679169"
---
# <a name="mov---vs"></a><span data-ttu-id="b1044-103">MOV-vs</span><span class="sxs-lookup"><span data-stu-id="b1044-103">mov - vs</span></span>

<span data-ttu-id="b1044-104">Déplacer des données à virgule flottante entre registres.</span><span class="sxs-lookup"><span data-stu-id="b1044-104">Move floating-point data between registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1044-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1044-105">Syntax</span></span>



| <span data-ttu-id="b1044-106">MOV DST, SRC</span><span class="sxs-lookup"><span data-stu-id="b1044-106">mov dst, src</span></span> |
|--------------|



 

<span data-ttu-id="b1044-107">where</span><span class="sxs-lookup"><span data-stu-id="b1044-107">where</span></span>

-   <span data-ttu-id="b1044-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="b1044-108">dst is the destination register.</span></span>
-   <span data-ttu-id="b1044-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="b1044-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1044-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b1044-110">Remarks</span></span>



| <span data-ttu-id="b1044-111">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="b1044-111">Vertex shader versions</span></span> | <span data-ttu-id="b1044-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="b1044-112">1\_1</span></span> | <span data-ttu-id="b1044-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1044-113">2\_0</span></span> | <span data-ttu-id="b1044-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b1044-114">2\_x</span></span> | <span data-ttu-id="b1044-115">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b1044-115">2\_sw</span></span> | <span data-ttu-id="b1044-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b1044-116">3\_0</span></span> | <span data-ttu-id="b1044-117">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b1044-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b1044-118">Moy</span><span class="sxs-lookup"><span data-stu-id="b1044-118">mov</span></span>                    | <span data-ttu-id="b1044-119">x</span><span class="sxs-lookup"><span data-stu-id="b1044-119">x</span></span>    | <span data-ttu-id="b1044-120">x</span><span class="sxs-lookup"><span data-stu-id="b1044-120">x</span></span>    | <span data-ttu-id="b1044-121">x</span><span class="sxs-lookup"><span data-stu-id="b1044-121">x</span></span>    | <span data-ttu-id="b1044-122">x</span><span class="sxs-lookup"><span data-stu-id="b1044-122">x</span></span>     | <span data-ttu-id="b1044-123">x</span><span class="sxs-lookup"><span data-stu-id="b1044-123">x</span></span>    | <span data-ttu-id="b1044-124">x</span><span class="sxs-lookup"><span data-stu-id="b1044-124">x</span></span>     |



 

<span data-ttu-id="b1044-125">Peut être utilisé pour les données à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="b1044-125">Can be used for floating point data.</span></span> <span data-ttu-id="b1044-126">Pour la version vs \_ 1 \_ 1, il peut également être utilisé pour écrire le registre d’adresses.</span><span class="sxs-lookup"><span data-stu-id="b1044-126">For version vs\_1\_1, it can also be used to write the address register.</span></span> <span data-ttu-id="b1044-127">Lorsqu’elles sont utilisées pour mettre à jour des registres d’adresses, les valeurs sont converties de la virgule flottante à l’aide de l’arrondi au plus proche.</span><span class="sxs-lookup"><span data-stu-id="b1044-127">When used to update address registers, the values are converted from floating point using rounding to nearest.</span></span>

<span data-ttu-id="b1044-128">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="b1044-128">The following code fragment shows the operations performed.</span></span>


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a><span data-ttu-id="b1044-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1044-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1044-130">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="b1044-130">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




