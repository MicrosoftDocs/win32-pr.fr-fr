---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de pixels.
ms.assetid: 4124eff2-1d88-429c-b7ed-8d87155b5ddc
title: 'ID3DXEffectStateManager :: SetPixelShader, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 71a16bc267df95ed7efc1e0f74871b131e34ebe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530981"
---
# <a name="id3dxeffectstatemanagersetpixelshader-method"></a><span data-ttu-id="6d4df-103">ID3DXEffectStateManager :: SetPixelShader, méthode</span><span class="sxs-lookup"><span data-stu-id="6d4df-103">ID3DXEffectStateManager::SetPixelShader method</span></span>

<span data-ttu-id="6d4df-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="6d4df-104">A callback function that must be implemented by a user to set a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d4df-105">Syntax</span></span>


```C++
HRESULT SetPixelShader(
  [in] LPDIRECT3DPIXELSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="6d4df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d4df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d4df-107">*pShader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d4df-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4df-108">Type : **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span><span class="sxs-lookup"><span data-stu-id="6d4df-108">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span></span>

<span data-ttu-id="6d4df-109">Pointeur vers un objet de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="6d4df-109">A pointer to a pixel shader object.</span></span> <span data-ttu-id="6d4df-110">Consultez [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span><span class="sxs-lookup"><span data-stu-id="6d4df-110">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d4df-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d4df-111">Return value</span></span>

<span data-ttu-id="6d4df-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d4df-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d4df-113">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d4df-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="6d4df-114">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="6d4df-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="6d4df-115">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="6d4df-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="6d4df-116">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) échouera.</span><span class="sxs-lookup"><span data-stu-id="6d4df-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4df-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d4df-117">Requirements</span></span>



| <span data-ttu-id="6d4df-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d4df-118">Requirement</span></span> | <span data-ttu-id="6d4df-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d4df-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4df-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d4df-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6d4df-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d4df-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6d4df-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6d4df-122">Library</span></span><br/> | <dl> <span data-ttu-id="6d4df-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d4df-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6d4df-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d4df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4df-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="6d4df-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
