---
description: La fonction StringToAddress convertit une chaîne en adresse.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: StringToAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbac01f5df9d32a65fe5afb1c1437064f6dd0d4480c95dacd0fe8f7d58e2fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676689"
---
# <a name="stringtoaddress-function"></a>StringToAddress fonction)

La fonction **StringToAddress** convertit une chaîne en adresse.

## <a name="syntax"></a>Syntaxe


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpAddress* \[ à\]
</dt> <dd>

Pointeur vers l’adresse vers laquelle la chaîne est convertie.

</dd> <dt>

*chaîne* \[ dans\]
</dt> <dd>

Chaîne convertie en adresse.

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



 

 




