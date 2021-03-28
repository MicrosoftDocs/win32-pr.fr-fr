---
title: Interface ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Une interface d’échantillonneur accède à l’état de l’échantillonneur.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Interface ID3DX11EffectSamplerVariable Direct3D 11
- Interface ID3DX11EffectSamplerVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116294"
---
# <a name="id3dx11effectsamplervariable-interface"></a><span data-ttu-id="98e3d-105">Interface ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="98e3d-105">ID3DX11EffectSamplerVariable interface</span></span>

<span data-ttu-id="98e3d-106">Une interface d’échantillonneur accède à l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="98e3d-106">A sampler interface accesses sampler state.</span></span>

## <a name="members"></a><span data-ttu-id="98e3d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="98e3d-107">Members</span></span>

<span data-ttu-id="98e3d-108">L’interface **ID3DX11EffectSamplerVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="98e3d-108">The **ID3DX11EffectSamplerVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="98e3d-109">**ID3DX11EffectSamplerVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="98e3d-109">**ID3DX11EffectSamplerVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="98e3d-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98e3d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="98e3d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="98e3d-111">Methods</span></span>

<span data-ttu-id="98e3d-112">L’interface **ID3DX11EffectSamplerVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="98e3d-112">The **ID3DX11EffectSamplerVariable** interface has these methods.</span></span>



| <span data-ttu-id="98e3d-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="98e3d-113">Method</span></span>                                                                  | <span data-ttu-id="98e3d-114">Description</span><span class="sxs-lookup"><span data-stu-id="98e3d-114">Description</span></span>                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="98e3d-115">**GetBackingStore**</span><span class="sxs-lookup"><span data-stu-id="98e3d-115">**GetBackingStore**</span></span>](id3dx11effectsamplervariable-getbackingstore.md) | <span data-ttu-id="98e3d-116">Obtient un pointeur vers une variable qui contient l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="98e3d-116">Get a pointer to a variable that contains sampler state.</span></span><br/> |
| [<span data-ttu-id="98e3d-117">**GetSampler**</span><span class="sxs-lookup"><span data-stu-id="98e3d-117">**GetSampler**</span></span>](id3dx11effectsamplervariable-getsampler.md)           | <span data-ttu-id="98e3d-118">Obtient un pointeur vers une interface d’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="98e3d-118">Get a pointer to a sampler interface.</span></span><br/>                    |
| [<span data-ttu-id="98e3d-119">**SetSampler**</span><span class="sxs-lookup"><span data-stu-id="98e3d-119">**SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)           | <span data-ttu-id="98e3d-120">Définissez l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="98e3d-120">Set sampler state.</span></span><br/>                                       |
| [<span data-ttu-id="98e3d-121">**UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="98e3d-121">**UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)   | <span data-ttu-id="98e3d-122">Rétablir un état d’échantillonneur précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="98e3d-122">Revert a previously set sampler state.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="98e3d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="98e3d-123">Remarks</span></span>

<span data-ttu-id="98e3d-124">Une interface [**ID3DX11EffectVariable**](id3dx11effectvariable.md) est créée lorsqu’un effet est lu dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="98e3d-124">An [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface is created when an effect is read into memory.</span></span>

<span data-ttu-id="98e3d-125">Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="98e3d-125">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="98e3d-126">Vous pouvez utiliser l’une ou l’autre de ces méthodes pour retourner l’État.</span><span class="sxs-lookup"><span data-stu-id="98e3d-126">You can use either of these methods to return state.</span></span>

> [!Note]  
> <span data-ttu-id="98e3d-127">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="98e3d-127">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="98e3d-128">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="98e3d-128">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="98e3d-129">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="98e3d-129">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98e3d-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="98e3d-130">Requirements</span></span>



| <span data-ttu-id="98e3d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98e3d-131">Requirement</span></span> | <span data-ttu-id="98e3d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="98e3d-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e3d-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="98e3d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="98e3d-134"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e3d-134"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="98e3d-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="98e3d-135">Library</span></span><br/> | <dl> <span data-ttu-id="98e3d-136"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="98e3d-136"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e3d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98e3d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e3d-138">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="98e3d-138">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="98e3d-139">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="98e3d-139">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="98e3d-140">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="98e3d-140">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





