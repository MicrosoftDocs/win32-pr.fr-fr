---
title: texbem-PS
description: Appliquez une transformation de mappage d’environnement factice. Pour ce faire, vous devez modifier les données d’adresse de texture du registre de destination, en utilisant les données de perturbation d’adresse (du, DV) et une matrice d’environnement de relief 2D.
ms.assetid: 8e773f4a-c7a2-4caf-973f-8f50dccc9c04
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f026819b268836fd7d4c1d550033ceefdf0bbbf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971719"
---
# <a name="texbem---ps"></a><span data-ttu-id="54c09-104">texbem-PS</span><span class="sxs-lookup"><span data-stu-id="54c09-104">texbem - ps</span></span>

<span data-ttu-id="54c09-105">Appliquez une transformation de mappage d’environnement factice.</span><span class="sxs-lookup"><span data-stu-id="54c09-105">Apply a fake bump environment-map transform.</span></span> <span data-ttu-id="54c09-106">Pour ce faire, vous devez modifier les données d’adresse de texture du registre de destination, en utilisant les données de perturbation d’adresse (du, DV) et une matrice d’environnement de relief 2D.</span><span class="sxs-lookup"><span data-stu-id="54c09-106">This is accomplished by modifying the texture address data of the destination register, using address perturbation data (du,dv), and a 2D bump environment matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="54c09-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54c09-107">Syntax</span></span>



| <span data-ttu-id="54c09-108">texbem DST, SRC</span><span class="sxs-lookup"><span data-stu-id="54c09-108">texbem dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="54c09-109">where</span><span class="sxs-lookup"><span data-stu-id="54c09-109">where</span></span>

-   <span data-ttu-id="54c09-110">l’heure d’été est le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="54c09-110">dst is the destination register.</span></span>
-   <span data-ttu-id="54c09-111">SRC est un registre source.</span><span class="sxs-lookup"><span data-stu-id="54c09-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="54c09-112">Notes</span><span class="sxs-lookup"><span data-stu-id="54c09-112">Remarks</span></span>



| <span data-ttu-id="54c09-113">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="54c09-113">Pixel shader versions</span></span> | <span data-ttu-id="54c09-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="54c09-114">1\_1</span></span> | <span data-ttu-id="54c09-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="54c09-115">1\_2</span></span> | <span data-ttu-id="54c09-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="54c09-116">1\_3</span></span> | <span data-ttu-id="54c09-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="54c09-117">1\_4</span></span> | <span data-ttu-id="54c09-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="54c09-118">2\_0</span></span> | <span data-ttu-id="54c09-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="54c09-119">2\_x</span></span> | <span data-ttu-id="54c09-120">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="54c09-120">2\_sw</span></span> | <span data-ttu-id="54c09-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="54c09-121">3\_0</span></span> | <span data-ttu-id="54c09-122">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="54c09-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="54c09-123">texbem</span><span class="sxs-lookup"><span data-stu-id="54c09-123">texbem</span></span>                | <span data-ttu-id="54c09-124">x</span><span class="sxs-lookup"><span data-stu-id="54c09-124">x</span></span>    | <span data-ttu-id="54c09-125">x</span><span class="sxs-lookup"><span data-stu-id="54c09-125">x</span></span>    | <span data-ttu-id="54c09-126">x</span><span class="sxs-lookup"><span data-stu-id="54c09-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="54c09-127">Les données de couleur rouge et verte dans le registre SRC sont interprétées comme les données de perturbation (du, DV).</span><span class="sxs-lookup"><span data-stu-id="54c09-127">The red and green color data in the src register is interpreted as the perturbation data (du,dv).</span></span>

<span data-ttu-id="54c09-128">Cette instruction transforme les composants rouge et vert dans le registre source à l’aide de la matrice de mappage d’environnement 2D Bump.</span><span class="sxs-lookup"><span data-stu-id="54c09-128">This instruction transforms red and green components in the source register using the 2D bump environment-mapping matrix.</span></span> <span data-ttu-id="54c09-129">Le résultat est ajouté au jeu de coordonnées de texture correspondant au numéro de registre de destination, et est utilisé pour échantillonner l’étape de texture actuelle.</span><span class="sxs-lookup"><span data-stu-id="54c09-129">The result is added to the texture coordinate set corresponding to the destination register number, and is used to sample the current texture stage.</span></span>

<span data-ttu-id="54c09-130">Cette opération interprète toujours les et DV comme des quantités signées.</span><span class="sxs-lookup"><span data-stu-id="54c09-130">This operation always interprets du and dv as signed quantities.</span></span> <span data-ttu-id="54c09-131">Pour les versions 1 \_ 0 et 1 \_ 1, le modificateur d’entrée de [mise à l’échelle signée du Registre source](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ BX2) n’est pas autorisé sur l’argument d’entrée.</span><span class="sxs-lookup"><span data-stu-id="54c09-131">For versions 1\_0 and 1\_1, the [Source Register Signed Scaling](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) input modifier (\_bx2) is not permitted on the input argument.</span></span>

