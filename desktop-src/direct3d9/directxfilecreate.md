---
description: Crée une instance d’un objet DirectXFile. Action déconseillée.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: DirectXFileCreate, fonction (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525864"
---
# <a name="directxfilecreate-function"></a>DirectXFileCreate fonction)

Crée une instance d’un objet DirectXFile. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Type : **[ **LPDIRECTXFILE**](idirectxfile.md)\***

Adresse d’un pointeur vers une interface [**IDirectXFile**](idirectxfile.md) , représentant l’objet DirectXFile créé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Notes

Après l’utilisation de cette fonction, utilisez [**RegisterTemplates**](idirectxfile--registertemplates.md) pour inscrire des modèles, [**CreateEnumObject**](idirectxfile--createenumobject.md) pour créer un objet énumérateur ou [**CreateSaveObject**](idirectxfile--createsaveobject.md) pour créer un objet Save.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dxof.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[X, fonctions de fichier](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](idirectxfile--createsaveobject.md)
</dt> <dt>

[**RegisterTemplates**](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




