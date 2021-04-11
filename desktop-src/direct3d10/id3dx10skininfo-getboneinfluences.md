---
description: Obtient la liste des vertex qu’un segment donné influence et une liste de la quantité d’influence que l’OS a sur chaque vertex.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'ID3DX10SkinInfo :: GetBoneInfluences, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211956"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>ID3DX10SkinInfo :: GetBoneInfluences, méthode

Obtient la liste des vertex qu’un segment donné influence et une liste de la quantité d’influence que l’OS a sur chaque vertex.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BoneIndex* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index qui spécifie un segment existant. Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Décalage* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Décalage à partir du haut de la liste des vertex influencés par le segment. Elle doit être comprise entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).

</dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’index et de poids à récupérer. Doit être compris entre 0 et la valeur retournée par ID3DX10SkinInfo :: GetBoneInfluenceCount.

</dd> <dt>

*pDestIndices* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Liste d’index dans la mémoire tampon de vertex, chacun représentant un vertex influencé par le segment. Ces valeurs correspondent aux valeurs de pDestWeights, de sorte que pDestIndices \[ i \] correspond à pDestWeights \[ i \] .

</dd> <dt>

*pDestWeights* \[ in, out\]
</dt> <dd>

Type : **float \***

Liste de la quantité d’influence du segment sur chaque vertex. Ces valeurs correspondent aux valeurs dans pDestIndices, de sorte que pDestWeights \[ i \] correspond à pDestIndices \[ i \] . f

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG ou e \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



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

 

 
