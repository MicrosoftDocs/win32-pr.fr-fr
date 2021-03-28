---
title: Interface ID3DX11EffectTechnique (D3dx11effect. h)
description: Une interface ID3DX11EffectTechnique est une collection de passes. La durée de vie d’un objet ID3DX11EffectTechnique est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- Interface ID3DX11EffectTechnique Direct3D 11
- Interface ID3DX11EffectTechnique Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982538"
---
# <a name="id3dx11effecttechnique-interface"></a><span data-ttu-id="d4a56-105">Interface ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="d4a56-105">ID3DX11EffectTechnique interface</span></span>

<span data-ttu-id="d4a56-106">Une interface **ID3DX11EffectTechnique** est une collection de passes.</span><span class="sxs-lookup"><span data-stu-id="d4a56-106">An **ID3DX11EffectTechnique** interface is a collection of passes.</span></span>

<span data-ttu-id="d4a56-107">La durée de vie d’un objet **ID3DX11EffectTechnique** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.</span><span class="sxs-lookup"><span data-stu-id="d4a56-107">The lifetime of an **ID3DX11EffectTechnique** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="d4a56-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d4a56-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d4a56-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d4a56-109">Methods</span></span>

<span data-ttu-id="d4a56-110">L’interface **ID3DX11EffectTechnique** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d4a56-110">The **ID3DX11EffectTechnique** interface has these methods.</span></span>



| <span data-ttu-id="d4a56-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="d4a56-111">Method</span></span>                                                                        | <span data-ttu-id="d4a56-112">Description</span><span class="sxs-lookup"><span data-stu-id="d4a56-112">Description</span></span>                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="d4a56-113">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="d4a56-113">**ComputeStateBlockMask**</span></span>](id3dx11effecttechnique-computestateblockmask.md) | <span data-ttu-id="d4a56-114">Calculez un masque de bloc d’État pour autoriser ou empêcher les modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="d4a56-114">Compute a state-block mask to allow/prevent state changes.</span></span><br/> |
| [<span data-ttu-id="d4a56-115">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="d4a56-115">**GetAnnotationByIndex**</span></span>](id3dx11effecttechnique-getannotationbyindex.md)   | <span data-ttu-id="d4a56-116">Obtient une annotation par index.</span><span class="sxs-lookup"><span data-stu-id="d4a56-116">Get an annotation by index.</span></span><br/>                                |
| [<span data-ttu-id="d4a56-117">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="d4a56-117">**GetAnnotationByName**</span></span>](id3dx11effecttechnique-getannotationbyname.md)     | <span data-ttu-id="d4a56-118">Obtient une annotation par nom.</span><span class="sxs-lookup"><span data-stu-id="d4a56-118">Get an annotation by name.</span></span><br/>                                 |
| [<span data-ttu-id="d4a56-119">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="d4a56-119">**GetDesc**</span></span>](id3dx11effecttechnique-getdesc.md)                             | <span data-ttu-id="d4a56-120">Obtenir une description technique.</span><span class="sxs-lookup"><span data-stu-id="d4a56-120">Get a technique description.</span></span><br/>                               |
| [<span data-ttu-id="d4a56-121">**GetPassByIndex**</span><span class="sxs-lookup"><span data-stu-id="d4a56-121">**GetPassByIndex**</span></span>](id3dx11effecttechnique-getpassbyindex.md)               | <span data-ttu-id="d4a56-122">Obtenir un passage par index.</span><span class="sxs-lookup"><span data-stu-id="d4a56-122">Get a pass by index.</span></span><br/>                                       |
| [<span data-ttu-id="d4a56-123">**GetPassByName**</span><span class="sxs-lookup"><span data-stu-id="d4a56-123">**GetPassByName**</span></span>](id3dx11effecttechnique-getpassbyname.md)                 | <span data-ttu-id="d4a56-124">Obtenir un passage par nom.</span><span class="sxs-lookup"><span data-stu-id="d4a56-124">Get a pass by name.</span></span><br/>                                        |
| [<span data-ttu-id="d4a56-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="d4a56-125">**IsValid**</span></span>](id3dx11effecttechnique-isvalid.md)                             | <span data-ttu-id="d4a56-126">Testez une technique pour voir si elle contient une syntaxe valide.</span><span class="sxs-lookup"><span data-stu-id="d4a56-126">Test a technique to see if it contains valid syntax.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="d4a56-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d4a56-127">Remarks</span></span>

<span data-ttu-id="d4a56-128">Un effet contient une ou plusieurs techniques ; chaque technique contient une ou plusieurs passes ; chaque passe contient des attributions d’État.</span><span class="sxs-lookup"><span data-stu-id="d4a56-128">An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments.</span></span>

<span data-ttu-id="d4a56-129">Pour obtenir une interface d’action-technique, appelez une méthode telle que [**ID3DX11Effect :: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span><span class="sxs-lookup"><span data-stu-id="d4a56-129">To get an effect-technique interface, call a method such as [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="d4a56-130">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="d4a56-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d4a56-131">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="d4a56-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d4a56-132">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d4a56-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d4a56-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d4a56-133">Requirements</span></span>



| <span data-ttu-id="d4a56-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4a56-134">Requirement</span></span> | <span data-ttu-id="d4a56-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4a56-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a56-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4a56-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d4a56-137"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4a56-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d4a56-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4a56-138">Library</span></span><br/> | <dl> <span data-ttu-id="d4a56-139"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="d4a56-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a56-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4a56-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a56-141">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="d4a56-141">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d4a56-142">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d4a56-142">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





