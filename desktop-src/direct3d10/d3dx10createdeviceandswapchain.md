---
description: Créez le meilleur appareil Direct3D et une chaîne de permutation.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: D3DX10CreateDeviceAndSwapChain, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323197"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>D3DX10CreateDeviceAndSwapChain fonction)

Créez le meilleur appareil Direct3D et une chaîne de permutation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAdapter* \[ dans\]
</dt> <dd>

Type : **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Pointeur vers un [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).

</dd> <dt>

*DriverType* \[ dans\]
</dt> <dd>

Type : **[ **\_ \_ type de pilote D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Type de pilote de l’appareil. Consultez [**\_ \_ type de pilote D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

</dd> <dt>

*Logiciel* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle vers la DLL qui implémente un rastériseur logiciel. Doit avoir la **valeur null** si DriverType est non-logiciel. Le HMODULE d’une DLL peut être obtenu avec [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)ou [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Optionnel. Indicateurs de création de l’appareil (voir [**D3D10 \_ créer un \_ \_ indicateur d’appareil**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)) qui active les couches d' [API](d3d10-graphics-programming-guide-api-features-layers.md). Ces indicateurs peuvent être des opérateurs de bits or ensemble.

</dd> <dt>

*pSwapChainDesc* \[ dans\]
</dt> <dd>

Type : description de la **[ **\_ \_ chaîne \_ de permutation dxgi**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Description de la chaîne de permutation. Consultez [**Description de la \_ \_ chaîne \_ de permutation dxgi**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).

</dd> <dt>

*ppSwapChain* \[ à\]
</dt> <dd>

Type : **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Adresse d’un pointeur vers un [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).

</dd> <dt>

*ppDevice* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse d’un pointeur vers une [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) qui recevra l’appareil nouvellement créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Cette méthode retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

Pour créer le meilleur appareil, cette méthode implémente plusieurs options de création d’appareil. Tout d’abord, la méthode tente de créer un appareil 10,1 (et une chaîne de permutation). En cas d’échec, la méthode tente de créer un appareil 10,0. En cas d’échec, la méthode échoue. Si votre application doit créer uniquement un appareil 10,1 ou un appareil 10,0 uniquement, utilisez plutôt ces API :

-   Utilisez [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) pour créer un appareil Direct3D 10,0 (uniquement) et une chaîne de permutation.
-   Utilisez [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) pour créer un appareil Direct3D 10,1 (uniquement) et une chaîne de permutation.

Cette méthode nécessite Windows Vista Service Pack 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
