---
title: Type struct
description: Type struct
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Type struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104990676"
---
# <a name="struct-type"></a><span data-ttu-id="1554f-104">Type struct</span><span class="sxs-lookup"><span data-stu-id="1554f-104">Struct Type</span></span>

<span data-ttu-id="1554f-105">Utilisez la syntaxe suivante pour déclarer une structure à l’aide du langage HLSL.</span><span class="sxs-lookup"><span data-stu-id="1554f-105">Use the following syntax to declare a structure using HLSL.</span></span>



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1554f-106">*nom* du struct { \[ *InterpolationModifier* \] *type* \[ *R* x *C* \] *MemberName*;     ... };</span><span class="sxs-lookup"><span data-stu-id="1554f-106">struct *Name*{     \[*InterpolationModifier*\] *Type*\[*R* x *C*\] *MemberName*;     ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="1554f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1554f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1554f-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*</span><span class="sxs-lookup"><span data-stu-id="1554f-108"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="1554f-109">Chaîne ASCII qui identifie de façon unique le nom de la structure.</span><span class="sxs-lookup"><span data-stu-id="1554f-109">An ASCII string that uniquely identifies the structure name.</span></span>

</dd> <dt>

<span data-ttu-id="1554f-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span><span class="sxs-lookup"><span data-stu-id="1554f-110"><span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]</span></span>
</dt> <dd>

