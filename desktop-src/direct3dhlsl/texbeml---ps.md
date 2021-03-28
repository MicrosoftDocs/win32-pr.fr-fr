---
title: texbeml-PS
description: Appliquez une transformation de placage d’environnement factice avec correction de luminance. Pour ce faire, vous devez modifier les données d’adresse de texture du registre de destination, en utilisant les données de perturbation d’adresse (du, DV), la matrice d’environnement de relief 2D et la luminance.
ms.assetid: 345a0b77-8d4e-4a0b-a31a-1153f8cb5961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d97877c67970f43a995fcfbe21d9aead2d792e09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941316"
---
# <a name="texbeml---ps"></a><span data-ttu-id="178fa-104">texbeml-PS</span><span class="sxs-lookup"><span data-stu-id="178fa-104">texbeml - ps</span></span>

<span data-ttu-id="178fa-105">Appliquez une transformation de placage d’environnement factice avec correction de luminance.</span><span class="sxs-lookup"><span data-stu-id="178fa-105">Apply a fake bump environment-map transform with luminance correction.</span></span> <span data-ttu-id="178fa-106">Pour ce faire, vous devez modifier les données d’adresse de texture du registre de destination, en utilisant les données de perturbation d’adresse (du, DV), la matrice d’environnement de relief 2D et la luminance.</span><span class="sxs-lookup"><span data-stu-id="178fa-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), a 2D bump environment matrix, and luminance.</span></span>

## <a name="syntax"></a><span data-ttu-id="178fa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="178fa-107">Syntax</span></span>



| <span data-ttu-id="178fa-108">texbeml DST, SRC</span><span class="sxs-lookup"><span data-stu-id="178fa-108">texbeml dst, src</span></span> |
|------------------|



 

<span data-ttu-id="178fa-109">where</span><span class="sxs-lookup"><span data-stu-id="178fa-109">where</span></span>

-   <span data-ttu-id="178fa-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="178fa-110">dst is the destination register.</span></span>
-   <span data-ttu-id="178fa-111">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="178fa-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="178fa-112">Notes</span><span class="sxs-lookup"><span data-stu-id="178fa-112">Remarks</span></span>



| <span data-ttu-id="178fa-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="178fa-113">Pixel shader versions</span></span> | <span data-ttu-id="178fa-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="178fa-114">1\_1</span></span> | <span data-ttu-id="178fa-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="178fa-115">1\_2</span></span> | <span data-ttu-id="178fa-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="178fa-116">1\_3</span></span> | <span data-ttu-id="178fa-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="178fa-117">1\_4</span></span> | <span data-ttu-id="178fa-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="178fa-118">2\_0</span></span> | <span data-ttu-id="178fa-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="178fa-119">2\_x</span></span> | <span data-ttu-id="178fa-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="178fa-120">2\_sw</span></span> | <span data-ttu-id="178fa-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="178fa-121">3\_0</span></span> | <span data-ttu-id="178fa-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="178fa-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="178fa-123">texbeml</span><span class="sxs-lookup"><span data-stu-id="178fa-123">texbeml</span></span>               | <span data-ttu-id="178fa-124">x</span><span class="sxs-lookup"><span data-stu-id="178fa-124">x</span></span>    | <span data-ttu-id="178fa-125">x</span><span class="sxs-lookup"><span data-stu-id="178fa-125">x</span></span>    | <span data-ttu-id="178fa-126">x</span><span class="sxs-lookup"><span data-stu-id="178fa-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="178fa-127">Les données de couleur rouge et verte dans le registre SRC sont interprétées comme les données de perturbation (du, DV).</span><span class="sxs-lookup"><span data-stu-id="178fa-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span> <span data-ttu-id="178fa-128">Les données de couleur bleue dans le registre SRC sont interprétées comme les données de luminance.</span><span class="sxs-lookup"><span data-stu-id="178fa-128">The blue color data in the src register is interpreted as the luminance data.</span></span>

<span data-ttu-id="178fa-129">Cette instruction transforme les composants rouge et vert dans le registre source à l’aide de la matrice de mappage d’environnement de relief 2D.</span><span class="sxs-lookup"><span data-stu-id="178fa-129">This instruction transforms the red and green components in the source register using the 2D bump environment mapping matrix.</span></span> <span data-ttu-id="178fa-130">Le résultat est ajouté au jeu de coordonnées de texture correspondant au numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="178fa-130">The result is added to the texture coordinate set corresponding to the destination register number.</span></span> <span data-ttu-id="178fa-131">Une correction de luminance est appliquée à l’aide de la valeur de luminance et des valeurs d’étape de texture biaisée.</span><span class="sxs-lookup"><span data-stu-id="178fa-131">A luminance correction is applied using the luminance value and the bias texture stage values.</span></span> <span data-ttu-id="178fa-132">Le résultat est utilisé pour échantillonner l’étape de texture actuelle.</span><span class="sxs-lookup"><span data-stu-id="178fa-132">The result is used to sample the current texture stage.</span></span>

<span data-ttu-id="178fa-133">Cela peut être utilisé pour diverses techniques basées sur la perturbation des adresses, telles que le mappage d’environnement factice par pixel.</span><span class="sxs-lookup"><span data-stu-id="178fa-133">This can be used for a variety of techniques based on address perturbation such as fake per-pixel environment mapping.</span></span>

