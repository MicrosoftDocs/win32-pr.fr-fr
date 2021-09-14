---
description: Activez un segment existant pour influencer un groupe de vertex et définissez l’influence du segment sur chaque vertex.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'ID3DX10SkinInfo :: AddBoneInfluences, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855297"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>ID3DX10SkinInfo :: AddBoneInfluences, méthode

Activez un segment existant pour influencer un groupe de vertex et définissez l’influence du segment sur chaque vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BoneIndex* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index qui spécifie un segment existant. Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex à ajouter à l’influence du segment.

</dd> <dt>

*pIndices* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers un tableau d’index de vertex. Chaque membre de ce tableau a un membre correspondant dans pWeights, de sorte que pIndices \[ i \] correspond à pWeights \[ i \] . La valeur correspondante dans pWeights \[ i \] détermine la quantité d’influence que BoneIndex aura sur le vertex indexé par pIndices \[ i \] . La taille du tableau pIndices doit être supérieure ou égale à InfluenceCount.

</dd> <dt>

*pWeights* \[ dans\]
</dt> <dd>

Type : **float \***

Pointeur vers un tableau de poids osseux. Chaque membre de ce tableau a un membre correspondant dans pIndices, de sorte que pWeights \[ i \] correspond à pIndices \[ i \] . Chaque valeur de pWeights est comprise entre 0 et 1 et définit la quantité d’influence du segment sur chaque vertex. La taille de pWeights doit être supérieure ou égale à InfluenceCount.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG ou e \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
