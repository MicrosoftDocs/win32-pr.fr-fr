---
description: Crée un objet énumérateur qui lira un fichier. x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'ID3DXFile :: CreateEnumObject, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916408"
---
# <a name="id3dxfilecreateenumobject-method"></a>ID3DXFile :: CreateEnumObject, méthode

Crée un objet énumérateur qui lira un fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pvSource* \[ à\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Source de données. Un des deux éléments suivants :

-   Un nom de fichier
-   Une structure [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)
-   Une structure [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)

En fonction de la valeur de loadflags.

</dd> <dt>

*loadflags* \[ dans\]
</dt> <dd>

Type : **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**

Valeur qui spécifie la source des données. Cette valeur peut être l’un des indicateurs [D3DXF \_ FILELOADOPTIONS](d3dxf.md) .

</dd> <dt>

*ppEnumObj* \[ à\]
</dt> <dd>

Type : **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Adresse d’un pointeur vers une interface [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , représentant l’objet énumérateur créé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Notes

Après l’utilisation de cette méthode, utilisez l’une des méthodes [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pour récupérer un objet de données.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
