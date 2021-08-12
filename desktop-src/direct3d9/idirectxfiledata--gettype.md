---
description: Récupère le GUID du modèle de l’objet. Action déconseillée.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'IDirectXFileData :: GetType, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 564d682c606d8b6bc0001f5d430d2d93f36c25210746169af4802512c330da08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292275"
---
# <a name="idirectxfiledatagettype-method"></a>IDirectXFileData :: GetType, méthode

Récupère le GUID du modèle de l’objet. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppGUID* \[ out, retval\]
</dt> <dd>

Type : **const [**GUID**](guid.md) \* \***

Adresse d’un pointeur devant recevoir le GUID du modèle de l’objet.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 




