---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de rendu.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'ID3DXEffectStateManager :: SetRenderState, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539166"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a><span data-ttu-id="38f5f-103">ID3DXEffectStateManager :: SetRenderState, méthode</span><span class="sxs-lookup"><span data-stu-id="38f5f-103">ID3DXEffectStateManager::SetRenderState method</span></span>

<span data-ttu-id="38f5f-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir l’état de rendu.</span><span class="sxs-lookup"><span data-stu-id="38f5f-104">A callback function that must be implemented by a user to set render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f5f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38f5f-105">Syntax</span></span>


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a><span data-ttu-id="38f5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38f5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f5f-107">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38f5f-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f5f-108">Type : **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="38f5f-108">Type: **[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span></span>

<span data-ttu-id="38f5f-109">État de rendu à définir.</span><span class="sxs-lookup"><span data-stu-id="38f5f-109">The render state to set.</span></span> [<span data-ttu-id="38f5f-110">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="38f5f-110">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)

</dd> <dt>

<span data-ttu-id="38f5f-111">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38f5f-111">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f5f-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38f5f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38f5f-113">Valeur de l’état de rendu.</span><span class="sxs-lookup"><span data-stu-id="38f5f-113">The render state value.</span></span> <span data-ttu-id="38f5f-114">Consultez [États d’effet (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="38f5f-114">See [Effect States (Direct3D 9)](effect-states.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f5f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38f5f-115">Return value</span></span>

<span data-ttu-id="38f5f-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38f5f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38f5f-117">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38f5f-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="38f5f-118">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="38f5f-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="38f5f-119">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="38f5f-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="38f5f-120">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) échouera.</span><span class="sxs-lookup"><span data-stu-id="38f5f-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f5f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38f5f-121">Requirements</span></span>



| <span data-ttu-id="38f5f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38f5f-122">Requirement</span></span> | <span data-ttu-id="38f5f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="38f5f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f5f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="38f5f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="38f5f-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="38f5f-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="38f5f-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38f5f-126">Library</span></span><br/> | <dl> <span data-ttu-id="38f5f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38f5f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="38f5f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38f5f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f5f-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="38f5f-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
