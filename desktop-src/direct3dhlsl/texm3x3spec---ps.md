---
title: texm3x3spec-PS
description: Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture. Cela peut être utilisé pour la réflexion spéculaire et le mappage d’environnement. texm3x3spec doit être utilisé conjointement avec deux instructions texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381157"
---
# <a name="texm3x3spec---ps"></a><span data-ttu-id="86809-105">texm3x3spec-PS</span><span class="sxs-lookup"><span data-stu-id="86809-105">texm3x3spec - ps</span></span>

<span data-ttu-id="86809-106">Effectue une multiplication de matrice 3x3 et utilise le résultat pour effectuer une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="86809-106">Performs a 3x3 matrix multiply and uses the result to perform a texture lookup.</span></span> <span data-ttu-id="86809-107">Cela peut être utilisé pour la réflexion spéculaire et le mappage d’environnement.</span><span class="sxs-lookup"><span data-stu-id="86809-107">This can be used for specular reflection and environment mapping.</span></span> <span data-ttu-id="86809-108">texm3x3spec doit être utilisé conjointement avec deux instructions [texm3x3pad-PS](texm3x3pad---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="86809-108">texm3x3spec must be used in conjunction with two [texm3x3pad - ps](texm3x3pad---ps.md) instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="86809-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86809-109">Syntax</span></span>



| <span data-ttu-id="86809-110">texm3x3spec DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="86809-110">texm3x3spec dst, src0, src1</span></span> |
|-----------------------------|



 

<span data-ttu-id="86809-111">where</span><span class="sxs-lookup"><span data-stu-id="86809-111">where</span></span>

-   <span data-ttu-id="86809-112">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="86809-112">dst is the destination register.</span></span>
-   <span data-ttu-id="86809-113">src0 et src1 sont des registres sources.</span><span class="sxs-lookup"><span data-stu-id="86809-113">src0 and src1 are source registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="86809-114">Notes</span><span class="sxs-lookup"><span data-stu-id="86809-114">Remarks</span></span>



| <span data-ttu-id="86809-115">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="86809-115">Pixel shader versions</span></span> | <span data-ttu-id="86809-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="86809-116">1\_1</span></span> | <span data-ttu-id="86809-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="86809-117">1\_2</span></span> | <span data-ttu-id="86809-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="86809-118">1\_3</span></span> | <span data-ttu-id="86809-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="86809-119">1\_4</span></span> | <span data-ttu-id="86809-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86809-120">2\_0</span></span> | <span data-ttu-id="86809-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="86809-121">2\_x</span></span> | <span data-ttu-id="86809-122">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="86809-122">2\_sw</span></span> | <span data-ttu-id="86809-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86809-123">3\_0</span></span> | <span data-ttu-id="86809-124">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="86809-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="86809-125">texm3x3spec</span><span class="sxs-lookup"><span data-stu-id="86809-125">texm3x3spec</span></span>           | <span data-ttu-id="86809-126">x</span><span class="sxs-lookup"><span data-stu-id="86809-126">x</span></span>    | <span data-ttu-id="86809-127">x</span><span class="sxs-lookup"><span data-stu-id="86809-127">x</span></span>    | <span data-ttu-id="86809-128">x</span><span class="sxs-lookup"><span data-stu-id="86809-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="86809-129">Cette instruction effectue une multiplication de la dernière ligne d’une matrice 3x3, utilise le vecteur résultant comme vecteur normal pour refléter un vecteur de rayons oculaires, puis utilise le vecteur réfléchi pour effectuer une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="86809-129">This instruction performs the final row of a 3x3 matrix multiply, uses the resulting vector as a normal vector to reflect an eye-ray vector, and then uses the reflected vector to perform a texture lookup.</span></span> <span data-ttu-id="86809-130">Le nuanceur lit le vecteur de rayon oculaire à partir d’un registre de constante.</span><span class="sxs-lookup"><span data-stu-id="86809-130">The shader reads the eye-ray vector from a constant register.</span></span> <span data-ttu-id="86809-131">La multiplication de matrice 3x3 est généralement utile pour orienter un vecteur normal vers l’espace tangent correct pour la surface rendue.</span><span class="sxs-lookup"><span data-stu-id="86809-131">The 3x3 matrix multiply is typically useful for orienting a normal vector to the correct tangent space for the surface being rendered.</span></span>

<span data-ttu-id="86809-132">La matrice 3x3 est composée des coordonnées de texture de la troisième étape de texture et des deux étapes de texture précédentes.</span><span class="sxs-lookup"><span data-stu-id="86809-132">The 3x3 matrix is comprised of the texture coordinates of the third texture stage and the two preceding texture stages.</span></span> <span data-ttu-id="86809-133">Le vecteur de réflexion de publication résultant (u, v, w) est utilisé pour échantillonner la texture à l’étape de texture finale.</span><span class="sxs-lookup"><span data-stu-id="86809-133">The resulting post reflection vector (u,v,w) is used to sample the texture on the final texture stage.</span></span> <span data-ttu-id="86809-134">Toute texture assignée aux deux étapes de texture précédentes est ignorée.</span><span class="sxs-lookup"><span data-stu-id="86809-134">Any texture assigned to the preceding two texture stages is ignored.</span></span>

<span data-ttu-id="86809-135">Cette instruction doit être utilisée avec deux instructions texm3x3pad.</span><span class="sxs-lookup"><span data-stu-id="86809-135">This instruction must be used with two texm3x3pad instructions.</span></span> <span data-ttu-id="86809-136">Les registres de texture doivent utiliser la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="86809-136">Texture registers must use the following sequence.</span></span>


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



<span data-ttu-id="86809-137">La première instruction texm3x3pad exécute la première ligne de la multiplication pour<sup>Rechercher u.</sup></span><span class="sxs-lookup"><span data-stu-id="86809-137">The first texm3x3pad instruction performs the first row of the multiply to find u<sup>'</sup>.</span></span>

<span data-ttu-id="86809-138">u<sup>'</sup> = TextureCoordinates (stage m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="86809-138">u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="86809-139">La deuxième instruction texm3x3pad exécute la deuxième ligne de la multiplication pour rechercher v<sup>»</sup>.</span><span class="sxs-lookup"><span data-stu-id="86809-139">The second texm3x3pad instruction performs the second row of the multiply to find v<sup>'</sup>.</span></span>

<span data-ttu-id="86809-140">v<sup>'</sup> = TextureCoordinates (étape m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="86809-140">v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="86809-141">L’instruction texm3x3spec effectue la troisième ligne de la multiplication pour rechercher w<sup>'</sup>.</span><span class="sxs-lookup"><span data-stu-id="86809-141">The texm3x3spec instruction performs the third row of the multiply to find w<sup>'</sup>.</span></span>

<span data-ttu-id="86809-142">w<sup>'</sup> = TextureCoordinates (étape m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="86809-142">w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="86809-143">L’instruction texm3x3spec effectue ensuite un calcul de réflexion.</span><span class="sxs-lookup"><span data-stu-id="86809-143">The texm3x3spec instruction then does a reflection calculation.</span></span>

<span data-ttu-id="86809-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* n-E</span><span class="sxs-lookup"><span data-stu-id="86809-144">(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2\*\[(N\*E)/(N\*N)\]\*N - E</span></span>

<span data-ttu-id="86809-145">où le N normal est donné par</span><span class="sxs-lookup"><span data-stu-id="86809-145">// where the normal N is given by</span></span>

<span data-ttu-id="86809-146">N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span><span class="sxs-lookup"><span data-stu-id="86809-146">// N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )</span></span>

<span data-ttu-id="86809-147">et le vecteur de rayon œil E est fourni par le registre de constante</span><span class="sxs-lookup"><span data-stu-id="86809-147">// and the eye-ray vector E is given by the constant register</span></span>

<span data-ttu-id="86809-148">E = c \# (n’importe quel Registre de constante--C0, C1, C2, etc.--peut être utilisé)</span><span class="sxs-lookup"><span data-stu-id="86809-148">// E = c\# (Any constant register--c0, c1, c2, etc.--can be used)</span></span>

<span data-ttu-id="86809-149">Enfin, l’instruction texm3x3spec échantillonne t (m + 2) avec (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) et stocke le résultat dans t (m + 2).</span><span class="sxs-lookup"><span data-stu-id="86809-149">Lastly, the texm3x3spec instruction samples t(m+2) with (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) and stores the result in t(m+2).</span></span>

<span data-ttu-id="86809-150">t (m + 2)<sub>RVBA</sub> = TextureSample (étape m + 2)<sub>RVBA</sub> à l’aide de (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) en tant que coordonnées</span><span class="sxs-lookup"><span data-stu-id="86809-150">t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) as coordinates</span></span>

