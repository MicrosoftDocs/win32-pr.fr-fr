---
title: Registres de sortie
description: Registres de sortie
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990600"
---
# <a name="output-registers"></a><span data-ttu-id="cc3b8-103">Registres de sortie</span><span class="sxs-lookup"><span data-stu-id="cc3b8-103">Output Registers</span></span>

-   <span data-ttu-id="cc3b8-104">Registre des couleurs des vertex</span><span class="sxs-lookup"><span data-stu-id="cc3b8-104">Vertex Color Register</span></span>
-   <span data-ttu-id="cc3b8-105">Registre de brouillard</span><span class="sxs-lookup"><span data-stu-id="cc3b8-105">Fog Register</span></span>
-   <span data-ttu-id="cc3b8-106">Registre de position \_</span><span class="sxs-lookup"><span data-stu-id="cc3b8-106">Position\_Register</span></span>
-   <span data-ttu-id="cc3b8-107">Registre de la taille du point \_ \_</span><span class="sxs-lookup"><span data-stu-id="cc3b8-107">Point\_Size\_Register</span></span>
-   <span data-ttu-id="cc3b8-108">\_Registre de coordonnées de texture \_</span><span class="sxs-lookup"><span data-stu-id="cc3b8-108">Texture\_Coordinate\_Register</span></span>

<span data-ttu-id="cc3b8-109">Les noms de registres sont précédés d’une lettre o minuscule, indiquant que les registres de sortie sont en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-109">Register names are preceded by a lowercase letter o, indicating that the output registers are write-only.</span></span>

## <a name="vertex-color-register---od0-od1"></a><span data-ttu-id="cc3b8-110">Registre des couleurs des vertex-oD0, oD1</span><span class="sxs-lookup"><span data-stu-id="cc3b8-110">Vertex Color Register - oD0, oD1</span></span>

<span data-ttu-id="cc3b8-111">oD0 est le registre de couleur diffuse.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-111">oD0 is the diffuse color register.</span></span> <span data-ttu-id="cc3b8-112">oD1 est le registre de couleurs spéculaire.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-112">oD1 is the specular color register.</span></span> <span data-ttu-id="cc3b8-113">La valeur oD0 est interpolée et écrite dans le registre de couleur d’entrée 0 (v0) du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-113">The oD0 value is interpolated and is written to the input color register 0 (v0) of the pixel shader.</span></span> <span data-ttu-id="cc3b8-114">La valeur oD1 est interpolée et écrite dans le registre des couleurs d’entrée 1 (v1) du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-114">The oD1 value is interpolated and written to the input color register 1 (v1) of the pixel shader.</span></span> <span data-ttu-id="cc3b8-115">Pour plus d’informations sur les registres de couleurs du nuanceur de pixels, consultez registres.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-115">For more information about pixel shader color registers, see Registers.</span></span>



| <span data-ttu-id="cc3b8-116">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="cc3b8-116">Vertex shader versions</span></span> | <span data-ttu-id="cc3b8-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="cc3b8-117">1\_1</span></span> | <span data-ttu-id="cc3b8-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-118">2\_0</span></span> | <span data-ttu-id="cc3b8-119">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-119">2\_sw</span></span> | <span data-ttu-id="cc3b8-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-120">2\_x</span></span> | <span data-ttu-id="cc3b8-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-121">3\_0</span></span> | <span data-ttu-id="cc3b8-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-122">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="cc3b8-123">Registre des couleurs des vertex</span><span class="sxs-lookup"><span data-stu-id="cc3b8-123">Vertex Color Register</span></span>  | <span data-ttu-id="cc3b8-124">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-124">x</span></span>    | <span data-ttu-id="cc3b8-125">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-125">x</span></span>    | <span data-ttu-id="cc3b8-126">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-126">x</span></span>     | <span data-ttu-id="cc3b8-127">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-127">x</span></span>    |      |       |



 

## <a name="fog-register---ofog"></a><span data-ttu-id="cc3b8-128">Registre de brouillard-oFog</span><span class="sxs-lookup"><span data-stu-id="cc3b8-128">Fog Register - oFog</span></span>

<span data-ttu-id="cc3b8-129">La valeur de brouillard de sortie est inscrite.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-129">The output fog value registers.</span></span> <span data-ttu-id="cc3b8-130">La valeur est le facteur de brouillard à interpoler, puis est routé vers la table de brouillard.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-130">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="cc3b8-131">Seul le composant x scalaire du brouillard est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-131">Only the scalar x-component of the fog is used.</span></span> <span data-ttu-id="cc3b8-132">Les valeurs sont ancrées entre zéro et un avant de passer au rastériseur.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-132">Values are clamped between zero and one before passing to the rasterizer.</span></span>



