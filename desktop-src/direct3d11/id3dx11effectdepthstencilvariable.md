---
title: Interface ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Une interface à profondeur variable de gabarit accède à l’état de gabarit de profondeur.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d7aa520df0c13c81435421d5f605f901a61da6e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953965"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a><span data-ttu-id="d8523-105">Interface ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="d8523-105">ID3DX11EffectDepthStencilVariable interface</span></span>

<span data-ttu-id="d8523-106">Une interface à profondeur variable de gabarit accède à l’état de gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="d8523-106">A depth-stencil-variable interface accesses depth-stencil state.</span></span>

## <a name="members"></a><span data-ttu-id="d8523-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d8523-107">Members</span></span>

<span data-ttu-id="d8523-108">L’interface **ID3DX11EffectDepthStencilVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="d8523-108">The **ID3DX11EffectDepthStencilVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="d8523-109">**ID3DX11EffectDepthStencilVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d8523-109">**ID3DX11EffectDepthStencilVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="d8523-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d8523-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d8523-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d8523-111">Methods</span></span>

<span data-ttu-id="d8523-112">L’interface **ID3DX11EffectDepthStencilVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d8523-112">The **ID3DX11EffectDepthStencilVariable** interface has these methods.</span></span>



| <span data-ttu-id="d8523-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="d8523-113">Method</span></span>                                                                                         | <span data-ttu-id="d8523-114">Description</span><span class="sxs-lookup"><span data-stu-id="d8523-114">Description</span></span>                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="d8523-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="d8523-115">**GetBackingStore**</span></span>](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | <span data-ttu-id="d8523-116">Obtient un pointeur vers une variable qui contient l’état du gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="d8523-116">Get a pointer to a variable that contains depth-stencil state.</span></span><br/> |
| [<span data-ttu-id="d8523-117">**GetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="d8523-117">**GetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | <span data-ttu-id="d8523-118">Obtient un pointeur vers une interface de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="d8523-118">Get a pointer to a depth-stencil interface.</span></span><br/>                    |
| [<span data-ttu-id="d8523-119">**SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="d8523-119">**SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | <span data-ttu-id="d8523-120">Définit l’état du stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="d8523-120">Sets the depth stencil state.</span></span><br/>                                  |
| [<span data-ttu-id="d8523-121">**UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="d8523-121">**UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | <span data-ttu-id="d8523-122">Rétablit un État du stencil de profondeur précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="d8523-122">Reverts a previously set depth stencil state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="d8523-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d8523-123">Remarks</span></span>

<span data-ttu-id="d8523-124">Une interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) est créée lorsqu’un effet est lu dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d8523-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="d8523-125">Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d8523-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="d8523-126">Vous pouvez utiliser l’une ou l’autre de ces méthodes pour retourner l’État.</span><span class="sxs-lookup"><span data-stu-id="d8523-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="d8523-127">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="d8523-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d8523-128">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="d8523-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d8523-129">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d8523-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8523-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8523-130">Requirements</span></span>



| <span data-ttu-id="d8523-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8523-131">Requirement</span></span> | <span data-ttu-id="d8523-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8523-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8523-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8523-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d8523-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8523-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d8523-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8523-135">Library</span></span><br/> | <dl> <span data-ttu-id="d8523-136"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="d8523-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8523-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8523-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8523-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="d8523-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="d8523-139">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="d8523-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d8523-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d8523-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





