---
title: Interface ID3DX11EffectBlendVariable (D3dx11effect. h)
description: L’interface de variable Blend accède à l’État Blend.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Interface ID3DX11EffectBlendVariable Direct3D 11
- Interface ID3DX11EffectBlendVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954009"
---
# <a name="id3dx11effectblendvariable-interface"></a><span data-ttu-id="e86ed-105">Interface ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="e86ed-105">ID3DX11EffectBlendVariable interface</span></span>

<span data-ttu-id="e86ed-106">L’interface de variable Blend accède à l’État Blend.</span><span class="sxs-lookup"><span data-stu-id="e86ed-106">The blend-variable interface accesses blend state.</span></span>

## <a name="members"></a><span data-ttu-id="e86ed-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e86ed-107">Members</span></span>

<span data-ttu-id="e86ed-108">L’interface **ID3DX11EffectBlendVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="e86ed-108">The **ID3DX11EffectBlendVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="e86ed-109">**ID3DX11EffectBlendVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e86ed-109">**ID3DX11EffectBlendVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="e86ed-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e86ed-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e86ed-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e86ed-111">Methods</span></span>

<span data-ttu-id="e86ed-112">L’interface **ID3DX11EffectBlendVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e86ed-112">The **ID3DX11EffectBlendVariable** interface has these methods.</span></span>



| <span data-ttu-id="e86ed-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="e86ed-113">Method</span></span>                                                                    | <span data-ttu-id="e86ed-114">Description</span><span class="sxs-lookup"><span data-stu-id="e86ed-114">Description</span></span>                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="e86ed-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="e86ed-115">**GetBackingStore**</span></span>](id3dx11effectblendvariable-getbackingstore.md)     | <span data-ttu-id="e86ed-116">Obtient un pointeur vers une variable d’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="e86ed-116">Get a pointer to a blend-state variable.</span></span><br/>  |
| [<span data-ttu-id="e86ed-117">**GetBlendState**</span><span class="sxs-lookup"><span data-stu-id="e86ed-117">**GetBlendState**</span></span>](id3dx11effectblendvariable-getblendstate.md)         | <span data-ttu-id="e86ed-118">Obtient un pointeur vers une interface d’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="e86ed-118">Get a pointer to a blend-state interface.</span></span><br/> |
| [<span data-ttu-id="e86ed-119">**SetBlendState**</span><span class="sxs-lookup"><span data-stu-id="e86ed-119">**SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)         | <span data-ttu-id="e86ed-120">Définit l’état de fusion d’un effet.</span><span class="sxs-lookup"><span data-stu-id="e86ed-120">Sets an effect's blend-state.</span></span><br/>             |
| [<span data-ttu-id="e86ed-121">**UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="e86ed-121">**UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md) | <span data-ttu-id="e86ed-122">Restaure un état de fusion précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="e86ed-122">Reverts a previously set blend-state.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e86ed-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e86ed-123">Remarks</span></span>

<span data-ttu-id="e86ed-124">Une interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) est créée lorsqu’un effet est lu dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e86ed-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="e86ed-125">Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e86ed-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="e86ed-126">Vous pouvez utiliser l’une ou l’autre de ces méthodes pour retourner l’État.</span><span class="sxs-lookup"><span data-stu-id="e86ed-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="e86ed-127">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="e86ed-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e86ed-128">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="e86ed-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e86ed-129">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e86ed-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e86ed-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e86ed-130">Requirements</span></span>



| <span data-ttu-id="e86ed-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e86ed-131">Requirement</span></span> | <span data-ttu-id="e86ed-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e86ed-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e86ed-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="e86ed-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e86ed-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e86ed-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e86ed-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e86ed-135">Library</span></span><br/> | <dl> <span data-ttu-id="e86ed-136"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="e86ed-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86ed-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e86ed-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86ed-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="e86ed-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="e86ed-139">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="e86ed-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="e86ed-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e86ed-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





