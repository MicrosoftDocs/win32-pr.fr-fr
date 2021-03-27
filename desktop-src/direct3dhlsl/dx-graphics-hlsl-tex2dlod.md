---
title: tex2Dlod
description: Échantillonne une texture 2D avec des mipmaps. Le LOD mipmap est spécifié dans t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- HLSL tex2Dlod
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971695"
---
# <a name="tex2dlod"></a><span data-ttu-id="603ea-105">tex2Dlod</span><span class="sxs-lookup"><span data-stu-id="603ea-105">tex2Dlod</span></span>

<span data-ttu-id="603ea-106">Échantillonne une texture 2D avec des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="603ea-106">Samples a 2D texture with mipmaps.</span></span> <span data-ttu-id="603ea-107">Le LOD mipmap est spécifié dans t.w.</span><span class="sxs-lookup"><span data-stu-id="603ea-107">The mipmap LOD is specified in t.w.</span></span>



| <span data-ttu-id="603ea-108">RET tex2Dlod (s, t)</span><span class="sxs-lookup"><span data-stu-id="603ea-108">ret tex2Dlod(s, t)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="603ea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="603ea-109">Parameters</span></span>



| <span data-ttu-id="603ea-110">Élément</span><span class="sxs-lookup"><span data-stu-id="603ea-110">Item</span></span>                                                   | <span data-ttu-id="603ea-111">Description</span><span class="sxs-lookup"><span data-stu-id="603ea-111">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="603ea-112"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="603ea-112"><span id="s"></span><span id="S"></span>*s*</span></span><br/> | <span data-ttu-id="603ea-113">\[dans \] l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="603ea-113">\[in\] The sampler state.</span></span><br/>      |
| <span data-ttu-id="603ea-114"><span id="t"></span><span id="T"></span>*t*</span><span class="sxs-lookup"><span data-stu-id="603ea-114"><span id="t"></span><span id="T"></span>*t*</span></span><br/> | <span data-ttu-id="603ea-115">\[dans \] la coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="603ea-115">\[in\] The texture coordinate.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="603ea-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="603ea-116">Return Value</span></span>

<span data-ttu-id="603ea-117">Valeur des données de texture.</span><span class="sxs-lookup"><span data-stu-id="603ea-117">The value of the texture data.</span></span>

## <a name="type-description"></a><span data-ttu-id="603ea-118">Description du type</span><span class="sxs-lookup"><span data-stu-id="603ea-118">Type Description</span></span>