<span data-ttu-id="178fa-134">Cette opération interprète toujours les et DV comme des quantités signées.</span><span class="sxs-lookup"><span data-stu-id="178fa-134">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="178fa-135">Pour les versions 1 \_ 0 et 1 \_ 1, le modificateur d’entrée de [mise à l’échelle signée du Registre source](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) n’est pas autorisé sur l’argument d’entrée.</span><span class="sxs-lookup"><span data-stu-id="178fa-135">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="178fa-136">Cette instruction produit des résultats définis lorsque les textures d’entrée contiennent des données au format mixte.</span><span class="sxs-lookup"><span data-stu-id="178fa-136">This instruction produces defined results when input textures contain mixed format data.</span></span> <span data-ttu-id="178fa-137">Pour plus d’informations sur les formats de surface, consultez [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="178fa-137">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>


```
// When using this instruction, texture registers must follow 
//   the following sequence:
// The texture assigned to stage tn contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbeml t(m),  t(n)      where m > n
```



<span data-ttu-id="178fa-138">Cet exemple montre les calculs effectués dans l’instruction.</span><span class="sxs-lookup"><span data-stu-id="178fa-138">This example shows the calculations done within the instruction.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
// 3. Luminance correction is applied
```



<span data-ttu-id="178fa-139">u' = TextureCoordinates (étape m)<sub>u</sub> +</span><span class="sxs-lookup"><span data-stu-id="178fa-139">u' = TextureCoordinates(stage m)<sub>u</sub> +</span></span>

<span data-ttu-id="178fa-140">D3DTSS \_ BUMPENVMAT00 (étape m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="178fa-140">D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="178fa-141">D3DTSS \_ BUMPENVMAT10 (étape m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="178fa-141">D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="178fa-142">v' = TextureCoordinates (étape m)<sub>v</sub> +</span><span class="sxs-lookup"><span data-stu-id="178fa-142">v' = TextureCoordinates(stage m)<sub>v</sub> +</span></span>

<span data-ttu-id="178fa-143">D3DTSS \_ BUMPENVMAT01 (étape m) \* t (n)<sub>R</sub> +</span><span class="sxs-lookup"><span data-stu-id="178fa-143">D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> +</span></span>

<span data-ttu-id="178fa-144">D3DTSS \_ BUMPENVMAT11 (étape m) \* t (n)<sub>G</sub></span><span class="sxs-lookup"><span data-stu-id="178fa-144">D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub></span></span>

<span data-ttu-id="178fa-145">t (m)<sub>RVBA</sub> = TextureSample (étape m) utilisation de (u’v') en tant que coordonnées</span><span class="sxs-lookup"><span data-stu-id="178fa-145">t(m)<sub>RGBA</sub> = TextureSample(stage m) using (u',v') as coordinates</span></span>

<span data-ttu-id="178fa-146">t (m)<sub>RVBA</sub> = t (m)<sub>RVBA</sub>\*</span><span class="sxs-lookup"><span data-stu-id="178fa-146">t(m)<sub>RGBA</sub> = t(m)<sub>RGBA</sub> \*</span></span>

<span data-ttu-id="178fa-147">\[(t (n)<sub>B</sub> \* D3DTSS \_ BUMPENVLSCALE (étape m)) +</span><span class="sxs-lookup"><span data-stu-id="178fa-147">\[(t(n)<sub>B</sub> \* D3DTSS\_BUMPENVLSCALE(stage m)) +</span></span>

<span data-ttu-id="178fa-148">D3DTSS \_ BUMPENVLOFFSET (étape m)\]</span><span class="sxs-lookup"><span data-stu-id="178fa-148">D3DTSS\_BUMPENVLOFFSET(stage m)\]</span></span>

<span data-ttu-id="178fa-149">Les données d’enregistrement qui ont été lues par une instruction [texbem](texbem---ps.md) ou texbeml ne peuvent pas être lues ultérieurement, sauf par un autre texbem ou texbeml.</span><span class="sxs-lookup"><span data-stu-id="178fa-149">Register data that has been read by a [texbem](texbem---ps.md) or texbeml instruction cannot be read later, except by another texbem or texbeml.</span></span>


```
// This example demonstrates the validation error caused by 
//   t0 being reread
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="178fa-150">Exemples</span><span class="sxs-lookup"><span data-stu-id="178fa-150">Examples</span></span>

<span data-ttu-id="178fa-151">Voici un exemple de nuanceur avec les cartes de texture identifiées et les étapes de texture identifiées.</span><span class="sxs-lookup"><span data-stu-id="178fa-151">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbeml t1, t0      ; Compute (u',v')
                    ; Apply luminance correction                    
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="178fa-152">Cet exemple requiert les textures suivantes dans les étapes de texture suivantes.</span><span class="sxs-lookup"><span data-stu-id="178fa-152">This example requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="178fa-153">Une carte de relief est assignée à l’étape 0 avec des données de perturbation (du, DV).</span><span class="sxs-lookup"><span data-stu-id="178fa-153">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="178fa-154">Une carte de texture avec des données de couleur est assignée à la phase 1.</span><span class="sxs-lookup"><span data-stu-id="178fa-154">Stage 1 is assigned a texture map with color data.</span></span>
-   <span data-ttu-id="178fa-155">texbeml définit les données de la matrice sur l’étape de texture échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="178fa-155">texbeml sets the matrix data on the texture stage that is sampled.</span></span> <span data-ttu-id="178fa-156">Cela diffère de la fonctionnalité du pipeline de fonction fixe dans lequel les données de perturbation et les matrices occupent la même étape de texture.</span><span class="sxs-lookup"><span data-stu-id="178fa-156">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="178fa-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="178fa-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="178fa-158">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="178fa-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 