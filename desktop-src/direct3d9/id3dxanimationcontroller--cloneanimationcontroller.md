---
description: Clone, ou copie, un contrôleur d’animation.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'ID3DXAnimationController :: CloneAnimationController, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5afb99126967163318c82bac6b8cac655fec65e8a28e4cdb349c7f2b1c679435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522780"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a>ID3DXAnimationController :: CloneAnimationController, méthode

Clone, ou copie, un contrôleur d’animation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MaxNumAnimationOutputs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre maximal de sorties d’animation que le contrôleur peut prendre en charge.

</dd> <dt>

*MaxNumAnimationSets* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre maximal de jeux d’animations que le contrôleur peut prendre en charge.

</dd> <dt>

*MaxNumTracks* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre maximal de pistes que le contrôleur peut prendre en charge.

</dd> <dt>

*MaxNumEvents* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre maximal d’événements que le contrôleur peut prendre en charge.

</dd> <dt>

*ppAnimController* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Adresse d’un pointeur vers le contrôleur d’animation [**ID3DXAnimationController**](id3dxanimationcontroller.md) cloné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
