---
title: Interface ID3DX11EffectVariable (D3dx11effect. h)
description: L’interface ID3DX11EffectVariable est la classe de base pour toutes les variables d’effet. La durée de vie d’un objet ID3DX11EffectVariable est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- Interface ID3DX11EffectVariable Direct3D 11
- Interface ID3DX11EffectVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762199"
---
# <a name="id3dx11effectvariable-interface"></a><span data-ttu-id="9397e-105">Interface ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="9397e-105">ID3DX11EffectVariable interface</span></span>

<span data-ttu-id="9397e-106">L’interface **ID3DX11EffectVariable** est la classe de base pour toutes les variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="9397e-106">The **ID3DX11EffectVariable** interface is the base class for all effect variables.</span></span>

<span data-ttu-id="9397e-107">La durée de vie d’un objet **ID3DX11EffectVariable** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.</span><span class="sxs-lookup"><span data-stu-id="9397e-107">The lifetime of an **ID3DX11EffectVariable** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="9397e-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9397e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9397e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9397e-109">Methods</span></span>

<span data-ttu-id="9397e-110">L’interface **ID3DX11EffectVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9397e-110">The **ID3DX11EffectVariable** interface has these methods.</span></span>



| <span data-ttu-id="9397e-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="9397e-111">Method</span></span>                                                                           | <span data-ttu-id="9397e-112">Description</span><span class="sxs-lookup"><span data-stu-id="9397e-112">Description</span></span>                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="9397e-113">**AsBlend**</span><span class="sxs-lookup"><span data-stu-id="9397e-113">**AsBlend**</span></span>](id3dx11effectvariable-asblend.md)                                 | <span data-ttu-id="9397e-114">Obtenir une variable Effect-Blend.</span><span class="sxs-lookup"><span data-stu-id="9397e-114">Get a effect-blend variable.</span></span><br/>                |
| [<span data-ttu-id="9397e-115">**AsClassInstance**</span><span class="sxs-lookup"><span data-stu-id="9397e-115">**AsClassInstance**</span></span>](id3dx11effectvariable-asclassinstance.md)                 | <span data-ttu-id="9397e-116">Obtenir une variable d’instance de classe.</span><span class="sxs-lookup"><span data-stu-id="9397e-116">Get a class-instance variable.</span></span><br/>              |
| [<span data-ttu-id="9397e-117">**AsConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="9397e-117">**AsConstantBuffer**</span></span>](id3dx11effectvariable-asconstantbuffer.md)               | <span data-ttu-id="9397e-118">Obtient une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="9397e-118">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="9397e-119">**AsDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="9397e-119">**AsDepthStencil**</span></span>](id3dx11effectvariable-asdepthstencil.md)                   | <span data-ttu-id="9397e-120">Obtenir une variable de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="9397e-120">Get a depth-stencil variable.</span></span><br/>               |
| [<span data-ttu-id="9397e-121">**AsDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="9397e-121">**AsDepthStencilView**</span></span>](id3dx11effectvariable-asdepthstencilview.md)           | <span data-ttu-id="9397e-122">Obtenir une variable de vue de gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="9397e-122">Get a depth-stencil-view variable.</span></span><br/>          |
| [<span data-ttu-id="9397e-123">**AsInterface**</span><span class="sxs-lookup"><span data-stu-id="9397e-123">**AsInterface**</span></span>](id3dx11effectvariable-asinterface.md)                         | <span data-ttu-id="9397e-124">Obtient une variable d’interface.</span><span class="sxs-lookup"><span data-stu-id="9397e-124">Get an interface variable.</span></span><br/>                  |
| [<span data-ttu-id="9397e-125">**AsMatrix**</span><span class="sxs-lookup"><span data-stu-id="9397e-125">**AsMatrix**</span></span>](id3dx11effectvariable-asmatrix.md)                               | <span data-ttu-id="9397e-126">Obtenir une variable de matrice.</span><span class="sxs-lookup"><span data-stu-id="9397e-126">Get a matrix variable.</span></span><br/>                      |
| [<span data-ttu-id="9397e-127">**AsRasterizer**</span><span class="sxs-lookup"><span data-stu-id="9397e-127">**AsRasterizer**</span></span>](id3dx11effectvariable-asrasterizer.md)                       | <span data-ttu-id="9397e-128">Obtenir une variable rastériseur.</span><span class="sxs-lookup"><span data-stu-id="9397e-128">Get a rasterizer variable.</span></span><br/>                  |
| [<span data-ttu-id="9397e-129">**AsRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="9397e-129">**AsRenderTargetView**</span></span>](id3dx11effectvariable-asrendertargetview.md)           | <span data-ttu-id="9397e-130">Obtenir une variable Render-Target-View.</span><span class="sxs-lookup"><span data-stu-id="9397e-130">Get a render-target-view variable.</span></span><br/>          |
| [<span data-ttu-id="9397e-131">**AsSampler**</span><span class="sxs-lookup"><span data-stu-id="9397e-131">**AsSampler**</span></span>](id3dx11effectvariable-assampler.md)                             | <span data-ttu-id="9397e-132">Obtenir une variable d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="9397e-132">Get a sampler variable.</span></span><br/>                     |
| [<span data-ttu-id="9397e-133">**AsScalar**</span><span class="sxs-lookup"><span data-stu-id="9397e-133">**AsScalar**</span></span>](id3dx11effectvariable-asscalar.md)                               | <span data-ttu-id="9397e-134">Obtenir une variable scalaire.</span><span class="sxs-lookup"><span data-stu-id="9397e-134">Get a scalar variable.</span></span><br/>                      |
| [<span data-ttu-id="9397e-135">**AsShader**</span><span class="sxs-lookup"><span data-stu-id="9397e-135">**AsShader**</span></span>](id3dx11effectvariable-asshader.md)                               | <span data-ttu-id="9397e-136">Obtenir une variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="9397e-136">Get a shader variable.</span></span><br/>                      |
| [<span data-ttu-id="9397e-137">**AsShaderResource**</span><span class="sxs-lookup"><span data-stu-id="9397e-137">**AsShaderResource**</span></span>](id3dx11effectvariable-asshaderresource.md)               | <span data-ttu-id="9397e-138">Obtenir une variable de nuanceur-ressource.</span><span class="sxs-lookup"><span data-stu-id="9397e-138">Get a shader-resource variable.</span></span><br/>             |
| [<span data-ttu-id="9397e-139">**AsString**</span><span class="sxs-lookup"><span data-stu-id="9397e-139">**AsString**</span></span>](id3dx11effectvariable-asstring.md)                               | <span data-ttu-id="9397e-140">Obtenir une variable de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9397e-140">Get a string variable.</span></span><br/>                      |
| [<span data-ttu-id="9397e-141">**AsUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="9397e-141">**AsUnorderedAccessView**</span></span>](id3dx11effectvariable-asunorderedaccessview.md)     | <span data-ttu-id="9397e-142">Obtenir une variable de vue d’accès non ordonnée.</span><span class="sxs-lookup"><span data-stu-id="9397e-142">Get an unordered-access-view variable.</span></span><br/>      |
| [<span data-ttu-id="9397e-143">**AsVector**</span><span class="sxs-lookup"><span data-stu-id="9397e-143">**AsVector**</span></span>](id3dx11effectvariable-asvector.md)                               | <span data-ttu-id="9397e-144">Obtenir une variable vectorielle.</span><span class="sxs-lookup"><span data-stu-id="9397e-144">Get a vector variable.</span></span><br/>                      |
| [<span data-ttu-id="9397e-145">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="9397e-145">**GetAnnotationByIndex**</span></span>](id3dx11effectvariable-getannotationbyindex.md)       | <span data-ttu-id="9397e-146">Obtient une annotation par index.</span><span class="sxs-lookup"><span data-stu-id="9397e-146">Get an annotation by index.</span></span><br/>                 |
| [<span data-ttu-id="9397e-147">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="9397e-147">**GetAnnotationByName**</span></span>](id3dx11effectvariable-getannotationbyname.md)         | <span data-ttu-id="9397e-148">Obtient une annotation par nom.</span><span class="sxs-lookup"><span data-stu-id="9397e-148">Get an annotation by name.</span></span><br/>                  |
| [<span data-ttu-id="9397e-149">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9397e-149">**GetDesc**</span></span>](id3dx11effectvariable-getdesc.md)                                 | <span data-ttu-id="9397e-150">Obtenir une description.</span><span class="sxs-lookup"><span data-stu-id="9397e-150">Get a description.</span></span><br/>                          |
| [<span data-ttu-id="9397e-151">**GetElement**</span><span class="sxs-lookup"><span data-stu-id="9397e-151">**GetElement**</span></span>](id3dx11effectvariable-getelement.md)                           | <span data-ttu-id="9397e-152">Obtient un élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="9397e-152">Get an array element.</span></span><br/>                       |
| [<span data-ttu-id="9397e-153">**GetMemberByIndex**</span><span class="sxs-lookup"><span data-stu-id="9397e-153">**GetMemberByIndex**</span></span>](id3dx11effectvariable-getmemberbyindex.md)               | <span data-ttu-id="9397e-154">Obtient un membre de structure par index.</span><span class="sxs-lookup"><span data-stu-id="9397e-154">Get a structure member by index.</span></span><br/>            |
| [<span data-ttu-id="9397e-155">**GetMemberByName**</span><span class="sxs-lookup"><span data-stu-id="9397e-155">**GetMemberByName**</span></span>](id3dx11effectvariable-getmemberbyname.md)                 | <span data-ttu-id="9397e-156">Obtient un membre de structure par nom.</span><span class="sxs-lookup"><span data-stu-id="9397e-156">Get a structure member by name.</span></span><br/>             |
| [<span data-ttu-id="9397e-157">**GetMemberBySemantic**</span><span class="sxs-lookup"><span data-stu-id="9397e-157">**GetMemberBySemantic**</span></span>](id3dx11effectvariable-getmemberbysemantic.md)         | <span data-ttu-id="9397e-158">Obtenir un membre de structure par sémantique.</span><span class="sxs-lookup"><span data-stu-id="9397e-158">Get a structure member by semantic.</span></span><br/>         |
| [<span data-ttu-id="9397e-159">**GetParentConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="9397e-159">**GetParentConstantBuffer**</span></span>](id3dx11effectvariable-getparentconstantbuffer.md) | <span data-ttu-id="9397e-160">Obtient une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="9397e-160">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="9397e-161">**GetRawValue**</span><span class="sxs-lookup"><span data-stu-id="9397e-161">**GetRawValue**</span></span>](id3dx11effectvariable-getrawvalue.md)                         | <span data-ttu-id="9397e-162">obtenir des données</span><span class="sxs-lookup"><span data-stu-id="9397e-162">Get data.</span></span><br/>                                   |
| [<span data-ttu-id="9397e-163">**GetType**</span><span class="sxs-lookup"><span data-stu-id="9397e-163">**GetType**</span></span>](id3dx11effectvariable-gettype.md)                                 | <span data-ttu-id="9397e-164">Obtient les informations de type.</span><span class="sxs-lookup"><span data-stu-id="9397e-164">Get type information.</span></span><br/>                       |
| [<span data-ttu-id="9397e-165">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="9397e-165">**IsValid**</span></span>](id3dx11effectvariable-isvalid.md)                                 | <span data-ttu-id="9397e-166">Comparez le type de données avec les données stockées.</span><span class="sxs-lookup"><span data-stu-id="9397e-166">Compare the data type with the data stored.</span></span><br/> |
| [<span data-ttu-id="9397e-167">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="9397e-167">**SetRawValue**</span></span>](id3dx11effectvariable-setrawvalue.md)                         | <span data-ttu-id="9397e-168">Définir des données.</span><span class="sxs-lookup"><span data-stu-id="9397e-168">Set data.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="9397e-169">Notes</span><span class="sxs-lookup"><span data-stu-id="9397e-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9397e-170">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="9397e-170">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9397e-171">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="9397e-171">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9397e-172">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9397e-172">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9397e-173">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9397e-173">Requirements</span></span>



| <span data-ttu-id="9397e-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9397e-174">Requirement</span></span> | <span data-ttu-id="9397e-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="9397e-175">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9397e-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="9397e-176">Header</span></span><br/>  | <dl> <span data-ttu-id="9397e-177"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9397e-177"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9397e-178">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9397e-178">Library</span></span><br/> | <dl> <span data-ttu-id="9397e-179"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="9397e-179"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9397e-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9397e-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9397e-181">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="9397e-181">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="9397e-182">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="9397e-182">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





