---
description: Créez le meilleur appareil Direct3D 10 qui représente la carte graphique. Si un appareil compatible Direct3D 10,1 peut être créé, il sera possible d’acquérir un pointeur d’interface ID3D10Device1 à partir du pointeur d’interface d’appareil retourné.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: D3DX10CreateDevice, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520342"
---
# <a name="d3dx10createdevice-function"></a>D3DX10CreateDevice fonction)

Créez le meilleur appareil Direct3D 10 qui représente la carte graphique. Si un appareil compatible Direct3D 10,1 peut être créé, il sera possible d’acquérir un pointeur d' [**interface ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) à partir du pointeur d’interface d’appareil retourné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAdapter* \[ dans\]
</dt> <dd>

Type : **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Pointeur vers l’adaptateur d’affichage (Voir l’interface [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) ) lors de la création d’un périphérique matériel ; Sinon, affectez la **valeur null** à ce paramètre. Si la **valeur null** est spécifiée lors de la création d’un périphérique matériel, Direct3D utilise la première carte énumérée par l’interface [**IDXGIFactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) .

</dd> <dt>

*DriverType* \[ dans\]
</dt> <dd>

Type : **[ **\_ \_ type de pilote D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Le type de pilote de périphérique (consultez l’énumération de [**\_ \_ type de pilote D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) ). Le type de pilote détermine le type d’appareil que vous allez créer.

</dd> <dt>

*Logiciel* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle d’un module chargé qui implémente un pilote logiciel (tel que D3D10Ref.dll). Pour obtenir un handle, appelez la fonction [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Indicateurs de création de l’appareil (consultez [**D3D10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) Enumeration) qui active les [couches API](d3d10-graphics-programming-guide-api-features-layers.md). Ces indicateurs peuvent être des opérateurs de bits or ensemble.

</dd> <dt>

*ppDevice* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse d’un pointeur vers l’appareil créé (consultez l’interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Cette fonction retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

Cette fonction tente de créer le meilleur appareil pour le matériel. Tout d’abord, la fonction tente de créer un appareil 10,1. Si un appareil 10,1 ne peut pas être créé, la fonction tente de créer un appareil 10,0. Si aucun appareil n’est correctement créé, la fonction retourne E \_ Fail.

Si votre application doit créer uniquement un appareil 10,1 ou un appareil 10,0 uniquement, utilisez les fonctions suivantes à la place :

-   Utilisez la fonction [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) pour créer un appareil Direct3D 10,0 uniquement.
-   Utilisez la fonction [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) pour créer un appareil Direct3D 10,1 uniquement.
-   Utilisez la fonction [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) pour récupérer un pointeur d’interface [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) à partir d’un pointeur d’interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

Un périphérique Direct3D 10,1 peut uniquement être créé sur des ordinateurs exécutant Windows Vista Service Pack 1 ou version ultérieure, et avec un matériel compatible Direct3D 10,1 installé. Toutefois, il est légal d’appeler cette fonction sur des ordinateurs exécutant n’importe quelle version de Windows sur laquelle la DLL D3DX10 est installée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