| <span data-ttu-id="cc3b8-133">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="cc3b8-133">Vertex shader versions</span></span> | <span data-ttu-id="cc3b8-134">1\_1</span><span class="sxs-lookup"><span data-stu-id="cc3b8-134">1\_1</span></span> | <span data-ttu-id="cc3b8-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-135">2\_0</span></span> | <span data-ttu-id="cc3b8-136">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-136">2\_sw</span></span> | <span data-ttu-id="cc3b8-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-137">2\_x</span></span> | <span data-ttu-id="cc3b8-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-138">3\_0</span></span> | <span data-ttu-id="cc3b8-139">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-139">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="cc3b8-140">Registre de brouillard</span><span class="sxs-lookup"><span data-stu-id="cc3b8-140">Fog Register</span></span>           | <span data-ttu-id="cc3b8-141">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-141">x</span></span>    | <span data-ttu-id="cc3b8-142">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-142">x</span></span>    | <span data-ttu-id="cc3b8-143">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-143">x</span></span>     | <span data-ttu-id="cc3b8-144">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-144">x</span></span>    |      |       |



 

## <a name="position-register---opos"></a><span data-ttu-id="cc3b8-145">Registre de position-oPos</span><span class="sxs-lookup"><span data-stu-id="cc3b8-145">Position Register - oPos</span></span>

<span data-ttu-id="cc3b8-146">La position de sortie est inscrite.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-146">The output position registers.</span></span> <span data-ttu-id="cc3b8-147">La valeur correspond à la position dans l’espace de découpage homogène.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-147">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="cc3b8-148">Cette valeur doit être écrite par le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-148">This value must be written by the vertex shader.</span></span>



| <span data-ttu-id="cc3b8-149">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="cc3b8-149">Vertex shader versions</span></span> | <span data-ttu-id="cc3b8-150">1\_1</span><span class="sxs-lookup"><span data-stu-id="cc3b8-150">1\_1</span></span> | <span data-ttu-id="cc3b8-151">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-151">2\_0</span></span> | <span data-ttu-id="cc3b8-152">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-152">2\_sw</span></span> | <span data-ttu-id="cc3b8-153">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-153">2\_x</span></span> | <span data-ttu-id="cc3b8-154">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-154">3\_0</span></span> | <span data-ttu-id="cc3b8-155">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-155">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="cc3b8-156">Registre de position</span><span class="sxs-lookup"><span data-stu-id="cc3b8-156">Position Register</span></span>      | <span data-ttu-id="cc3b8-157">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-157">x</span></span>    | <span data-ttu-id="cc3b8-158">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-158">x</span></span>    | <span data-ttu-id="cc3b8-159">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-159">x</span></span>     | <span data-ttu-id="cc3b8-160">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-160">x</span></span>    |      |       |



 

## <a name="point-size-register---opts"></a><span data-ttu-id="cc3b8-161">Registre de la taille du point-oPts</span><span class="sxs-lookup"><span data-stu-id="cc3b8-161">Point Size Register - oPts</span></span>

<span data-ttu-id="cc3b8-162">Registres de taille de point de sortie.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-162">The output point-size registers.</span></span> <span data-ttu-id="cc3b8-163">Seul le composant x scalaire de la taille en points est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-163">Only the scalar x-component of the point size is used.</span></span>



| <span data-ttu-id="cc3b8-164">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="cc3b8-164">Vertex shader versions</span></span> | <span data-ttu-id="cc3b8-165">1\_1</span><span class="sxs-lookup"><span data-stu-id="cc3b8-165">1\_1</span></span> | <span data-ttu-id="cc3b8-166">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-166">2\_0</span></span> | <span data-ttu-id="cc3b8-167">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-167">2\_sw</span></span> | <span data-ttu-id="cc3b8-168">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-168">2\_x</span></span> | <span data-ttu-id="cc3b8-169">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-169">3\_0</span></span> | <span data-ttu-id="cc3b8-170">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-170">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="cc3b8-171">Registre de la taille du point</span><span class="sxs-lookup"><span data-stu-id="cc3b8-171">Point Size Register</span></span>    | <span data-ttu-id="cc3b8-172">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-172">x</span></span>    | <span data-ttu-id="cc3b8-173">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-173">x</span></span>    | <span data-ttu-id="cc3b8-174">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-174">x</span></span>     | <span data-ttu-id="cc3b8-175">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-175">x</span></span>    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a><span data-ttu-id="cc3b8-176">Registre des coordonnées de texture-oT0 à oT7</span><span class="sxs-lookup"><span data-stu-id="cc3b8-176">Texture Coordinate Register - oT0 to oT7</span></span>

