---
title: Modificateurs d’instruction (référence HLSL VS)
description: Modificateurs d’instruction
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104462623"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a><span data-ttu-id="2cd23-103">Modificateurs d’instruction (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="2cd23-103">Instruction modifiers (HLSL VS reference)</span></span>

<span data-ttu-id="2cd23-104">Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="2cd23-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

## <a name="_sat"></a><span data-ttu-id="2cd23-105">\_sot</span><span class="sxs-lookup"><span data-stu-id="2cd23-105">\_sat</span></span>

<span data-ttu-id="2cd23-106">Sature (ou bride) le résultat de l’instruction à \[ 0,1 \] intervalle avant d’écrire dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="2cd23-106">Saturates (or clamps) the instruction result to \[0,1\] range before writing to the destination register.</span></span>

<span data-ttu-id="2cd23-107">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2cd23-107">For example:</span></span>


```
add_sat dst, src0, src1
```



<span data-ttu-id="2cd23-108">Où :</span><span class="sxs-lookup"><span data-stu-id="2cd23-108">Where:</span></span>

<span data-ttu-id="2cd23-109">DST = clamp \_ entre \_ 0 \_ et \_ 1 (src0 + src1)</span><span class="sxs-lookup"><span data-stu-id="2cd23-109">dst = clamp\_between\_0\_and\_1(src0 + src1)</span></span>

<span data-ttu-id="2cd23-110">Le \_ modificateur d’instruction SAT ne coûte aucun emplacement d’instruction supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="2cd23-110">The \_sat instruction modifier costs no additional instruction slots.</span></span>

<span data-ttu-id="2cd23-111">En cas de prise en charge, le \_ modificateur d’instruction SAT peut être utilisé avec n’importe quelle instruction, à l’exception de : [FRC-vs](frc---vs.md), [SinCos,-vs](sincos---vs.md)et [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="2cd23-111">If supported, the \_sat instruction modifier can be used with any instruction except: [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md), and [texldl - vs](texldl---vs.md).</span></span>



| <span data-ttu-id="2cd23-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="2cd23-112">Vertex shader versions</span></span> | <span data-ttu-id="2cd23-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="2cd23-113">1\_1</span></span> | <span data-ttu-id="2cd23-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2cd23-114">2\_0</span></span> | <span data-ttu-id="2cd23-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2cd23-115">2\_x</span></span> | <span data-ttu-id="2cd23-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2cd23-116">2\_sw</span></span> | <span data-ttu-id="2cd23-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2cd23-117">3\_0</span></span> | <span data-ttu-id="2cd23-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="2cd23-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2cd23-119">\_sot</span><span class="sxs-lookup"><span data-stu-id="2cd23-119">\_sat</span></span>                  |      |      |      |       | <span data-ttu-id="2cd23-120">x</span><span class="sxs-lookup"><span data-stu-id="2cd23-120">x</span></span>    | <span data-ttu-id="2cd23-121">x</span><span class="sxs-lookup"><span data-stu-id="2cd23-121">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="2cd23-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2cd23-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd23-123">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="2cd23-123">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




