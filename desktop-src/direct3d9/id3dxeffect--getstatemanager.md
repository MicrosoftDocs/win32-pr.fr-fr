---
description: Obtient le gestionnaire d’état des effets.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'ID3DXEffect :: GetStateManager, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527095"
---
# <a name="id3dxeffectgetstatemanager-method"></a><span data-ttu-id="9dd65-103">ID3DXEffect :: GetStateManager, méthode</span><span class="sxs-lookup"><span data-stu-id="9dd65-103">ID3DXEffect::GetStateManager method</span></span>

<span data-ttu-id="9dd65-104">Obtient le gestionnaire d’état des effets.</span><span class="sxs-lookup"><span data-stu-id="9dd65-104">Get the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd65-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9dd65-105">Syntax</span></span>


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="9dd65-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9dd65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd65-107">*ppManager* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9dd65-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd65-108">Type : **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span><span class="sxs-lookup"><span data-stu-id="9dd65-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span></span>

<span data-ttu-id="9dd65-109">Retourne un pointeur vers le gestionnaire d’État.</span><span class="sxs-lookup"><span data-stu-id="9dd65-109">Returns a pointer to the state manager.</span></span> <span data-ttu-id="9dd65-110">Consultez [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="9dd65-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd65-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9dd65-111">Return value</span></span>

<span data-ttu-id="9dd65-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9dd65-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9dd65-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9dd65-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9dd65-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="9dd65-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd65-115">Notes</span><span class="sxs-lookup"><span data-stu-id="9dd65-115">Remarks</span></span>

<span data-ttu-id="9dd65-116">Le [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) est une interface implémentée par l’utilisateur qui fournit des rappels dans une application pour définir l’état de l’appareil à partir d’un effet.</span><span class="sxs-lookup"><span data-stu-id="9dd65-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd65-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dd65-117">Requirements</span></span>



| <span data-ttu-id="9dd65-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dd65-118">Requirement</span></span> | <span data-ttu-id="9dd65-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dd65-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd65-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9dd65-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9dd65-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd65-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9dd65-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9dd65-122">Library</span></span><br/> | <dl> <span data-ttu-id="9dd65-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dd65-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9dd65-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dd65-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd65-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="9dd65-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="9dd65-126">**ID3DXEffect::SetStateManager**</span><span class="sxs-lookup"><span data-stu-id="9dd65-126">**ID3DXEffect::SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




