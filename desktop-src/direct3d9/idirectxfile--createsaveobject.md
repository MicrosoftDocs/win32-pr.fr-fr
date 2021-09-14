---
description: Crée un objet Save. Action déconseillée.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'IDirectXFile :: CreateSaveObject, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118441"
---
# <a name="idirectxfilecreatesaveobject-method"></a>IDirectXFile :: CreateSaveObject, méthode

Crée un objet Save. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*szFileName* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers le nom du fichier à utiliser pour enregistrer les données.

</dd> <dt>

*dwFileFormat* \[ dans\]
</dt> <dd>

Type : **[ **DXFILEFORMAT**](dxfile.md)**

Indique le format à utiliser lors de l’enregistrement du fichier DirectX. Cette valeur peut être l’un des \_ indicateurs DXFILEFORMAT xxx dans les [constantes DXFILE](dxfile.md). Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*ppSaveObj* \[ out, retval\]
</dt> <dd>

Type : **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

Adresse d’un pointeur vers une interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) , représentant l’objet Save créé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADALLOC, DXFILEERR \_ BadFile, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Notes

Après l’utilisation de cette méthode, utilisez les méthodes de l’interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) pour créer des objets de données et enregistrer des modèles ou des données.

La valeur par défaut pour le format de fichier est DXFILEFORMAT \_ binaire. Les valeurs de format de fichier peuvent être combinées dans un ou logique pour créer du texte compressé ou des fichiers binaires compressés. Si un fichier est spécifié à la fois comme binaire (0) et texte (1), il est enregistré en tant que fichier texte, car la valeur ne peut pas être différenciée de la valeur de format de fichier texte (0 + 1 = 1). Si vous indiquez que le format de fichier doit être texte et compressé, le fichier est d’abord écrit sous forme de texte, puis compressé. Toutefois, les fichiers texte compressés ne sont pas aussi efficaces que les fichiers texte binaires. par conséquent, dans la plupart des cas, vous devez indiquer binary et Compressed. La définition d’un fichier à compresser sans spécifier de format entraînera un fichier binaire et compressé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 
