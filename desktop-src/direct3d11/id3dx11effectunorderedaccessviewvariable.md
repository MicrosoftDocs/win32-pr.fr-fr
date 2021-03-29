---
title: Interface ID3DX11EffectUnorderedAccessViewVariable (D3dx11effect. h)
description: Accède à une vue d’accès non ordonnée.
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11
- Interface ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48161ad4d9fc1773889fab0e8a0fd9a21ec793e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992141"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a><span data-ttu-id="29b60-105">Interface ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="29b60-105">ID3DX11EffectUnorderedAccessViewVariable interface</span></span>

<span data-ttu-id="29b60-106">Accède à une vue d’accès non ordonnée.</span><span class="sxs-lookup"><span data-stu-id="29b60-106">Accesses an unordered access view.</span></span>

## <a name="members"></a><span data-ttu-id="29b60-107">Membres</span><span class="sxs-lookup"><span data-stu-id="29b60-107">Members</span></span>

<span data-ttu-id="29b60-108">L’interface **ID3DX11EffectUnorderedAccessViewVariable** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="29b60-108">The **ID3DX11EffectUnorderedAccessViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="29b60-109">**ID3DX11EffectUnorderedAccessViewVariable** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="29b60-109">**ID3DX11EffectUnorderedAccessViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="29b60-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="29b60-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="29b60-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="29b60-111">Methods</span></span>

<span data-ttu-id="29b60-112">L’interface **ID3DX11EffectUnorderedAccessViewVariable** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="29b60-112">The **ID3DX11EffectUnorderedAccessViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="29b60-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="29b60-113">Method</span></span>                                                                                                      | <span data-ttu-id="29b60-114">Description</span><span class="sxs-lookup"><span data-stu-id="29b60-114">Description</span></span>                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="29b60-115">**GetUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="29b60-115">**GetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | <span data-ttu-id="29b60-116">Obtenir un mode d’accès non ordonné.</span><span class="sxs-lookup"><span data-stu-id="29b60-116">Get an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="29b60-117">**GetUnorderedAccessViewArray**</span><span class="sxs-lookup"><span data-stu-id="29b60-117">**GetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | <span data-ttu-id="29b60-118">Obtient un tableau de vues d’accès non ordonnées.</span><span class="sxs-lookup"><span data-stu-id="29b60-118">Get an array of unordered-access-views.</span></span><br/> |
| [<span data-ttu-id="29b60-119">**SetUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="29b60-119">**SetUnorderedAccessView**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | <span data-ttu-id="29b60-120">Définissez un mode d’accès non ordonné.</span><span class="sxs-lookup"><span data-stu-id="29b60-120">Set an unordered-access-view.</span></span><br/>           |
| [<span data-ttu-id="29b60-121">**SetUnorderedAccessViewArray**</span><span class="sxs-lookup"><span data-stu-id="29b60-121">**SetUnorderedAccessViewArray**</span></span>](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | <span data-ttu-id="29b60-122">Définissez un tableau de vues d’accès non ordonnées.</span><span class="sxs-lookup"><span data-stu-id="29b60-122">Set an array of unordered-access-views.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29b60-123">Notes</span><span class="sxs-lookup"><span data-stu-id="29b60-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="29b60-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="29b60-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="29b60-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="29b60-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="29b60-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="29b60-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29b60-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="29b60-127">Requirements</span></span>



| <span data-ttu-id="29b60-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29b60-128">Requirement</span></span> | <span data-ttu-id="29b60-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="29b60-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b60-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="29b60-130">Header</span></span><br/>  | <dl> <span data-ttu-id="29b60-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="29b60-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="29b60-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="29b60-132">Library</span></span><br/> | <dl> <span data-ttu-id="29b60-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="29b60-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29b60-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29b60-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29b60-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="29b60-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="29b60-136">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="29b60-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="29b60-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="29b60-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