<span data-ttu-id="54c09-132">Cette instruction produit des résultats définis lorsque les textures d’entrée contiennent des données au format signé.</span><span class="sxs-lookup"><span data-stu-id="54c09-132">This instruction produces defined results when input textures contain signed format data.</span></span> <span data-ttu-id="54c09-133">Les données au format mixte fonctionnent uniquement si les deux premiers canaux contiennent des données signées.</span><span class="sxs-lookup"><span data-stu-id="54c09-133">Mixed format data works only if the first two channels contain signed data.</span></span> <span data-ttu-id="54c09-134">Pour plus d’informations sur les formats de surface, consultez [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="54c09-134">For more information about surface formats, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

<span data-ttu-id="54c09-135">Cela peut être utilisé pour diverses techniques basées sur la perturbation des adresses, y compris le mappage d’environnement factice par pixel et l’éclairage diffus (placage de relief).</span><span class="sxs-lookup"><span data-stu-id="54c09-135">This can be used for a variety of techniques based on address perturbation, including fake per-pixel environment mapping and diffuse lighting (bump mapping).</span></span>

<span data-ttu-id="54c09-136">Lors de l’utilisation de cette instruction, les registres de texture doivent respecter la séquence suivante.</span><span class="sxs-lookup"><span data-stu-id="54c09-136">When using this instruction, texture registers must follow the following sequence.</span></span>


```
// The texture assigned to stage t(n) contains the (du,dv) data
// The texture assigned to stage t(m) is sampled
tex     t(n)                    
texbem  t(m),  t(n)      where m > n
```



<span data-ttu-id="54c09-137">Les calculs effectués dans l’instruction sont indiqués ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="54c09-137">The calculations done within the instruction are shown below.</span></span>


```
// 1. New values for texture addresses (u',v') are calculated
// 2. Sample the texture using (u',v')
```



<span data-ttu-id="54c09-138">u' = TextureCoordinates (stage m)<sub>u</sub> + D3DTSS \_ BUMPENVMAT00 (étape m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT10 (étape m) \* t (n)<sub>G</sub> v' = TextureCoordinates (étape m)<sub>v</sub> + D3DTSS \_ BUMPENVMAT01 (étape m) \* t (n)<sub>R</sub> + D3DTSS \_ BUMPENVMAT11 (étape m) \* t (n)<sub>G</sub> t (m)<sub>RVBA</sub> = TextureSample (étape m)</span><span class="sxs-lookup"><span data-stu-id="54c09-138">u' = TextureCoordinates(stage m)<sub>u</sub> + D3DTSS\_BUMPENVMAT00(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT10(stage m)\*t(n)<sub>G</sub> v' = TextureCoordinates(stage m)<sub>v</sub> + D3DTSS\_BUMPENVMAT01(stage m)\*t(n)<sub>R</sub> + D3DTSS\_BUMPENVMAT11(stage m)\*t(n)<sub>G</sub> t(m)<sub>RGBA</sub> = TextureSample(stage m)</span></span>

<span data-ttu-id="54c09-139">utilisation de (u', v') comme coordonnées</span><span class="sxs-lookup"><span data-stu-id="54c09-139">// using (u',v') as coordinates</span></span>

<span data-ttu-id="54c09-140">Les données d’enregistrement qui ont été lues par une instruction texbem-PS ou [texbeml-PS](texbeml---ps.md) ne peuvent pas être lues ultérieurement, sauf par un autre texbem-PS ou texbeml-PS.</span><span class="sxs-lookup"><span data-stu-id="54c09-140">Register data that has been read by a texbem - ps or [texbeml - ps](texbeml---ps.md) instruction cannot be read later, except by another texbem - ps or texbeml - ps.</span></span>


```
// This example demonstrates the validation error caused by t0 being reread:
ps_1_1
tex t0
texbem t1, t0
add r0, t1, t0

(Instruction Error) (Statement 4) Register data that has been read by 
texbem or texbeml instruction cannot be read by other instructions
```



## <a name="examples"></a><span data-ttu-id="54c09-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="54c09-141">Examples</span></span>

<span data-ttu-id="54c09-142">Voici un exemple de nuanceur avec les cartes de texture identifiées et les étapes de texture identifiées.</span><span class="sxs-lookup"><span data-stu-id="54c09-142">Here is an example shader with the texture maps identified and the texture stages identified.</span></span>


```
ps_1_1
tex t0              ; Define t0 to get a 2-tuple DuDv
texbem t1, t0       ; Compute (u',v')
                    ; Sample t1 using (u',v')
mov r0, t1          ; Output result
```



<span data-ttu-id="54c09-143">texbem requiert les textures suivantes dans les étapes de texture suivantes.</span><span class="sxs-lookup"><span data-stu-id="54c09-143">texbem requires the following textures in the following texture stages.</span></span>

-   <span data-ttu-id="54c09-144">Une carte de relief est assignée à l’étape 0 avec des données de perturbation (du, DV).</span><span class="sxs-lookup"><span data-stu-id="54c09-144">Stage 0 is assigned a bump map with (du, dv) perturbation data.</span></span>
-   <span data-ttu-id="54c09-145">L’étape 1 utilise une carte de texture avec des données de couleur.</span><span class="sxs-lookup"><span data-stu-id="54c09-145">Stage 1 uses a texture map with color data.</span></span>
-   <span data-ttu-id="54c09-146">Cette instruction définit les données de la matrice sur l’étape de texture échantillonnée.</span><span class="sxs-lookup"><span data-stu-id="54c09-146">This instruction sets the matrix data on the texture stage that is sampled.</span></span>
-   <span data-ttu-id="54c09-147">Cela diffère de la fonctionnalité du pipeline de fonction fixe dans lequel les données de perturbation et les matrices occupent la même étape de texture.</span><span class="sxs-lookup"><span data-stu-id="54c09-147">This is different from the functionality of the fixed function pipeline where the perturbation data and the matrices occupy the same texture stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54c09-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54c09-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54c09-149">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="54c09-149">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 