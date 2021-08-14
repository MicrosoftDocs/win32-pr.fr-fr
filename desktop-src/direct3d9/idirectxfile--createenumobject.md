---
description: Crée un objet énumérateur. Action déconseillée.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'IDirectXFile :: CreateEnumObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1af10a0f46877a159ab8c6543fba9c1406d083e6b3f4a57cf1c41b9fb2d92612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985149"
---
# <a name="idirectxfilecreateenumobject-method"></a>IDirectXFile :: CreateEnumObject, méthode

Crée un objet énumérateur. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pvSource* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers des données dont le contenu dépend de la valeur de dwLoadOptions

</dd> <dt>

*dwLoadOptions* \[ dans\]
</dt> <dd>

Type : **[ **DXFILELOADOPTIONS**](dxfile.md)**

Valeur qui spécifie la source des données. Cette valeur peut être l’un des \_ indicateurs DXFILELOAD xxx dans les [constantes DXFILE](dxfile.md).

</dd> <dt>

*ppEnumObj* \[ out, retval\]
</dt> <dd>

Type : **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***

Adresse d’un pointeur vers une interface [**IDirectXFileEnumObject**](idirectxfileenumobject.md) , représentant l’objet énumérateur créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.

## <a name="remarks"></a>Remarques

Après l’utilisation de cette méthode, utilisez l’une des méthodes IDirectXFileEnumObject pour récupérer un objet de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 
