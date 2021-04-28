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
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103597"
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

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes 

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

 

 




