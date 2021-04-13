---
description: Récupère l’objet de niveau supérieur suivant dans le fichier DirectX. Action déconseillée.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'IDirectXFileEnumObject :: GetNextDataObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322669"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a>IDirectXFileEnumObject :: GetNextDataObject, méthode

Récupère l’objet de niveau supérieur suivant dans le fichier DirectX. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDataObj* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS

## <a name="remarks"></a>Notes

Les objets de niveau supérieur sont toujours des objets de données. Les objets de référence de données et les objets binaires peuvent uniquement être des enfants d’objets de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 




