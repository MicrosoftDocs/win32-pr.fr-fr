---
title: FRC-vs
description: Retourne la partie fractionnaire de chaque composant d’entrée. | FRC-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322341"
---
# <a name="frc---vs"></a><span data-ttu-id="3dd11-104">FRC-vs</span><span class="sxs-lookup"><span data-stu-id="3dd11-104">frc - vs</span></span>

<span data-ttu-id="3dd11-105">Retourne la partie fractionnaire de chaque composant d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3dd11-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd11-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3dd11-106">Syntax</span></span>



| <span data-ttu-id="3dd11-107">FRC DST, SRC</span><span class="sxs-lookup"><span data-stu-id="3dd11-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="3dd11-108">where</span><span class="sxs-lookup"><span data-stu-id="3dd11-108">where</span></span>

-   <span data-ttu-id="3dd11-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="3dd11-109">dst is the destination register.</span></span>
-   <span data-ttu-id="3dd11-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="3dd11-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd11-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3dd11-111">Remarks</span></span>



| <span data-ttu-id="3dd11-112">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="3dd11-112">Vertex shader versions</span></span> | <span data-ttu-id="3dd11-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="3dd11-113">1\_1</span></span> | <span data-ttu-id="3dd11-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dd11-114">2\_0</span></span> | <span data-ttu-id="3dd11-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3dd11-115">2\_x</span></span> | <span data-ttu-id="3dd11-116">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3dd11-116">2\_sw</span></span> | <span data-ttu-id="3dd11-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3dd11-117">3\_0</span></span> | <span data-ttu-id="3dd11-118">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="3dd11-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3dd11-119">frc</span><span class="sxs-lookup"><span data-stu-id="3dd11-119">frc</span></span>                    | <span data-ttu-id="3dd11-120">x</span><span class="sxs-lookup"><span data-stu-id="3dd11-120">x</span></span>    | <span data-ttu-id="3dd11-121">x</span><span class="sxs-lookup"><span data-stu-id="3dd11-121">x</span></span>    | <span data-ttu-id="3dd11-122">x</span><span class="sxs-lookup"><span data-stu-id="3dd11-122">x</span></span>    | <span data-ttu-id="3dd11-123">x</span><span class="sxs-lookup"><span data-stu-id="3dd11-123">x</span></span>     | <span data-ttu-id="3dd11-124">x</span><span class="sxs-lookup"><span data-stu-id="3dd11-124">x</span></span>    | <span data-ttu-id="3dd11-125">x</span><span class="sxs-lookup"><span data-stu-id="3dd11-125">x</span></span>     |



 

<span data-ttu-id="3dd11-126">Le fragment de code suivant illustre le fonctionnement conceptuel de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="3dd11-126">The following code fragment shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="3dd11-127">La fonction Floor convertit l’argument passé dans le plus grand entier qui est inférieur ou égal à l’argument.</span><span class="sxs-lookup"><span data-stu-id="3dd11-127">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="3dd11-128">Elle est convertie en valeur float, puis soustraite de la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="3dd11-128">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="3dd11-129">La valeur fractionnaire qui en résulte est comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="3dd11-129">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

<span data-ttu-id="3dd11-130">Pour la version 1 \_ 1, les masques d’écriture autorisés sont. y et. XY (. x n’est pas autorisé).</span><span class="sxs-lookup"><span data-stu-id="3dd11-130">For version 1\_1, the allowable write masks are .y and .xy (.x is not allowed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dd11-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3dd11-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd11-132">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="3dd11-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




