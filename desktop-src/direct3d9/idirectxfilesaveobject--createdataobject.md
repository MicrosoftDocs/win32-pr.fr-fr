---
description: Crée un objet de données. Action déconseillée.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'IDirectXFileSaveObject :: CreateDataObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e1497ad06919833e0ba716877dc81b8df51a99361a49e43fa9a0f756e296040c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728911"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a>IDirectXFileSaveObject :: CreateDataObject, méthode

Crée un objet de données. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rguidTemplate* \[ dans\]
</dt> <dd>

Type : **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

GUID représentant le modèle de l’objet de données.

</dd> <dt>

*szName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom de l’objet de données. Spécifiez **null** si l’objet n’a pas de nom.

</dd> <dt>

*pguid* \[ dans\]
</dt> <dd>

Type : **const [**GUID**](guid.md) \***

Pointeur vers un GUID représentant l’objet de données. Spécifiez **null** si l’objet n’a pas de GUID.

</dd> <dt>

*cbSize* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Taille de l’objet de données, en octets.

</dd> <dt>

*pvData* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers une mémoire tampon contenant toutes les données du membre requis.

</dd> <dt>

*ppDataObj* \[ out, retval\]
</dt> <dd>

Type : **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

Adresse d’un pointeur vers une interface [**IDirectXFileData**](idirectxfiledata.md) , représentant l’objet de données de fichier créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>Remarques

Si un objet de référence de données fait référence à l’objet de données, le paramètre szName ou pguid doit avoir une **valeur non null**.

Enregistrez les modèles à l’aide de la méthode [**IDirectXFileSaveObject :: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) avant d’enregistrer les données créées par cette méthode. Enregistrez les données créées à l’aide de la méthode [**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md) .

Si vous devez enregistrer des données facultatives, utilisez la méthode [**IDirectXFileData :: AddDataObject**](idirectxfiledata--adddataobject.md) après avoir utilisé cette méthode et avant d’utiliser [**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md). Si l’objet a des objets enfants, ajoutez-les avant d’appeler **IDirectXFileSaveObject :: SaveData**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md)
</dt> <dt>

[**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
