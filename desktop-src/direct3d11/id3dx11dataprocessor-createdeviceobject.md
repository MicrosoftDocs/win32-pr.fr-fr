---
title: Méthode ID3DX11DataProcessor CreateDeviceObject (D3DX11core. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Crée un objet appareil.'
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Méthode CreateDeviceObject Direct3D 11
- Méthode CreateDeviceObject Direct3D 11, interface ID3DX11DataProcessor
- Interface ID3DX11DataProcessor Direct3D 11, méthode CreateDeviceObject
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ff178cec1830d1b0213af23a2a70654416d35e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122462"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a>ID3DX11DataProcessor :: CreateDeviceObject, méthode

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Crée un objet appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDataObject* \[ à\]
</dt> <dd>

Type : **void \* \***

Adresse d’un pointeur vers l’objet appareil créé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Cette méthode est utilisée par une [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





