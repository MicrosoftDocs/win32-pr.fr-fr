---
title: DSX-PS
description: Calcule le taux de modification de l’axe x de la cible de rendu.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 701dbe0125d10850760e6a1f08a2f84a50c55fe2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940575"
---
# <a name="dsx---ps"></a><span data-ttu-id="6915b-103">DSX-PS</span><span class="sxs-lookup"><span data-stu-id="6915b-103">dsx - ps</span></span>

<span data-ttu-id="6915b-104">Calcule le taux de modification de l’axe x de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="6915b-104">Compute the rate of change in the render target's x-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="6915b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6915b-105">Syntax</span></span>



| <span data-ttu-id="6915b-106">DSX DST, SRC</span><span class="sxs-lookup"><span data-stu-id="6915b-106">dsx dst, src</span></span> |
|--------------|



 

<span data-ttu-id="6915b-107">Où :</span><span class="sxs-lookup"><span data-stu-id="6915b-107">Where:</span></span>

-   <span data-ttu-id="6915b-108">l’heure d’été est un registre de destination.</span><span class="sxs-lookup"><span data-stu-id="6915b-108">dst is a destination register.</span></span>
-   <span data-ttu-id="6915b-109">SRC est un registre de source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6915b-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="6915b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6915b-110">Remarks</span></span>



| <span data-ttu-id="6915b-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6915b-111">Pixel shader versions</span></span> | <span data-ttu-id="6915b-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="6915b-112">1\_1</span></span> | <span data-ttu-id="6915b-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="6915b-113">1\_2</span></span> | <span data-ttu-id="6915b-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6915b-114">1\_3</span></span> | <span data-ttu-id="6915b-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="6915b-115">1\_4</span></span> | <span data-ttu-id="6915b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6915b-116">2\_0</span></span> | <span data-ttu-id="6915b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6915b-117">2\_x</span></span> | <span data-ttu-id="6915b-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="6915b-118">2\_sw</span></span> | <span data-ttu-id="6915b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6915b-119">3\_0</span></span> | <span data-ttu-id="6915b-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="6915b-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6915b-121">dsx</span><span class="sxs-lookup"><span data-stu-id="6915b-121">dsx</span></span>                   |      |      |      |      |      | <span data-ttu-id="6915b-122">x</span><span class="sxs-lookup"><span data-stu-id="6915b-122">x</span></span>    | <span data-ttu-id="6915b-123">x</span><span class="sxs-lookup"><span data-stu-id="6915b-123">x</span></span>     | <span data-ttu-id="6915b-124">x</span><span class="sxs-lookup"><span data-stu-id="6915b-124">x</span></span>    | <span data-ttu-id="6915b-125">x</span><span class="sxs-lookup"><span data-stu-id="6915b-125">x</span></span>     |



 

<span data-ttu-id="6915b-126">Le taux de modification calculé à partir du Registre source est une approximation sur le contenu du même registre dans le ou les pixels adjacents qui exécutent le nuanceur de pixels dans l’étape de verrouillage avec le pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="6915b-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="6915b-127">Les instructions DSX et [DSY](dsy---ps.md) calculent leur résultat en examinant le contenu actuel du Registre source (par composant) pour les différents pixels de la zone locale s’exécutant dans l’étape de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="6915b-127">The dsx And [dsy](dsy---ps.md) instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="6915b-128">La formule exacte utilisée pour calculer le dégradé varie en fonction du matériel, mais doit être cohérente avec la manière dont le matériel effectue les mêmes opérations dans le cadre du processus de calcul du niveau de détail pour l’échantillonnage de texture.</span><span class="sxs-lookup"><span data-stu-id="6915b-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6915b-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6915b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6915b-130">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="6915b-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="6915b-131">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="6915b-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




