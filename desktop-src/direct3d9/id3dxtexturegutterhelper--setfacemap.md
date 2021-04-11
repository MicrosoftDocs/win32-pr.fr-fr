---
description: Définit l’index du type de maillage auquel appartient chaque Texel.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'ID3DXTextureGutterHelper :: SetFaceMap, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211905"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a>ID3DXTextureGutterHelper :: SetFaceMap, méthode

Définit l’index du type de maillage auquel appartient chaque Texel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetFaceMap(
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

## <a name="remarks"></a>Notes

L’entrée de données de la maille de cette méthode est valide uniquement pour les texels valides (non de classe 0). [**ID3DXTextureGutterHelper :: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retourne des valeurs non nulles pour les texels valides.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
