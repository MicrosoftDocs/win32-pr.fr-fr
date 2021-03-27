---
title: Adressage relatif (référence du PS HLSL)
description: La syntaxe \ \ ne peut être utilisée que dans les types de registres qui peuvent être traités relativement dans certains modèles de nuanceur.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38c7be68245cfedbb27898e0fbb689e9e43755ca
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103679218"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="96f53-103">Adressage relatif (référence du PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="96f53-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="96f53-104">La \[ \] syntaxe peut être utilisée uniquement dans les types de registres qui peuvent être traités relativement dans certains modèles de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="96f53-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="96f53-105">Les formes de syntaxe prises en charge \[ \] sont répertoriées comme suit :</span><span class="sxs-lookup"><span data-stu-id="96f53-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="96f53-106">Où :</span><span class="sxs-lookup"><span data-stu-id="96f53-106">Where:</span></span>

-   <span data-ttu-id="96f53-107">« R » désigne tout type de Registre pouvant être relativement adressé.</span><span class="sxs-lookup"><span data-stu-id="96f53-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="96f53-108">« A » désigne tout registre pouvant être utilisé en tant qu’index pour adresser de manière relativement à d’autres registres.</span><span class="sxs-lookup"><span data-stu-id="96f53-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="96f53-109">N0-ni, M0-MJ et k sont des entiers >= 0.</span><span class="sxs-lookup"><span data-stu-id="96f53-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="96f53-110">\[\]syntaxe</span><span class="sxs-lookup"><span data-stu-id="96f53-110">\[ \] syntax</span></span>                              | <span data-ttu-id="96f53-111">Index effectif</span><span class="sxs-lookup"><span data-stu-id="96f53-111">Effective index</span></span>                       | <span data-ttu-id="96f53-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="96f53-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="96f53-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="96f53-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="96f53-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="96f53-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="96f53-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="96f53-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="96f53-116">R \[ k \] (= RK)</span><span class="sxs-lookup"><span data-stu-id="96f53-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="96f53-117">k</span><span class="sxs-lookup"><span data-stu-id="96f53-117">k</span></span>                                     | <span data-ttu-id="96f53-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="96f53-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="96f53-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="96f53-119">R\[ A \]</span></span>                                  | <span data-ttu-id="96f53-120">Un</span><span class="sxs-lookup"><span data-stu-id="96f53-120">A</span></span>                                     | <span data-ttu-id="96f53-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="96f53-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="96f53-122">RK \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="96f53-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="96f53-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="96f53-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="96f53-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="96f53-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="96f53-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="96f53-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="96f53-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="96f53-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="96f53-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="96f53-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="96f53-128">RK \[ A \]</span><span class="sxs-lookup"><span data-stu-id="96f53-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="96f53-129">A + k</span><span class="sxs-lookup"><span data-stu-id="96f53-129">A + k</span></span>                                 | <span data-ttu-id="96f53-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="96f53-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="96f53-131">RK \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="96f53-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="96f53-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="96f53-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="96f53-133">v1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="96f53-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="96f53-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="96f53-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="96f53-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="96f53-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="96f53-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="96f53-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="96f53-137">RK \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="96f53-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="96f53-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="96f53-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="96f53-139">O1 \[ 2 + 1 + 3 + al \]</span><span class="sxs-lookup"><span data-stu-id="96f53-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="96f53-140">Les registres sont disponibles dans les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="96f53-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="96f53-141">Type de Registre</span><span class="sxs-lookup"><span data-stu-id="96f53-141">Register type</span></span>                                                                                   | <span data-ttu-id="96f53-142">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="96f53-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="96f53-143">[compteur de boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md): Al sur les registres d’entrée</span><span class="sxs-lookup"><span data-stu-id="96f53-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="96f53-144">PS \_ 3 \_ 0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="96f53-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="96f53-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96f53-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96f53-146">Inscrit</span><span class="sxs-lookup"><span data-stu-id="96f53-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




