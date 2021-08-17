---
description: Récupère l’index du type de maillage auquel appartient chaque Texel.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'ID3DXTextureGutterHelper :: GetFaceMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5fce4400b1f778581f830fff60ef4e1519ad73752da02f5194abe64f433d43c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729188"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a>ID3DXTextureGutterHelper :: GetFaceMap, méthode

Récupère l’index du type de maillage auquel appartient chaque Texel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFaceData* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

Pointeur vers l’index du type de maillage auquel appartient chaque Texel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Remarques

Les données de la maille retournées par cette méthode sont valides uniquement pour les texels valides (non de classe 0). [**ID3DXTextureGutterHelper :: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retourne des valeurs non nulles pour les texels valides (non de classe 0).

Pour les [**texels de classe 2**](id3dxtexturegutterhelper.md), cette méthode récupère la face la plus proche.

L’application doit allouer et gérer pFaceData.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
