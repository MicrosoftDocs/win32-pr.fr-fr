---
description: La fonction AddressToString convertit une adresse en chaîne.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: AddressToString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021120"
---
# <a name="addresstostring-function"></a>AddressToString fonction)

La fonction **AddressToString** convertit une adresse en chaîne.

## <a name="syntax"></a>Syntaxe


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*chaîne* \[ à\]
</dt> <dd>

Chaîne dans laquelle l’adresse est convertie.

</dd> <dt>

*lpAddress* \[ dans\]
</dt> <dd>

Adresse qui est imprimée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est un pointeur vers la chaîne convertie.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




