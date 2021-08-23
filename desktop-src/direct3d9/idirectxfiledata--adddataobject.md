---
description: Ajoute un objet de données en tant qu’objet enfant. Action déconseillée.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'IDirectXFileData :: AddDataObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: db11f5f3c0d9078663c87db8948bc483ab05d229cd4d7fd0950efaf5143e1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491829"
---
# <a name="idirectxfiledataadddataobject-method"></a>IDirectXFileData :: AddDataObject, méthode

Ajoute un objet de données en tant qu’objet enfant. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDataObj* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

Pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier à ajouter en tant qu’objet enfant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Remarques

Utilisez la méthode [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer l’objet [**IDirectXFileData**](idirectxfiledata.md) avant d’appeler cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




