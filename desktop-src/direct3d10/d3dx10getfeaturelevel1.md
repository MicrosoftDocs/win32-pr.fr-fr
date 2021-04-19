---
description: Obtient un pointeur d’interface de périphérique Direct3D 10,1 à partir d’un pointeur d’interface Direct3D 10,0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: D3DX10GetFeatureLevel1, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522337"
---
# <a name="d3dx10getfeaturelevel1-function"></a>D3DX10GetFeatureLevel1 fonction)

Obtient un pointeur d’interface de périphérique Direct3D 10,1 à partir d’un pointeur d’interface Direct3D 10,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Pointeur vers l’appareil Direct3D 10,0 (Voir l’interface [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).

</dd> <dt>

*ppDevice* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Pointeur vers l’appareil Direct3D 10,1 (Voir l’interface [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) ).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Cette fonction retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants. Si une interface de périphérique Direct3D 10,1 peut être acquise, cette fonction réussit et passe un pointeur vers l’interface 10,1 à l’aide du paramètre *ppDevice* . Si une interface de périphérique Direct3D 10,1 ne peut pas être acquise, cette fonction retourne E \_ Fail et ne retourne rien pour le paramètre *ppDevice* .

## <a name="remarks"></a>Notes

Pour que cette fonction aboutisse, vous devez avoir acquis le pointeur [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) fourni à l’aide d’un appel à la fonction [**D3DX10CreateDevice**](d3dx10createdevice.md) , à la fonction [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) , à la fonction [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) ou à la fonction [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) .

Vous pouvez uniquement créer un périphérique Direct3D 10,1 sur des ordinateurs exécutant Windows Vista Service Pack 1 ou une version ultérieure et sur lequel le matériel compatible Direct3D 10,1 est installé. Cette fonction renvoie E \_ Fail sur tout ordinateur qui ne répond pas à ces exigences. Toutefois, vous pouvez appeler cette fonction sur n’importe quelle version de Windows sur laquelle la DLL D3DX10 est installée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




