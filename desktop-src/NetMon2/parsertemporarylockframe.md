---
description: La fonction ParserTemporaryLockFrame verrouille un frame lorsqu’il entre dans un analyseur et déverrouille le frame lorsque la fonction quitte l’analyseur.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: ParserTemporaryLockFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 47a8c02a29007084161897e34bd3ba6fbe3b5f53460aaced2acaf8e4924d67f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364385"
---
# <a name="parsertemporarylockframe-function"></a>ParserTemporaryLockFrame fonction)

La fonction **ParserTemporaryLockFrame** verrouille un frame lorsqu’il entre dans un analyseur et déverrouille le frame lorsque la fonction quitte l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame vers lequel pointe l’analyseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers le premier octet de données dans le frame.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Remarques

Les analyseurs ne doivent pas appeler la fonction **LockFrame** . Si un analyseur prend un verrou, puis génère une erreur ou retourne sans déverrouiller le frame, l’analyseur laisse le système dans un État où il ne peut pas modifier les protocoles ni couper ou copier les frames. Les analyseurs doivent utiliser la fonction **ParserTemporaryLockFrame** , qui accorde un verrou uniquement pendant le contexte de l’entrée de la fonction dans l’analyseur. À la sortie de l’analyseur, le verrou de ce frame est libéré. Par conséquent, le pointeur est valide uniquement après le retour de l’analyseur à partir de l’appel à la fonction **AttachProperties** ou **RecognizeFrame** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




