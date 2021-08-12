---
description: 'ID3DXFileData :: GetChild, méthode-récupère un objet enfant dans cet objet de données de fichier.'
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: 'ID3DXFileData :: GetChild, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8442577ab70b3ce4b08229d1b21989e614d8f328d3012042d3b1b5dc524f4604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295335"
---
# <a name="id3dxfiledatagetchild-method"></a>ID3DXFileData :: GetChild, méthode

Récupère un objet enfant dans cet objet de données de fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uiChild* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**

ID de l’objet enfant à récupérer.

</dd> <dt>

*ppChild* \[ dans\]
</dt> <dd>

Type : **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Adresse d’un pointeur pour recevoir le pointeur d’interface de l’objet enfant.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
