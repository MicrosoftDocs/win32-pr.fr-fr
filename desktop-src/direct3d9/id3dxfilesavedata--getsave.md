---
description: Récupère un pointeur vers ce nœud de données de fichier ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'ID3DXFileSaveData :: GetSave, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 05b30c34f7e9d1383270c06ee70aca63d3f24b0f4f721d6859366794f2df361a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856639"
---
# <a name="id3dxfilesavedatagetsave-method"></a>ID3DXFileSaveData :: GetSave, méthode

Récupère un pointeur vers ce nœud de données de fichier [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppObj* \[ à\]
</dt> <dd>

Type : **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Adresse d’un pointeur vers une interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) représentant ce nœud de données de fichier.

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

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




