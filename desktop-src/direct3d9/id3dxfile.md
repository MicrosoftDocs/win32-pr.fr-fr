---
description: Les applications utilisent les méthodes de l’interface ID3DXFile pour créer des instances des interfaces ID3DXFileEnumObject et ID3DXFileSaveObject, et pour inscrire des modèles.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Interface ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbfaf93250f6c80888d82b291f4294d893703a383552fbef94d50c6fc57f1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893349"
---
# <a name="id3dxfile-interface"></a>Interface ID3DXFile

Les applications utilisent les méthodes de l’interface ID3DXFile pour créer des instances des interfaces [**ID3DXFileEnumObject**](id3dxfileenumobject.md) et [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , et pour inscrire des modèles.

## <a name="members"></a>Membres

L’interface **ID3DXFile** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFile** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXFile** possède ces méthodes.



| Méthode                                                            | Description                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateEnumObject**](id3dxfile--createenumobject.md)           | Crée un objet énumérateur qui lira un fichier. x.<br/>                                                      |
| [**CreateSaveObject**](id3dxfile--createsaveobject.md)           | Crée un objet Save qui sera utilisé pour enregistrer des données dans un fichier. x.<br/>                                          |
| [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) | Inscrit des modèles personnalisés, à partir d’un objet d’énumération [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .<br/> |
| [**RegisterTemplates**](id3dxfile--registertemplates.md)         | Inscrit des modèles personnalisés.<br/>                                                                                 |



 

## <a name="remarks"></a>Remarques

Un objet ID3DXFile contient également un magasin de modèles local. Ce stockage local peut être ajouté à uniquement avec les méthodes [**ID3DXFile :: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) et [**ID3DXFile :: RegisterTemplates**](id3dxfile--registertemplates.md) .

Les objets [**ID3DXFileEnumObject**](id3dxfileenumobject.md) et [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) créés avec [**ID3DXFile :: CreateEnumObject**](id3dxfile--createenumobject.md) et [**ID3DXFile :: CreateSaveObject**](id3dxfile--createsaveobject.md) utilisent également le magasin de modèles de l’objet ID3DXFile parent.

L’interface ID3DXFile est obtenue en appelant la fonction [**D3DXFileCreate**](d3dxfilecreate.md) .

L’identificateur global unique (GUID) de l’interface ID3DXFile est IID \_ ID3DXFile.

Le type LPD3DXFILE est défini comme un pointeur vers l’interface ID3DXFile.


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces de fichiers D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
