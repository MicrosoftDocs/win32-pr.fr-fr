---
description: Enregistre un objet de données et ses enfants dans un fichier. x sur le disque.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'ID3DXFileSaveObject :: Save, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517461"
---
# <a name="id3dxfilesaveobjectsave-method"></a>ID3DXFileSaveObject :: Save, méthode

Enregistre un objet de données et ses enfants dans un fichier. x sur le disque.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Save();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être la suivante : D3DXFERR \_ BADOBJECT.

## <a name="remarks"></a>Notes

Une fois cette méthode réussie, [**ID3DXFileSaveObject :: AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData :: AddDataObject**](id3dxfilesavedata--adddataobject.md) et [**ID3DXFileSaveData :: AddDataReference**](id3dxfilesavedata--adddatareference.md) ne peuvent plus être appelés jusqu’à la création d’un nouvel objet [**ID3DXFile**](id3dxfile.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




