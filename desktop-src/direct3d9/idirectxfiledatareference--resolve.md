---
description: Résout les références de données. Action déconseillée.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'IDirectXFileDataReference :: Resolve, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520339"
---
# <a name="idirectxfiledatareferenceresolve-method"></a>IDirectXFileDataReference :: Resolve, méthode

Résout les références de données. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDataObj* \[ out, retval\]
</dt> <dd>

Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileDataReference](idirectxfiledatareference.md)
</dt> </dl>

 

 




