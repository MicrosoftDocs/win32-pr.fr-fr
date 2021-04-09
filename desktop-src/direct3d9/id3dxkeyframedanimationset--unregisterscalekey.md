---
description: Supprime les données de mise à l’échelle au niveau de l’image clé spécifiée.
ms.assetid: b0bf5665-ccfb-4b87-8e88-9a717ef57955
title: 'ID3DXKeyframedAnimationSet :: UnregisterScaleKey, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d1ac3f500b80d8922646fddff9f05d8c91d9c48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953990"
---
# <a name="id3dxkeyframedanimationsetunregisterscalekey-method"></a>ID3DXKeyframedAnimationSet :: UnregisterScaleKey, méthode

Supprime les données de mise à l’échelle au niveau de l’image clé spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnregisterScaleKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Animation* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur d’animation.

</dd> <dt>

*Clé* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Image clé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Cette méthode est lente et ne doit pas être utilisée une fois que l’animation a commencé à jouer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
