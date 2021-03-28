---
title: texm3x3vspec-PS
description: Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture.
ms.assetid: 3798bc23-2929-48fe-93ae-5aa025823714
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 28f1ee1ddb0193f9ccdaa4976e4963e748091f37
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940573"
---
# <a name="texm3x3vspec---ps"></a><span data-ttu-id="8765f-103">texm3x3vspec-PS</span><span class="sxs-lookup"><span data-stu-id="8765f-103">texm3x3vspec - ps</span></span>

<span data-ttu-id="8765f-104">Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="8765f-104">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="8765f-105">Cela peut être utilisé pour la réflexion spéculaire et le mappage d’environnement où le vecteur de rayons oculaires n’est pas constant.</span><span class="sxs-lookup"><span data-stu-id="8765f-105">This can be used for specular reflection and environment mapping where the eye-ray vector is not constant.</span></span> <span data-ttu-id="8765f-106">texm3x3vspec doit être utilisé conjointement avec deux instructions [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="8765f-106">texm3x3vspec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span> <span data-ttu-id="8765f-107">Si le vecteur de rayon oculaire est constant, l’instruction [texm3x3spec-PS](texm3x3spec---ps.md) effectue la même multiplication de matrices et la même recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="8765f-107">If the eye-ray vector is constant, the [texm3x3spec - ps](texm3x3spec---ps.md) instruction will perform the same matrix multiply and texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="8765f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8765f-108">Syntax</span></span>



| <span data-ttu-id="8765f-109">texm3x3vspec DST, SRC</span><span class="sxs-lookup"><span data-stu-id="8765f-109">texm3x3vspec dst, src</span></span> |
|-----------------------|



 

<span data-ttu-id="8765f-110">where</span><span class="sxs-lookup"><span data-stu-id="8765f-110">where</span></span>

-   <span data-ttu-id="8765f-111">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="8765f-111">dst is the destination register.</span></span>
-   <span data-ttu-id="8765f-112">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="8765f-112">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8765f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8765f-113">Remarks</span></span>



| <span data-ttu-id="8765f-114">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8765f-114">Pixel shader versions</span></span> | <span data-ttu-id="8765f-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="8765f-115">1\_1</span></span> | <span data-ttu-id="8765f-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="8765f-116">1\_2</span></span> | <span data-ttu-id="8765f-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="8765f-117">1\_3</span></span> | <span data-ttu-id="8765f-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="8765f-118">1\_4</span></span> | <span data-ttu-id="8765f-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8765f-119">2\_0</span></span> | <span data-ttu-id="8765f-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8765f-120">2\_x</span></span> | <span data-ttu-id="8765f-121">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8765f-121">2\_sw</span></span> | <span data-ttu-id="8765f-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8765f-122">3\_0</span></span> | <span data-ttu-id="8765f-123">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="8765f-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="8765f-124">texm3x3vspec</span><span class="sxs-lookup"><span data-stu-id="8765f-124">texm3x3vspec</span></span>          | <span data-ttu-id="8765f-125">x</span><span class="sxs-lookup"><span data-stu-id="8765f-125">x</span></span>    | <span data-ttu-id="8765f-126">x</span><span class="sxs-lookup"><span data-stu-id="8765f-126">x</span></span>    | <span data-ttu-id="8765f-127">x</span><span class="sxs-lookup"><span data-stu-id="8765f-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="8765f-128">Cette instruction effectue la dernière ligne d’une opération de multiplication de matrice 3x3, interprète le vecteur résultant comme un vecteur normal pour refléter un vecteur de rayons oculaires, puis utilise le vecteur réfléchi comme une adresse de texture pour une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="8765f-128">This instruction performs the final row of a 3x3 matrix multiply operation, interprets the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector as a texture address for a texture lookup.</span></span> <span data-ttu-id="8765f-129">Il fonctionne de la même façon que [texm3x3spec-PS](texm3x3spec---ps.md), sauf que le vecteur de rayon oculaire est extrait du quatrième composant des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="8765f-129">It works just like [texm3x3spec - ps](texm3x3spec---ps.md), except that the eye-ray vector is taken from the fourth component of the texture coordinates.</span></span> <span data-ttu-id="8765f-130">La multiplication de matrice 3x3 est généralement utile pour orienter un vecteur normal vers l’espace tangent correct pour la surface rendue.</span><span class="sxs-lookup"><span data-stu-id="8765f-130">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="8765f-131">La matrice 3x3 est composée des coordonnées de texture de la troisième étape de texture et des deux étapes de texture précédentes.</span><span class="sxs-lookup"><span data-stu-id="8765f-131">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="8765f-132">Le vecteur de publication (UVW) qui en résulte est utilisé pour échantillonner la texture à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="8765f-132">The resulting post-reflection vector (UVW) is used to sample the texture in stage 3.</span></span> <span data-ttu-id="8765f-133">Toute texture assignée aux deux étapes de texture précédentes est ignorée.</span><span class="sxs-lookup"><span data-stu-id="8765f-133">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="8765f-134">Cette instruction doit être utilisée avec l’instruction texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="8765f-134">This instruction must be used with the texm3x3pad instruction.</span></span> <span data-ttu-id="8765f-135">Les registres de texture doivent utiliser la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="8765f-135">Texture registers must use the following sequence.</span></span>


```
tex t(n)                    // Define tn as a standard 3-vector (tn must
                            //   be defined in some way before it is used)
texm3x3pad   t(m),   t(n)   // where m > n
                            // Perform first row of matrix multiply
texm3x3pad   t(m+1), t(n)   // Perform second row of matrix multiply
texm3x3vspec t(m+2), t(n)   // Perform third row of matrix multiply
                            // Then do a texture lookup on the texture
                            // associated with texture stage m+2
```



<span data-ttu-id="8765f-136">La première instruction texm3x3pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup></span><span class="sxs-lookup"><span data-stu-id="8765f-136">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="8765f-137">u<sup>'</sup> = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n) <sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="8765f-137">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n) <sub>RGB</sub></span></span>

<span data-ttu-id="8765f-138">La deuxième instruction texm3x3pad exécute la deuxième ligne de la multiplication pour rechercher v<sup>»</sup>.</span><span class="sxs-lookup"><span data-stu-id="8765f-138">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="8765f-139">v<sup>'</sup> = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="8765f-139">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="8765f-140">L’instruction texm3x3spec effectue la troisième ligne de la multiplication pour rechercher w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="8765f-140">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="8765f-141">w<sup>'</sup> = TextureCoordinates (étape m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="8765f-141">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="8765f-142">L’instruction texm3x3vspec effectue également un calcul de réflexion.</span><span class="sxs-lookup"><span data-stu-id="8765f-142">The texm3x3vspec instruction also does a reflection calculation.</span></span>

<span data-ttu-id="8765f-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* n-E</span><span class="sxs-lookup"><span data-stu-id="8765f-143">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="8765f-144">où le N normal est donné par</span><span class="sxs-lookup"><span data-stu-id="8765f-144">// where the normal N is given by</span></span>

<span data-ttu-id="8765f-145">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="8765f-145">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="8765f-146">et le vecteur de rayon œil E est fourni par</span><span class="sxs-lookup"><span data-stu-id="8765f-146">// and the eye-ray vector E is given by</span></span>

<span data-ttu-id="8765f-147">E = (TextureCoordinates (étape m)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="8765f-147">// E = (TextureCoordinates(stage m)<sub>Q</sub> ,</span></span>

<span data-ttu-id="8765f-148">TextureCoordinates (étape m + 1)<sub>Q</sub> ,</span><span class="sxs-lookup"><span data-stu-id="8765f-148">// TextureCoordinates(stage m+1)<sub>Q</sub> ,</span></span>

<span data-ttu-id="8765f-149">TextureCoordinates (étape m + 2)<sub>Q</sub> )</span><span class="sxs-lookup"><span data-stu-id="8765f-149">// TextureCoordinates(stage m+2)<sub>Q</sub> )</span></span>

<span data-ttu-id="8765f-150">Enfin, l’instruction texm3x3vspec échantillonne t (m + 2) avec (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) et stocke le résultat dans t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="8765f-150">Lastly, the texm3x3vspec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>)and stores the result in t(m+2).</span></span>

<span data-ttu-id="8765f-151">t (m + 2)<sub>RVBA</sub> = TextureSample (étape m + 2)<sub>RVBA</sub> à l’aide de (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) en tant que coordonnées</span><span class="sxs-lookup"><span data-stu-id="8765f-151">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="8765f-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="8765f-152">Examples</span></span>

<span data-ttu-id="8765f-153">Voici un exemple de nuanceur avec les cartes de texture identifiées et les étapes de texture identifiées.</span><span class="sxs-lookup"><span data-stu-id="8765f-153">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad   t1,  t0  // First row of matrix multiply
texm3x3pad   t2,  t0  // Second row of matrix multiply
texm3x3vspec t3,  t0  // Third row of matrix multiply to get a 3-vector
                      // Reflect 3-vector by the eye-ray vector
                      // Use reflected vector to do a texture lookup
                      //   at stage 3
mov r0, t3            // Output the result
```



<span data-ttu-id="8765f-154">Cet exemple requiert la configuration de la phase de texture suivante.</span><span class="sxs-lookup"><span data-stu-id="8765f-154">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="8765f-155">Une carte de texture avec des données normales est assignée à l’étape 0.</span><span class="sxs-lookup"><span data-stu-id="8765f-155">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="8765f-156">On parle souvent de carte de relief.</span><span class="sxs-lookup"><span data-stu-id="8765f-156">This is often referred to as a bump map.</span></span> <span data-ttu-id="8765f-157">Les données sont (XYZ) normales pour chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="8765f-157">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="8765f-158">Les coordonnées de texture à l’étape n définissent comment échantillonner cette carte normale.</span><span class="sxs-lookup"><span data-stu-id="8765f-158">Texture coordinates at stage n defines how to sample this normal map.</span></span>
-   <span data-ttu-id="8765f-159">Le jeu de coordonnées de texture m est affecté à la ligne 1 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="8765f-159">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="8765f-160">Toute texture assignée à l’étape m est ignorée.</span><span class="sxs-lookup"><span data-stu-id="8765f-160">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="8765f-161">Le jeu de coordonnées de texture m + 1 est affecté à la ligne 2 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="8765f-161">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="8765f-162">Toute texture assignée à l’étape m + 1 est ignorée.</span><span class="sxs-lookup"><span data-stu-id="8765f-162">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="8765f-163">Le jeu de coordonnées de texture m + 2 est affecté à la ligne 3 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="8765f-163">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="8765f-164">L’étape m + 2 est assignée à un mappage de texture de volume ou de cube.</span><span class="sxs-lookup"><span data-stu-id="8765f-164">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="8765f-165">La texture fournit des données de couleur (RVBA).</span><span class="sxs-lookup"><span data-stu-id="8765f-165">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="8765f-166">Le vecteur de rayon œil E est passé dans l’instruction dans le quatrième composant (q) des données de coordonnée de texture aux étapes m, m + 1 et m + 2.</span><span class="sxs-lookup"><span data-stu-id="8765f-166">The eye-ray vector E is passed into the instruction in the fourth component (q) of the texture coordinate data at stages m, m+1, and m+2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8765f-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8765f-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8765f-168">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="8765f-168">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




