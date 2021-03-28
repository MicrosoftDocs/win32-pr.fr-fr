---
title: Shader Model 3 (référence HLSL)
description: Les nuanceurs de sommets et les nuanceurs de pixels sont considérablement simplifiés par rapport aux versions précédentes du nuanceur.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382139"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="f4667-103">Shader Model 3 (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4667-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="f4667-104">Les nuanceurs de sommets et les nuanceurs de pixels sont considérablement simplifiés par rapport aux versions précédentes du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f4667-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="f4667-105">Si vous implémentez des nuanceurs dans le matériel, vous ne pouvez pas utiliser vs \_ 3 \_ 0 ou PS \_ 3 \_ 0 avec d’autres versions de nuanceur, et vous ne pouvez pas utiliser un type de nuanceur avec le pipeline de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="f4667-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="f4667-106">Ces modifications permettent de simplifier les pilotes et le Runtime.</span><span class="sxs-lookup"><span data-stu-id="f4667-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="f4667-107">La seule exception est que les nuanceurs logiciels uniquement et \_ 3 \_ 0 peuvent être utilisés avec une version de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f4667-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="f4667-108">En outre, si vous utilisez un nuanceur logiciel-uniquement vs \_ 3 \_ 0 avec une version de nuanceur de pixels précédente, le nuanceur vertex peut uniquement utiliser la sémantique de sortie qui est compatible avec les codes de format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="f4667-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="f4667-109">La sémantique utilisée sur les sorties de nuanceur de sommets doit être utilisée sur les entrées de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f4667-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="f4667-110">La sémantique est utilisée pour mapper les sorties du nuanceur de sommets aux entrées de nuanceur de pixels, de la même façon que la déclaration de vertex est mappée aux registres d’entrée du nuanceur de sommets et aux modèles de nuanceur précédents.</span><span class="sxs-lookup"><span data-stu-id="f4667-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="f4667-111">Consultez sémantique de correspondance sur les nuanceurs vs 3,0 et PS 3,0.</span><span class="sxs-lookup"><span data-stu-id="f4667-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="f4667-112">Des États de rendu supplémentaires du mode habillage ont été ajoutés pour couvrir la possibilité de coordonnées de texture supplémentaires dans ce nouveau schéma.</span><span class="sxs-lookup"><span data-stu-id="f4667-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="f4667-113">Les attributs avec D3DDECLUSAGE \_ texcoord et l’index d’utilisation de 0 à 15 sont interpolés en mode Wrap lorsque la valeur de retour à la [**\_ ligne \* D3DRS**](/windows/desktop/direct3d9/d3drenderstatetype) correspondante est définie.</span><span class="sxs-lookup"><span data-stu-id="f4667-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="f4667-114">Fonctionnalités du modèle de nuanceur de sommets 3</span><span class="sxs-lookup"><span data-stu-id="f4667-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="f4667-115">Caractéristiques du modèle de nuanceur de pixels 3</span><span class="sxs-lookup"><span data-stu-id="f4667-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="f4667-116">Sémantique de correspondance sur \_ \_ les nuanceurs vs 3 0 et PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f4667-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="f4667-117">Modifications du mode de brouillard, de profondeur et d’ombrage</span><span class="sxs-lookup"><span data-stu-id="f4667-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="f4667-118">Conversions à virgule flottante et entiers</span><span class="sxs-lookup"><span data-stu-id="f4667-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="f4667-119">Spécification de la précision complète ou partielle</span><span class="sxs-lookup"><span data-stu-id="f4667-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="f4667-120">Nuanceur de pixels et vertex logiciels</span><span class="sxs-lookup"><span data-stu-id="f4667-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="f4667-121">Fonctionnalités du modèle de nuanceur de sommets 3</span><span class="sxs-lookup"><span data-stu-id="f4667-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="f4667-122">Les types de registres de sortie du nuanceur de sommets ont été réduits en douze registres (consultez [registres de sortie](dx9-graphics-reference-asm-vs-registers-output.md)).</span><span class="sxs-lookup"><span data-stu-id="f4667-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="f4667-123">Chaque registre utilisé doit être déclaré à l’aide de l’instruction [DCL](dcl-usage---ps.md) et d’une sémantique (par exemple, DCL \_ Color0 o0. XYZW).</span><span class="sxs-lookup"><span data-stu-id="f4667-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="f4667-124">Le \_ modèle de nuanceur de sommets 3 0 (vs \_ 3 \_ 0) étend les fonctionnalités de vs \_ 2 \_ 0 avec l’indexation de registre plus puissante, un ensemble de registres de sortie simplifiés, la possibilité d’échantillonner une texture dans un nuanceur de vertex et la possibilité de contrôler la vitesse à laquelle les entrées du nuanceur sont initialisées.</span><span class="sxs-lookup"><span data-stu-id="f4667-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="f4667-125">Indexer un registre</span><span class="sxs-lookup"><span data-stu-id="f4667-125">Index Any Register</span></span>

