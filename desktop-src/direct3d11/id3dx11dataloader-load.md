---
title: ID3DX11DataLoader, méthode de chargement (D3DX11core. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Charge des données à partir d’un disque.'
ms.assetid: 21dee078-af8f-4ca1-bb2e-d4ecc0471609
keywords:
- Charger la méthode Direct3D 11
- Charger la méthode Direct3D 11, interface ID3DX11DataLoader
- Interface ID3DX11DataLoader Direct3D 11, méthode Load
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Load
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f698896ca696a6d63b4738f1246deb35be0139f3bff817518cc5f81b52a191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632989"
---
# <a name="id3dx11dataloaderload-method"></a>ID3DX11DataLoader :: Load, méthode

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Charge des données à partir d’un disque.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Load();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarques

Cette méthode est utilisée par une [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





