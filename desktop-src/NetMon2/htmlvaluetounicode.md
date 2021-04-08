---
description: La fonction HTMLValueToUnicode convertit une chaîne HTML FP \_ UTF8 en chaîne Unicode.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: HTMLValueToUnicode, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750068"
---
# <a name="htmlvaluetounicode-function"></a>HTMLValueToUnicode fonction)

La fonction **HTMLValueToUnicode** convertit une chaîne HTML FP \_ UTF8 en chaîne Unicode.

## <a name="syntax"></a>Syntaxe


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pValue* \[ in, out\]
</dt> <dd>

Sur entrée, pointeur vers la chaîne HTML fournie par MCSVC.

Sur la sortie, pointeur vers la chaîne Unicode convertie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne l’équivalent Unicode de la chaîne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