<span data-ttu-id="f4667-126">Tous les registres (Registre [d’entrée](dx9-graphics-reference-asm-vs-registers-input.md) et [registres de sortie](dx9-graphics-reference-asm-vs-registers-output.md)) peuvent être indexés à l’aide du registre de compteur de [boucles](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (seuls les registres constants peuvent être indexés dans les versions antérieures.)</span><span class="sxs-lookup"><span data-stu-id="f4667-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="f4667-127">Vous devez déclarer les registres d’entrée et de sortie avant de les indexer.</span><span class="sxs-lookup"><span data-stu-id="f4667-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="f4667-128">Toutefois, vous ne pouvez pas indexer un registre de sortie qui a été déclaré avec une sémantique de taille de position ou de point.</span><span class="sxs-lookup"><span data-stu-id="f4667-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="f4667-129">En fait, si l’indexation est utilisée, les sémantiques position et psize doivent être déclarées respectivement dans les registres o0 et O1.</span><span class="sxs-lookup"><span data-stu-id="f4667-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="f4667-130">Vous êtes uniquement autorisé à indexer une plage continue de registres. autrement dit, vous ne pouvez pas indexer entre des registres qui n’ont pas été déclarés.</span><span class="sxs-lookup"><span data-stu-id="f4667-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="f4667-131">Bien que cette restriction puisse être gênante, elle permet l’optimisation du matériel.</span><span class="sxs-lookup"><span data-stu-id="f4667-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="f4667-132">Toute tentative d’indexation dans des registres non contigus produira des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="f4667-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="f4667-133">La validation du nuanceur n’applique pas cette restriction.</span><span class="sxs-lookup"><span data-stu-id="f4667-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="f4667-134">Simplifier les registres de sortie</span><span class="sxs-lookup"><span data-stu-id="f4667-134">Simplify Output Registers</span></span>

<span data-ttu-id="f4667-135">Tous les différents types de registres de sortie ont été réduits dans douze registres de sortie : 1 pour la position, 2 pour la couleur, 8 pour la texture et 1 pour la taille du brouillard ou du point.</span><span class="sxs-lookup"><span data-stu-id="f4667-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="f4667-136">Ces registres interpolent les données qu’ils contiennent pour le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f4667-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="f4667-137">Les déclarations de registre de sortie sont obligatoires et la sémantique est assignée à chaque registre.</span><span class="sxs-lookup"><span data-stu-id="f4667-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="f4667-138">Les registres peuvent être décomposés comme suit :</span><span class="sxs-lookup"><span data-stu-id="f4667-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="f4667-139">Au moins un registre doit être déclaré en tant que Registre de position à quatre composants.</span><span class="sxs-lookup"><span data-stu-id="f4667-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="f4667-140">Il s’agit du seul registre de nuanceur de vertex requis.</span><span class="sxs-lookup"><span data-stu-id="f4667-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="f4667-141">Les dix premiers registres consommés par un nuanceur peuvent utiliser jusqu’à quatre composants (XYZW) au maximum.</span><span class="sxs-lookup"><span data-stu-id="f4667-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="f4667-142">Le dernier (ou douzième) Registre peut uniquement contenir une valeur scalaire (par exemple, la taille du point).</span><span class="sxs-lookup"><span data-stu-id="f4667-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="f4667-143">Pour obtenir la liste des registres, consultez [registres-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="f4667-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="f4667-144">Échantillon de texture dans un nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="f4667-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="f4667-145">Vertex Shader 3 \_ 0 prend en charge la recherche de texture dans le nuanceur de sommets à l’aide de [texldl-vs](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="f4667-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="f4667-146">Caractéristiques du modèle de nuanceur de pixels 3</span><span class="sxs-lookup"><span data-stu-id="f4667-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="f4667-147">Les registres de couleur et de texture du nuanceur de pixels ont été réduits en dix registres d’entrée (voir [types de registres d’entrée](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="f4667-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="f4667-148">Le registre de visages est un registre scalaire à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="f4667-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="f4667-149">Seul le signe de ce registre est valide.</span><span class="sxs-lookup"><span data-stu-id="f4667-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="f4667-150">Si le signe est négatif, la primitive est une face arrière.</span><span class="sxs-lookup"><span data-stu-id="f4667-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="f4667-151">Cela peut être utilisé à l’intérieur d’un nuanceur de pixels pour obtenir un éclairage à deux côtés, par exemple.</span><span class="sxs-lookup"><span data-stu-id="f4667-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="f4667-152">Le registre de position fait référence aux pixels actifs (x, y).</span><span class="sxs-lookup"><span data-stu-id="f4667-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="f4667-153">Les registres de constantes de nuanceur peuvent être définis à l’aide de :</span><span class="sxs-lookup"><span data-stu-id="f4667-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="f4667-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="f4667-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="f4667-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="f4667-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="f4667-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="f4667-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="f4667-157">Sémantique de correspondance sur \_ \_ les nuanceurs vs 3 0 et PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f4667-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="f4667-158">Il existe des restrictions sur l’utilisation de la sémantique avec vs \_ 3 \_ 0 et PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="f4667-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="f4667-159">En général, vous devez être prudent lors de l’utilisation d’une sémantique pour une entrée de nuanceur qui correspond à une sémantique utilisée sur une sortie de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f4667-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="f4667-160">Par exemple, ce nuanceur de pixels compresse plusieurs noms dans un seul registre :</span><span class="sxs-lookup"><span data-stu-id="f4667-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="f4667-161">Chaque registre a une sémantique différente.</span><span class="sxs-lookup"><span data-stu-id="f4667-161">Each register has a different semantic.</span></span> <span data-ttu-id="f4667-162">Notez que vous pouvez également nommer v0. x et v0. YZ avec une sémantique différente (multiple) en raison de l’utilisation du masque d’écriture.</span><span class="sxs-lookup"><span data-stu-id="f4667-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="f4667-163">Étant donné le nuanceur de pixels, \_ le \_ nuanceur vs 3 0 suivant ne peut pas être associé :</span><span class="sxs-lookup"><span data-stu-id="f4667-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="f4667-164">Ces deux nuanceurs sont en conflit avec leur utilisation de la sémantique [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) et **D3DDECLUSAGE \_ TEXCOORD1** .</span><span class="sxs-lookup"><span data-stu-id="f4667-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="f4667-165">Réécrivez le nuanceur de sommets comme suit pour éviter la collision sémantique :</span><span class="sxs-lookup"><span data-stu-id="f4667-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="f4667-166">De même, un nom sémantique déclaré sur des registres d’entrée différents dans le nuanceur de pixels (v0 et V1 dans le nuanceur de pixels) ne peut pas être utilisé dans un registre de sortie unique dans ce nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="f4667-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="f4667-167">Par exemple, ce nuanceur vertex ne peut pas être couplé au nuanceur de pixels, car D3DDECLUSAGE \_ TEXCOORD1 est utilisé pour les registres d’entrée de nuanceur de pixels (v0, v1) et le registre de sortie du nuanceur de sommets O3.</span><span class="sxs-lookup"><span data-stu-id="f4667-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="f4667-168">En revanche, ce nuanceur vertex ne peut pas être couplé au nuanceur de pixels, car le masque de sortie d’un paramètre avec une sémantique donnée ne fournit pas les données demandées par le nuanceur de pixels :</span><span class="sxs-lookup"><span data-stu-id="f4667-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="f4667-169">Ce nuanceur vertex ne fournit pas de sortie avec l’un des noms sémantiques demandés par le nuanceur de pixels, de sorte que l’appariement du nuanceur n’est pas valide :</span><span class="sxs-lookup"><span data-stu-id="f4667-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="f4667-170">Modifications du mode de brouillard, de profondeur et d’ombrage</span><span class="sxs-lookup"><span data-stu-id="f4667-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="f4667-171">Lorsque D3DRS \_ SHADEMODE est défini pour l’ombrage plat lors du découpage et de la pixellisation des triangles, les attributs avec \_ couleur D3DDECLUSAGE sont interpolés comme étant à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="f4667-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="f4667-172">Si des composants d’un registre sont déclarés avec une sémantique de couleur, mais que d’autres composants du même registre reçoivent une sémantique différente, l’interpolation d’ombrage plat (linéaire ou plat) est non définie sur les composants de ce registre sans sémantique de couleur.</span><span class="sxs-lookup"><span data-stu-id="f4667-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="f4667-173">Si le rendu de brouillard est souhaité \_ , \_ les nuanceurs vs 3 0 et PS \_ 3 \_ 0 doivent implémenter le brouillard.</span><span class="sxs-lookup"><span data-stu-id="f4667-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="f4667-174">Aucun calcul de brouillard n’est effectué en dehors des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="f4667-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="f4667-175">Il n’y a pas de registre de brouillard dans vs \_ 3 \_ 0, et la sémantique supplémentaire D3DDECLUSAGE \_ brouillard (pour le facteur de fusion de brouillard calculé par vertex) et la \_ profondeur D3DDECLUSAGE (pour transmettre une valeur de profondeur au nuanceur de pixels pour calculer le facteur de mélange de brouillard) ont été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="f4667-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="f4667-176">L’état de l’étape de texture D3DTSS \_ TEXCOORDINDEX est ignoré lors de l’utilisation du nuanceur de pixels 3,0.</span><span class="sxs-lookup"><span data-stu-id="f4667-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="f4667-177">Les valeurs suivantes ont été ajoutées pour prendre en compte les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4667-177">The following values have been added to accommodate these changes:</span></span>


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="f4667-178">Conversions à virgule flottante et entiers</span><span class="sxs-lookup"><span data-stu-id="f4667-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="f4667-179">La mathématique à virgule flottante se produit à des plages et à une précision différentes (16 bits, 24 bits et 32 bits) dans différentes parties du pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4667-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="f4667-180">Une valeur supérieure à la plage dynamique du pipeline qui entre dans ce pipeline (par exemple, une carte de texture flottante de 32 bits est échantillonnée dans un pipeline à virgule flottante de 24 bits dans PS \_ 2 \_ 0) crée un résultat non défini.</span><span class="sxs-lookup"><span data-stu-id="f4667-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="f4667-181">Pour un comportement prévisible, vous devez fixer une telle valeur au maximum de la plage dynamique.</span><span class="sxs-lookup"><span data-stu-id="f4667-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="f4667-182">La conversion d’une valeur à virgule flottante en un entier se produit à plusieurs endroits, par exemple :</span><span class="sxs-lookup"><span data-stu-id="f4667-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="f4667-183">Lorsque vous rencontrez une instruction [Mova-vs](mova---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="f4667-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="f4667-184">Pendant l’adressage de la texture.</span><span class="sxs-lookup"><span data-stu-id="f4667-184">During texture addressing.</span></span>
-   <span data-ttu-id="f4667-185">Lors de l’écriture dans une cible de rendu à virgule non flottante.</span><span class="sxs-lookup"><span data-stu-id="f4667-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="f4667-186">Spécification de la précision complète ou partielle</span><span class="sxs-lookup"><span data-stu-id="f4667-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="f4667-187">PS \_ 3 \_ 0 et PS \_ 2 \_ x assurent la prise en charge de deux niveaux de précision :</span><span class="sxs-lookup"><span data-stu-id="f4667-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="f4667-188">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f4667-188">ps\_3\_0</span></span> | <span data-ttu-id="f4667-189">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f4667-189">ps\_2\_0</span></span> | <span data-ttu-id="f4667-190">Précision</span><span class="sxs-lookup"><span data-stu-id="f4667-190">Precision</span></span>         | <span data-ttu-id="f4667-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4667-191">Value</span></span>                |
| <span data-ttu-id="f4667-192">x</span><span class="sxs-lookup"><span data-stu-id="f4667-192">x</span></span>        |          | <span data-ttu-id="f4667-193">Complète</span><span class="sxs-lookup"><span data-stu-id="f4667-193">Full</span></span>              | <span data-ttu-id="f4667-194">fp32 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f4667-194">fp32 or higher</span></span>       |
| <span data-ttu-id="f4667-195">x</span><span class="sxs-lookup"><span data-stu-id="f4667-195">x</span></span>        |          | <span data-ttu-id="f4667-196">Précision partielle</span><span class="sxs-lookup"><span data-stu-id="f4667-196">Partial precision</span></span> | <span data-ttu-id="f4667-197">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="f4667-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="f4667-198">x</span><span class="sxs-lookup"><span data-stu-id="f4667-198">x</span></span>        | <span data-ttu-id="f4667-199">x</span><span class="sxs-lookup"><span data-stu-id="f4667-199">x</span></span>        | <span data-ttu-id="f4667-200">Complète</span><span class="sxs-lookup"><span data-stu-id="f4667-200">Full</span></span>              | <span data-ttu-id="f4667-201">fp24 = s16e7 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f4667-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="f4667-202">x</span><span class="sxs-lookup"><span data-stu-id="f4667-202">x</span></span>        | <span data-ttu-id="f4667-203">x</span><span class="sxs-lookup"><span data-stu-id="f4667-203">x</span></span>        | <span data-ttu-id="f4667-204">Précision partielle</span><span class="sxs-lookup"><span data-stu-id="f4667-204">Partial precision</span></span> | <span data-ttu-id="f4667-205">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="f4667-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="f4667-206">PS \_ 3 \_ 0 prend en charge une précision supérieure à celle de PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="f4667-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="f4667-207">Par défaut, toutes les opérations se produisent au niveau de précision complet.</span><span class="sxs-lookup"><span data-stu-id="f4667-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="f4667-208">La précision partielle (consultez [modificateurs de registre de nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers.md)) est demandée en ajoutant le \_ modificateur pp au code du nuanceur (à condition que l’implémentation sous-jacente le prenne en charge).</span><span class="sxs-lookup"><span data-stu-id="f4667-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="f4667-209">Les implémentations sont toujours gratuites pour ignorer le modificateur et effectuer les opérations affectées en toute précision.</span><span class="sxs-lookup"><span data-stu-id="f4667-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="f4667-210">Le \_ modificateur pp peut se produire dans deux contextes :</span><span class="sxs-lookup"><span data-stu-id="f4667-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="f4667-211">Sur une déclaration de coordonnée de texture pour passer des coordonnées de texture de précision partielle au nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f4667-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="f4667-212">Cela peut être utilisé lorsque les coordonnées de texture relayent les données de couleur vers le nuanceur de pixels, ce qui peut être plus rapide avec une précision partielle qu’avec une précision totale dans certaines implémentations.</span><span class="sxs-lookup"><span data-stu-id="f4667-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="f4667-213">Sur n’importe quelle instruction pour demander l’utilisation de la précision partielle, y compris des instructions de chargement de texture.</span><span class="sxs-lookup"><span data-stu-id="f4667-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="f4667-214">Cela indique que l’implémentation est autorisée à exécuter l’instruction avec une précision partielle et à stocker un résultat de précision partielle.</span><span class="sxs-lookup"><span data-stu-id="f4667-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="f4667-215">En l’absence d’un modificateur explicite, l’instruction doit être exécutée à la précision totale (quelle que soit la précision des opérandes d’entrée).</span><span class="sxs-lookup"><span data-stu-id="f4667-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="f4667-216">Une application peut choisir délibérément de commercialiser la précision des performances.</span><span class="sxs-lookup"><span data-stu-id="f4667-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="f4667-217">Il existe plusieurs types de données d’entrée de nuanceur qui sont des candidats naturels pour le traitement de la précision partielle :</span><span class="sxs-lookup"><span data-stu-id="f4667-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="f4667-218">Les itérateurs de couleur sont bien représentés par des valeurs de précision partielle.</span><span class="sxs-lookup"><span data-stu-id="f4667-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="f4667-219">Les valeurs de texture de la plupart des formats peuvent être correctement représentées par des valeurs de précision partielle (les valeurs échantillonnées à partir de 32 bits, les textures de format à virgule flottante sont une exception évidente).</span><span class="sxs-lookup"><span data-stu-id="f4667-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="f4667-220">Les constantes peuvent être représentées par une représentation partielle de précision appropriée au nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f4667-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="f4667-221">Dans tous ces cas, le développeur peut choisir de spécifier une précision partielle pour traiter les données, sachant qu’aucune précision de données d’entrée n’est perdue.</span><span class="sxs-lookup"><span data-stu-id="f4667-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="f4667-222">Dans certains cas, un nuanceur peut exiger que les étapes internes d’un calcul soient effectuées à pleine précision même lorsque les valeurs de sortie d’entrée et finales n’ont pas plus que la précision partielle.</span><span class="sxs-lookup"><span data-stu-id="f4667-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="f4667-223">Nuanceur de pixels et vertex logiciels</span><span class="sxs-lookup"><span data-stu-id="f4667-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="f4667-224">Les implémentations logicielles (au moment de l’exécution et la référence pour les nuanceurs vertex et la référence pour les nuanceurs de pixels) des nuanceurs de version 2 \_ 0 et versions ultérieures ont une validation assouplie.</span><span class="sxs-lookup"><span data-stu-id="f4667-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="f4667-225">Cela est utile à des fins de débogage et de prototypage.</span><span class="sxs-lookup"><span data-stu-id="f4667-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="f4667-226">L’application indique au runtime/assembleur qu’elle a besoin d’une partie de la validation assouplie à l’aide de l' \_ indicateur SW dans l’assembleur (par exemple, vs \_ 2 \_ SW).</span><span class="sxs-lookup"><span data-stu-id="f4667-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="f4667-227">Un nuanceur de logiciels ne fonctionnera pas avec le matériel.</span><span class="sxs-lookup"><span data-stu-id="f4667-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="f4667-228">vs \_ 2 \_ SW est un assouplissement aux limites maximales de vs \_ 2 \_ x ; de même, \_ \_ le logiciel PS 2 est une relaxation aux limites maximales de PS \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="f4667-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="f4667-229">Plus précisément, les validations suivantes sont assouplies :</span><span class="sxs-lookup"><span data-stu-id="f4667-229">Specifically, the following validations are relaxed:</span></span>



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4667-230">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="f4667-230">Shader Model</span></span>                               | <span data-ttu-id="f4667-231">Ressource</span><span class="sxs-lookup"><span data-stu-id="f4667-231">Resource</span></span>                             | <span data-ttu-id="f4667-232">Limite</span><span class="sxs-lookup"><span data-stu-id="f4667-232">Limit</span></span>                                                                                                                             |
| <span data-ttu-id="f4667-233">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4667-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="f4667-234">Nombre d’instructions</span><span class="sxs-lookup"><span data-stu-id="f4667-234">Instruction Counts</span></span>                   | <span data-ttu-id="f4667-235">Illimité</span><span class="sxs-lookup"><span data-stu-id="f4667-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="f4667-236">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4667-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="f4667-237">Registres à constante flottante</span><span class="sxs-lookup"><span data-stu-id="f4667-237">Float Constant Registers</span></span>             | <span data-ttu-id="f4667-238">8 192</span><span class="sxs-lookup"><span data-stu-id="f4667-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="f4667-239">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4667-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="f4667-240">Registres de constantes entières</span><span class="sxs-lookup"><span data-stu-id="f4667-240">Integer Constant Registers</span></span>           | <span data-ttu-id="f4667-241">2 048</span><span class="sxs-lookup"><span data-stu-id="f4667-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="f4667-242">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4667-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="f4667-243">Registres de constantes booléennes</span><span class="sxs-lookup"><span data-stu-id="f4667-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="f4667-244">2 048</span><span class="sxs-lookup"><span data-stu-id="f4667-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="f4667-245">\_logiciel PS 2 \_</span><span class="sxs-lookup"><span data-stu-id="f4667-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="f4667-246">Profondeur de lecture dépendante</span><span class="sxs-lookup"><span data-stu-id="f4667-246">Dependent-read depth</span></span>                 | <span data-ttu-id="f4667-247">Illimité</span><span class="sxs-lookup"><span data-stu-id="f4667-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="f4667-248">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4667-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="f4667-249">instructions et étiquettes de contrôle de Flow</span><span class="sxs-lookup"><span data-stu-id="f4667-249">flow control instructions and labels</span></span> | <span data-ttu-id="f4667-250">Illimité</span><span class="sxs-lookup"><span data-stu-id="f4667-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="f4667-251">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4667-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="f4667-252">Nombre de boucles Start/Step/Count</span><span class="sxs-lookup"><span data-stu-id="f4667-252">Loop start/step/counts</span></span>               | <span data-ttu-id="f4667-253">Le début de l’itération et la taille de l’étape de l’itération pour les instructions du REP et de la boucle sont des entiers signés 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f4667-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="f4667-254">Le nombre peut atteindre un maximum de \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="f4667-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="f4667-255">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4667-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="f4667-256">Limites de port</span><span class="sxs-lookup"><span data-stu-id="f4667-256">Port limits</span></span>                          | <span data-ttu-id="f4667-257">Les limites de port pour tous les fichiers de Registre sont assouplies.</span><span class="sxs-lookup"><span data-stu-id="f4667-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="f4667-258">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f4667-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="f4667-259">Nombre d’interpolateurs</span><span class="sxs-lookup"><span data-stu-id="f4667-259">Number of interpolators</span></span>              | <span data-ttu-id="f4667-260">16 registres de sortie dans vs \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="f4667-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="f4667-261">\_logiciel PS 3 \_</span><span class="sxs-lookup"><span data-stu-id="f4667-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="f4667-262">Nombre d’interpolateurs</span><span class="sxs-lookup"><span data-stu-id="f4667-262">Number of interpolators</span></span>              | <span data-ttu-id="f4667-263">14 (16-2) registres d’entrée pour le \_ logiciel PS 3 \_ .</span><span class="sxs-lookup"><span data-stu-id="f4667-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="f4667-264">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4667-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4667-265">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f4667-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 