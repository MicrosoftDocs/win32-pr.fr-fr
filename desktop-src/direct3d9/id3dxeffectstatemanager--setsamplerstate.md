---
description: Fonction de rappel qui doit être implémentée par un utilisateur pour définir un échantillonneur.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'ID3DXEffectStateManager :: SetSamplerState, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323049"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a><span data-ttu-id="b8228-103">ID3DXEffectStateManager :: SetSamplerState, méthode</span><span class="sxs-lookup"><span data-stu-id="b8228-103">ID3DXEffectStateManager::SetSamplerState method</span></span>

<span data-ttu-id="b8228-104">Fonction de rappel qui doit être implémentée par un utilisateur pour définir un échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="b8228-104">A callback function that must be implemented by a user to set a sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8228-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8228-105">Syntax</span></span>


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a><span data-ttu-id="b8228-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8228-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8228-107">*Échantillonneur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8228-107">*Sampler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8228-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8228-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8228-109">Numéro de l’échantillonneur de base zéro.</span><span class="sxs-lookup"><span data-stu-id="b8228-109">The zero-based sampler number.</span></span>

</dd> <dt>

<span data-ttu-id="b8228-110">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8228-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8228-111">Type : **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="b8228-111">Type: **[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span></span>

<span data-ttu-id="b8228-112">Identifie l’état de l’échantillonneur, qui peut spécifier le filtrage, l’adressage ou la couleur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="b8228-112">Identifies sampler state, which can specify the filtering, addressing, or the border color.</span></span> <span data-ttu-id="b8228-113">Consultez [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="b8228-113">See [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8228-114">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8228-114">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8228-115">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8228-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8228-116">Valeur de l’un des types d’état de l’échantillonneur dans le type.</span><span class="sxs-lookup"><span data-stu-id="b8228-116">A value from one of the sampler state types in Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8228-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8228-117">Return value</span></span>

<span data-ttu-id="b8228-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8228-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8228-119">La méthode implémentée par l’utilisateur doit retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b8228-119">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b8228-120">Si le rappel échoue lors de la définition de l’état de l’appareil, l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="b8228-120">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b8228-121">L’effet échouera pendant [**ID3DXEffect :: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="b8228-121">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b8228-122">L’appel d’état d’effet dynamique (par exemple, [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) échouera.</span><span class="sxs-lookup"><span data-stu-id="b8228-122">The dynamic effect state call (such as [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8228-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8228-123">Requirements</span></span>



| <span data-ttu-id="b8228-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8228-124">Requirement</span></span> | <span data-ttu-id="b8228-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8228-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8228-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8228-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b8228-127"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8228-127"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b8228-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8228-128">Library</span></span><br/> | <dl> <span data-ttu-id="b8228-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8228-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b8228-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8228-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8228-131">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b8228-131">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
