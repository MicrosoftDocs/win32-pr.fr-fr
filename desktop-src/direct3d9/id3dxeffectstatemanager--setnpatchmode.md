---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir le nombre de segments de la sous-division pour N-patchs.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'ID3DXEffectStateManager :: SetNPatchMode, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103954000"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a><span data-ttu-id="5a62a-103">ID3DXEffectStateManager :: SetNPatchMode, méthode</span><span class="sxs-lookup"><span data-stu-id="5a62a-103">ID3DXEffectStateManager::SetNPatchMode method</span></span>

<span data-ttu-id="5a62a-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir le nombre de segments de la sous-division pour N-patchs.</span><span class="sxs-lookup"><span data-stu-id="5a62a-104">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a62a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a62a-105">Syntax</span></span>


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a><span data-ttu-id="5a62a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a62a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a62a-107">*nSegments* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a62a-107">*nSegments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a62a-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a62a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a62a-109">Scinder la surface en ce nombre de sous-divisions.</span><span class="sxs-lookup"><span data-stu-id="5a62a-109">Break the surface into this number of subdivisions.</span></span> <span data-ttu-id="5a62a-110">Il s’agit du même numéro que celui utilisé par [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="5a62a-110">This is the same as the number used by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a62a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a62a-111">Return value</span></span>

<span data-ttu-id="5a62a-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a62a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a62a-113">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a62a-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="5a62a-114">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="5a62a-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="5a62a-115">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="5a62a-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="5a62a-116">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) échouera.</span><span class="sxs-lookup"><span data-stu-id="5a62a-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a62a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a62a-117">Requirements</span></span>



| <span data-ttu-id="5a62a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a62a-118">Requirement</span></span> | <span data-ttu-id="5a62a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a62a-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a62a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a62a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5a62a-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a62a-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5a62a-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a62a-122">Library</span></span><br/> | <dl> <span data-ttu-id="5a62a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a62a-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5a62a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a62a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a62a-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="5a62a-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
