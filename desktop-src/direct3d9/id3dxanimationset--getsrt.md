---
description: Obtient les valeurs de mise à l’échelle, de rotation et de translation de l’ensemble d’animations.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'ID3DXAnimationSet :: GetSRT, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: baa1b882972a91626b19194f83655ea1839877943f7463be8991167eb72d17fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791069"
---
# <a name="id3dxanimationsetgetsrt-method"></a>ID3DXAnimationSet :: GetSRT, méthode

Obtient les valeurs de mise à l’échelle, de rotation et de translation de l’ensemble d’animations.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PeriodicPosition* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Position de l’ensemble d’animations. La position peut être obtenue en appelant [**ID3DXAnimationSet :: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).

</dd> <dt>

*Animation* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index d’animation.

</dd> <dt>

*pScale* \[ à\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers le vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit l’échelle de l’ensemble d’animations.

</dd> <dt>

*protique* \[ à\]
</dt> <dd>

Type : **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Pointeur vers le Quaternion [**D3DXQUATERNION**](d3dxquaternion.md) qui décrit la rotation de l’ensemble d’animations.

</dd> <dt>

*pTranslation* \[ à\]
</dt> <dd>

Type : **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Pointeur vers le vecteur [**D3DXVECTOR3**](d3dxvector3.md) qui décrit la traduction de l’ensemble d’animations.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications. En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK. Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
