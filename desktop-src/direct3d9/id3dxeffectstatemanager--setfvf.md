---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un code de Commission.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'ID3DXEffectStateManager :: SetFVF, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545889"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a><span data-ttu-id="5127c-103">ID3DXEffectStateManager :: SetFVF, méthode</span><span class="sxs-lookup"><span data-stu-id="5127c-103">ID3DXEffectStateManager::SetFVF method</span></span>

<span data-ttu-id="5127c-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un code de Commission.</span><span class="sxs-lookup"><span data-stu-id="5127c-104">A callback function that must be implemented by a user to set a FVF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5127c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5127c-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="5127c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5127c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5127c-107">*Commission* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5127c-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5127c-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5127c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5127c-109">Constante du prix de la Commission, qui détermine comment interpréter les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="5127c-109">The FVF constant, that determines how to interpret vertex data.</span></span> <span data-ttu-id="5127c-110">Consultez [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="5127c-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5127c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5127c-111">Return value</span></span>

<span data-ttu-id="5127c-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5127c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5127c-113">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5127c-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="5127c-114">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="5127c-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="5127c-115">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="5127c-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="5127c-116">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) échouera.</span><span class="sxs-lookup"><span data-stu-id="5127c-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="5127c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5127c-117">Requirements</span></span>



| <span data-ttu-id="5127c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5127c-118">Requirement</span></span> | <span data-ttu-id="5127c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5127c-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5127c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5127c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5127c-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5127c-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5127c-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5127c-122">Library</span></span><br/> | <dl> <span data-ttu-id="5127c-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5127c-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5127c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5127c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5127c-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="5127c-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
