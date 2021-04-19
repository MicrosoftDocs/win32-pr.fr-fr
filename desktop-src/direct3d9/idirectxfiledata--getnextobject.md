---
description: Récupère l’objet de données enfants, l’objet de référence de données ou l’objet binaire suivant dans le fichier DirectX. Action déconseillée.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'IDirectXFileData :: GetNextObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531563"
---
# <a name="idirectxfiledatagetnextobject-method"></a>IDirectXFileData :: GetNextObject, méthode

Récupère l’objet de données enfants, l’objet de référence de données ou l’objet binaire suivant dans le fichier DirectX. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppChildObj* \[ out, retval\]
</dt> <dd>

Type : **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***

Adresse d’un pointeur vers une interface [**IDirectXFileObject**](idirectxfileobject.md) , représentant l’interface d’objet fichier de l’objet enfant retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS.

## <a name="remarks"></a>Notes

Pour déterminer le type d’objet récupéré, utilisez QueryInterface pour interroger l’objet récupéré pour la prise en charge des interfaces [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md)ou [**IDirectXFileBinary**](idirectxfilebinary.md) . L’interface prise en charge indique le type d’objet (données, référence de données ou binaire).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDirectXFileBinary**](idirectxfilebinary.md)
</dt> <dt>

[**IDirectXFileData**](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileDataReference**](idirectxfiledatareference.md)
</dt> </dl>

 

 




