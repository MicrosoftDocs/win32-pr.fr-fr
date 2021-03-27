---
title: Interface ID3DX11EffectDepthStencilViewVariable (D3dx11effect. h)
description: Une interface à profondeur variable de vue de gabarit accède à une vue de stencil de profondeur.
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11
- Interface ID3DX11EffectDepthStencilViewVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51961bd1300157eef4acb4dd15484d5146a166f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211851"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a><span data-ttu-id="e10ce-105">Interface ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="e10ce-105">ID3DX11EffectDepthStencilViewVariable interface</span></span>

<span data-ttu-id="e10ce-106">Une interface à profondeur variable de vue de gabarit accède à une vue de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="e10ce-106">A depth-stencil-view-variable interface accesses a depth-stencil view.</span></span>

## <a name="members"></a><span data-ttu-id="e10ce-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e10ce-107">Members</span></span>

<span data-ttu-id="e10ce-108">L’interface **ID3DX11EffectDepthStencilViewVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="e10ce-108">The **ID3DX11EffectDepthStencilViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e10ce-109">**ID3DX11EffectDepthStencilViewVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e10ce-109">**ID3DX11EffectDepthStencilViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="e10ce-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e10ce-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e10ce-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e10ce-111">Methods</span></span>

<span data-ttu-id="e10ce-112">L’interface **ID3DX11EffectDepthStencilViewVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e10ce-112">The **ID3DX11EffectDepthStencilViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="e10ce-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="e10ce-113">Method</span></span>                                                                                     | <span data-ttu-id="e10ce-114">Description</span><span class="sxs-lookup"><span data-stu-id="e10ce-114">Description</span></span>                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="e10ce-115">**GetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="e10ce-115">**GetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | <span data-ttu-id="e10ce-116">Obtenir une ressource de vue de gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="e10ce-116">Get a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="e10ce-117">**GetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="e10ce-117">**GetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | <span data-ttu-id="e10ce-118">Obtenir un tableau de ressources de profondeur-stencil-vue.</span><span class="sxs-lookup"><span data-stu-id="e10ce-118">Get an array of depth-stencil-view resources.</span></span><br/> |
| [<span data-ttu-id="e10ce-119">**SetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="e10ce-119">**SetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | <span data-ttu-id="e10ce-120">Définissez une ressource de vue de gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="e10ce-120">Set a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="e10ce-121">**SetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="e10ce-121">**SetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | <span data-ttu-id="e10ce-122">Définir un tableau de ressources de profondeur-stencil-affichage.</span><span class="sxs-lookup"><span data-stu-id="e10ce-122">Set an array of depth-stencil-view resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e10ce-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e10ce-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e10ce-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="e10ce-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e10ce-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="e10ce-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e10ce-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e10ce-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e10ce-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e10ce-127">Requirements</span></span>



| <span data-ttu-id="e10ce-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e10ce-128">Requirement</span></span> | <span data-ttu-id="e10ce-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e10ce-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10ce-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="e10ce-130">Header</span></span><br/>  | <dl> <span data-ttu-id="e10ce-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e10ce-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e10ce-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e10ce-132">Library</span></span><br/> | <dl> <span data-ttu-id="e10ce-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="e10ce-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e10ce-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e10ce-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10ce-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="e10ce-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="e10ce-136">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="e10ce-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e10ce-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e10ce-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





