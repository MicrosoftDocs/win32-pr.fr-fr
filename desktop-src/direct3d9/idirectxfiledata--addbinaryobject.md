---
description: Crée un objet binaire et l’ajoute en tant qu’objet enfant. Action déconseillée.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'IDirectXFileData :: AddBinaryObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404047"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a>IDirectXFileData :: AddBinaryObject, méthode

Crée un objet binaire et l’ajoute en tant qu’objet enfant. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom de l’objet. Spécifiez **null** si l’objet n’a pas besoin d’un nom.

</dd> <dt>

*pguid* \[ dans\]
</dt> <dd>

Type : **const [**GUID**](guid.md) \***

Pointeur vers le GUID représentant l’objet. Spécifiez **null** si l’objet n’a pas besoin d’un GUID.

</dd> <dt>

*szMimeType* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le type MIME de l’objet.

</dd> <dt>

*pvData* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers les données de l’objet.

</dd> <dt>

*cbSize* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Taille de la mémoire tampon vers laquelle pointe pvData, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileBinary::GetMimeType**](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
