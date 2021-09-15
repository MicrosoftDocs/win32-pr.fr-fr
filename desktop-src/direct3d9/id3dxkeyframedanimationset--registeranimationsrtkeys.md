---
description: Enregistre les données de l’image clé de l’échelle, de rotation et de translation (SRT) pour une animation.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'ID3DXKeyframedAnimationSet :: RegisterAnimationSRTKeys, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517460"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>ID3DXKeyframedAnimationSet :: RegisterAnimationSRTKeys, méthode

Enregistre les données de l’image clé de l’échelle, de rotation et de translation (SRT) pour une animation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom de l’animation.

</dd> <dt>

*NumScaleKeys* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de clés de mise à l’échelle.

</dd> <dt>

*NumRotationKeys* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de clés de rotation.

</dd> <dt>

*NumTranslationKeys* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de clés de traduction.

</dd> <dt>

*pScaleKeys* \[ dans\]
</dt> <dd>

Type : **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Adresse d’un pointeur vers un tableau alloué par l’utilisateur de vecteurs [**\_ VECTOR3 D3DXKEY**](d3dxkey-vector3.md) que la méthode remplit avec les données de mise à l’échelle.

</dd> <dt>

*pRotationKeys* \[ dans\]
</dt> <dd>

Type : **const [**LPD3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) \***

Adresse d’un pointeur vers un tableau alloué par l’utilisateur de quaternions [**D3DXKEY \_ Quaternion**](d3dxkey-quaternion.md) que la méthode remplit avec les données de rotation.

</dd> <dt>

*pTranslationKeys* \[ dans\]
</dt> <dd>

Type : **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Adresse d’un pointeur vers un tableau alloué par l’utilisateur de vecteurs [**\_ VECTOR3 D3DXKEY**](d3dxkey-vector3.md) que la méthode remplit avec les données de traduction.

</dd> <dt>

*pAnimationIndex* \[ à\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Retourne l’index d’animation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
