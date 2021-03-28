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
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030617"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a><span data-ttu-id="8cbd6-103">DCL \_ samplerType (SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="8cbd6-103">dcl\_samplerType (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="8cbd6-104">Déclarez un échantillon de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-104">Declare a pixel shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cbd6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cbd6-105">Syntax</span></span>



|                      |
|----------------------|
| <span data-ttu-id="8cbd6-106">DCL \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="8cbd6-106">dcl\_samplerType s\#</span></span> |



 

<span data-ttu-id="8cbd6-107">où :</span><span class="sxs-lookup"><span data-stu-id="8cbd6-107">where:</span></span>

-   <span data-ttu-id="8cbd6-108">\_samplerType définit le type de données de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="8cbd6-109">Cela détermine le nombre de coordonnées requises par chaque coordonnée de texture lors de l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="8cbd6-110">Les dimensions de coordonnée de texture suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="8cbd6-111">\_dimensionnel</span><span class="sxs-lookup"><span data-stu-id="8cbd6-111">\_2d</span></span>
    -   <span data-ttu-id="8cbd6-112">\_dernier</span><span class="sxs-lookup"><span data-stu-id="8cbd6-112">\_cube</span></span>
    -   <span data-ttu-id="8cbd6-113">\_agrégat</span><span class="sxs-lookup"><span data-stu-id="8cbd6-113">\_volume</span></span>
-   <span data-ttu-id="8cbd6-114">s \# identifie un échantillonneur où s est l’abréviation de l’échantillonneur, et \# est le numéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="8cbd6-115">Les échantillonneurs sont des Pseudo-registres, car vous ne pouvez pas les lire ou les écrire directement.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-115">Samplers are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cbd6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8cbd6-116">Remarks</span></span>



| <span data-ttu-id="8cbd6-117">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8cbd6-117">Pixel shader versions</span></span> | <span data-ttu-id="8cbd6-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="8cbd6-118">1\_1</span></span> | <span data-ttu-id="8cbd6-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="8cbd6-119">1\_2</span></span> | <span data-ttu-id="8cbd6-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8cbd6-120">1\_3</span></span> | <span data-ttu-id="8cbd6-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="8cbd6-121">1\_4</span></span> | <span data-ttu-id="8cbd6-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8cbd6-122">2\_0</span></span> | <span data-ttu-id="8cbd6-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8cbd6-123">2\_x</span></span> | <span data-ttu-id="8cbd6-124">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8cbd6-124">2\_sw</span></span> | <span data-ttu-id="8cbd6-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8cbd6-125">3\_0</span></span> | <span data-ttu-id="8cbd6-126">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8cbd6-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8cbd6-127">\_samplerType DCL</span><span class="sxs-lookup"><span data-stu-id="8cbd6-127">dcl\_samplerType</span></span>      |      |      |      |      | <span data-ttu-id="8cbd6-128">x</span><span class="sxs-lookup"><span data-stu-id="8cbd6-128">x</span></span>    | <span data-ttu-id="8cbd6-129">x</span><span class="sxs-lookup"><span data-stu-id="8cbd6-129">x</span></span>    | <span data-ttu-id="8cbd6-130">x</span><span class="sxs-lookup"><span data-stu-id="8cbd6-130">x</span></span>     | <span data-ttu-id="8cbd6-131">x</span><span class="sxs-lookup"><span data-stu-id="8cbd6-131">x</span></span>    | <span data-ttu-id="8cbd6-132">x</span><span class="sxs-lookup"><span data-stu-id="8cbd6-132">x</span></span>     |



 

<span data-ttu-id="8cbd6-133">Toutes les \_ instructions DCL samplerType doivent apparaître avant la première instruction exécutable.</span><span class="sxs-lookup"><span data-stu-id="8cbd6-133">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="example"></a><span data-ttu-id="8cbd6-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="8cbd6-134">Example</span></span>


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a><span data-ttu-id="8cbd6-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8cbd6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cbd6-136">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8cbd6-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




