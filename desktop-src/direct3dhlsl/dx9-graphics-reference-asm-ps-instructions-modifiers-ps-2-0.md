---
title: Modificateurs pour ps_2_0 et versions ultérieures
description: Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840869"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="b7014-103">Modificateurs pour PS \_ 2 \_ 0 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="b7014-103">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="b7014-104">Les modificateurs d’instruction affectent le résultat de l’instruction avant qu’elle ne soit écrite dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="b7014-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="b7014-105">Cette section contient des informations de référence pour les modificateurs d’instruction implémentés par le nuanceur de pixels version 2 \_ 0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b7014-105">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="b7014-106">Nom</span><span class="sxs-lookup"><span data-stu-id="b7014-106">Name</span></span>                                     | <span data-ttu-id="b7014-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7014-107">Syntax</span></span>     | <span data-ttu-id="b7014-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7014-108">2\_0</span></span> | <span data-ttu-id="b7014-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b7014-109">2\_x</span></span> | <span data-ttu-id="b7014-110">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b7014-110">2\_sw</span></span> | <span data-ttu-id="b7014-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7014-111">3\_0</span></span> | <span data-ttu-id="b7014-112">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b7014-112">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="b7014-113">Centroïde</span><span class="sxs-lookup"><span data-stu-id="b7014-113">Centroid</span></span>](#centroid)                    | <span data-ttu-id="b7014-114">\_centroïde</span><span class="sxs-lookup"><span data-stu-id="b7014-114">\_centroid</span></span> | <span data-ttu-id="b7014-115">x</span><span class="sxs-lookup"><span data-stu-id="b7014-115">x</span></span>    | <span data-ttu-id="b7014-116">x</span><span class="sxs-lookup"><span data-stu-id="b7014-116">x</span></span>    | <span data-ttu-id="b7014-117">x</span><span class="sxs-lookup"><span data-stu-id="b7014-117">x</span></span>     | <span data-ttu-id="b7014-118">x</span><span class="sxs-lookup"><span data-stu-id="b7014-118">x</span></span>    | <span data-ttu-id="b7014-119">x</span><span class="sxs-lookup"><span data-stu-id="b7014-119">x</span></span>     |
| [<span data-ttu-id="b7014-120">\_Précision partielle</span><span class="sxs-lookup"><span data-stu-id="b7014-120">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="b7014-121">\_p</span><span class="sxs-lookup"><span data-stu-id="b7014-121">\_pp</span></span>       | <span data-ttu-id="b7014-122">x</span><span class="sxs-lookup"><span data-stu-id="b7014-122">x</span></span>    | <span data-ttu-id="b7014-123">x</span><span class="sxs-lookup"><span data-stu-id="b7014-123">x</span></span>    | <span data-ttu-id="b7014-124">x</span><span class="sxs-lookup"><span data-stu-id="b7014-124">x</span></span>     | <span data-ttu-id="b7014-125">x</span><span class="sxs-lookup"><span data-stu-id="b7014-125">x</span></span>    | <span data-ttu-id="b7014-126">x</span><span class="sxs-lookup"><span data-stu-id="b7014-126">x</span></span>     |
| [<span data-ttu-id="b7014-127">Saturer</span><span class="sxs-lookup"><span data-stu-id="b7014-127">Saturate</span></span>](#saturate)                    | <span data-ttu-id="b7014-128">\_sot</span><span class="sxs-lookup"><span data-stu-id="b7014-128">\_sat</span></span>      | <span data-ttu-id="b7014-129">x</span><span class="sxs-lookup"><span data-stu-id="b7014-129">x</span></span>    | <span data-ttu-id="b7014-130">x</span><span class="sxs-lookup"><span data-stu-id="b7014-130">x</span></span>    | <span data-ttu-id="b7014-131">x</span><span class="sxs-lookup"><span data-stu-id="b7014-131">x</span></span>     | <span data-ttu-id="b7014-132">x</span><span class="sxs-lookup"><span data-stu-id="b7014-132">x</span></span>    | <span data-ttu-id="b7014-133">x</span><span class="sxs-lookup"><span data-stu-id="b7014-133">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="b7014-134">Centroïde</span><span class="sxs-lookup"><span data-stu-id="b7014-134">Centroid</span></span>

<span data-ttu-id="b7014-135">Le modificateur de centre de gravité est un modificateur facultatif qui fixe l’interpolation d’attribut dans la plage de la primitive quand un centre de pixels à plusieurs échantillons n’est pas couvert par la primitive.</span><span class="sxs-lookup"><span data-stu-id="b7014-135">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="b7014-136">Cela peut être observé dans l’échantillonnage de centre de [gravité](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="b7014-136">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="b7014-137">Vous pouvez appliquer le modificateur de centre de gravité à une instruction d’assembly comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="b7014-137">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="b7014-138">Vous pouvez également appliquer le modificateur de centre de gravité à une sémantique comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="b7014-138">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="b7014-139">De plus, tout [Registre de couleur d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) déclaré avec une sémantique de couleur aura automatiquement le niveau de gravité appliqué.</span><span class="sxs-lookup"><span data-stu-id="b7014-139">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="b7014-140">Il n’est pas garanti que les dégradés calculés à partir des attributs de centre de gravité de l’échantillonnage sont exacts.</span><span class="sxs-lookup"><span data-stu-id="b7014-140">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="b7014-141">Précision partielle</span><span class="sxs-lookup"><span data-stu-id="b7014-141">Partial Precision</span></span>

<span data-ttu-id="b7014-142">Le modificateur d’instruction de précision partielle ( \_ pp) indique les zones où la précision partielle est acceptable, à condition que l’implémentation sous-jacente la prenne en charge.</span><span class="sxs-lookup"><span data-stu-id="b7014-142">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="b7014-143">Les implémentations sont toujours gratuites pour ignorer le modificateur et effectuer les opérations affectées en toute précision.</span><span class="sxs-lookup"><span data-stu-id="b7014-143">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="b7014-144">Le \_ modificateur pp peut se produire dans deux contextes :</span><span class="sxs-lookup"><span data-stu-id="b7014-144">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="b7014-145">Sur une déclaration de coordonnée de texture pour permettre le passage de coordonnées de texture au nuanceur de pixels en forme de précision partielle.</span><span class="sxs-lookup"><span data-stu-id="b7014-145">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="b7014-146">Cela permet, par exemple, d’utiliser des coordonnées de texture pour transmettre des données de couleur au nuanceur de pixels, ce qui peut être plus rapide avec une précision partielle qu’avec une précision totale dans certaines implémentations.</span><span class="sxs-lookup"><span data-stu-id="b7014-146">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="b7014-147">En l’absence de ce modificateur, les coordonnées de texture doivent être passées en pleine précision.</span><span class="sxs-lookup"><span data-stu-id="b7014-147">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="b7014-148">Sur toute instruction, y compris les instructions de chargement de texture.</span><span class="sxs-lookup"><span data-stu-id="b7014-148">On any instruction including texture load instructions.</span></span> <span data-ttu-id="b7014-149">Cela indique que l’implémentation est autorisée à exécuter l’instruction avec une précision partielle et à stocker un résultat de précision partielle.</span><span class="sxs-lookup"><span data-stu-id="b7014-149">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="b7014-150">En l’absence d’un modificateur explicite, l’instruction doit être exécutée à la précision totale (quelle que soit la précision d’entrée).</span><span class="sxs-lookup"><span data-stu-id="b7014-150">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="b7014-151">Exemples :</span><span class="sxs-lookup"><span data-stu-id="b7014-151">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="b7014-152">Saturer :</span><span class="sxs-lookup"><span data-stu-id="b7014-152">Saturate</span></span>

<span data-ttu-id="b7014-153">Le modificateur d’instruction saturé ( \_ SAT) sature (ou bride) le résultat de l’instruction dans la plage \[ 0, 1 \] avant d’écrire dans le registre de destination.</span><span class="sxs-lookup"><span data-stu-id="b7014-153">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="b7014-154">Le \_ modificateur d’instruction SAT peut être utilisé avec n’importe quelle instruction, à l’exception [de FRC-PS](frc---ps.md), [SinCos,-PS](sincos---ps.md)et de toute instruction Tex \* .</span><span class="sxs-lookup"><span data-stu-id="b7014-154">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="b7014-155">Pour PS \_ 2 \_ 0, PS \_ 2 \_ x et PS \_ 2 \_ SW, le \_ modificateur d’instruction SAT ne peut pas être utilisé avec des instructions qui écrivent dans des registres de sortie (registre de[couleur de sortie](dx9-graphics-reference-asm-ps-registers-output-color.md) ou registre de [profondeur de sortie](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span><span class="sxs-lookup"><span data-stu-id="b7014-155">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="b7014-156">Cette restriction ne s’applique pas à PS \_ 3 \_ 0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b7014-156">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="b7014-157">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b7014-157">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="b7014-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7014-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7014-159">Instructions sur le nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="b7014-159">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




