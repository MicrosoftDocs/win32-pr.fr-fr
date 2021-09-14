---
description: Définit le degré d’influence d’un segment donné sur un sommet donné.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'ID3DX10SkinInfo :: SetBoneInfluence, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915591"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a>ID3DX10SkinInfo :: SetBoneInfluence, méthode

Définit le degré d’influence d’un segment donné sur un sommet donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*BoneIndex* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index qui spécifie un segment existant. Doit être compris entre 0 et la valeur retournée par [**ID3DX10SkinInfo :: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceIndex* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index dans la liste des vertex du segment qu’il influence.

</dd> <dt>

*Poids* \[ dans\]
</dt> <dd>

Type : **float**

La quantité d’influence, comprise entre 0 et 1, que le segment a sur le vertex.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être E \_ INVALIDARG.

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

 

 