## <a name="examples"></a><span data-ttu-id="86809-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="86809-151">Examples</span></span>

<span data-ttu-id="86809-152">Voici un exemple de nuanceur avec les cartes de texture et les étapes de texture identifiées.</span><span class="sxs-lookup"><span data-stu-id="86809-152">Here is an example shader with the texture maps and the texture stages identified.</span></span>


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



<span data-ttu-id="86809-153">Cet exemple requiert la configuration de la phase de texture suivante.</span><span class="sxs-lookup"><span data-stu-id="86809-153">This example requires the following texture stage setup.</span></span>

-   <span data-ttu-id="86809-154">Une carte de texture avec des données normales est assignée à l’étape 0.</span><span class="sxs-lookup"><span data-stu-id="86809-154">Stage 0 is assigned a texture map with normal data.</span></span> <span data-ttu-id="86809-155">On parle souvent de carte de relief.</span><span class="sxs-lookup"><span data-stu-id="86809-155">This is often referred to as a bump map.</span></span> <span data-ttu-id="86809-156">Les données sont (XYZ) normales pour chaque Texel.</span><span class="sxs-lookup"><span data-stu-id="86809-156">The data is (XYZ) normals for each texel.</span></span> <span data-ttu-id="86809-157">Les coordonnées de texture à l’étape n définissent où échantillonner cette carte normale.</span><span class="sxs-lookup"><span data-stu-id="86809-157">Texture coordinates at stage n defines where to sample this normal map.</span></span>
-   <span data-ttu-id="86809-158">Le jeu de coordonnées de texture m est affecté à la ligne 1 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="86809-158">Texture coordinate set m is assigned to row 1 of the 3x3 matrix.</span></span> <span data-ttu-id="86809-159">Toute texture assignée à l’étape m est ignorée.</span><span class="sxs-lookup"><span data-stu-id="86809-159">Any texture assigned to stage m is ignored.</span></span>
-   <span data-ttu-id="86809-160">Le jeu de coordonnées de texture m + 1 est affecté à la ligne 2 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="86809-160">Texture coordinate set m+1 is assigned to row 2 of the 3x3 matrix.</span></span> <span data-ttu-id="86809-161">Toute texture assignée à l’étape m + 1 est ignorée.</span><span class="sxs-lookup"><span data-stu-id="86809-161">Any texture assigned to stage m+1 is ignored.</span></span>
-   <span data-ttu-id="86809-162">Le jeu de coordonnées de texture m + 2 est affecté à la ligne 3 de la matrice 3x3.</span><span class="sxs-lookup"><span data-stu-id="86809-162">Texture coordinate set m+2 is assigned to row 3 of the 3x3 matrix.</span></span> <span data-ttu-id="86809-163">L’étape m + 2 est assignée à un mappage de texture de volume ou de cube.</span><span class="sxs-lookup"><span data-stu-id="86809-163">Stage m+2 is assigned a volume or cube texture map.</span></span> <span data-ttu-id="86809-164">La texture fournit des données de couleur (RVBA).</span><span class="sxs-lookup"><span data-stu-id="86809-164">The texture provides color data (RGBA).</span></span>
-   <span data-ttu-id="86809-165">Le vecteur de rayon œil E est fourni par un registre constant E = c \# .</span><span class="sxs-lookup"><span data-stu-id="86809-165">The eye-ray vector E is given by a constant register E = c\#.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86809-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86809-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86809-167">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="86809-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




