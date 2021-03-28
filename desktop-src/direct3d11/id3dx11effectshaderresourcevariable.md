---
title: Interface ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Une interface de nuanceur-ressource accède à une ressource de nuanceur.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11
- Interface ID3DX11EffectShaderResourceVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996296"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a><span data-ttu-id="f0a9f-105">Interface ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="f0a9f-105">ID3DX11EffectShaderResourceVariable interface</span></span>

<span data-ttu-id="f0a9f-106">Une interface de nuanceur-ressource accède à une ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-106">A shader-resource interface accesses a shader resource.</span></span>

## <a name="members"></a><span data-ttu-id="f0a9f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f0a9f-107">Members</span></span>

<span data-ttu-id="f0a9f-108">L’interface **ID3DX11EffectShaderResourceVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-108">The **ID3DX11EffectShaderResourceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="f0a9f-109">**ID3DX11EffectShaderResourceVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f0a9f-109">**ID3DX11EffectShaderResourceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="f0a9f-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f0a9f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f0a9f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f0a9f-111">Methods</span></span>

<span data-ttu-id="f0a9f-112">L’interface **ID3DX11EffectShaderResourceVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-112">The **ID3DX11EffectShaderResourceVariable** interface has these methods.</span></span>



| <span data-ttu-id="f0a9f-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="f0a9f-113">Method</span></span>                                                                           | <span data-ttu-id="f0a9f-114">Description</span><span class="sxs-lookup"><span data-stu-id="f0a9f-114">Description</span></span>                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="f0a9f-115">**GetResource**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-115">**GetResource**</span></span>](id3dx11effectshaderresourcevariable-getresource.md)           | <span data-ttu-id="f0a9f-116">Obtenir une ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-116">Get a shader resource.</span></span><br/>            |
| [<span data-ttu-id="f0a9f-117">**GetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-117">**GetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-getresourcearray.md) | <span data-ttu-id="f0a9f-118">Obtient un tableau de ressources de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-118">Get an array of shader resources.</span></span><br/> |
| [<span data-ttu-id="f0a9f-119">**SetResource**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-119">**SetResource**</span></span>](id3dx11effectshaderresourcevariable-setresource.md)           | <span data-ttu-id="f0a9f-120">Définissez une ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-120">Set a shader resource.</span></span><br/>            |
| [<span data-ttu-id="f0a9f-121">**SetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-121">**SetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-setresourcearray.md) | <span data-ttu-id="f0a9f-122">Définir un tableau de ressources de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-122">Set an array of shader resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0a9f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f0a9f-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0a9f-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f0a9f-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="f0a9f-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f0a9f-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f0a9f-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0a9f-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f0a9f-127">Requirements</span></span>



| <span data-ttu-id="f0a9f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0a9f-128">Requirement</span></span> | <span data-ttu-id="f0a9f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0a9f-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a9f-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0a9f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f0a9f-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0a9f-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f0a9f-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f0a9f-132">Library</span></span><br/> | <dl> <span data-ttu-id="f0a9f-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="f0a9f-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0a9f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0a9f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a9f-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="f0a9f-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="f0a9f-136">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="f0a9f-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f0a9f-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f0a9f-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





