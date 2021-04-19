---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir une lumière.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'ID3DXEffectStateManager :: SetLight, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532459"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a><span data-ttu-id="152d3-103">ID3DXEffectStateManager :: SetLight, méthode</span><span class="sxs-lookup"><span data-stu-id="152d3-103">ID3DXEffectStateManager::SetLight method</span></span>

<span data-ttu-id="152d3-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir une lumière.</span><span class="sxs-lookup"><span data-stu-id="152d3-104">A callback function that must be implemented by a user to set a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="152d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="152d3-105">Syntax</span></span>


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a><span data-ttu-id="152d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="152d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152d3-107">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="152d3-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="152d3-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="152d3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="152d3-109">Index de base zéro de la lumière.</span><span class="sxs-lookup"><span data-stu-id="152d3-109">The zero-based index of the light.</span></span> <span data-ttu-id="152d3-110">Il s’agit du même index dans [**IDirect3DDevice9 :: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="152d3-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="152d3-111">*pLight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="152d3-111">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="152d3-112">Type : **const [**D3DLight9**](d3dlight9.md) \***</span><span class="sxs-lookup"><span data-stu-id="152d3-112">Type: **const [**D3DLight9**](d3dlight9.md)\***</span></span>

<span data-ttu-id="152d3-113">Objet Light.</span><span class="sxs-lookup"><span data-stu-id="152d3-113">The light object.</span></span> <span data-ttu-id="152d3-114">Consultez [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="152d3-114">See [**D3DLIGHT9**](d3dlight9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="152d3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="152d3-115">Return value</span></span>

<span data-ttu-id="152d3-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="152d3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="152d3-117">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="152d3-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="152d3-118">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="152d3-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="152d3-119">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="152d3-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="152d3-120">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) échouera.</span><span class="sxs-lookup"><span data-stu-id="152d3-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="152d3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="152d3-121">Requirements</span></span>



| <span data-ttu-id="152d3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="152d3-122">Requirement</span></span> | <span data-ttu-id="152d3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="152d3-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="152d3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="152d3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="152d3-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="152d3-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="152d3-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="152d3-126">Library</span></span><br/> | <dl> <span data-ttu-id="152d3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="152d3-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="152d3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="152d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152d3-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="152d3-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
