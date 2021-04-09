---
description: Obtient l’animation définie pour le suivi donné.
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'ID3DXAnimationController :: GetTrackAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7ba397fb876d94aa48f635785737ab0448ecef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953920"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a>ID3DXAnimationController :: GetTrackAnimationSet, méthode

Obtient l’animation définie pour le suivi donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de suivi.

</dd> <dt>

*ppAnimSet* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Pointeur vers l’animation [**ID3DXAnimationSet**](id3dxanimationset.md) définie pour la piste donnée.

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

 

 
