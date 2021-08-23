---
description: Récupère le nombre d’objets enfants dans cet objet de données de fichier.
ms.assetid: 4409819f-a346-40b1-8e12-86e8128ece47
title: 'ID3DXFileEnumObject :: GetChildren, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChildren
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 857a52692fe0ef2390628f0d838129e6e00d1202e7615577f1e2e20b2ce74268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121405"
---
# <a name="id3dxfileenumobjectgetchildren-method"></a>ID3DXFileEnumObject :: GetChildren, méthode

Récupère le nombre d’objets enfants dans cet objet de données de fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetChildren(
  [in] SIZE_T *puiChildren
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*puiChildren* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***

Adresse d’un pointeur qui reçoit le nombre d’objets enfants dans cet objet de données de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
