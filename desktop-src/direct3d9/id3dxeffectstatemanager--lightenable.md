---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour activer/désactiver une lumière.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'ID3DXEffectStateManager :: méthode éclaircie (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211846"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a><span data-ttu-id="f7444-103">ID3DXEffectStateManager :: méthode éclaircie</span><span class="sxs-lookup"><span data-stu-id="f7444-103">ID3DXEffectStateManager::LightEnable method</span></span>

<span data-ttu-id="f7444-104">Fonction de rappel qui doit être implémentée par un utilisateur pour activer/désactiver une lumière.</span><span class="sxs-lookup"><span data-stu-id="f7444-104">A callback function that must be implemented by a user to enable/disable a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7444-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7444-105">Syntax</span></span>


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a><span data-ttu-id="f7444-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7444-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7444-107">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7444-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7444-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7444-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7444-109">Index de base zéro de la lumière.</span><span class="sxs-lookup"><span data-stu-id="f7444-109">The zero-based index of the light.</span></span> <span data-ttu-id="f7444-110">Il s’agit du même index dans [**IDirect3DDevice9 :: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="f7444-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="f7444-111">*Activer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7444-111">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7444-112">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7444-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7444-113">True pour activer la lumière ; sinon, false.</span><span class="sxs-lookup"><span data-stu-id="f7444-113">True to enable the light, false otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7444-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7444-114">Return value</span></span>

<span data-ttu-id="f7444-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7444-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7444-116">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f7444-116">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="f7444-117">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="f7444-117">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="f7444-118">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="f7444-118">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="f7444-119">L’appel de l’état d’effet dynamique (tel que [**IDirect3DDevice9 :: Eclaircir**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) échouera.</span><span class="sxs-lookup"><span data-stu-id="f7444-119">The dynamic effect state call (such as [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7444-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7444-120">Requirements</span></span>



| <span data-ttu-id="f7444-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7444-121">Requirement</span></span> | <span data-ttu-id="f7444-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7444-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7444-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7444-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f7444-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7444-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f7444-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f7444-125">Library</span></span><br/> | <dl> <span data-ttu-id="f7444-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7444-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f7444-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7444-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7444-128">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="f7444-128">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
