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
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194528"
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



 

 




