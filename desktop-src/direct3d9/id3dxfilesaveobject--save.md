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
ms.openlocfilehash: a49c4776f9ce590d287869436b329ddf9a378e73f04f0127246fc890944ffee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563959"
---
# <a name="id3dxfilesaveobjectsave-method"></a>ID3DXFileSaveObject :: Save, méthode

Enregistre un objet de données et ses enfants dans un fichier. x sur le disque.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Save();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être la suivante : D3DXFERR \_ BADOBJECT.

## <a name="remarks"></a>Remarques

Une fois cette méthode réussie, [**ID3DXFileSaveObject :: AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData :: AddDataObject**](id3dxfilesavedata--adddataobject.md) et [**ID3DXFileSaveData :: AddDataReference**](id3dxfilesavedata--adddatareference.md) ne peuvent plus être appelés jusqu’à la création d’un nouvel objet [**ID3DXFile**](id3dxfile.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