<span data-ttu-id="1554f-111">Modificateur facultatif qui spécifie un type d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="1554f-111">Optional modifier that specifies an interpolation type.</span></span> <span data-ttu-id="1554f-112">Pour plus d’informations, consultez [Remarques](#remarks).</span><span class="sxs-lookup"><span data-stu-id="1554f-112">See [Remarks](#remarks) for details.</span></span>

</dd> <dt>

<span data-ttu-id="1554f-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type* \[ *R* x *C*\]</span><span class="sxs-lookup"><span data-stu-id="1554f-113"><span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Type*\[*R* x *C*\]</span></span>
</dt> <dd>

<span data-ttu-id="1554f-114">Type de membre avec une taille de tableau de colonne (C) x de *ligne (\*\*C*) facultative.</span><span class="sxs-lookup"><span data-stu-id="1554f-114">The member type with an optional row (*R*) x column (*C*) array size.</span></span> <span data-ttu-id="1554f-115">Une structure contient au moins un élément ; s’il contient plus d’un élément, les éléments sont tous du même type.</span><span class="sxs-lookup"><span data-stu-id="1554f-115">A structure contains at least one element; if it contains more than one element, the elements are all of the same type.</span></span> <span data-ttu-id="1554f-116">Le nombre de lignes et de colonnes est un entier non signé compris entre 1 et 4 inclus.</span><span class="sxs-lookup"><span data-stu-id="1554f-116">The number of rows and columns are unsigned integers between 1 and 4 inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="1554f-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span><span class="sxs-lookup"><span data-stu-id="1554f-117"><span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*</span></span>
</dt> <dd>

<span data-ttu-id="1554f-118">Chaîne ASCII qui identifie de façon unique le nom du membre.</span><span class="sxs-lookup"><span data-stu-id="1554f-118">An ASCII string that uniquely identifies the member name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1554f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="1554f-119">Remarks</span></span>

<span data-ttu-id="1554f-120">Un modificateur d’interpolation peut être spécifié sur n’importe quel membre de structure ou sur un argument d’une fonction de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="1554f-120">An interpolation modifier can be specified on any structure member or on an argument to a pixel shader function.</span></span> <span data-ttu-id="1554f-121">Si un modificateur apparaît aux deux emplacements, le modificateur outside (modificateur d’argument de nuanceur de pixels) est en cours de la même façon que le modificateur interne (modificateur de structure).</span><span class="sxs-lookup"><span data-stu-id="1554f-121">If a modifier appears in both places, the outside modifier (the pixel shader argument modifier) overrules the inside modifier (the structure modifier).</span></span>

<span data-ttu-id="1554f-122">Lors de la compilation d’un nuanceur ou d’un effet, le compilateur de nuanceur compresse les membres de structure conformément aux [règles de compression HLSL](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="1554f-122">When compiling a shader or an effect, the shader compiler packs structure members according to [HLSL packing rules](dx-graphics-hlsl-packing-rules.md).</span></span>

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a><span data-ttu-id="1554f-123">Modificateurs d’interpolation introduits dans le Shader Model 4</span><span class="sxs-lookup"><span data-stu-id="1554f-123">Interpolation Modifiers Introduced in Shader Model 4</span></span>

<span data-ttu-id="1554f-124">Les sorties de nuanceur de sommets utilisées pour les entrées de nuanceur de pixels sont interpolées de manière linéaire pour obtenir des valeurs par pixel pendant la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="1554f-124">Vertex shader outputs that are used for pixel shader inputs are linearly interpolated to get per-pixel values during rasterization.</span></span> <span data-ttu-id="1554f-125">Pour définir la méthode d’interpolation, utilisez l’une des valeurs suivantes, qui sont prises en charge dans le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1554f-125">To set the method of interpolation, use any of the following values, which are supported in [shader model 4](dx-graphics-hlsl-sm4.md) or later.</span></span> <span data-ttu-id="1554f-126">Le modificateur est ignoré sur toute sortie de nuanceur de vertex qui n’est pas utilisée comme entrée de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="1554f-126">The modifier is ignored on any vertex shader output that is not used as a pixel shader input.</span></span>



| <span data-ttu-id="1554f-127">Modificateur d’interpolation</span><span class="sxs-lookup"><span data-stu-id="1554f-127">Interpolation Modifier</span></span> | <span data-ttu-id="1554f-128">Description</span><span class="sxs-lookup"><span data-stu-id="1554f-128">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1554f-129">**proportionnelle**</span><span class="sxs-lookup"><span data-stu-id="1554f-129">**linear**</span></span>             | <span data-ttu-id="1554f-130">Interpoler entre les entrées de nuanceur ; **linéaire** est la valeur par défaut si aucun modificateur d’interpolation n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="1554f-130">Interpolate between shader inputs; **linear** is the default value if no interpolation modifier is specified.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="1554f-131">**centroïde**</span><span class="sxs-lookup"><span data-stu-id="1554f-131">**centroid**</span></span>           | <span data-ttu-id="1554f-132">Interpoler entre des échantillons situés quelque part dans la zone couverte du pixel (cela peut nécessiter l’extrapolation des points de terminaison à partir d’un centre de pixels).</span><span class="sxs-lookup"><span data-stu-id="1554f-132">Interpolate between samples that are somewhere within the covered area of the pixel (this may require extrapolating end points from a pixel center).</span></span> <span data-ttu-id="1554f-133">L’échantillonnage de centre de gravité peut améliorer l’anticrénelage si un pixel est partiellement couvert (même si le centre de pixels n’est pas couvert).</span><span class="sxs-lookup"><span data-stu-id="1554f-133">Centroid sampling may improve antialiasing if a pixel is partially covered (even if the pixel center is not covered).</span></span> <span data-ttu-id="1554f-134">Le modificateur de centre de **gravité** doit être combiné avec le modificateur **Linear** ou **noperspective** .</span><span class="sxs-lookup"><span data-stu-id="1554f-134">The **centroid** modifier must be combined with either the **linear** or **noperspective** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1554f-135">**nointerpolation**</span><span class="sxs-lookup"><span data-stu-id="1554f-135">**nointerpolation**</span></span>    | <span data-ttu-id="1554f-136">Ne pas interpoler.</span><span class="sxs-lookup"><span data-stu-id="1554f-136">Do not interpolate .</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="1554f-137">**noperspective**</span><span class="sxs-lookup"><span data-stu-id="1554f-137">**noperspective**</span></span>      | <span data-ttu-id="1554f-138">N’effectuez pas de correction de perspective pendant l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="1554f-138">Do not perform perspective-correction during interpolation.</span></span> <span data-ttu-id="1554f-139">Le modificateur **noperspective** peut être combiné avec le modificateur de centre de **gravité** .</span><span class="sxs-lookup"><span data-stu-id="1554f-139">The **noperspective** modifier can be combined with the **centroid** modifier.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1554f-140">**exemple**</span><span class="sxs-lookup"><span data-stu-id="1554f-140">**sample**</span></span>             | <span data-ttu-id="1554f-141">**Disponible dans le modèle de nuanceur 4,1 et versions ultérieures** Interpoler à l’emplacement de l’échantillon plutôt qu’au centre de pixels.</span><span class="sxs-lookup"><span data-stu-id="1554f-141">**Available in shader model 4.1 and later** Interpolate at sample location rather than at the pixel center.</span></span> <span data-ttu-id="1554f-142">Le nuanceur de pixels s’exécute par exemple plutôt que par pixel.</span><span class="sxs-lookup"><span data-stu-id="1554f-142">This causes the pixel shader to execute per-sample rather than per-pixel.</span></span> <span data-ttu-id="1554f-143">Une autre façon d’effectuer une exécution par exemple consiste à avoir une entrée avec la valeur [sémantique SV \_ SampleIndex](dx-graphics-hlsl-semantics.md), qui indique l’exemple actuel.</span><span class="sxs-lookup"><span data-stu-id="1554f-143">Another way to cause per-sample execution is to have an input with [semantic SV\_SampleIndex](dx-graphics-hlsl-semantics.md), which indicates the current sample.</span></span> <span data-ttu-id="1554f-144">Seules les entrées avec l' **échantillon** spécifié (ou l’entrée de SV \_ SampleIndex) diffèrent entre les appels de nuanceur du pixel, alors que d’autres entrées qui ne spécifient pas de modificateurs (par exemple, si vous mélangez des modificateurs sur des entrées différentes) sont toujours interpolées au centre de pixels.</span><span class="sxs-lookup"><span data-stu-id="1554f-144">Only the inputs with **sample** specified (or inputting SV\_SampleIndex) differ between shader invocations in the pixel, whereas other inputs that do not specify modifiers (for example, if you mix modifiers on different inputs) still interpolate at the pixel center.</span></span> <span data-ttu-id="1554f-145">L’appel de nuanceur de pixels et le test de profondeur/stencil se produisent pour chaque échantillon couvert dans le pixel.</span><span class="sxs-lookup"><span data-stu-id="1554f-145">Both pixel shader invocation and depth/stencil testing occur for every covered sample in the pixel.</span></span> <span data-ttu-id="1554f-146">Cela est parfois appelé *superéchantillonnage*.</span><span class="sxs-lookup"><span data-stu-id="1554f-146">This is sometimes known as *supersampling*.</span></span> <span data-ttu-id="1554f-147">En revanche, en l’absence d’un exemple d’appel de fréquence, connu sous le nom d' *échantillonnage multiple*, le nuanceur de pixels est appelé une fois par pixel, quel que soit le nombre d’échantillons couverts, tandis que le test de profondeur/stencil se produit à la fréquence d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="1554f-147">In contrast, in the absence of sample frequency invocation, known as *multisampling*, the pixel shader is invoked once per pixel regardless of how many samples are covered, while depth/stencil testing occurs at sample frequency.</span></span> <span data-ttu-id="1554f-148">Les deux modes offrent un anticrénelage de bord équivalent.</span><span class="sxs-lookup"><span data-stu-id="1554f-148">Both modes provide equivalent edge antialiasing.</span></span> <span data-ttu-id="1554f-149">Toutefois, le superéchantillonnage offre une meilleure qualité d’ombrage en invoquant le nuanceur de pixels plus fréquemment.</span><span class="sxs-lookup"><span data-stu-id="1554f-149">However, supersampling provides better shading quality by invoking the pixel shader more frequently.</span></span><br/> |



 

<dl> <span data-ttu-id="1554f-150">1. En cas d’utilisation d’un type int/uint, la seule option valide est **nointerpolation**.</span><span class="sxs-lookup"><span data-stu-id="1554f-150">1. When using an int/uint type, the only valid option is **nointerpolation**.</span></span>  
</dl>

<span data-ttu-id="1554f-151">Les modificateurs d’interpolation peuvent être appliqués à des membres de structure ou à des [arguments de fonction](dx-graphics-hlsl-function-parameters.md), ou les deux.</span><span class="sxs-lookup"><span data-stu-id="1554f-151">Interpolation modifiers can be applied to structure members or [function arguments](dx-graphics-hlsl-function-parameters.md), or both.</span></span>

## <a name="examples"></a><span data-ttu-id="1554f-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="1554f-152">Examples</span></span>

<span data-ttu-id="1554f-153">Voici quelques exemples de déclarations de structure.</span><span class="sxs-lookup"><span data-stu-id="1554f-153">Here are some example structure declarations.</span></span>


```
struct struct1
{
  int    a;
}
```



<span data-ttu-id="1554f-154">Cette déclaration comprend un tableau.</span><span class="sxs-lookup"><span data-stu-id="1554f-154">This declaration includes an array.</span></span>


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



<span data-ttu-id="1554f-155">Cette déclaration comprend un modificateur d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="1554f-155">This declaration includes an interpolation modifier.</span></span>


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a><span data-ttu-id="1554f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1554f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1554f-157">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1554f-157">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





