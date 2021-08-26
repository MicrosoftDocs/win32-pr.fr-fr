---
description: D3DX10CreateSkinInfo fonction-crée un objet de maillage d’apparence vide à l’aide d’un déclarateur.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: D3DX10CreateSkinInfo, fonction (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 52a6d1116e46771c4c092fb08f3d59f43277d2437db1bd2c5b750f4a381043fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070189"
---
# <a name="d3dx10createskininfo-function"></a>D3DX10CreateSkinInfo fonction)

Crée un objet de maillage d’apparence vide à l’aide d’un déclarateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSkinInfo* \[ à\]
</dt> <dd>

Type : **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Adresse d’un pointeur vers une [**interface ID3DX10SkinInfo**](id3dx10skininfo.md)représentant l’objet de maillage d’apparence créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Utilisez [**ID3DX10SkinInfo :: SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) pour remplir l’objet de maillage d’apparence vide retourné par cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[D3DX, fonctions](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




