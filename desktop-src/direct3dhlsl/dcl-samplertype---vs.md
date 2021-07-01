---
title: dcl_samplerType (SM3-vs ASM)
description: Déclarez un échantillon de nuanceur de sommets.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129867"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a><span data-ttu-id="d16f7-103">DCL \_ samplerType (SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="d16f7-103">dcl\_samplerType (sm3 - vs asm)</span></span>

<span data-ttu-id="d16f7-104">Déclarez un échantillon de nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="d16f7-104">Declare a vertex shader sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d16f7-105">Syntax</span></span>

<span data-ttu-id="d16f7-106">DCL \_ samplerType s\#</span><span class="sxs-lookup"><span data-stu-id="d16f7-106">dcl\_samplerType s\#</span></span>



 

<span data-ttu-id="d16f7-107">où :</span><span class="sxs-lookup"><span data-stu-id="d16f7-107">where:</span></span>

-   <span data-ttu-id="d16f7-108">\_samplerType définit le type de données de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d16f7-108">\_samplerType defines the sampler data type.</span></span> <span data-ttu-id="d16f7-109">Cela détermine le nombre de coordonnées requises par chaque coordonnée de texture lors de l’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="d16f7-109">This determines how many coordinates are required by each texture coordinate when sampling.</span></span> <span data-ttu-id="d16f7-110">Les dimensions de coordonnée de texture suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="d16f7-110">The following texture coordinate dimensions are defined.</span></span>
    -   <span data-ttu-id="d16f7-111">\_dimensionnel</span><span class="sxs-lookup"><span data-stu-id="d16f7-111">\_2d</span></span>
    -   <span data-ttu-id="d16f7-112">\_dernier</span><span class="sxs-lookup"><span data-stu-id="d16f7-112">\_cube</span></span>
    -   <span data-ttu-id="d16f7-113">\_agrégat</span><span class="sxs-lookup"><span data-stu-id="d16f7-113">\_volume</span></span>
-   <span data-ttu-id="d16f7-114">s \# identifie un échantillonneur où s est l’abréviation de l’échantillonneur, et \# est le numéro de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="d16f7-114">s\# identifies a sampler where s is an abbreviation for the sampler, and \# is the sampler number.</span></span> <span data-ttu-id="d16f7-115">L' [échantillonneur (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)est un Pseudo-Registre, car vous ne pouvez pas y lire ou écrire directement.</span><span class="sxs-lookup"><span data-stu-id="d16f7-115">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s are pseudo registers because you cannot directly read or write to them.</span></span>

## <a name="remarks"></a><span data-ttu-id="d16f7-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d16f7-116">Remarks</span></span>



| <span data-ttu-id="d16f7-117">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="d16f7-117">Vertex shader versions</span></span> | <span data-ttu-id="d16f7-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="d16f7-118">1\_1</span></span> | <span data-ttu-id="d16f7-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d16f7-119">2\_0</span></span> | <span data-ttu-id="d16f7-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d16f7-120">2\_x</span></span> | <span data-ttu-id="d16f7-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d16f7-121">2\_sw</span></span> | <span data-ttu-id="d16f7-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d16f7-122">3\_0</span></span> | <span data-ttu-id="d16f7-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d16f7-123">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d16f7-124">\_samplerType DCL</span><span class="sxs-lookup"><span data-stu-id="d16f7-124">dcl\_samplerType</span></span>       |      |      |      |       | <span data-ttu-id="d16f7-125">x</span><span class="sxs-lookup"><span data-stu-id="d16f7-125">x</span></span>    | <span data-ttu-id="d16f7-126">x</span><span class="sxs-lookup"><span data-stu-id="d16f7-126">x</span></span>     |



 

<span data-ttu-id="d16f7-127">Toutes les \_ instructions DCL samplerType doivent apparaître avant la première instruction exécutable.</span><span class="sxs-lookup"><span data-stu-id="d16f7-127">All dcl\_samplerType instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d16f7-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d16f7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d16f7-129">Instructions du nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="d16f7-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




