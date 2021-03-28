---
title: Interface ID3DX11EffectRasterizerVariable (D3dx11effect. h)
description: Une interface de la variable rastériseur accède à l’état du rastériseur.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- Interface ID3DX11EffectRasterizerVariable Direct3D 11
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a19c5d529d6134ebad238be6e7c6195dc628a7f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996261"
---
# <a name="id3dx11effectrasterizervariable-interface"></a><span data-ttu-id="70b6f-105">Interface ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="70b6f-105">ID3DX11EffectRasterizerVariable interface</span></span>

<span data-ttu-id="70b6f-106">Une interface de la variable rastériseur accède à l’état du rastériseur.</span><span class="sxs-lookup"><span data-stu-id="70b6f-106">A rasterizer-variable interface accesses rasterizer state.</span></span>

## <a name="members"></a><span data-ttu-id="70b6f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="70b6f-107">Members</span></span>

<span data-ttu-id="70b6f-108">L’interface **ID3DX11EffectRasterizerVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="70b6f-108">The **ID3DX11EffectRasterizerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="70b6f-109">**ID3DX11EffectRasterizerVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70b6f-109">**ID3DX11EffectRasterizerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="70b6f-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="70b6f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="70b6f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="70b6f-111">Methods</span></span>

<span data-ttu-id="70b6f-112">L’interface **ID3DX11EffectRasterizerVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="70b6f-112">The **ID3DX11EffectRasterizerVariable** interface has these methods.</span></span>



| <span data-ttu-id="70b6f-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="70b6f-113">Method</span></span>                                                                                   | <span data-ttu-id="70b6f-114">Description</span><span class="sxs-lookup"><span data-stu-id="70b6f-114">Description</span></span>                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="70b6f-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="70b6f-115">**GetBackingStore**</span></span>](id3dx11effectrasterizervariable-getbackingstore.md)               | <span data-ttu-id="70b6f-116">Obtient un pointeur vers une variable qui contient l’État rasteriser.</span><span class="sxs-lookup"><span data-stu-id="70b6f-116">Get a pointer to a variable that contains rasteriser state.</span></span><br/> |
| [<span data-ttu-id="70b6f-117">**GetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="70b6f-117">**GetRasterizerState**</span></span>](id3dx11effectrasterizervariable-getrasterizerstate.md)         | <span data-ttu-id="70b6f-118">Obtient un pointeur vers une interface de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="70b6f-118">Get a pointer to a rasterizer interface.</span></span><br/>                    |
| [<span data-ttu-id="70b6f-119">**SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="70b6f-119">**SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)         | <span data-ttu-id="70b6f-120">Définit l’état du rastériseur.</span><span class="sxs-lookup"><span data-stu-id="70b6f-120">Sets the rasterizer state.</span></span><br/>                                  |
| [<span data-ttu-id="70b6f-121">**UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="70b6f-121">**UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | <span data-ttu-id="70b6f-122">Restaure un état de rastériseur précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="70b6f-122">Reverts a previously set rasterizer state.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="70b6f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="70b6f-123">Remarks</span></span>

<span data-ttu-id="70b6f-124">Une interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) est créée lorsqu’un effet est lu dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="70b6f-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="70b6f-125">Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="70b6f-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="70b6f-126">Vous pouvez utiliser l’une ou l’autre de ces méthodes pour retourner l’État.</span><span class="sxs-lookup"><span data-stu-id="70b6f-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="70b6f-127">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="70b6f-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="70b6f-128">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="70b6f-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="70b6f-129">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="70b6f-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70b6f-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="70b6f-130">Requirements</span></span>



| <span data-ttu-id="70b6f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70b6f-131">Requirement</span></span> | <span data-ttu-id="70b6f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="70b6f-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b6f-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="70b6f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="70b6f-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="70b6f-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="70b6f-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70b6f-135">Library</span></span><br/> | <dl> <span data-ttu-id="70b6f-136"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="70b6f-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70b6f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70b6f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b6f-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="70b6f-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="70b6f-139">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="70b6f-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="70b6f-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="70b6f-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





