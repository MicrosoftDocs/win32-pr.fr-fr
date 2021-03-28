---
title: Interface ID3DX11EffectShaderVariable (D3dx11effect. h)
description: Une interface de variable de nuanceur accède à une variable de nuanceur.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Interface ID3DX11EffectShaderVariable Direct3D 11
- Interface ID3DX11EffectShaderVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992221"
---
# <a name="id3dx11effectshadervariable-interface"></a><span data-ttu-id="28de6-105">Interface ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="28de6-105">ID3DX11EffectShaderVariable interface</span></span>

<span data-ttu-id="28de6-106">Une interface de variable de nuanceur accède à une variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="28de6-106">A shader-variable interface accesses a shader variable.</span></span>

## <a name="members"></a><span data-ttu-id="28de6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="28de6-107">Members</span></span>

<span data-ttu-id="28de6-108">L’interface **ID3DX11EffectShaderVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="28de6-108">The **ID3DX11EffectShaderVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="28de6-109">**ID3DX11EffectShaderVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="28de6-109">**ID3DX11EffectShaderVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="28de6-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="28de6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="28de6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="28de6-111">Methods</span></span>

<span data-ttu-id="28de6-112">L’interface **ID3DX11EffectShaderVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="28de6-112">The **ID3DX11EffectShaderVariable** interface has these methods.</span></span>



| <span data-ttu-id="28de6-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="28de6-113">Method</span></span>                                                                                                           | <span data-ttu-id="28de6-114">Description</span><span class="sxs-lookup"><span data-stu-id="28de6-114">Description</span></span>                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="28de6-115">**GetComputeShader**</span><span class="sxs-lookup"><span data-stu-id="28de6-115">**GetComputeShader**</span></span>](id3dx11effectshadervariable-getcomputeshader.md)                                         | <span data-ttu-id="28de6-116">Obtenir un nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="28de6-116">Get a compute shader.</span></span><br/>                       |
| [<span data-ttu-id="28de6-117">**GetDomainShader**</span><span class="sxs-lookup"><span data-stu-id="28de6-117">**GetDomainShader**</span></span>](id3dx11effectshadervariable-getdomainshader.md)                                           | <span data-ttu-id="28de6-118">Obtenir un nuanceur de domaine.</span><span class="sxs-lookup"><span data-stu-id="28de6-118">Get a domain shader.</span></span><br/>                        |
| [<span data-ttu-id="28de6-119">**GetGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="28de6-119">**GetGeometryShader**</span></span>](id3dx11effectshadervariable-getgeometryshader.md)                                       | <span data-ttu-id="28de6-120">Obtenir un nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="28de6-120">Get a geometry shader.</span></span><br/>                      |
| [<span data-ttu-id="28de6-121">**GetHullShader**</span><span class="sxs-lookup"><span data-stu-id="28de6-121">**GetHullShader**</span></span>](id3dx11effectshadervariable-gethullshader.md)                                               | <span data-ttu-id="28de6-122">Obtenir un nuanceur de coque.</span><span class="sxs-lookup"><span data-stu-id="28de6-122">Get a hull shader.</span></span><br/>                          |
| [<span data-ttu-id="28de6-123">**GetInputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="28de6-123">**GetInputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | <span data-ttu-id="28de6-124">Obtient une description de la signature d’entrée.</span><span class="sxs-lookup"><span data-stu-id="28de6-124">Get an input-signature description.</span></span><br/>         |
| [<span data-ttu-id="28de6-125">**GetOutputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="28de6-125">**GetOutputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | <span data-ttu-id="28de6-126">Obtient une description de la signature de sortie.</span><span class="sxs-lookup"><span data-stu-id="28de6-126">Get an output-signature description.</span></span><br/>        |
| [<span data-ttu-id="28de6-127">**GetPatchConstantSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="28de6-127">**GetPatchConstantSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | <span data-ttu-id="28de6-128">Obtenir une description de la signature constante de patch.</span><span class="sxs-lookup"><span data-stu-id="28de6-128">Get a patch constant signature description.</span></span><br/> |
| [<span data-ttu-id="28de6-129">**GetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="28de6-129">**GetPixelShader**</span></span>](id3dx11effectshadervariable-getpixelshader.md)                                             | <span data-ttu-id="28de6-130">Obtenir un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="28de6-130">Get a pixel shader.</span></span><br/>                         |
| [<span data-ttu-id="28de6-131">**GetShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="28de6-131">**GetShaderDesc**</span></span>](id3dx11effectshadervariable-getshaderdesc.md)                                               | <span data-ttu-id="28de6-132">Obtenir une description du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="28de6-132">Get a shader description.</span></span><br/>                   |
| [<span data-ttu-id="28de6-133">**GetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="28de6-133">**GetVertexShader**</span></span>](id3dx11effectshadervariable-getvertexshader.md)                                           | <span data-ttu-id="28de6-134">Obtenir un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="28de6-134">Get a vertex shader.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="28de6-135">Notes</span><span class="sxs-lookup"><span data-stu-id="28de6-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="28de6-136">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="28de6-136">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="28de6-137">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="28de6-137">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="28de6-138">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="28de6-138">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="28de6-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="28de6-139">Requirements</span></span>



| <span data-ttu-id="28de6-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28de6-140">Requirement</span></span> | <span data-ttu-id="28de6-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="28de6-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28de6-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="28de6-142">Header</span></span><br/>  | <dl> <span data-ttu-id="28de6-143"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="28de6-143"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="28de6-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="28de6-144">Library</span></span><br/> | <dl> <span data-ttu-id="28de6-145"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="28de6-145"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28de6-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28de6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28de6-147">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="28de6-147">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="28de6-148">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="28de6-148">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="28de6-149">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="28de6-149">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





