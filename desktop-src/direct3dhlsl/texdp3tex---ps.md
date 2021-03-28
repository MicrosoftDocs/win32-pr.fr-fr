---
title: texdp3tex-PS
description: Exécute un produit scalaire à trois composants et utilise le résultat pour effectuer une recherche de texture 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104990712"
---
# <a name="texdp3tex---ps"></a><span data-ttu-id="459c1-103">texdp3tex-PS</span><span class="sxs-lookup"><span data-stu-id="459c1-103">texdp3tex - ps</span></span>

<span data-ttu-id="459c1-104">Exécute un produit scalaire à trois composants et utilise le résultat pour effectuer une recherche de texture 1D.</span><span class="sxs-lookup"><span data-stu-id="459c1-104">Performs a three-component dot product and uses the result to do a 1D texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="459c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="459c1-105">Syntax</span></span>



| <span data-ttu-id="459c1-106">texdp3tex DST, SRC</span><span class="sxs-lookup"><span data-stu-id="459c1-106">texdp3tex dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="459c1-107">where</span><span class="sxs-lookup"><span data-stu-id="459c1-107">where</span></span>

-   <span data-ttu-id="459c1-108">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="459c1-108">dst is the destination register.</span></span>
-   <span data-ttu-id="459c1-109">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="459c1-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="459c1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="459c1-110">Remarks</span></span>



| <span data-ttu-id="459c1-111">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="459c1-111">Pixel shader versions</span></span> | <span data-ttu-id="459c1-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="459c1-112">1\_1</span></span> | <span data-ttu-id="459c1-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="459c1-113">1\_2</span></span> | <span data-ttu-id="459c1-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="459c1-114">1\_3</span></span> | <span data-ttu-id="459c1-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="459c1-115">1\_4</span></span> | <span data-ttu-id="459c1-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="459c1-116">2\_0</span></span> | <span data-ttu-id="459c1-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="459c1-117">2\_x</span></span> | <span data-ttu-id="459c1-118">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="459c1-118">2\_sw</span></span> | <span data-ttu-id="459c1-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="459c1-119">3\_0</span></span> | <span data-ttu-id="459c1-120">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="459c1-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="459c1-121">texdp3tex</span><span class="sxs-lookup"><span data-stu-id="459c1-121">texdp3tex</span></span>             |      | <span data-ttu-id="459c1-122">x</span><span class="sxs-lookup"><span data-stu-id="459c1-122">x</span></span>    | <span data-ttu-id="459c1-123">x</span><span class="sxs-lookup"><span data-stu-id="459c1-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="459c1-124">Les registres de texture doivent utiliser la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="459c1-124">Texture registers must use the following sequence.</span></span>


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



<span data-ttu-id="459c1-125">Voici plus de détails sur la façon dont le produit scalaire et la recherche de texture sont effectués.</span><span class="sxs-lookup"><span data-stu-id="459c1-125">Here is more detail about how the dot product and texture lookup are done.</span></span>

<span data-ttu-id="459c1-126">L’instruction texdp3tex exécute un produit à trois composants.</span><span class="sxs-lookup"><span data-stu-id="459c1-126">The texdp3tex instruction performs a three-component dot product.</span></span>

<span data-ttu-id="459c1-127">u' = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="459c1-127">u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="459c1-128">Le résultat est utilisé pour échantillonner la texture à l’étape de texture m en effectuant une recherche 1D.</span><span class="sxs-lookup"><span data-stu-id="459c1-128">The result is used to sample the texture at texture stage m by performing a 1D lookup.</span></span>

<span data-ttu-id="459c1-129">t (m)<sub>RVBA</sub> = TextureSample (stage m)<sub>RVBA</sub> utilisant (u', 0,0) comme coordonnées</span><span class="sxs-lookup"><span data-stu-id="459c1-129">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates</span></span>

## <a name="related-topics"></a><span data-ttu-id="459c1-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="459c1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="459c1-131">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="459c1-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




