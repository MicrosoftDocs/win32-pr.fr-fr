---
title: Adressage relatif (référence du PS HLSL)
description: Pour les nuanceurs de pixels, la syntaxe \ \ ne peut être utilisée que dans les types de registres qui peuvent être traités relativement dans certains modèles de nuanceur.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405482"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="0305a-103">Adressage relatif (référence du PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="0305a-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="0305a-104">La \[ \] syntaxe peut être utilisée uniquement dans les types de registres qui peuvent être traités relativement dans certains modèles de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="0305a-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="0305a-105">Les formes de syntaxe prises en charge \[ \] sont répertoriées comme suit :</span><span class="sxs-lookup"><span data-stu-id="0305a-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="0305a-106">Où :</span><span class="sxs-lookup"><span data-stu-id="0305a-106">Where:</span></span>

-   <span data-ttu-id="0305a-107">« R » désigne tout type de Registre pouvant être relativement adressé.</span><span class="sxs-lookup"><span data-stu-id="0305a-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="0305a-108">« A » désigne tout registre pouvant être utilisé en tant qu’index pour adresser de manière relativement à d’autres registres.</span><span class="sxs-lookup"><span data-stu-id="0305a-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="0305a-109">N0-ni, M0-MJ et k sont des entiers >= 0.</span><span class="sxs-lookup"><span data-stu-id="0305a-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="0305a-110">\[\]syntaxe</span><span class="sxs-lookup"><span data-stu-id="0305a-110">\[ \] syntax</span></span>                              | <span data-ttu-id="0305a-111">Index effectif</span><span class="sxs-lookup"><span data-stu-id="0305a-111">Effective index</span></span>                       | <span data-ttu-id="0305a-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="0305a-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="0305a-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="0305a-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="0305a-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="0305a-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="0305a-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="0305a-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="0305a-116">R \[ k \] (= RK)</span><span class="sxs-lookup"><span data-stu-id="0305a-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="0305a-117">k</span><span class="sxs-lookup"><span data-stu-id="0305a-117">k</span></span>                                     | <span data-ttu-id="0305a-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="0305a-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="0305a-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="0305a-119">R\[ A \]</span></span>                                  | <span data-ttu-id="0305a-120">Un</span><span class="sxs-lookup"><span data-stu-id="0305a-120">A</span></span>                                     | <span data-ttu-id="0305a-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="0305a-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="0305a-122">RK \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="0305a-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="0305a-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="0305a-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="0305a-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="0305a-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="0305a-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="0305a-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="0305a-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="0305a-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="0305a-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="0305a-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="0305a-128">RK \[ A \]</span><span class="sxs-lookup"><span data-stu-id="0305a-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="0305a-129">A + k</span><span class="sxs-lookup"><span data-stu-id="0305a-129">A + k</span></span>                                 | <span data-ttu-id="0305a-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="0305a-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="0305a-131">RK \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="0305a-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="0305a-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="0305a-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="0305a-133">v1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="0305a-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="0305a-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="0305a-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="0305a-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="0305a-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="0305a-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="0305a-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="0305a-137">RK \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="0305a-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="0305a-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="0305a-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="0305a-139">O1 \[ 2 + 1 + 3 + al \]</span><span class="sxs-lookup"><span data-stu-id="0305a-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="0305a-140">Les registres sont disponibles dans les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0305a-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="0305a-141">Type de Registre</span><span class="sxs-lookup"><span data-stu-id="0305a-141">Register type</span></span>                                                                                   | <span data-ttu-id="0305a-142">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="0305a-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="0305a-143">[compteur de boucle](dx9-graphics-reference-asm-ps-registers-loop-counter.md): Al sur les registres d’entrée</span><span class="sxs-lookup"><span data-stu-id="0305a-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="0305a-144">PS \_ 3 \_ 0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0305a-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="0305a-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0305a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0305a-146">Inscrit</span><span class="sxs-lookup"><span data-stu-id="0305a-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




