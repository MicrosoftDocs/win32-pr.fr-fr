---
description: Applique l’animation définie à la piste spécifiée.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'ID3DXAnimationController :: SetTrackAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531788"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>ID3DXAnimationController :: SetTrackAnimationSet, méthode

Applique l’animation définie à la piste spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de la piste à laquelle l’ensemble d’animations est appliqué.

</dd> <dt>

*pAnimSet* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Pointeur vers l’animation [**ID3DXAnimationSet**](id3dxanimationset.md) définie à ajouter à la piste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Cette méthode définit l’animation définie sur la piste spécifiée pour mélanger. L’animation définie pour chaque piste est fusionnée en fonction du poids de la piste et de la vitesse de l’appel de [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
