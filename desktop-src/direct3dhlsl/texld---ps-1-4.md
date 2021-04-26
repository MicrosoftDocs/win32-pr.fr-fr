---
title: texld-ps_1_4
description: Charge le registre de destination avec les données de couleur (RVBA) échantillonnées en utilisant le contenu du Registre source comme coordonnées de texture. La texture échantillonnée est la texture associée au numéro de registre de destination.
ms.assetid: 1970aed4-4da7-40a1-960d-fba4dfd8c433
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca305b16db0f390354962a3e959f08b6e956f2ef
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996866"
---
# <a name="texld---ps_1_4"></a><span data-ttu-id="aa56c-104">texld-PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="aa56c-104">texld - ps\_1\_4</span></span>

<span data-ttu-id="aa56c-105">Charge le registre de destination avec les données de couleur (RVBA) échantillonnées en utilisant le contenu du Registre source comme coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="aa56c-105">Loads the destination register with color data (RGBA) sampled using the contents of the source register as texture coordinates.</span></span> <span data-ttu-id="aa56c-106">La texture échantillonnée est la texture associée au numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="aa56c-106">The sampled texture is the texture associated with the destination register number.</span></span>



| <span data-ttu-id="aa56c-107">texld DST, SRC</span><span class="sxs-lookup"><span data-stu-id="aa56c-107">texld dst, src</span></span> |
|----------------|



 

## <a name="registers"></a><span data-ttu-id="aa56c-108">Registres</span><span class="sxs-lookup"><span data-stu-id="aa56c-108">Registers</span></span>



|          |                      | <span data-ttu-id="aa56c-109">VN</span><span class="sxs-lookup"><span data-stu-id="aa56c-109">vₙ</span></span>        | <span data-ttu-id="aa56c-110">8525</span><span class="sxs-lookup"><span data-stu-id="aa56c-110">cₙ</span></span>  | <span data-ttu-id="aa56c-111">TN</span><span class="sxs-lookup"><span data-stu-id="aa56c-111">tₙ</span></span>  | <span data-ttu-id="aa56c-112">RN</span><span class="sxs-lookup"><span data-stu-id="aa56c-112">rₙ</span></span>  |              |
|----------|----------------------|-----------|-----|-----|-----|--------------|
| <span data-ttu-id="aa56c-113">dst</span><span class="sxs-lookup"><span data-stu-id="aa56c-113">dst</span></span>      | <span data-ttu-id="aa56c-114">Registre de destination</span><span class="sxs-lookup"><span data-stu-id="aa56c-114">Destination register</span></span> |           |     |     | <span data-ttu-id="aa56c-115">x</span><span class="sxs-lookup"><span data-stu-id="aa56c-115">x</span></span>   | <span data-ttu-id="aa56c-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="aa56c-116">1\_4</span></span>         |
| <span data-ttu-id="aa56c-117">src</span><span class="sxs-lookup"><span data-stu-id="aa56c-117">src</span></span>      | <span data-ttu-id="aa56c-118">Registre source</span><span class="sxs-lookup"><span data-stu-id="aa56c-118">Source register</span></span>      |           |     | <span data-ttu-id="aa56c-119">x</span><span class="sxs-lookup"><span data-stu-id="aa56c-119">x</span></span>   |     | <span data-ttu-id="aa56c-120">1 \_ 4 phase 1</span><span class="sxs-lookup"><span data-stu-id="aa56c-120">1\_4 phase 1</span></span> |
|          |                      |           |     | <span data-ttu-id="aa56c-121">x</span><span class="sxs-lookup"><span data-stu-id="aa56c-121">x</span></span>   | <span data-ttu-id="aa56c-122">x</span><span class="sxs-lookup"><span data-stu-id="aa56c-122">x</span></span>   | <span data-ttu-id="aa56c-123">1 \_ phase</span><span class="sxs-lookup"><span data-stu-id="aa56c-123">1\_4 phase</span></span>   |



 

<span data-ttu-id="aa56c-124">Lors de l’utilisation de r (n) comme Registre source, les trois premiers composants (XYZ) doivent avoir été initialisés au cours de la phase précédente du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="aa56c-124">When using r(n) as a source register, the first three components (XYZ) must have been initialized in the previous phase of the shader.</span></span>

<span data-ttu-id="aa56c-125">Pour en savoir plus sur les registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="aa56c-125">To learn more about registers, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aa56c-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="aa56c-126">Remarks</span></span>

<span data-ttu-id="aa56c-127">Cette instruction échantillonne la texture dans l’étape de texture associée au numéro de registre de destination.</span><span class="sxs-lookup"><span data-stu-id="aa56c-127">This instruction samples the texture in the texture stage associated with the destination register number.</span></span> <span data-ttu-id="aa56c-128">La texture est échantillonnée à l’aide des données de coordonnée de texture du Registre source.</span><span class="sxs-lookup"><span data-stu-id="aa56c-128">The texture is sampled using texture coordinate data from the source register.</span></span>