| <span data-ttu-id="603ea-119">Nom</span><span class="sxs-lookup"><span data-stu-id="603ea-119">Name</span></span> | <span data-ttu-id="603ea-120">Entrée/Sortie</span><span class="sxs-lookup"><span data-stu-id="603ea-120">In/Out</span></span> | [<span data-ttu-id="603ea-121">**Type de modèle**</span><span class="sxs-lookup"><span data-stu-id="603ea-121">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="603ea-122">**Type de composant**</span><span class="sxs-lookup"><span data-stu-id="603ea-122">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="603ea-123">Taille</span><span class="sxs-lookup"><span data-stu-id="603ea-123">Size</span></span> |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="603ea-124">s</span><span class="sxs-lookup"><span data-stu-id="603ea-124">s</span></span>    | <span data-ttu-id="603ea-125">in</span><span class="sxs-lookup"><span data-stu-id="603ea-125">in</span></span>     | [<span data-ttu-id="603ea-126">**object**</span><span class="sxs-lookup"><span data-stu-id="603ea-126">**object**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="603ea-127">sampler2D</span><span class="sxs-lookup"><span data-stu-id="603ea-127">sampler2D</span></span>](dx-graphics-hlsl-sampler.md)                      | <span data-ttu-id="603ea-128">1</span><span class="sxs-lookup"><span data-stu-id="603ea-128">1</span></span>    |
| <span data-ttu-id="603ea-129">t</span><span class="sxs-lookup"><span data-stu-id="603ea-129">t</span></span>    | <span data-ttu-id="603ea-130">in</span><span class="sxs-lookup"><span data-stu-id="603ea-130">in</span></span>     | [<span data-ttu-id="603ea-131">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="603ea-131">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="603ea-132">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="603ea-132">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="603ea-133">4</span><span class="sxs-lookup"><span data-stu-id="603ea-133">4</span></span>    |
| <span data-ttu-id="603ea-134">Av</span><span class="sxs-lookup"><span data-stu-id="603ea-134">ret</span></span>  | <span data-ttu-id="603ea-135">out</span><span class="sxs-lookup"><span data-stu-id="603ea-135">out</span></span>    | [<span data-ttu-id="603ea-136">**graphiques**</span><span class="sxs-lookup"><span data-stu-id="603ea-136">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="603ea-137">**dissocié**</span><span class="sxs-lookup"><span data-stu-id="603ea-137">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="603ea-138">4</span><span class="sxs-lookup"><span data-stu-id="603ea-138">4</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="603ea-139">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="603ea-139">Minimum Shader Model</span></span>

<span data-ttu-id="603ea-140">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="603ea-140">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="603ea-141">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="603ea-141">Shader Model</span></span>                                                                       | <span data-ttu-id="603ea-142">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="603ea-142">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="603ea-143">[Nuancier modèle 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) et modèles de nuanceur plus élevés</span><span class="sxs-lookup"><span data-stu-id="603ea-143">[Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) and higher shader models</span></span> | <span data-ttu-id="603ea-144">Oui</span><span class="sxs-lookup"><span data-stu-id="603ea-144">yes</span></span>       |
| [<span data-ttu-id="603ea-145">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="603ea-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)                          | <span data-ttu-id="603ea-146">non</span><span class="sxs-lookup"><span data-stu-id="603ea-146">no</span></span>        |
| [<span data-ttu-id="603ea-147">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="603ea-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="603ea-148">non</span><span class="sxs-lookup"><span data-stu-id="603ea-148">no</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="603ea-149">Notes</span><span class="sxs-lookup"><span data-stu-id="603ea-149">Remarks</span></span>

<span data-ttu-id="603ea-150">À partir de Direct3D 10, vous pouvez utiliser la nouvelle syntaxe HLSL pour accéder aux textures et autres ressources.</span><span class="sxs-lookup"><span data-stu-id="603ea-150">Starting with Direct3D 10, you can use new HLSL syntax to access textures and other resources.</span></span> <span data-ttu-id="603ea-151">Vous pouvez remplacer les fonctions de recherche de texture de style intrinsèque, telles que **tex2Dlod**, par un style plus orienté objet.</span><span class="sxs-lookup"><span data-stu-id="603ea-151">You can replace intrinsic-style texture lookup functions, such as **tex2Dlod**, with a more object-oriented style.</span></span> <span data-ttu-id="603ea-152">Dans ce style orienté objet, les textures sont dissociées des échantillonneurs et ont des méthodes de chargement et d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="603ea-152">In this object-oriented style, textures are decoupled from samplers and have methods for loading and sampling.</span></span>

<span data-ttu-id="603ea-153">Pour échantillonner une texture 2D, au lieu d’utiliser **tex2Dlod** comme dans ce code :</span><span class="sxs-lookup"><span data-stu-id="603ea-153">To sample a 2D texture, instead of using **tex2Dlod** as in this code:</span></span>


```
sampler S;
...
color = tex2Dlod(S, Location);
```



<span data-ttu-id="603ea-154">Utilisez la méthode [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) d’un [**objet texture**](dx-graphics-hlsl-to-type.md) comme dans ce code :</span><span class="sxs-lookup"><span data-stu-id="603ea-154">Use the [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) method of a [**Texture Object**](dx-graphics-hlsl-to-type.md) as in this code:</span></span>


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



<span data-ttu-id="603ea-155">Pour utiliser les fonctions de recherche de texture de style intrinsèque, telles que **tex2Dlod**, avec le [nuanceur modèle 4](dx-graphics-hlsl-sm4.md) et versions ultérieures, utilisez [**D3DCOMPILE \_ activer la \_ \_ compatibilité descendante**](d3dcompile-constants.md) pour la compilation.</span><span class="sxs-lookup"><span data-stu-id="603ea-155">To use the intrinsic-style texture lookup functions, such as **tex2Dlod**, with [shader model 4](dx-graphics-hlsl-sm4.md) and higher, use [**D3DCOMPILE\_ENABLE\_BACKWARDS\_COMPATIBILITY**](d3dcompile-constants.md) to compile.</span></span> <span data-ttu-id="603ea-156">Toutefois, si vous souhaitez cibler le modèle de nuanceur 4 et les versions ultérieures (même [ \* \_ 4 \_ 0 \_ niveau \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) avec un code de style orienté objet plus récent, migrez vers la syntaxe HLSL la plus récente.</span><span class="sxs-lookup"><span data-stu-id="603ea-156">However, if you want to target shader model 4 and higher (even [\*\_4\_0\_level\_9\_\*](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) with newer object-oriented style code, migrate to the newer HLSL syntax.</span></span>

## <a name="see-also"></a><span data-ttu-id="603ea-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603ea-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603ea-158">**Fonctions intrinsèques (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="603ea-158">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

