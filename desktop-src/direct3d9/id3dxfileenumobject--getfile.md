---
description: Récupère l’objet ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'ID3DXFileEnumObject :: GetFile, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953906"
---
# <a name="id3dxfileenumobjectgetfile-method"></a>ID3DXFileEnumObject :: GetFile, méthode

Récupère l’objet [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppFile* \[ à\]
</dt> <dd>

Type : **[ **ID3DXFile**](id3dxfile.md)\*\***

Adresse d’un pointeur vers une interface [**ID3DXFile**](id3dxfile.md) représentant l’objet retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 




