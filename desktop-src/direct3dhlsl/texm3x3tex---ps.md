---
title: texm3x3tex-PS
description: Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture. texm3x3tex doit être utilisé avec deux instructions texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381245"
---
# <a name="texm3x3tex---ps"></a><span data-ttu-id="d58a4-104">texm3x3tex-PS</span><span class="sxs-lookup"><span data-stu-id="d58a4-104">texm3x3tex - ps</span></span>

<span data-ttu-id="d58a4-105">Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="d58a4-105">Performs a 3x3 matrix multiply and uses the result to do a texture lookup.</span></span> <span data-ttu-id="d58a4-106">texm3x3tex doit être utilisé avec deux instructions [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="d58a4-106">texm3x3tex must be used with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d58a4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d58a4-107">Syntax</span></span>



| <span data-ttu-id="d58a4-108">texm3x3tex DST, SRC</span><span class="sxs-lookup"><span data-stu-id="d58a4-108">texm3x3tex dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="d58a4-109">where</span><span class="sxs-lookup"><span data-stu-id="d58a4-109">where</span></span>

-   <span data-ttu-id="d58a4-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="d58a4-110">dst is the destination register.</span></span>
-   <span data-ttu-id="d58a4-111">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="d58a4-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d58a4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d58a4-112">Remarks</span></span>



| <span data-ttu-id="d58a4-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d58a4-113">Pixel shader versions</span></span> | <span data-ttu-id="d58a4-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="d58a4-114">1\_1</span></span> | <span data-ttu-id="d58a4-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="d58a4-115">1\_2</span></span> | <span data-ttu-id="d58a4-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d58a4-116">1\_3</span></span> | <span data-ttu-id="d58a4-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="d58a4-117">1\_4</span></span> | <span data-ttu-id="d58a4-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d58a4-118">2\_0</span></span> | <span data-ttu-id="d58a4-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d58a4-119">2\_x</span></span> | <span data-ttu-id="d58a4-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d58a4-120">2\_sw</span></span> | <span data-ttu-id="d58a4-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d58a4-121">3\_0</span></span> | <span data-ttu-id="d58a4-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="d58a4-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d58a4-123">texm3x3tex</span><span class="sxs-lookup"><span data-stu-id="d58a4-123">texm3x3tex</span></span>            | <span data-ttu-id="d58a4-124">x</span><span class="sxs-lookup"><span data-stu-id="d58a4-124">x</span></span>    | <span data-ttu-id="d58a4-125">x</span><span class="sxs-lookup"><span data-stu-id="d58a4-125">x</span></span>    | <span data-ttu-id="d58a4-126">x</span><span class="sxs-lookup"><span data-stu-id="d58a4-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="d58a4-127">Cette instruction est utilisée comme dernière des trois instructions représentant une opération de multiplication de matrice 3x3, suivie d’une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="d58a4-127">This instruction is used as the final of three instructions representing a 3x3 matrix multiply operation, followed by a texture lookup.</span></span> <span data-ttu-id="d58a4-128">La matrice 3x3 est composée des coordonnées de texture de la troisième étape de texture et des deux étapes de texture précédentes.</span><span class="sxs-lookup"><span data-stu-id="d58a4-128">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="d58a4-129">Le vecteur à trois composants résultant (u, v, w) est utilisé pour échantillonner la texture à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="d58a4-129">The resulting three-component vector (u,v,w) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="d58a4-130">Toute texture assignée aux deux étapes de texture précédentes est ignorée.</span><span class="sxs-lookup"><span data-stu-id="d58a4-130">Any texture assigned to the preceding two texture stages is ignored.</span></span> <span data-ttu-id="d58a4-131">La multiplication de matrice 3x3 est généralement utile pour orienter un vecteur normal vers l’espace tangent correct pour la surface rendue.</span><span class="sxs-lookup"><span data-stu-id="d58a4-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="d58a4-132">Cette instruction doit être utilisée avec l’instruction texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="d58a4-132">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="d58a4-133">Les registres de texture doivent utiliser la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="d58a4-133">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



<span data-ttu-id="d58a4-134">Voici plus de détails sur la façon dont la multiplication 3x3 est accomplie.</span><span class="sxs-lookup"><span data-stu-id="d58a4-134">Here is more detail about how the 3x3 multiply is accomplished.</span></span>

<span data-ttu-id="d58a4-135">La première instruction texm3x3pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup></span><span class="sxs-lookup"><span data-stu-id="d58a4-135">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="d58a4-136">u<sup>'</sup> = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="d58a4-136">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="d58a4-137">La deuxième instruction texm3x3pad exécute la deuxième ligne de la multiplication pour rechercher v<sup>»</sup>.</span><span class="sxs-lookup"><span data-stu-id="d58a4-137">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="d58a4-138">v<sup>'</sup> = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="d58a4-138">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="d58a4-139">L’instruction texm3x3spec effectue la troisième ligne de la multiplication pour rechercher w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="d58a4-139">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="d58a4-140">w<sup>'</sup> = TextureCoordinates (étape m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="d58a4-140">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="d58a4-141">Enfin, l’instruction texm3x3tex échantillonne t (m + 2) avec (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) et stocke le résultat dans t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="d58a4-141">Lastly, the texm3x3tex instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="d58a4-142">t (m + 2)<sub>RVBA</sub> = TextureSample (étape m + 2)<sub>RVBA</sub> en utilisant (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) comme coordonnées.</span><span class="sxs-lookup"><span data-stu-id="d58a4-142">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates.</span></span>

## <a name="examples"></a><span data-ttu-id="d58a4-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="d58a4-143">Examples</span></span>

<span data-ttu-id="d58a4-144">Voici un exemple de nuanceur avec les cartes de texture identifiées et les étapes de texture identifiées.</span><span class="sxs-lookup"><span data-stu-id="d58a4-144">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



<span data-ttu-id="d58a4-145">Cet exemple requiert la configuration de la phase de texture suivante.</span><span class="sxs-lookup"><span data-stu-id="d58a4-145">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="d58a4-146">Une carte de texture avec des données normales est assignée à l’étape 0.</span><span class="sxs-lookup"><span data-stu-id="d58a4-146">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="d58a4-147">On parle souvent de carte de relief.</span><span class="sxs-lookup"><span data-stu-id="d58a4-147">This is often referred to as a bump map.</span></span> <span data-ttu-id="d58a4-148">Les données sont (XYZ) normales pour chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="d58a4-148">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="d58a4-149">Le jeu de coordonnées de texture 0 définit comment échantillonner cette carte normale.</span><span class="sxs-lookup"><span data-stu-id="d58a4-149">Texture coordinate set 0 defines how to sample this normal map.</span></span>
-   <span data-ttu-id="d58a4-150">Le jeu de coordonnées de texture 1 est affecté à la ligne 1 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="d58a4-150">Texture coordinate set 1 is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="d58a4-151">Toute texture assignée à l’étape 1 est ignorée.</span><span class="sxs-lookup"><span data-stu-id="d58a4-151">Any texture assigned to stage 1 is ignored.</span></span>
-   <span data-ttu-id="d58a4-152">Le jeu de coordonnées de texture 2 est affecté à la ligne 2 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="d58a4-152">Texture coordinate set 2 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="d58a4-153">Toute texture assignée à l’étape 2 est ignorée.</span><span class="sxs-lookup"><span data-stu-id="d58a4-153">Any texture assigned to stage 2 is ignored.</span></span>
-   <span data-ttu-id="d58a4-154">Le jeu de coordonnées de texture 3 est affecté à la ligne 3 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="d58a4-154">Texture coordinate set 3 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="d58a4-155">Une texture de volume ou de cube doit être définie sur la phase 3 pour la recherche par le vecteur 3D transformé.</span><span class="sxs-lookup"><span data-stu-id="d58a4-155">A volume or cube texture should be set to stage 3 for lookup by the transformed 3D vector.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d58a4-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d58a4-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d58a4-157">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="d58a4-157">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




