---
title: SGN-vs
description: Calcule le signe de l’entrée.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381178"
---
# <a name="sgn---vs"></a><span data-ttu-id="8d95e-103">SGN-vs</span><span class="sxs-lookup"><span data-stu-id="8d95e-103">sgn - vs</span></span>

<span data-ttu-id="8d95e-104">Calcule le signe de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="8d95e-104">Computes the sign of the input.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d95e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d95e-105">Syntax</span></span>



| <span data-ttu-id="8d95e-106">SGN DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="8d95e-106">sgn dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="8d95e-107">where</span><span class="sxs-lookup"><span data-stu-id="8d95e-107">where</span></span>

-   <span data-ttu-id="8d95e-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="8d95e-108">dst is the destination register.</span></span>
-   <span data-ttu-id="8d95e-109">src0 est un registre source.</span><span class="sxs-lookup"><span data-stu-id="8d95e-109">src0 is a source register.</span></span>
-   <span data-ttu-id="8d95e-110">src1 est un registre temporaire qui contient les résultats intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="8d95e-110">src1 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="8d95e-111">Après l’exécution, le contenu n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8d95e-111">Following execution, contents are undefined.</span></span>
-   <span data-ttu-id="8d95e-112">src2 est un registre temporaire qui contient les résultats intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="8d95e-112">src2 is a temporary register that holds intermediate results.</span></span> <span data-ttu-id="8d95e-113">Après l’exécution, le contenu n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="8d95e-113">Following execution, contents are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d95e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8d95e-114">Remarks</span></span>



| <span data-ttu-id="8d95e-115">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="8d95e-115">Vertex shader versions</span></span> | <span data-ttu-id="8d95e-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="8d95e-116">1\_1</span></span> | <span data-ttu-id="8d95e-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8d95e-117">2\_0</span></span> | <span data-ttu-id="8d95e-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8d95e-118">2\_x</span></span> | <span data-ttu-id="8d95e-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8d95e-119">2\_sw</span></span> | <span data-ttu-id="8d95e-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8d95e-120">3\_0</span></span> | <span data-ttu-id="8d95e-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8d95e-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8d95e-122">SGN</span><span class="sxs-lookup"><span data-stu-id="8d95e-122">sgn</span></span>                    |      | <span data-ttu-id="8d95e-123">x</span><span class="sxs-lookup"><span data-stu-id="8d95e-123">x</span></span>    | <span data-ttu-id="8d95e-124">x</span><span class="sxs-lookup"><span data-stu-id="8d95e-124">x</span></span>    | <span data-ttu-id="8d95e-125">x</span><span class="sxs-lookup"><span data-stu-id="8d95e-125">x</span></span>     | <span data-ttu-id="8d95e-126">x</span><span class="sxs-lookup"><span data-stu-id="8d95e-126">x</span></span>    | <span data-ttu-id="8d95e-127">x</span><span class="sxs-lookup"><span data-stu-id="8d95e-127">x</span></span>     |



 

<span data-ttu-id="8d95e-128">Cette instruction fonctionne comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8d95e-128">This instruction works as shown below.</span></span>


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



<span data-ttu-id="8d95e-129">src1 et src2 doivent être des [registres temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)différents.</span><span class="sxs-lookup"><span data-stu-id="8d95e-129">src1 and src2 must be different [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d95e-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d95e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d95e-131">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="8d95e-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




