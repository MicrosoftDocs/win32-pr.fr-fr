---
title: Interface ID3DX11EffectGroup (D3dx11effect. h)
description: L’interface ID3DX11EffectGroup accède à un groupe d’effets. La durée de vie d’un objet ID3DX11EffectGroup est égale à la durée de vie de son objet ID3DX11Effect parent.
ms.assetid: f5a35c47-0bac-4559-bd6c-5e8bc7699e10
keywords:
- Interface ID3DX11EffectGroup Direct3D 11
- Interface ID3DX11EffectGroup Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5970506b850d164a4018cd371e19bfab6cd3624
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974563"
---
# <a name="id3dx11effectgroup-interface"></a><span data-ttu-id="0fd0e-105">Interface ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="0fd0e-105">ID3DX11EffectGroup interface</span></span>

<span data-ttu-id="0fd0e-106">L’interface **ID3DX11EffectGroup** accède à un groupe d’effets.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-106">The **ID3DX11EffectGroup** interface accesses an Effect group.</span></span>

<span data-ttu-id="0fd0e-107">La durée de vie d’un objet **ID3DX11EffectGroup** est égale à la durée de vie de son objet [**ID3DX11Effect**](id3dx11effect.md) parent.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-107">The lifetime of an **ID3DX11EffectGroup** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="0fd0e-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0fd0e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0fd0e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0fd0e-109">Methods</span></span>

<span data-ttu-id="0fd0e-110">L’interface **ID3DX11EffectGroup** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-110">The **ID3DX11EffectGroup** interface has these methods.</span></span>



| <span data-ttu-id="0fd0e-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="0fd0e-111">Method</span></span>                                                                  | <span data-ttu-id="0fd0e-112">Description</span><span class="sxs-lookup"><span data-stu-id="0fd0e-112">Description</span></span>                                                   |
|:------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="0fd0e-113">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="0fd0e-113">**GetAnnotationByIndex**</span></span>](id3dx11effectgroup-getannotationbyindex.md) | <span data-ttu-id="0fd0e-114">Obtient une annotation par index.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-114">Get an annotation by index.</span></span><br/>                        |
| [<span data-ttu-id="0fd0e-115">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="0fd0e-115">**GetAnnotationByName**</span></span>](id3dx11effectgroup-getannotationbyname.md)   | <span data-ttu-id="0fd0e-116">Obtient une annotation par nom.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-116">Get an annotation by name.</span></span><br/>                         |
| [<span data-ttu-id="0fd0e-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="0fd0e-117">**GetDesc**</span></span>](id3dx11effectgroup-getdesc.md)                           | <span data-ttu-id="0fd0e-118">Obtient une description de groupe.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-118">Gets a group description.</span></span><br/>                          |
| [<span data-ttu-id="0fd0e-119">**GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="0fd0e-119">**GetTechniqueByIndex**</span></span>](id3dx11effectgroup-gettechniquebyindex.md)   | <span data-ttu-id="0fd0e-120">Obtient une technique par index.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-120">Get a technique by index.</span></span><br/>                          |
| [<span data-ttu-id="0fd0e-121">**GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="0fd0e-121">**GetTechniqueByName**</span></span>](id3dx11effectgroup-gettechniquebyname.md)     | <span data-ttu-id="0fd0e-122">Obtient une technique par nom.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-122">Get a technique by name.</span></span><br/>                           |
| [<span data-ttu-id="0fd0e-123">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="0fd0e-123">**IsValid**</span></span>](id3dx11effectgroup-isvalid.md)                           | <span data-ttu-id="0fd0e-124">Testez un effet pour voir s’il contient une syntaxe valide.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-124">Test an effect to see if it contains valid syntax.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0fd0e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0fd0e-125">Remarks</span></span>

<span data-ttu-id="0fd0e-126">Pour obtenir une interface **ID3DX11EffectGroup** , appelez une méthode comme [**ID3DX11Effect :: GetGroupByName**](id3dx11effect-getgroupbyname.md).</span><span class="sxs-lookup"><span data-stu-id="0fd0e-126">To get an **ID3DX11EffectGroup** interface, call a method like [**ID3DX11Effect::GetGroupByName**](id3dx11effect-getgroupbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="0fd0e-127">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0fd0e-128">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0fd0e-129">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0fd0e-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0fd0e-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0fd0e-130">Requirements</span></span>



| <span data-ttu-id="0fd0e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0fd0e-131">Requirement</span></span> | <span data-ttu-id="0fd0e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="0fd0e-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd0e-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="0fd0e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0fd0e-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd0e-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0fd0e-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0fd0e-135">Library</span></span><br/> | <dl> <span data-ttu-id="0fd0e-136"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="0fd0e-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd0e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fd0e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd0e-138">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="0fd0e-138">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="0fd0e-139">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="0fd0e-139">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





