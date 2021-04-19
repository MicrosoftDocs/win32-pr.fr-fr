---
description: Récupère un pointeur vers le GUID qui identifie un objet fichier DirectX. Action déconseillée.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'IDirectXFileObject :: GetId, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535808"
---
# <a name="idirectxfileobjectgetid-method"></a>IDirectXFileObject :: GetId, méthode

Récupère un pointeur vers le GUID qui identifie un objet fichier DirectX. Action déconseillée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguid* \[ out, retval\]
</dt> <dd>

Type : **LPGUID**

Pointeur vers un GUID pour recevoir l’ID de l’objet. La fonction définit le GUID sur un GUID **null** si l’objet n’a pas d’ID.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est DXFILE \_ OK. Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 




