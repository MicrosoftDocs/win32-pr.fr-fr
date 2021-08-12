---
description: Récupère l’objet de données qui a le GUID spécifié. Action déconseillée.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'IDirectXFileEnumObject :: GetDataObjectById, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 49bee0f513bcca71a98e72fb3f51e1bcc458083ce9b165b3e5163fb5f6b71708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292230"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a>IDirectXFileEnumObject :: GetDataObjectById, méthode

Récupère l’objet de données qui a le GUID spécifié. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rguid* \[ dans\]
</dt> <dd>

Type : **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Référence au GUID demandé.

</dd> <dt>

*ppDataObj* \[ à\]
</dt> <dd>

Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 
