---
title: FRC-PS
description: Retourne la partie fractionnaire de chaque composant d’entrée. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322342"
---
# <a name="frc---ps"></a><span data-ttu-id="da925-104">FRC-PS</span><span class="sxs-lookup"><span data-stu-id="da925-104">frc - ps</span></span>

<span data-ttu-id="da925-105">Retourne la partie fractionnaire de chaque composant d’entrée.</span><span class="sxs-lookup"><span data-stu-id="da925-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="da925-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da925-106">Syntax</span></span>



| <span data-ttu-id="da925-107">FRC DST, SRC</span><span class="sxs-lookup"><span data-stu-id="da925-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="da925-108">where</span><span class="sxs-lookup"><span data-stu-id="da925-108">where</span></span>

-   <span data-ttu-id="da925-109">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="da925-109">dst is the destination register.</span></span>
-   <span data-ttu-id="da925-110">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="da925-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="da925-111">Notes</span><span class="sxs-lookup"><span data-stu-id="da925-111">Remarks</span></span>



| <span data-ttu-id="da925-112">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="da925-112">Pixel shader versions</span></span> | <span data-ttu-id="da925-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="da925-113">1\_1</span></span> | <span data-ttu-id="da925-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="da925-114">1\_2</span></span> | <span data-ttu-id="da925-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="da925-115">1\_3</span></span> | <span data-ttu-id="da925-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="da925-116">1\_4</span></span> | <span data-ttu-id="da925-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da925-117">2\_0</span></span> | <span data-ttu-id="da925-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="da925-118">2\_x</span></span> | <span data-ttu-id="da925-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="da925-119">2\_sw</span></span> | <span data-ttu-id="da925-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da925-120">3\_0</span></span> | <span data-ttu-id="da925-121">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="da925-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="da925-122">frc</span><span class="sxs-lookup"><span data-stu-id="da925-122">frc</span></span>                   |      |      |      |      | <span data-ttu-id="da925-123">x</span><span class="sxs-lookup"><span data-stu-id="da925-123">x</span></span>    | <span data-ttu-id="da925-124">x</span><span class="sxs-lookup"><span data-stu-id="da925-124">x</span></span>    | <span data-ttu-id="da925-125">x</span><span class="sxs-lookup"><span data-stu-id="da925-125">x</span></span>     | <span data-ttu-id="da925-126">x</span><span class="sxs-lookup"><span data-stu-id="da925-126">x</span></span>    | <span data-ttu-id="da925-127">x</span><span class="sxs-lookup"><span data-stu-id="da925-127">x</span></span>     |



 

<span data-ttu-id="da925-128">L’extrait de code suivant montre le fonctionnement conceptuel de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="da925-128">The following code snippet shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="da925-129">La fonction Floor convertit l’argument passé dans le plus grand entier qui est inférieur ou égal à l’argument.</span><span class="sxs-lookup"><span data-stu-id="da925-129">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="da925-130">Elle est convertie en valeur float, puis soustraite de la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="da925-130">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="da925-131">La valeur fractionnaire qui en résulte est comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="da925-131">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da925-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da925-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da925-133">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="da925-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




