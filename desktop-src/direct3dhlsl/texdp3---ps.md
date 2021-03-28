---
title: texdp3-PS
description: Exécute un produit scalaire à trois composants entre les données du numéro du registre de texture et le jeu de coordonnées de texture correspondant au numéro de registre de destination.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313618"
---
# <a name="texdp3---ps"></a><span data-ttu-id="7cdd4-103">texdp3-PS</span><span class="sxs-lookup"><span data-stu-id="7cdd4-103">texdp3 - ps</span></span>

<span data-ttu-id="7cdd4-104">Exécute un produit scalaire à trois composants entre les données du numéro du registre de texture et le jeu de coordonnées de texture correspondant au numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="7cdd4-104">Performs a three-component dot product between data in the texture register number and the texture coordinate set corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cdd4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cdd4-105">Syntax</span></span>



| <span data-ttu-id="7cdd4-106">texdp3 DST, SRC</span><span class="sxs-lookup"><span data-stu-id="7cdd4-106">texdp3 dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="7cdd4-107">where</span><span class="sxs-lookup"><span data-stu-id="7cdd4-107">where</span></span>

-   <span data-ttu-id="7cdd4-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="7cdd4-108">dst is the destination register.</span></span>
-   <span data-ttu-id="7cdd4-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="7cdd4-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cdd4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7cdd4-110">Remarks</span></span>



| <span data-ttu-id="7cdd4-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="7cdd4-111">Pixel shader versions</span></span> | <span data-ttu-id="7cdd4-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="7cdd4-112">1\_1</span></span> | <span data-ttu-id="7cdd4-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="7cdd4-113">1\_2</span></span> | <span data-ttu-id="7cdd4-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7cdd4-114">1\_3</span></span> | <span data-ttu-id="7cdd4-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="7cdd4-115">1\_4</span></span> | <span data-ttu-id="7cdd4-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cdd4-116">2\_0</span></span> | <span data-ttu-id="7cdd4-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7cdd4-117">2\_x</span></span> | <span data-ttu-id="7cdd4-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="7cdd4-118">2\_sw</span></span> | <span data-ttu-id="7cdd4-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cdd4-119">3\_0</span></span> | <span data-ttu-id="7cdd4-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="7cdd4-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7cdd4-121">texdp3</span><span class="sxs-lookup"><span data-stu-id="7cdd4-121">texdp3</span></span>                |      | <span data-ttu-id="7cdd4-122">x</span><span class="sxs-lookup"><span data-stu-id="7cdd4-122">x</span></span>    | <span data-ttu-id="7cdd4-123">x</span><span class="sxs-lookup"><span data-stu-id="7cdd4-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="7cdd4-124">Les registres de texture doivent utiliser la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="7cdd4-124">Texture registers must use the following sequence.</span></span>


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



<span data-ttu-id="7cdd4-125">Voici plus de détails sur la façon dont le produit scalaire est accompli.</span><span class="sxs-lookup"><span data-stu-id="7cdd4-125">Here is more detail about how the dot product is accomplished.</span></span>

<span data-ttu-id="7cdd4-126">L’instruction texdp3 exécute un produit à trois composants et la réplique sur les quatre canaux de couleurs.</span><span class="sxs-lookup"><span data-stu-id="7cdd4-126">The texdp3 instruction performs a three-component dot product and replicates it to all four color channels.</span></span>

<span data-ttu-id="7cdd4-127">t (m)<sub>RVBA</sub> = TextureCoordinates (étape m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="7cdd4-127">t(m)<sub>RGBA</sub> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

## <a name="related-topics"></a><span data-ttu-id="7cdd4-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7cdd4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cdd4-129">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="7cdd4-129">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




