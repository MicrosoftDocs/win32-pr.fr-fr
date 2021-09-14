---
description: Crée une instance d’un objet ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: D3DXFileCreate, fonction (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012802"
---
# <a name="d3dxfilecreate-function"></a>D3DXFileCreate fonction)

Crée une instance d’un objet [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Type : **[ **ID3DXFile**](id3dxfile.md)\*\***

Adresse d’un pointeur vers une interface [**ID3DXFile**](id3dxfile.md) , représentant l’objet fichier. x créé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est S \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : \_ pointeur e, e \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Après l’utilisation de cette fonction, utilisez [**RegisterTemplates**](id3dxfile--registertemplates.md) ou [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) pour inscrire des modèles, [**CreateEnumObject**](id3dxfile--createenumobject.md) pour créer un objet énumérateur ou [**CreateSaveObject**](id3dxfile--createsaveobject.md) pour créer un objet Save.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de fichier D3DX X](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](id3dxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](id3dxfile--createsaveobject.md)
</dt> <dt>

[**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




