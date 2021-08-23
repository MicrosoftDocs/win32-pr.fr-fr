---
description: Remplit un tableau avec les données de la clé de mise à l’échelle utilisées pour l’animation d’image clé.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'ID3DXKeyframedAnimationSet :: GetScaleKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1158195ae84f8215869571fc400950a6dfd475fc37050572ffb5e3e77f96d719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493509"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a>ID3DXKeyframedAnimationSet :: GetScaleKeys, méthode

Remplit un tableau avec les données de la clé de mise à l’échelle utilisées pour l’animation d’image clé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Animation* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index d’animation.

</dd> <dt>

*pScaleKeys* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Pointeur vers un tableau alloué par l’utilisateur de vecteurs [**\_ VECTOR3 D3DXKEY**](d3dxkey-vector3.md) que la méthode doit remplir avec les données de mise à l’échelle de l’animation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
