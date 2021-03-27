---
title: ENDLOOP-PS
description: Fin d’une boucle-PS... bloc ENDLOOP.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a7eb10146e40a39c05bcecb99d3a7667dee2c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940561"
---
# <a name="endloop---ps"></a><span data-ttu-id="0b5fb-103">ENDLOOP-PS</span><span class="sxs-lookup"><span data-stu-id="0b5fb-103">endloop - ps</span></span>

<span data-ttu-id="0b5fb-104">Fin d’une [boucle-PS](loop---ps.md)... bloc ENDLOOP.</span><span class="sxs-lookup"><span data-stu-id="0b5fb-104">End of a [loop - ps](loop---ps.md)...endloop block.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b5fb-105">Notes</span><span class="sxs-lookup"><span data-stu-id="0b5fb-105">Remarks</span></span>



| <span data-ttu-id="0b5fb-106">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0b5fb-106">Pixel shader versions</span></span> | <span data-ttu-id="0b5fb-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="0b5fb-107">1\_1</span></span> | <span data-ttu-id="0b5fb-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="0b5fb-108">1\_2</span></span> | <span data-ttu-id="0b5fb-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0b5fb-109">1\_3</span></span> | <span data-ttu-id="0b5fb-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="0b5fb-110">1\_4</span></span> | <span data-ttu-id="0b5fb-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0b5fb-111">2\_0</span></span> | <span data-ttu-id="0b5fb-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0b5fb-112">2\_x</span></span> | <span data-ttu-id="0b5fb-113">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="0b5fb-113">2\_sw</span></span> | <span data-ttu-id="0b5fb-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0b5fb-114">3\_0</span></span> | <span data-ttu-id="0b5fb-115">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="0b5fb-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0b5fb-116">ENDLOOP</span><span class="sxs-lookup"><span data-stu-id="0b5fb-116">endloop</span></span>               |      |      |      |      |      |      |       | <span data-ttu-id="0b5fb-117">x</span><span class="sxs-lookup"><span data-stu-id="0b5fb-117">x</span></span>    | <span data-ttu-id="0b5fb-118">x</span><span class="sxs-lookup"><span data-stu-id="0b5fb-118">x</span></span>     |



 

<span data-ttu-id="0b5fb-119">ENDLOOP doit suivre la dernière instruction d’un bloc [Loop-PS](loop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="0b5fb-119">endloop must follow the last instruction of a [loop - ps](loop---ps.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="0b5fb-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="0b5fb-120">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="0b5fb-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b5fb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b5fb-122">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0b5fb-122">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




