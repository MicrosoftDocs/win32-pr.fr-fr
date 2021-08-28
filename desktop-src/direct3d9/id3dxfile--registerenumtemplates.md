---
description: Inscrit des modèles personnalisés, à partir d’un objet d’énumération ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'ID3DXFile :: RegisterEnumTemplates, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a7c63ed8c4a2c3a65a80ba18f1b0455111917e99dce2982eb7be1d85314b6541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630069"
---
# <a name="id3dxfileregisterenumtemplates-method"></a>ID3DXFile :: RegisterEnumTemplates, méthode

Inscrit des modèles personnalisés, à partir d’un objet d’énumération [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pEnum* \[ dans\]
</dt> <dd>

Type : **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***

Pointeur vers un objet d’énumération [**ID3DXFileEnumObject**](id3dxfileenumobject.md) qui contient des modèles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK.

Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Remarques

Lorsque cette méthode est appelée, elle copie les modèles stockés avec ID3DXFileEnumObject, représentant le fichier, dans le magasin de modèles local de l’objet [**ID3DXFile**](id3dxfile.md) .

Si un pointeur [**ID3DXFileEnumObject**](id3dxfileenumobject.md) n’est pas disponible, appelez la méthode [**RegisterTemplates**](id3dxfile--registertemplates.md) à la place.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




