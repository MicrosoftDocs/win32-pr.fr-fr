---
title: DCL-(SM2, SM3-PS ASM)
description: Déclarez un registre d’entrée de nuanceur de pixels.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f2ba81650611351970ff4068edaa75d27d34fc4
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130098"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="cd881-103">DCL-(SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="cd881-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="cd881-104">Déclarez un registre d’entrée de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="cd881-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd881-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd881-105">Syntax</span></span>

<span data-ttu-id="cd881-106">DCL \[ \_ pp \] dest \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="cd881-106">dcl\[\_pp\] dest\[.mask\]</span></span>



 

<span data-ttu-id="cd881-107">Où :</span><span class="sxs-lookup"><span data-stu-id="cd881-107">Where:</span></span>

-   <span data-ttu-id="cd881-108">\[\_pp \] est une précision partielle facultative.</span><span class="sxs-lookup"><span data-stu-id="cd881-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="cd881-109">Consultez [précision partielle](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="cd881-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="cd881-110">dest est un registre de destination.</span><span class="sxs-lookup"><span data-stu-id="cd881-110">dest is a destination register.</span></span> <span data-ttu-id="cd881-111">Il doit s’agir d’un [Registre de couleur d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN) ou d’un [Registre de coordonnées de texture](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN).</span><span class="sxs-lookup"><span data-stu-id="cd881-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="cd881-112">\[. Mask \] est un masque d’écriture facultatif qui contrôle les composants du registre de destination dans lesquels il est possible d’écrire.</span><span class="sxs-lookup"><span data-stu-id="cd881-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="cd881-113">Voir [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="cd881-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd881-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd881-114">Remarks</span></span>



| <span data-ttu-id="cd881-115">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="cd881-115">Pixel shader versions</span></span> | <span data-ttu-id="cd881-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="cd881-116">1\_1</span></span> | <span data-ttu-id="cd881-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="cd881-117">1\_2</span></span> | <span data-ttu-id="cd881-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cd881-118">1\_3</span></span> | <span data-ttu-id="cd881-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="cd881-119">1\_4</span></span> | <span data-ttu-id="cd881-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd881-120">2\_0</span></span> | <span data-ttu-id="cd881-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cd881-121">2\_x</span></span> | <span data-ttu-id="cd881-122">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cd881-122">2\_sw</span></span> | <span data-ttu-id="cd881-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd881-123">3\_0</span></span> | <span data-ttu-id="cd881-124">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cd881-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="cd881-125">DCL</span><span class="sxs-lookup"><span data-stu-id="cd881-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="cd881-126">x</span><span class="sxs-lookup"><span data-stu-id="cd881-126">x</span></span>    | <span data-ttu-id="cd881-127">x</span><span class="sxs-lookup"><span data-stu-id="cd881-127">x</span></span>    | <span data-ttu-id="cd881-128">x</span><span class="sxs-lookup"><span data-stu-id="cd881-128">x</span></span>     | <span data-ttu-id="cd881-129">x</span><span class="sxs-lookup"><span data-stu-id="cd881-129">x</span></span>    | <span data-ttu-id="cd881-130">x</span><span class="sxs-lookup"><span data-stu-id="cd881-130">x</span></span>     |



 

<span data-ttu-id="cd881-131">Toutes les instructions DCL doivent apparaître avant la première instruction exécutable.</span><span class="sxs-lookup"><span data-stu-id="cd881-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd881-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd881-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd881-133">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="cd881-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