<span data-ttu-id="aa56c-129">La syntaxe des instructions texld et texcrd expose la prise en charge d’une division projective avec un modificateur de registre de texture.</span><span class="sxs-lookup"><span data-stu-id="aa56c-129">The syntax for the texld and texcrd instructions expose support for a projective divide with a Texture Register Modifier.</span></span> <span data-ttu-id="aa56c-130">Pour le nuanceur de pixels version 1,4, l' \_ indicateur de transformation de texture projeté D3DTTFF est toujours ignoré.</span><span class="sxs-lookup"><span data-stu-id="aa56c-130">For pixel shader version 1.4, the D3DTTFF\_PROJECTED texture transform flag is always ignored.</span></span>

<span data-ttu-id="aa56c-131">Règles d’utilisation de texld :</span><span class="sxs-lookup"><span data-stu-id="aa56c-131">Rules for using texld:</span></span>

1.  <span data-ttu-id="aa56c-132">Le même modificateur. xyz ou. XYW doit être appliqué à chaque lecture d’un registre t (n) individuel dans les instructions texcrd ou texld.</span><span class="sxs-lookup"><span data-stu-id="aa56c-132">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within both texcrd or texld instructions.</span></span> <span data-ttu-id="aa56c-133">Si. XYW est utilisé sur les lectures de Registre t (n), il peut être mélangé à d’autres lectures du même registre t (n) à l’aide de la fonction dw. XYW \_ .</span><span class="sxs-lookup"><span data-stu-id="aa56c-133">If .xyw is being used on t(n) register reads, this can be mixed with other reads of the same t(n) register using .xyw\_dw.</span></span>
2.  <span data-ttu-id="aa56c-134">Le \_ modificateur de source DZ est uniquement valide sur texld avec le registre source r (n) (donc la phase 2 uniquement).</span><span class="sxs-lookup"><span data-stu-id="aa56c-134">The \_dz source modifier is only valid on texld with r(n) source register (thus phase 2 only).</span></span>
3.  <span data-ttu-id="aa56c-135">Le \_ modificateur de source DZ ne peut pas être utilisé plus de deux fois par nuanceur.</span><span class="sxs-lookup"><span data-stu-id="aa56c-135">The \_dz source modifier may be used no more than two times per shader.</span></span>



| <span data-ttu-id="aa56c-136">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="aa56c-136">Pixel shader versions</span></span> | <span data-ttu-id="aa56c-137">1\_1</span><span class="sxs-lookup"><span data-stu-id="aa56c-137">1\_1</span></span> | <span data-ttu-id="aa56c-138">1\_2</span><span class="sxs-lookup"><span data-stu-id="aa56c-138">1\_2</span></span> | <span data-ttu-id="aa56c-139">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="aa56c-139">1\_3</span></span> | <span data-ttu-id="aa56c-140">1\_4</span><span class="sxs-lookup"><span data-stu-id="aa56c-140">1\_4</span></span> | <span data-ttu-id="aa56c-141">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa56c-141">2\_0</span></span> | <span data-ttu-id="aa56c-142">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="aa56c-142">2\_x</span></span> | <span data-ttu-id="aa56c-143">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="aa56c-143">2\_sw</span></span> | <span data-ttu-id="aa56c-144">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa56c-144">3\_0</span></span> | <span data-ttu-id="aa56c-145">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="aa56c-145">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="aa56c-146">texld</span><span class="sxs-lookup"><span data-stu-id="aa56c-146">texld</span></span>                 |      |      |      | <span data-ttu-id="aa56c-147">x</span><span class="sxs-lookup"><span data-stu-id="aa56c-147">x</span></span>    |      |      |       |      |       |



 

## <a name="examples"></a><span data-ttu-id="aa56c-148">Exemples</span><span class="sxs-lookup"><span data-stu-id="aa56c-148">Examples</span></span>

<span data-ttu-id="aa56c-149">L’instruction texld offre un certain contrôle sur les composants des données de coordonnée de texture source qui sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="aa56c-149">The texld instruction offers some control over which components of the source texture coordinate data are used.</span></span> <span data-ttu-id="aa56c-150">L’ensemble complet de syntaxe autorisée pour texld suit et comprend tous les modificateurs de Registre source valides, les sélecteurs et les combinaisons de masques d’écriture.</span><span class="sxs-lookup"><span data-stu-id="aa56c-150">The complete set of allowed syntax for texld follows, and includes all valid source register modifiers, selectors, and write mask combinations.</span></span>


```
texld  r(m), t(n).xyz
// Uses xyz from t(n) to sample 1D, 2D, or 3D texture
```




```
texld  r(m), t(n)
// Same as previous
```




```
texld  r(m), t(n).xyw
// Uses xyw (skipping z) from t(n) to sample 1D, 2D or 3D texture
```




```
texld  r(m), t(n)_dw.xyw  
// Samples 1D or 2D texture at x/w, y/w from t(n). The result
// is undefined for a cube-map lookup.
```




```
texld  r(m), r(n).xyz
// Samples 1D, 2D, or 3D texture at xyz from r(m) 
// This is possible in the second phase of the shader
```




```
texld  r(m), r(n)
// Same as previous
```




```
texld  r(m), r(n)_dz.xyz
// Samples 1D or 2D texture at x/z, y/z from r(m)
// Possible only in second phase
// The result is undefined for a cube-map lookup
```




```
texld  r(n), r(n)_dz
// Same as previous
```



## <a name="related-topics"></a><span data-ttu-id="aa56c-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa56c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa56c-152">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="aa56c-152">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




