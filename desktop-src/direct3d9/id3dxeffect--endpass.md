---
description: Terminer une passe active.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'ID3DXEffect :: EndPass, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322981"
---
# <a name="id3dxeffectendpass-method"></a><span data-ttu-id="8f4a6-103">ID3DXEffect :: EndPass, méthode</span><span class="sxs-lookup"><span data-stu-id="8f4a6-103">ID3DXEffect::EndPass method</span></span>

<span data-ttu-id="8f4a6-104">Terminer une passe active.</span><span class="sxs-lookup"><span data-stu-id="8f4a6-104">End an active pass.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f4a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f4a6-105">Syntax</span></span>


```C++
HRESULT EndPass();
```



## <a name="parameters"></a><span data-ttu-id="8f4a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f4a6-106">Parameters</span></span>

<span data-ttu-id="8f4a6-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8f4a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f4a6-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f4a6-108">Return value</span></span>

<span data-ttu-id="8f4a6-109">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8f4a6-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8f4a6-110">Cette méthode retourne toujours la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8f4a6-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f4a6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8f4a6-111">Remarks</span></span>

<span data-ttu-id="8f4a6-112">Une application signale la fin du rendu d’une passe active en appelant **ID3DXEffect :: EndPass**.</span><span class="sxs-lookup"><span data-stu-id="8f4a6-112">An application signals the end of rendering an active pass by calling **ID3DXEffect::EndPass**.</span></span> <span data-ttu-id="8f4a6-113">Chaque **ID3DXEffect :: EndPass** doit faire partie d’une paire correspondante d’appels [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) et **ID3DXEffect :: EndPass** .</span><span class="sxs-lookup"><span data-stu-id="8f4a6-113">Each **ID3DXEffect::EndPass** must be part of a matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls.</span></span>

<span data-ttu-id="8f4a6-114">Chaque paire correspondante d’appels [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) et **ID3DXEffect :: EndPass** doit se trouver dans une paire correspondante d’appels [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) et [**ID3DXEffect :: end**](id3dxeffect--end.md) .</span><span class="sxs-lookup"><span data-stu-id="8f4a6-114">Each matching pair of [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) and **ID3DXEffect::EndPass** calls must be located within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="8f4a6-115">Si l’application modifie un état d’effet à l’aide de l’une des méthodes [**Effect :: setX**](id3dxeffect.md) à l’intérieur d’une paire de correspondances [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md) / **ID3DXEffect :: EndPass** , l’application doit appeler [**ID3DXEffect :: CommitChanges**](id3dxeffect--commitchanges.md) avant tout appel DrawxPrimitive pour propager les modifications d’État à l’appareil avant le rendu.</span><span class="sxs-lookup"><span data-stu-id="8f4a6-115">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md)/**ID3DXEffect::EndPass** matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) before any DrawxPrimitive call to propagate state changes to the device before rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f4a6-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f4a6-116">Requirements</span></span>



| <span data-ttu-id="8f4a6-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f4a6-117">Requirement</span></span> | <span data-ttu-id="8f4a6-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f4a6-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f4a6-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f4a6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8f4a6-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f4a6-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8f4a6-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8f4a6-121">Library</span></span><br/> | <dl> <span data-ttu-id="8f4a6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f4a6-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8f4a6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f4a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f4a6-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8f4a6-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




