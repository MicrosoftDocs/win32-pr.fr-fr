---
title: Interface ID3DX11EffectRenderTargetViewVariable (D3dx11effect. h)
description: Une interface de rendu-cible-vue accède à une cible de rendu.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11
- Interface ID3DX11EffectRenderTargetViewVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974511"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a><span data-ttu-id="cbd1d-105">Interface ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="cbd1d-105">ID3DX11EffectRenderTargetViewVariable interface</span></span>

<span data-ttu-id="cbd1d-106">Une interface de rendu-cible-vue accède à une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-106">A render-target-view interface accesses a render target.</span></span>

## <a name="members"></a><span data-ttu-id="cbd1d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="cbd1d-107">Members</span></span>

<span data-ttu-id="cbd1d-108">L’interface **ID3DX11EffectRenderTargetViewVariable** hérite de [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="cbd1d-108">The **ID3DX11EffectRenderTargetViewVariable** interface inherits from [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="cbd1d-109">**ID3DX11EffectRenderTargetViewVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cbd1d-109">**ID3DX11EffectRenderTargetViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="cbd1d-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cbd1d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cbd1d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cbd1d-111">Methods</span></span>

<span data-ttu-id="cbd1d-112">L’interface **ID3DX11EffectRenderTargetViewVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-112">The **ID3DX11EffectRenderTargetViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="cbd1d-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="cbd1d-113">Method</span></span>                                                                                     | <span data-ttu-id="cbd1d-114">Description</span><span class="sxs-lookup"><span data-stu-id="cbd1d-114">Description</span></span>                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [<span data-ttu-id="cbd1d-115">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="cbd1d-115">**GetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | <span data-ttu-id="cbd1d-116">Obtenir une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-116">Get a render-target.</span></span><br/>            |
| [<span data-ttu-id="cbd1d-117">**GetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="cbd1d-117">**GetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | <span data-ttu-id="cbd1d-118">Obtient un tableau de cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-118">Get an array of render-targets.</span></span><br/> |
| [<span data-ttu-id="cbd1d-119">**SetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="cbd1d-119">**SetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | <span data-ttu-id="cbd1d-120">Définissez une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-120">Set a render-target.</span></span><br/>            |
| [<span data-ttu-id="cbd1d-121">**SetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="cbd1d-121">**SetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | <span data-ttu-id="cbd1d-122">Définissez un tableau de cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-122">Set an array of render-targets.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbd1d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cbd1d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cbd1d-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cbd1d-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cbd1d-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cbd1d-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cbd1d-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cbd1d-127">Requirements</span></span>



| <span data-ttu-id="cbd1d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbd1d-128">Requirement</span></span> | <span data-ttu-id="cbd1d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbd1d-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbd1d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbd1d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cbd1d-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbd1d-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cbd1d-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cbd1d-132">Library</span></span><br/> | <dl> <span data-ttu-id="cbd1d-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="cbd1d-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbd1d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbd1d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd1d-135">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="cbd1d-135">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="cbd1d-136">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="cbd1d-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cbd1d-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cbd1d-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





