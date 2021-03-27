---
title: ID3DX11DataLoader, méthode de chargement (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Charge des données à partir d’un disque.'
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
ms.openlocfilehash: c0f720a5e6884bfdf1935c6d93f7a05decae5e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982615"
---
# <a name="id3dx11dataloaderload-method"></a>ID3DX11DataLoader :: Load, méthode

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

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

## <a name="remarks"></a>Notes

Cette méthode est utilisée par une [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).

## <a name="requirements"></a>Spécifications



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

 

 