<span data-ttu-id="cc3b8-177">Les coordonnées de la texture de sortie s’inscrivent.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-177">The output texture coordinates registers.</span></span> <span data-ttu-id="cc3b8-178">Plus précisément, il s’agit d’un tableau de registres de données de sortie qui sont itérés et utilisés comme coordonnées de texture par les étapes d’échantillonnage de texture qui acheminent les données vers le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-178">Specifically, these are an array of output data registers that are iterated and used as texture coordinates by the texture sampling stages routing data to the pixel shader.</span></span>



| <span data-ttu-id="cc3b8-179">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="cc3b8-179">Vertex shader versions</span></span>      | <span data-ttu-id="cc3b8-180">1\_1</span><span class="sxs-lookup"><span data-stu-id="cc3b8-180">1\_1</span></span> | <span data-ttu-id="cc3b8-181">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-181">2\_0</span></span> | <span data-ttu-id="cc3b8-182">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-182">2\_sw</span></span> | <span data-ttu-id="cc3b8-183">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-183">2\_x</span></span> | <span data-ttu-id="cc3b8-184">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc3b8-184">3\_0</span></span> | <span data-ttu-id="cc3b8-185">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="cc3b8-185">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="cc3b8-186">Registre de coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="cc3b8-186">Texture Coordinate Register</span></span> | <span data-ttu-id="cc3b8-187">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-187">x</span></span>    | <span data-ttu-id="cc3b8-188">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-188">x</span></span>    | <span data-ttu-id="cc3b8-189">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-189">x</span></span>     | <span data-ttu-id="cc3b8-190">x</span><span class="sxs-lookup"><span data-stu-id="cc3b8-190">x</span></span>    |      |       |



 

<span data-ttu-id="cc3b8-191">Lors de l’écriture dans un registre de coordonnées de texture, il est recommandé de passer uniquement les valeurs à virgule flottante en tant que dimension de la carte de texture correspondante.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-191">When writing to a texture coordinate register, it is recommended to pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="cc3b8-192">Contrôler les valeurs passées avec un modificateur.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-192">Control the values passed with a modifier.</span></span> <span data-ttu-id="cc3b8-193">Par exemple, utilisez. XY pour une carte de texture 2D.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-193">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="cc3b8-194">Lorsque la projection de texture est activée pour une étape de texture, les quatre valeurs à virgule flottante doivent être écrites dans le registre de texture correspondant.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-194">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span>

<span data-ttu-id="cc3b8-195">L’un des \* indicateurs de transformation de texture D3DTTFF doit être égal à zéro lorsque le pipeline programmable est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-195">Any of the D3DTTFF\* texture transform flags should be zero when the programmable pipeline is being used.</span></span>

### <a name="texture-coordinate-range"></a><span data-ttu-id="cc3b8-196">Plage de coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="cc3b8-196">Texture Coordinate Range</span></span>

<span data-ttu-id="cc3b8-197">Les données de vertex d’objet fournissent des coordonnées de texture d’entrée.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-197">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="cc3b8-198">Les objets qui n’utilisent pas les textures en mosaïque ont généralement des coordonnées de texture dans la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="cc3b8-198">Objects that do not used tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="cc3b8-199">Les objets qui utilisent des textures en mosaïque, telles que le terrain, ont généralement des coordonnées de texture allant de \[ - ?, + ? \] où ?</span><span class="sxs-lookup"><span data-stu-id="cc3b8-199">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-?,+?\] where ?</span></span> <span data-ttu-id="cc3b8-200">Il peut s’agir d’un grand nombre à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-200">can be a large floating point number.</span></span>

<span data-ttu-id="cc3b8-201">L’interpolation de coordonnée de texture est effectuée sur les données de vertex pour la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-201">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="cc3b8-202">Pendant la pixellisation, les coordonnées de texture sont interpolées entre les vertex d’objet, modifiées par l’habillage de texture et mises à l’échelle par la taille de la texture (en tenant également compte du mode d’adresse de texture) pour produire un index d’entiers.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-202">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping and scaled by the texture size (also taking into account texture address mode) to produce an integer index.</span></span> <span data-ttu-id="cc3b8-203">L’index est ensuite utilisé pour effectuer une recherche de texture.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-203">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="cc3b8-204">MaxTextureRepeat peut être utilisé pour déterminer le nombre de fois qu’une texture peut être affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-204">MaxTextureRepeat can be used to determine how many times a texture can be tiled.</span></span>

<span data-ttu-id="cc3b8-205">Si les coordonnées de texture sont lues directement dans un nuanceur de pixels (à l’aide de texcoord ou texcrd), la plage de coordonnées de texture dépend de l’instruction et de la version du nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="cc3b8-205">If texture coordinates are read directly into a pixel shader (using texcoord or texcrd), the texture coordinate range depends on the instruction and the pixel shader version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc3b8-206">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc3b8-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc3b8-207">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="cc3b8-207">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




