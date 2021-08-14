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
ms.openlocfilehash: 58c105fb8fa646fbffcc7d7d4a3f1dad3a9cd86e7bb6ef8cc426dc982873f720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796369"
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

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un pointeur vers la chaîne convertie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




