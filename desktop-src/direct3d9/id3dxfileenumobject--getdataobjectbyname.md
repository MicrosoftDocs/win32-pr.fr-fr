---
description: Récupère l’objet de données qui porte le nom spécifié.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'ID3DXFileEnumObject :: GetDataObjectByName, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f42c82fb2eeedf6c1ec6c0f8099e6fbc1f6bac8d9e96bafbb6a94bacbf8f20e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951539"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a>ID3DXFileEnumObject :: GetDataObjectByName, méthode

Récupère l’objet de données qui porte le nom spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom demandé.

</dd> <dt>

*ppObj* \[ à\]
</dt> <dd>

Type : **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Adresse d’un pointeur vers une interface [**ID3DXFileData**](id3dxfiledata.md) , représentant l’objet de données de fichier retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.

## <a name="remarks"></a>Remarques

Obtenez le nom szName de l’objet de données de fichier actuel à l’aide de la méthode [**ID3DXFileData :: GetName**](id3dxfiledata--getname.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
