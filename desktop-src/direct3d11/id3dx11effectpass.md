---
title: Interface ID3DX11EffectPass (D3dx11effect. h)
description: Une interface ID3DX11EffectPass encapsule les assignations d’État au sein d’une technique. La durée de vie d’un objet ID3DX11EffectPass est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- Interface ID3DX11EffectPass Direct3D 11
- Interface ID3DX11EffectPass Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211896"
---
# <a name="id3dx11effectpass-interface"></a><span data-ttu-id="2c29d-105">Interface ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="2c29d-105">ID3DX11EffectPass interface</span></span>

<span data-ttu-id="2c29d-106">Une interface **ID3DX11EffectPass** encapsule les assignations d’État au sein d’une technique.</span><span class="sxs-lookup"><span data-stu-id="2c29d-106">An **ID3DX11EffectPass** interface encapsulates state assignments within a technique.</span></span>

<span data-ttu-id="2c29d-107">La durée de vie d’un objet **ID3DX11EffectPass** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.</span><span class="sxs-lookup"><span data-stu-id="2c29d-107">The lifetime of an **ID3DX11EffectPass** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="2c29d-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2c29d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2c29d-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2c29d-109">Methods</span></span>

<span data-ttu-id="2c29d-110">L’interface **ID3DX11EffectPass** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2c29d-110">The **ID3DX11EffectPass** interface has these methods.</span></span>



| <span data-ttu-id="2c29d-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="2c29d-111">Method</span></span>                                                                   | <span data-ttu-id="2c29d-112">Description</span><span class="sxs-lookup"><span data-stu-id="2c29d-112">Description</span></span>                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="2c29d-113">**Appliquer**</span><span class="sxs-lookup"><span data-stu-id="2c29d-113">**Apply**</span></span>](id3dx11effectpass-apply.md)                                 | <span data-ttu-id="2c29d-114">Définit l’État contenu dans un passage à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2c29d-114">Set the state contained in a pass to the device.</span></span><br/>       |
| [<span data-ttu-id="2c29d-115">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="2c29d-115">**ComputeStateBlockMask**</span></span>](id3dx11effectpass-computestateblockmask.md) | <span data-ttu-id="2c29d-116">Générez un masque pour autoriser ou empêcher les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="2c29d-116">Generate a mask for allowing/preventing state changes.</span></span><br/> |
| [<span data-ttu-id="2c29d-117">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="2c29d-117">**GetAnnotationByIndex**</span></span>](id3dx11effectpass-getannotationbyindex.md)   | <span data-ttu-id="2c29d-118">Obtient une annotation par index.</span><span class="sxs-lookup"><span data-stu-id="2c29d-118">Get an annotation by index.</span></span><br/>                            |
| [<span data-ttu-id="2c29d-119">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="2c29d-119">**GetAnnotationByName**</span></span>](id3dx11effectpass-getannotationbyname.md)     | <span data-ttu-id="2c29d-120">Obtient une annotation par nom.</span><span class="sxs-lookup"><span data-stu-id="2c29d-120">Get an annotation by name.</span></span><br/>                             |
| [<span data-ttu-id="2c29d-121">**GetComputeShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="2c29d-121">**GetComputeShaderDesc**</span></span>](id3dx11effectpass-getcomputeshaderdesc.md)   | <span data-ttu-id="2c29d-122">Obtenir une description du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="2c29d-122">Get a compute-shader description.</span></span><br/>                      |
| [<span data-ttu-id="2c29d-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="2c29d-123">**GetDesc**</span></span>](id3dx11effectpass-getdesc.md)                             | <span data-ttu-id="2c29d-124">Obtenir une description du passage.</span><span class="sxs-lookup"><span data-stu-id="2c29d-124">Get a pass description.</span></span><br/>                                |
| [<span data-ttu-id="2c29d-125">**GetDomainShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="2c29d-125">**GetDomainShaderDesc**</span></span>](id3dx11effectpass-getdomainshaderdesc.md)     | <span data-ttu-id="2c29d-126">Obtenir une description du nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="2c29d-126">Get a domain-shader description.</span></span><br/>                       |
| [<span data-ttu-id="2c29d-127">**GetGeometryShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="2c29d-127">**GetGeometryShaderDesc**</span></span>](id3dx11effectpass-getgeometryshaderdesc.md) | <span data-ttu-id="2c29d-128">Obtient une géométrie-Description du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="2c29d-128">Get a geometry-shader description.</span></span><br/>                     |
| [<span data-ttu-id="2c29d-129">**GetHullShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="2c29d-129">**GetHullShaderDesc**</span></span>](id3dx11effectpass-gethullshaderdesc.md)         | <span data-ttu-id="2c29d-130">Obtient la description de la coque-Shader.</span><span class="sxs-lookup"><span data-stu-id="2c29d-130">Get hull-shader description.</span></span><br/>                           |
| [<span data-ttu-id="2c29d-131">**GetPixelShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="2c29d-131">**GetPixelShaderDesc**</span></span>](id3dx11effectpass-getpixelshaderdesc.md)       | <span data-ttu-id="2c29d-132">Obtenir une description de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="2c29d-132">Get a pixel-shader description.</span></span><br/>                        |
| [<span data-ttu-id="2c29d-133">**GetVertexShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="2c29d-133">**GetVertexShaderDesc**</span></span>](id3dx11effectpass-getvertexshaderdesc.md)     | <span data-ttu-id="2c29d-134">Obtenir une description du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="2c29d-134">Get a vertex-shader description.</span></span><br/>                       |
| [<span data-ttu-id="2c29d-135">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="2c29d-135">**IsValid**</span></span>](id3dx11effectpass-isvalid.md)                             | <span data-ttu-id="2c29d-136">Testez un passage pour voir s’il contient une syntaxe valide.</span><span class="sxs-lookup"><span data-stu-id="2c29d-136">Test a pass to see if it contains valid syntax.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="2c29d-137">Notes</span><span class="sxs-lookup"><span data-stu-id="2c29d-137">Remarks</span></span>

<span data-ttu-id="2c29d-138">Une passe est un bloc de code qui définit des objets d’état de rendu et des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="2c29d-138">A pass is a block of code that sets render-state objects and shaders.</span></span> <span data-ttu-id="2c29d-139">Une passe est déclarée au sein d’une technique.</span><span class="sxs-lookup"><span data-stu-id="2c29d-139">A pass is declared within a technique.</span></span>

<span data-ttu-id="2c29d-140">Pour obtenir une interface Effect-Pass, appelez une méthode comme [**ID3DX11EffectTechnique :: GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span><span class="sxs-lookup"><span data-stu-id="2c29d-140">To get an effect-pass interface, call a method like [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="2c29d-141">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="2c29d-141">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2c29d-142">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="2c29d-142">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2c29d-143">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2c29d-143">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c29d-144">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2c29d-144">Requirements</span></span>



| <span data-ttu-id="2c29d-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c29d-145">Requirement</span></span> | <span data-ttu-id="2c29d-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c29d-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c29d-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c29d-147">Header</span></span><br/>  | <dl> <span data-ttu-id="2c29d-148"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c29d-148"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2c29d-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c29d-149">Library</span></span><br/> | <dl> <span data-ttu-id="2c29d-150"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="2c29d-150"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c29d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c29d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c29d-152">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="2c29d-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2c29d-153">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2c29d-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





