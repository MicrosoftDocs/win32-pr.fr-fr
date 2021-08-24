---
description: Récupère l’objet d’énumération dans cet objet de données de fichier.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'ID3DXFileData :: GetEnum, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79ee6272f6b685c5e80b7c7b76b39925a08bb67cc07ba7af23a5b276b414f194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748549"
---
# <a name="id3dxfiledatagetenum-method"></a>ID3DXFileData :: GetEnum, méthode

Récupère l’objet d’énumération dans cet objet de données de fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppObj* \[ dans\]
</dt> <dd>

Type : **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Adresse d’un pointeur devant recevoir l’objet d’énumération dans cet objet de données de fichier.

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

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




