---
description: Crée un objet Save qui sera utilisé pour enregistrer des données dans un fichier. x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'ID3DXFile :: CreateSaveObject, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aaf9f884a651182429de20fe261a250c8c6567eacd99d635213682e4d755b79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951609"
---
# <a name="id3dxfilecreatesaveobject-method"></a>ID3DXFile :: CreateSaveObject, méthode

Crée un objet Save qui sera utilisé pour enregistrer des données dans un fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers le nom du fichier à utiliser pour enregistrer les données.

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Type : **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**

Valeur qui spécifie le nom du fichier dans lequel les données doivent être enregistrées. Cette valeur peut être l’un des indicateurs d' [options d’enregistrement de fichier](d3dxf.md) .

</dd> <dt>

*dwFileFormat* \[ dans\]
</dt> <dd>

Type : **[D3DXF \_ FILEFORMAT](d3dxf.md)**

Indique le format à utiliser lors de l’enregistrement du fichier. x. Cette valeur peut être l’un des indicateurs de [formats de fichier](d3dxf.md) . Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*ppSaveObj* \[ à\]
</dt> <dd>

Type : **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Adresse d’un pointeur vers une interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , représentant l’objet Save créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Remarques

Après l’utilisation de cette méthode, utilisez les méthodes de l’interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) pour créer des objets de données et enregistrer des modèles ou des données.

Pour le format de fichier enregistré *dwFileFormat*, l’un des indicateurs binaires, binaires hérités ou de texte dans les [formats de fichier](d3dxf.md) doit être spécifié. Le fichier peut être compressé à l’aide de l' \_ indicateur de compression D3DXF FILEFORMAT facultatif \_ .

Les valeurs de format de fichier peuvent être combinées dans un ou logique pour créer du texte compressé ou des fichiers binaires compressés. Si vous indiquez que le format de fichier doit être texte et compressé, le fichier est écrit en premier sous forme de texte, puis compressé. Toutefois, les fichiers texte compressés ne sont pas aussi efficaces que les fichiers texte binaires ; dans la plupart des cas, vous souhaiterez donc indiquer binaire et compressé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
