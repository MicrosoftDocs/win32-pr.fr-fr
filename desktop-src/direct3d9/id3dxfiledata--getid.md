---
description: Récupère le GUID de cet objet de données de fichier.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'ID3DXFileData :: GetId, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a9a1cbf98792b0ac36c35aabf40b8c125a497201b27c6a161c0706f077ffc491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295325"
---
# <a name="id3dxfiledatagetid-method"></a>ID3DXFileData :: GetId, méthode

Récupère le GUID de cet objet de données de fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PID* \[ à\]
</dt> <dd>

Type : **LPGUID**

Pointeur vers un GUID pour recevoir l’ID de cet objet de données de fichier. Si l’objet de données de fichier n’a pas d’ID, la valeur de paramètre retournée est le GUID \_ null.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

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

 

 




