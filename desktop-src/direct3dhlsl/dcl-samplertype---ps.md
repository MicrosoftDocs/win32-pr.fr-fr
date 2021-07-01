---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Déclarez un échantillon de nuanceur de pixels.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129666"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="d573f-103">DCL \_ samplerType (SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="d573f-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="d573f-104">Déclarez un échantillon de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="d573f-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="d573f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d573f-105">Syntax</span></span>

<span data-ttu-id="d573f-106">DCL \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="d573f-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="d573f-107">où :</span><span class="sxs-lookup"><span data-stu-id="d573f-107">where:</span></span>

-   <span data-ttu-id="d573f-108">\_samplerType définit le type de données de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d573f-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="d573f-109">Cela détermine le nombre de coordonnées requises par chaque coordonnée de texture lors de l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="d573f-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="d573f-110">Les dimensions de coordonnée de texture suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="d573f-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="d573f-111">\_dimensionnel</span><span class="sxs-lookup"><span data-stu-id="d573f-111">\_2d</span></span>
    -   <span data-ttu-id="d573f-112">\_dernier</span><span class="sxs-lookup"><span data-stu-id="d573f-112">\_cube</span></span>
    -   <span data-ttu-id="d573f-113">\_agrégat</span><span class="sxs-lookup"><span data-stu-id="d573f-113">\_volume</span></span>
-   <span data-ttu-id="d573f-114">s \# identifie un échantillonneur où s est l’abréviation de l’échantillonneur, et \# est le numéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d573f-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="d573f-115">Les échantillonneurs sont des Pseudo-registres, car vous ne pouvez pas les lire ou les écrire directement.</span><span class="sxs-lookup"><span data-stu-id="d573f-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="d573f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d573f-116">Remarks</span></span>



| <span data-ttu-id="d573f-117">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d573f-117">Pixel shader versions</span></span> | <span data-ttu-id="d573f-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="d573f-118">1\_1</span></span> | <span data-ttu-id="d573f-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="d573f-119">1\_2</span></span> | <span data-ttu-id="d573f-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d573f-120">1\_3</span></span> | <span data-ttu-id="d573f-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="d573f-121">1\_4</span></span> | <span data-ttu-id="d573f-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d573f-122">2\_0</span></span> | <span data-ttu-id="d573f-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d573f-123">2\_x</span></span> | <span data-ttu-id="d573f-124">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d573f-124">2\_sw</span></span> | <span data-ttu-id="d573f-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d573f-125">3\_0</span></span> | <span data-ttu-id="d573f-126">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d573f-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d573f-127">\_samplerType DCL</span><span class="sxs-lookup"><span data-stu-id="d573f-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="d573f-128">x</span><span class="sxs-lookup"><span data-stu-id="d573f-128">x</span></span>    | <span data-ttu-id="d573f-129">x</span><span class="sxs-lookup"><span data-stu-id="d573f-129">x</span></span>    | <span data-ttu-id="d573f-130">x</span><span class="sxs-lookup"><span data-stu-id="d573f-130">x</span></span>     | <span data-ttu-id="d573f-131">x</span><span class="sxs-lookup"><span data-stu-id="d573f-131">x</span></span>    | <span data-ttu-id="d573f-132">x</span><span class="sxs-lookup"><span data-stu-id="d573f-132">x</span></span>     |



 

<span data-ttu-id="d573f-133">Toutes les \_ instructions DCL samplerType doivent apparaître avant la première instruction exécutable.</span><span class="sxs-lookup"><span data-stu-id="d573f-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="d573f-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="d573f-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="d573f-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d573f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d573f-136">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d573f-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




