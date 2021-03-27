---
title: lit-vs
description: Fournit une prise en charge partielle de l’éclairage en calculant les coefficients d’éclairage à partir de deux produits points et d’un exposant.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104971570"
---
# <a name="lit---vs"></a><span data-ttu-id="f6434-103">lit-vs</span><span class="sxs-lookup"><span data-stu-id="f6434-103">lit - vs</span></span>

<span data-ttu-id="f6434-104">Fournit une prise en charge partielle de l’éclairage en calculant les coefficients d’éclairage à partir de deux produits points et d’un exposant.</span><span class="sxs-lookup"><span data-stu-id="f6434-104">Provides partial support for lighting by calculating lighting coefficients from two dot products and an exponent.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6434-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6434-105">Syntax</span></span>



| <span data-ttu-id="f6434-106">allumé DST, SRC</span><span class="sxs-lookup"><span data-stu-id="f6434-106">lit dst, src</span></span> |
|--------------|



 

<span data-ttu-id="f6434-107">where</span><span class="sxs-lookup"><span data-stu-id="f6434-107">where</span></span>

-   <span data-ttu-id="f6434-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="f6434-108">dst is the destination register.</span></span>
-   <span data-ttu-id="f6434-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="f6434-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6434-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f6434-110">Remarks</span></span>



| <span data-ttu-id="f6434-111">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="f6434-111">Vertex shader versions</span></span> | <span data-ttu-id="f6434-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="f6434-112">1\_1</span></span> | <span data-ttu-id="f6434-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6434-113">2\_0</span></span> | <span data-ttu-id="f6434-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f6434-114">2\_x</span></span> | <span data-ttu-id="f6434-115">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="f6434-115">2\_sw</span></span> | <span data-ttu-id="f6434-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6434-116">3\_0</span></span> | <span data-ttu-id="f6434-117">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="f6434-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f6434-118">orange</span><span class="sxs-lookup"><span data-stu-id="f6434-118">lit</span></span>                    | <span data-ttu-id="f6434-119">x</span><span class="sxs-lookup"><span data-stu-id="f6434-119">x</span></span>    | <span data-ttu-id="f6434-120">x</span><span class="sxs-lookup"><span data-stu-id="f6434-120">x</span></span>    | <span data-ttu-id="f6434-121">x</span><span class="sxs-lookup"><span data-stu-id="f6434-121">x</span></span>    | <span data-ttu-id="f6434-122">x</span><span class="sxs-lookup"><span data-stu-id="f6434-122">x</span></span>     | <span data-ttu-id="f6434-123">x</span><span class="sxs-lookup"><span data-stu-id="f6434-123">x</span></span>    | <span data-ttu-id="f6434-124">x</span><span class="sxs-lookup"><span data-stu-id="f6434-124">x</span></span>     |



 

<span data-ttu-id="f6434-125">Le vecteur source est supposé contenir les valeurs indiquées dans le pseudo-code suivant.</span><span class="sxs-lookup"><span data-stu-id="f6434-125">The source vector is assumed to contain the values shown in the following pseudocode.</span></span>


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



<span data-ttu-id="f6434-126">Le fragment de code suivant montre les opérations effectuées.</span><span class="sxs-lookup"><span data-stu-id="f6434-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



<span data-ttu-id="f6434-127">Une opération arithmétique de précision réduite est acceptable pour l’évaluation du composant y de destination (dest. y).</span><span class="sxs-lookup"><span data-stu-id="f6434-127">Reduced precision arithmetic is acceptable in evaluating the destination y component (dest.y).</span></span> <span data-ttu-id="f6434-128">Une implémentation doit prendre en charge au moins huit bits fractionnaires dans l’argument Power.</span><span class="sxs-lookup"><span data-stu-id="f6434-128">An implementation must support at least eight fraction bits in the power argument.</span></span> <span data-ttu-id="f6434-129">Les produits scalaires sont calculés avec des vecteurs normalisés, et les limites de fixation sont com128 à 128.</span><span class="sxs-lookup"><span data-stu-id="f6434-129">Dot products are calculated with normalized vectors, and clamp limits are -128 to 128.</span></span>

<span data-ttu-id="f6434-130">L’erreur doit correspondre à une combinaison [logP-vs](logp---vs.md) et [exp-vs](exp---vs.md) , ou à environ un bit significatif pour un composant de couleur de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="f6434-130">Error should correspond to a [logp - vs](logp---vs.md) and [exp - vs](exp---vs.md) combination, or no more than approximately one significant bit for an 8-bit color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6434-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6434-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6434-132">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="f6434-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




