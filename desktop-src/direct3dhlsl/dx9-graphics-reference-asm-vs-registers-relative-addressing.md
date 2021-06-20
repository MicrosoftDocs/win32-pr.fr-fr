---
title: Adressage relatif (référence HLSL VS)
description: Pour les nuanceurs de vertex, la syntaxe \ \ ne peut être utilisée que dans les types de registres qui peuvent être traités relativement dans certains modèles de nuanceur.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406692"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="9269c-103">Adressage relatif (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="9269c-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="9269c-104">La \[ \] syntaxe peut être utilisée uniquement dans les types de registres qui peuvent être traités relativement dans certains modèles de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="9269c-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="9269c-105">Les formes de syntaxe prises en charge \[ \] sont répertoriées comme suit :</span><span class="sxs-lookup"><span data-stu-id="9269c-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="9269c-106">Où :</span><span class="sxs-lookup"><span data-stu-id="9269c-106">Where:</span></span>

-   <span data-ttu-id="9269c-107">« R » désigne tout type de Registre pouvant être relativement adressé.</span><span class="sxs-lookup"><span data-stu-id="9269c-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="9269c-108">« A » désigne tout registre pouvant être utilisé en tant qu’index pour adresser de manière relativement à d’autres registres.</span><span class="sxs-lookup"><span data-stu-id="9269c-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="9269c-109">N0-ni, M0-MJ et k sont des entiers >= 0.</span><span class="sxs-lookup"><span data-stu-id="9269c-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="9269c-110">\[\]syntaxe</span><span class="sxs-lookup"><span data-stu-id="9269c-110">\[ \] syntax</span></span>                              | <span data-ttu-id="9269c-111">Index effectif</span><span class="sxs-lookup"><span data-stu-id="9269c-111">Effective index</span></span>                       | <span data-ttu-id="9269c-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="9269c-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="9269c-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="9269c-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="9269c-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="9269c-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="9269c-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="9269c-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="9269c-116">R \[ k \] (= RK)</span><span class="sxs-lookup"><span data-stu-id="9269c-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="9269c-117">k</span><span class="sxs-lookup"><span data-stu-id="9269c-117">k</span></span>                                     | <span data-ttu-id="9269c-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="9269c-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="9269c-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="9269c-119">R\[ A \]</span></span>                                  | <span data-ttu-id="9269c-120">Un</span><span class="sxs-lookup"><span data-stu-id="9269c-120">A</span></span>                                     | <span data-ttu-id="9269c-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="9269c-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="9269c-122">RK \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="9269c-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="9269c-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="9269c-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="9269c-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="9269c-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="9269c-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="9269c-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="9269c-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="9269c-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="9269c-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="9269c-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="9269c-128">RK \[ A \]</span><span class="sxs-lookup"><span data-stu-id="9269c-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="9269c-129">A + k</span><span class="sxs-lookup"><span data-stu-id="9269c-129">A + k</span></span>                                 | <span data-ttu-id="9269c-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="9269c-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="9269c-131">RK \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="9269c-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="9269c-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="9269c-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="9269c-133">v1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="9269c-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="9269c-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="9269c-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="9269c-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="9269c-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="9269c-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="9269c-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="9269c-137">RK \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="9269c-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="9269c-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="9269c-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="9269c-139">O1 \[ 2 + 1 + 3 + al \]</span><span class="sxs-lookup"><span data-stu-id="9269c-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="9269c-140">Les registres sont disponibles dans les versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="9269c-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="9269c-141">Type de Registre</span><span class="sxs-lookup"><span data-stu-id="9269c-141">Register type</span></span> | <span data-ttu-id="9269c-142">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="9269c-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="9269c-143">a0</span><span class="sxs-lookup"><span data-stu-id="9269c-143">a0</span></span>            | <span data-ttu-id="9269c-144">Tous</span><span class="sxs-lookup"><span data-stu-id="9269c-144">All</span></span>                    |
| <span data-ttu-id="9269c-145">&</span><span class="sxs-lookup"><span data-stu-id="9269c-145">aL</span></span>            | <span data-ttu-id="9269c-146">vs \_ 2 \_ 0 et supérieure</span><span class="sxs-lookup"><span data-stu-id="9269c-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="9269c-147">cn</span><span class="sxs-lookup"><span data-stu-id="9269c-147">cn</span></span>            | <span data-ttu-id="9269c-148">vs \_ 1 \_ 1 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="9269c-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="9269c-149">sur</span><span class="sxs-lookup"><span data-stu-id="9269c-149">on</span></span>            | <span data-ttu-id="9269c-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9269c-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="9269c-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9269c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9269c-152">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="9269c-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




